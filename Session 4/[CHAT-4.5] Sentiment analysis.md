# [CHAT-4.5] Sentiment analysis

## Input

You are expected to perform a sentiment analysis of short messages. You have to label every text as either "positive", "neutral" or "negative", based on its emotional tone. Use JSON format, as in the collection of examples that follow.

```
<example>
Message: I'm so proud of you

{"message": I'm so proud of you", "label": "positive"}
</example>

<example>
Message: What a great time to be alive

{"message": "What a great time to be alive", "label": "positive"}
</example>

<example>
Message: What a great time to be alive

{"message": "The service was amazing", "label": "positive"}
</example>

<example>
Message: They don't care about me

{"message": "They don't care about me", "label": "negative"}
</example>

<example>
Message: I hate this place

{"message": "I hate this place", "label": "negative"}
</example>

<example>
Message: I am really frustrated

{"message": "I am really frustrated", "label": "negative"}
</example>

<example>
Message: This made me think

{"message": "This made me think", "label": "neutral"}
</example>

<example>
Message: The good old days

{"message": "The good old days", "label": "neutral"}
</example>

<example>
Message: You can't ignore this

{"message": "You can't ignore this", "label": "neutral"}
</example>
```

Message: I'm excited about the new course on AI

## Output (gemma-3-4b-it)

```
{
    "message": "I'm excited about the new course on AI",
    "label": "positive"
}
```
