# [CHAT-5.2] Product review summary

## Input

Your task is to extract relevant information from a product review from an ecommerce site to give feedback to the Marketing department.

From the review below, extract the information relevant to product quality and price. Present your analysis according to following guidelines:
(a) Maximum length: 30 words.
(b) Language: Spanish.

```
<review>
A qualidade JBL é algo indiscutível, ótima qualidade de som, acabamento impecável, funcionamento perfeito. Os produtos JBL são caros, mas valem a pena, pelo preço poderiam fornecer um carregador. Uso em pequenos eventos como churrasco em família ou amigos e ela atende perfeitamente. A bateria não é das melhores, entrega umas 4 a 5 horas de uso moderado. Seu carregamento é bem rápido. O atendimento da loja me surpreendeu. Adorei a aquisição.
</review>
```

## Output (ChatGPT)

El producto funciona bien y es resistente, pero el precio resulta elevado en comparación con la calidad percibida.

---

## Input

Your task is to extract relevant information from a product review from an ecommerce site to give feedback to the Marketing department.

From the review below, extract the information relevant to product quality and price. Present your analysis in Spanish, as a JSON object with keys "quality" and "price". Use no more than 10 words for each key.

```
<review>
A qualidade JBL é algo indiscutível, ótima qualidade de som, acabamento impecável, funcionamento perfeito. Os produtos JBL são caros, mas valem a pena, pelo preço poderiam fornecer um carregador. Uso em pequenos eventos como churrasco em família ou amigos e ela atende perfeitamente. A bateria não é das melhores, entrega umas 4 a 5 horas de uso moderado. Seu carregamento é bem rápido. O atendimento da loja me surpreendeu. Adorei a aquisição.
</review>
```

## Output (ChatGPT)

```
json
{
  "quality": "Ótima calidad de sonido, batería limitada",
  "price": "Caro pero vale la pena, sin cargador incluido"
}
```
---

## Input

Your task is to extract relevant information from a product review from an ecommerce site to give feedback to the Marketing department.

From the review below, extract the information relevant to product quality and price. Present your analysis in Spanish, as a JSON object with keys "quality" and "price". 

```
<review>
A qualidade JBL é algo indiscutível, ótima qualidade de som, acabamento impecável, funcionamento perfeito. Os produtos JBL são caros, mas valem a pena, pelo preço poderiam fornecer um carregador. Uso em pequenos eventos como churrasco em família ou amigos e ela atende perfeitamente. A bateria não é das melhores, entrega umas 4 a 5 horas de uso moderado. Seu carregamento é bem rápido. O atendimento da loja me surpreendeu. Adorei a aquisição.
</review>
```

## Output (ChatGPT)

```
json
{
  "quality": "La calidad del producto es excelente: sonido de alta calidad, acabado impecable y funcionamiento perfecto. Es adecuado para eventos pequeños y cumple bien su función. Sin embargo, la batería podría ser mejor, ya que dura entre 4 y 5 horas con uso moderado, aunque se carga rápidamente.",
  "price": "El producto es caro, pero vale la pena por lo que ofrece. El cliente considera que, dado el precio, debería incluir un cargador."
}
```
---

## Input

You are an AI assistant helping the Marketing department to summarize the information extracted from product reviews.

You are provided with a JSON object with the keys "quality" and "price". Your task is to shorten the value of each key to no more than 10 words.

```
{
  "quality": "El producto tiene una calidad de sonido excelente, con un acabado impecable y funcionamiento perfecto. Cumple bien en eventos pequeños como reuniones familiares o con amigos. Sin embargo, la batería es un punto débil, ya que solo dura entre 4 y 5 horas con uso moderado, aunque el tiempo de carga es rápido.",
  "price": "Los productos JBL son considerados caros, aunque el cliente señala que valen la pena. Se menciona que, por el precio, deberían incluir un cargador."
}
```

## Output (ChatGPT)

```
{
"quality": "Excelente sonido y acabado, batería limitada pero carga rápida.",
"price": "Caro, vale la pena, debería incluir cargador."
}
```
---

## Input

Your task is to extract relevant information from a product review from an ecommerce site to give feedback to the Marketing department.
Given a review:

1. Extract the information relevant to product quality and price. 

2. Write that information in Spanish.

3. Summarize the information about quality and price in no more than 10 words for each topic.

4. Present the information as a JSON object with keys "quality" and "price". 

```
<review>
A qualidade JBL é algo indiscutível, ótima qualidade de som, acabamento impecável, funcionamento perfeito. Os produtos JBL são caros, mas valem a pena, pelo preço poderiam fornecer um carregador. Uso em pequenos eventos como churrasco em família ou amigos e ela atende perfeitamente. A bateria não é das melhores, entrega umas 4 a 5 horas de uso moderado. Seu carregamento é bem rápido. O atendimento da loja me surpreendeu. Adorei a aquisição.
</review>
```

## Output (ChatGPT)

```
json
{
  "quality": "Excelente sonido, acabado impecable, batería limitada, carga rápida.",
  "price": "Productos caros, valen la pena, falta cargador incluido."
}
```
