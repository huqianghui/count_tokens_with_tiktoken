## count_tokens_with_tiktoken

相比较于gpt3.5 和gpt-4-turbo，gpt-4o模型，很重要的一个更新就是变更了编码集。
从原来的cl100k_base 变成了o200k_base。
<img width="743" alt="Chinese_Tokenizer" src="https://github.com/user-attachments/assets/770f20c9-9fbb-44c1-b3ea-dd9d5ee1aa1c">

从图片中我们可以看出o200k_base对中文优化了很多。
其中对一个token：

token1： 你好

token2： 世界

token3： ，你

token4： 叫什么

token 5： 名字。


Try a pip install --upgrade tiktoken 

against your python environment.

可以得到，最新的embedding 模型也是cl100k_base.

[tiktokne-model-encoding](https://github.com/openai/tiktoken/blob/main/tiktoken/model.py#L20)

MODEL_TO_ENCODING: dict[str, str] = {

    # chat

    "gpt-4": "cl100k_base",
    
    "gpt-3.5-turbo": "cl100k_base",
    
    "gpt-3.5": "cl100k_base",  # Common shorthand
    
    "gpt-35-turbo": "cl100k_base",  # Azure deployment name
    
    # base
    
    "davinci-002": "cl100k_base",
    
    "babbage-002": "cl100k_base",
    
    # embeddings
    
    "text-embedding-ada-002": "cl100k_base",
    
    "text-embedding-3-small": "cl100k_base",
    
    "text-embedding-3-large": "cl100k_base",
    
    # DEPRECATED MODELS
    
    # text (DEPRECATED)
    
    "text-davinci-003": "p50k_base",
    
    "text-davinci-002": "p50k_base",
    
    "text-davinci-001": "r50k_base",
    
    "text-curie-001": "r50k_base",


但是gpt-4o随着编码集的提升，对应的语言的token数量都有所优化减少，特别是小语种优化的程度更多。

通过引用两个测试集合，来验证对中文简体和中文繁体的测试，来验证相应的结果。

结论与官方纰漏的很接近。


## The o200k_base Tokenizer 

The o200k_base tokenizer is a new tokenization algorithm that forms the backbone of the GPT-4-o model. Tokenization is a critical process in natural language processing that involves breaking down text into smaller units called tokens. These tokens can be words, subwords, or even characters, depending on the tokenizer's design. 

The o200k_base tokenizer represents an evolution in this process, designed to be faster and more efficient than its predecessors. It allows GPT-4-o to process and generate language at speeds that were previously unattainable. 

## Features and Capabilities 

Multimodal Inputs and Outputs: GPT-4-o accepts and emits a variety of data types, setting it apart from earlier models that were limited to text. This makes it an "omni" model, capable of more complex tasks that mirror human interaction with various forms of data. 

Improved Token Generation Speed: GPT-4-o is reported to generate tokens twice as fast as GPT-4 Turbo, enhancing its efficiency and making it suitable for real-time applications. 

Cost-Effectiveness: Despite its advanced capabilities, GPT-4-o is more affordable than its predecessors. The API costs have been significantly reduced, making it accessible for a broader range of users and developers. 

Enhanced Vision Capabilities: Compared to previous models, GPT-4-o has improved vision capabilities, allowing it to handle tasks involving image recognition and manipulation with greater finesse. 


## Conclusion 

The GPT-4-o model with the o200k_base tokenizer is a testament to OpenAI's commitment to advancing AI technology. By enhancing speed, reducing costs, and expanding capabilities, GPT-4-o stands to democratize access to cutting-edge AI tools and pave the way for innovative applications that were once the realm of science fiction. As we stand on the brink of this new AI era, it is clear that OpenAI's GPT-4-o is not just a technological milestone but also a harbinger of a future where AI and human creativity converge in exciting and transformative ways. 

 
