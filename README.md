# LISTEN-prototype


- [HPV](https://hpv.streamlit.app/)
- [Measles](https://measles.streamlit.app/)

[Figure 1](figs/user_location_gt5_vert.html)


<details>
  <summary>Q/A</summary>

<details>

<summary>Q: How to determine context length? (aka how to calculate token size of your prompt?)</summary>

Option 1: https://platform.openai.com/tokenizer

Option 2: Code:

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
