# [CHAT-4.4] Customer feedback categorization

---

## Input

Analyze this customer feedback and categorize the issues. Use these categories: UI/UX, Performance, Feature Request, Integration, Pricing, and Other. Also rate the sentiment (Positive/Neutral/Negative) and priority (High/Medium/Low).

Here is the feedback: The new dashboard is a mess! It takes forever to load, and I can't find the export button. Fix this ASAP! 

## Output (Gemini 2.5 Flash)

Here’s the analysis of the feedback:

* **Categories:**

  * UI/UX → "The new dashboard is a mess" / "can't find the export button"
  * Performance → "It takes forever to load"

* **Sentiment:** Negative

* **Priority:** High (urgent tone, multiple critical issues, request to fix ASAP)

---

## Input

Our CS team is overwhelmed with unstructured feedback. Your task is to analyze feedback and categorize issues for our product and engineering teams. Use these categories: UI/UX, Performance, Feature Request, Integration, Pricing, and Other. Also rate the sentiment (Positive/Neutral/Negative) and priority (High/Medium/Low). Use JSON format in your response, as in the following example:

```
<example>
Feedback: The new dashboard is a mess! It takes forever to load, and I cant find the export button. Fix this ASAP!
{
    "feedback": "The new dashboard is a mess! It takes forever to load, and I cant find the export button. Fix this ASAP!",
    "category": "UI/UX",
    "sentiment": "Negative",
    "priority": "High"
}
</example>
```

Feedback: Your pricing is ridiculous! $99/mo for basic features? I'm switching to a competitor.

## Output (gemma-3-4b-it)

```
{
    "feedback": "Your pricing is ridiculous! $99/mo for basic features? I'm switching to a competitor.",
    "category": "Pricing",
    "sentiment": "Negative",
    "priority": "High"
}
```
