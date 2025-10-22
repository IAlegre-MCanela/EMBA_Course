# [CHAT-5.0] Reasoning models

---

## Chain-of-Thought prompting

- **A chain of thought** (CoT) is sequence of logical steps, called **reasoning steps**, to be followed in order to arrive at an answer.

- In Chain-of-Thought prompting, we include a list of the reasoning steps in the prompt. This helps the LLM generate more accurate answers. It can combined with few-shot prompting.

--- 

## Prompt chaining

- Use a sequence of prompts to hide the model's reasoning process.

- Summarize or filter previous dialogue.

- Ask the model if it missed anything on previous passes.

- Not all tasks require in-depth thinking. Use prompt chaining judiciously to ensure the right balance of performance and **latency**.

- Summarize documents piecewise and construct a full summary recursively.

---

## In favor of chaining prompts

- Easier to test.

- Same reasons as for splitting a computer program in code chunks.

- Less tokens per prompt. This may matter, because of cost and context window issues.

- Allows skipping part of the workflow when not needed for the task.

- For complex tasks, allows to keep track of what happens out of the model.

- Allows the use of external tools.

---

## Reasoning models

- A **reasoning model** is a large language model (LLM) that has been fine-tuned to break complex problems into reasoning steps, prior to generating a final output. 

- A reasoning model builds the chain of thought by itself. This part is presented separately in some chat apps. For instance, DeepSeek encloses it between the tags `<think>` and `</think>`.

---

## Continuation

- In chat apps, most of the prompts do not require reasoning, and reasoning delays the response, so it is presented as an option. Under the hood, the choice involves choosing between two different models (possibly with ther same architecture but different parameter values).

- Reasoning involves managing very long sequences of tokens. A small reasoning model may have trouble with this.
