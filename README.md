# LISTEN-prototype

## Links to demo:
- [mpox](https://mpox.streamlit.app)
  - [Figure 1](figs/user_location_gt5_vert.html)
- [HPV](https://hpv.streamlit.app/)
- [Measles](https://measles.streamlit.app/)

## Evaluation

- [Datasets](data) that can be used for model evaluation

<details>

<summary>Q/A</summary>

<details>

  <summary>Future work?</summary>

  Evaluate on large datasets, e.g.: 
  - https://huggingface.co/datasets/allenai/c4

</details>


<details>

<summary>Q: How to determine context length? (aka how to calculate token size of your prompt?)</summary>

Option 1: https://platform.openai.com/tokenizer

Option 2: Callculate with Python `tiktoken` package:

```
import tiktoken

# Use a tokenizer compatible with LLaMA/Gemma models, such as llama2 tokenizer
enc = tiktoken.get_encoding("cl100k_base")  # Use this as a general approximation

with open('your_prompt.txt', 'r') as f:
    text = f.read()
tokens = enc.encode(text)
print(f"Token count: {len(tokens)}")
```

</details>

</details>
