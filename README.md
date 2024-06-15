## count_tokens_with_tiktoken

相比较于gpt3.5 和gpt-4-turbo，gpt-4o模型，很重要的一个更新就是变更了编码集。
从原来的cl100k_base 变成了o200k_base。

随着编码集的提升，对应的语言的token数量都有所优化减少，特别是小语种优化的程度更多。

通过引用两个测试集合，来验证对中文简体和中文繁体的测试，来验证相应的结果。

结论与官方纰漏的很接近。


The o200k_base Tokenizer 

The o200k_base tokenizer is a new tokenization algorithm that forms the backbone of the GPT-4-o model. Tokenization is a critical process in natural language processing that involves breaking down text into smaller units called tokens. These tokens can be words, subwords, or even characters, depending on the tokenizer's design. 

The o200k_base tokenizer represents an evolution in this process, designed to be faster and more efficient than its predecessors. It allows GPT-4-o to process and generate language at speeds that were previously unattainable. 

Features and Capabilities 

Multimodal Inputs and Outputs: GPT-4-o accepts and emits a variety of data types, setting it apart from earlier models that were limited to text. This makes it an "omni" model, capable of more complex tasks that mirror human interaction with various forms of data. 

Improved Token Generation Speed: GPT-4-o is reported to generate tokens twice as fast as GPT-4 Turbo, enhancing its efficiency and making it suitable for real-time applications. 

Cost-Effectiveness: Despite its advanced capabilities, GPT-4-o is more affordable than its predecessors. The API costs have been significantly reduced, making it accessible for a broader range of users and developers. 

Enhanced Vision Capabilities: Compared to previous models, GPT-4-o has improved vision capabilities, allowing it to handle tasks involving image recognition and manipulation with greater finesse. 
