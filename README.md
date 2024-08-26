### What is a Tokenizer?
A tokenizer is a software component that breaks down text into smaller units called tokens. These tokens can be words, characters, or subwords.

### How does a Tokenizer work?
A tokenizer typically works by applying a set of rules to the input text.

### BPE Tokenizer
BPE (Byte Pair Encoding) is a type of tokenizer that is particularly well-suited for languages with complex scripts, such as Hindi.

### How did you build this Llama Hindi Tokenizer?
We built this Llama Hindi Tokenizer by combining the AI4Bharat corpus with the Llama 2 32k Tokenizer.

### Tokenizer Architecture
1) Base Architecture: Llama 2 Tokeniser
2) Input: Hindi text
3) Tokenization: BPE Tokenizer
4) Vocabulary: Learned from the AI4Bharat corpus
5) Output: Sequence of tokens

# How to use this Tokeniser
1) Download `special_tokens_map.json`, `tokenizer.model` and `tokenizer_config.json` to a folder.
2) Create your Notebook in the parent directory and use this code below to use the tokeniser to finetune a new Llama 2 model using a dataset or something else
```python
from transformers import LlamaForCausalLM, LlamaTokenizer

tokenizer = LlamaTokenizer.from_pretrained("Path_to_the_downloaded_tokeniser_folder")
model = LlamaForCausalLM.from_pretrained("meta-llama/Llama-2-7b-hf")

```
