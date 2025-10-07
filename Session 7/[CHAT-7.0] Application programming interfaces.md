# [CHAT-7.0] Application programming interfaces

---

## Application programming interface (APIs)

- An **application programming interface** (API) is a way for two or more computer programs or components to communicate with each other. 

- The main players in the LLM arena (OpenAI, Anthropic, Meta, Google, etc) offer API platforms which allow us to use their models in a remote way. 

- For proprietory models, this is the only way you have to include the tasks performed by the model in your programs.

- The remote connection with an LLM API is managed by means of an API key and a **software development kit** (SDK). The API key is given by the provider through its website. Before asking for the API key, you must register, providing a user name and a password. The SDK can be a **Pyhton** package, but other languages like Java or node.js are available in most cases.

---

## Signing up

- E-mail account.

- Password.

- API keys.

- Terms of use.

---

## Technicalities

- Messages list.

- Roles: system, user, assistant and tools.

- Response structure.

---

## The OpenAI API

- The OpenAI API provides an interface to **OpenAI** models. The Python SDK is a package called `openai` that you can install, *e.g*. with `pip install openai`. After importing the package, you create a client using your API key:

```
! pip install openai
from openai import OpenAI
client = OpenAI(api_key = 'OPENAI_API_KEY')
model_name = 'gpt-4o-mini'
query = 'Who is Miguel Ángel Canela?'
message = [{'role': 'user', 'content': query}]
response = client.chat.completions.create(messages = message, model = model_name)
print(response.choices[0].message.content)
```

---

## The Gemini API

- The Gemini API provides an interface to **Google Gemini** models. The Python SDK is a package called `google.generativeai` that you can install, *e.g*. with `pip install google-genai`. After importing the package, you create a client using your API key:

```
! pip install google-genai
from google import genai
client = genai.Client(api_key = 'GOOGLE_API_KEY')
model_name = 'gemini-2.5-flash'
query = 'Who is Miguel Ángel Canela?'
response = client.models.generate_content(contents = query, model = model_name)
print(resp1.text)
```

---

## The Groq API

- The Groq API provides an interface to open source models hosted by **Groq**. The Python SDK is a package called `groq` that you can install, *e.g*. with `pip install qroq`. After importing the package, you create a client using your API key:

```
! pip install groq
from groq import Groq
client = Groq(api_key = 'GROQ_API_KEY')
model_name = 'openai/gpt-oss-120b'
query = 'Who is Miguel Ángel Canela?'
message = [{'role': 'user', 'content': query}]
response = client.chat.completions.create(messages = message, model = model_name)
print(response.choices[0].message.content)
```
---

## The LM Studio API

- LM Studio can be used as a local LLM API server. provides an interface to open source models downloaded to a local instance of **LM Studio**. In the LM Studio's Developer tab, you have to set the status as "Running" and to load the model (previously downloaded to your local machine).

The Python SDK is a package called `lms` that you can install, *e.g*. with `pip install lms`. The recommended practice is to follow the **OpenAI compatibility mode**, which means that you can use the same code as in the OpenAi API. To do this, you need the package `openai`, which you can install, *e.g*. with `pip install openai`. with  the After importing the packages, you create a client using with a API key:

```
! pip install lms openai
import lmstudio as lms
from openai import OpenAI
client = OpenAI(base_url = 'http://localhost:1234/v1', api_key = 'lm-studio')
model_name = 'gemma-3-4b-it'
query = 'Who is Miguel Ángel Canela?'
message = [{'role': 'user', 'content': query}]
response = client.chat.completions.create(messages = message, model = model_name)
print(response.choices[0].message.content)
```
---
