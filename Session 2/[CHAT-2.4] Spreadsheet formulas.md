# [CHAT-2.4] Spreadsheet formulas

## Input

Google Sheet formula which copies all rows from sheet1 where column "A" contains word "iphone".

## Output (GPT-5 mini)

To copy all rows from `Sheet1` where column "A" contains the word "iphone" (case-insensitive), you can use the following formula in a new sheet or in a new range on the same sheet:

Use FILTER with SEARCH (case-insensitive) or REGEXMATCH. Two options:

1) Case-insensitive (matches "iphone" anywhere in A):

```
=FILTER(Sheet1!A:Z, IFERROR(SEARCH("iphone", Sheet1!A:A), 0)>0)
```

2) Using REGEXMATCH (also case-insensitive):

```
=FILTER(Sheet1!A:Z, REGEXMATCH(LOWER(Sheet1!A:A), "iphone"))
```

If you only need specific columns (e.g., A:C), replace A:Z with Sheet1!A:C. If you want whole rows including headers, put the formula below the header row or include header handling like:

```
={Sheet1!A1:Z1; FILTER(Sheet1!A2:Z, REGEXMATCH(LOWER(Sheet1!A2:A), "iphone"))}
```

---

## Input

Excel formula which copies all rows from sheet1 where column "A" contains word "iphone".

## Output (GPT-5 mini)

If you have Excel 365 / Excel 2021 (FILTER available):

- Case-insensitive, matches "iphone" anywhere in A:

```
=FILTER(Sheet1!A:Z, ISNUMBER(SEARCH("iphone", Sheet1!A:A)))
```

- Whole rows except header, with header preserved:

```
=VSTACK(Sheet1!A1:Z1, FILTER(Sheet1!A2:Z, ISNUMBER(SEARCH("iphone", Sheet1!A2:A))))
```

If you don't have FILTER (older Excel), use an helper column on Sheet1 (e.g., column AA) with:

```
=IF(ISNUMBER(SEARCH("iphone", A2)), ROW(), "")
```

Then on the destination sheet use this array formula (entered with Ctrl+Shift+Enter) to pull matching rows, assuming helper in AA:

```
=IFERROR(INDEX(Sheet1!A:Z, SMALL(IF(Sheet1!AA:AA<>"", Sheet1!AA:AA), ROWS($1:1)), COLUMN(A:A)), "")
```

and copy across/right/down to retrieve all matches.