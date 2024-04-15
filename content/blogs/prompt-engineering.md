---
title: What developers need to know about Prompt Engineering
cover: >-
  https://res.cloudinary.com/dwphg8fpc/image/upload/v1712302788/1_Rp6x69Ruif29tN7FYDA1Ng_voymtz.jpg
date: 2023-08-20T18:30:00.000Z
tagName: Prompt engineering
position: 0
isVisible: true
description: >-
  Today we are all in the world of Generative AI, And we all are using some of
  the powerful GEN AI tools like ChatGPT, DALL-E, and GitHub Copilot.
---

1st edit\
Today we are all in the world of Generative AI, And we all are using some of the powerful GEN AI tools like [ChatGPT](https://chat.openai.com/chat), [DALL-E](https://openai.com/product/dall-e-2), and [GitHub Copilot](https://github.com/features/copilot/).\
But the most important part while working with these tools is, How efficient you are in Prompt Engineering.

![image](https://res.cloudinary.com/dwphg8fpc/image/upload/v1712302788/1_Rp6x69Ruif29tN7FYDA1Ng_voymtz.jpg "image2")

So the question is now: What is Prompt Engineering?

Prompt engineering involves deliberately crafting input instructions to steer AI language models, enhancing output precision and control while generating responses.

Here are some Basic and Advance Prompt Engineering Techniques:

1. Zero Shot Prompting
2. Few Shot Prompting
3. Chain of Thought Prompting (COT)
4. Tree of Thought Prompting (TOT)

![image](https://res.cloudinary.com/dwphg8fpc/image/upload/v1712309644/0_TgsfGF2EwppdFnaB_tt81xl.jpg "image")

Let’s discuss each Prompting Technique with code examples.
So for that we will use [OpenAI](https://platform.openai.com/overview), [Langchain](https://python.langchain.com/docs/get_started/introduction.html) (Open source framework for development of LLM based applications).

Initial setup code :

```python
import openai
import os
from langchain.llms import OpenAI
from langchain.agents import load_tools
from langchain.agents import initialize_agent

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv())

openai.api_key  = os.getenv('OPENAI_API_KEY')
def get_completion(prompt, model="gpt-3.5-turbo"):
    messages = [{"role": "user", "content": prompt}]
    response = openai.ChatCompletion.create(
        model=model,
        messages=messages,
        temperature=0, # this is the degree of randomness of the model's output
    )
    return response.choices[0].message["content"]
```

We need to Install openai, langchain and dotenv. We can use the pip command for that. And for OPEN\_API\_KEY create an account on openai, generate the key and then set it in your environment. Command to set up the OPEN\_API\_KEY in the environment.

export OPEN\_API\_KEY=sk..........
