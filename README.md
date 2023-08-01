# Github 條件搜索，目標---找到優秀項目下的主要貢獻工程師(現在先尋找方向)

## 純關鍵字+star數/fork數
- LLM（11.5K repo）
    - 最多 57K stars 
        - [repo: langChain](https://github.com/langchain-ai/langchain)---57K stars
        - [repo: gpt_academic](https://github.com/binary-husky/gpt_academic)---39K stars
        - [repo: milvus](https://github.com/milvus-io/milvus)---2.4K stars
    - 最多 7.5K forks（[repo: langChain](https://github.com/langchain-ai/langchain)）
        - [repo: langChain](https://github.com/langchain-ai/langchain)---7.5K forks
        - [repo: gpt_academic](https://github.com/binary-husky/gpt_academic)---5.1K forks
        - [repo: Flowise](https://github.com/FlowiseAI/Flowise)---4.5K forks

- GLM(General Language Model)（4.9K repo）
    - 最多 39K stars
        - [repo: gpt_academic](https://github.com/binary-husky/gpt_academic)---39K stars
        - [repo: ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)---32.8K stars
        - [repo: langchain-ChatGLM](https://github.com/chatchat-space/langchain-ChatGLM)---12.9K stars
    - 最多 5.1K forks（[repo: gpt_academic](https://github.com/binary-husky/gpt_academic)）
        - [repo: gpt_academic](https://github.com/binary-husky/gpt_academic)---5.1K forks
        - [repo: ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)---4.4K forks
        - [repo: langchain-ChatGLM](https://github.com/chatchat-space/langchain-ChatGLM)---2K forks
- Large language model（2.1K repo）
    - 最高25.6K stars
        - [repo: FastChat](https://github.com/lm-sys/FastChat)---25.6K stars
        - [repo: MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4)---21.9K stars
        - [repo: text-generation-webui](https://github.com/oobabooga/text-generation-webui)---20K stars
    - 最多 5.1K forks
        - [repo: FastChat](https://github.com/lm-sys/FastChat)---3K forks
        - [repo: text-generation-webui](https://github.com/oobabooga/text-generation-webui)---2.6K forks
        - [repo: MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4)---2.6K forks
- GPT（78.9K repo）
    - 最高 145K stars
        - [repo: Auto-GPT](https://github.com/Significant-Gravitas/Auto-GPT)---145K stars
        - [repo: funNLP](https://github.com/fighting41love/funNLP)---53.3K stars
        - [repo: gpt4all](https://github.com/nomic-ai/gpt4all)---50.1K stars
    - 最多 36.2K forks
        - [repo: ChatGPT-Next-Web](https://github.com/Yidadaa/ChatGPT-Next-Web)---36.2K forks
        - [repo: Auto-GPT](https://github.com/Significant-Gravitas/Auto-GPT)---31.4K forks
        - [repo: funNLP](https://github.com/fighting41love/funNLP)---13.1K forks
### 思考
- GPT這個關鍵字搜出來的排名，repo都比較偏應用層面的，所以應該擴散的很快（？
- 應該要找的是，像是langChain一樣是許多應用的dependency。這樣一來，其實有點像page rank的算法？該repo是多少repo的dependency、然後那些dependency中有多少的star/fork數很多。但感覺現在要來寫這個算法有點麻煩。。。
- 用API來call的話，最多一次獲取100筆資料。以`LLM`關鍵字為例，總共有一萬多筆資料，所以應該是要call個100多次api才能拿到所有資料。另外，60 requests per hour
    - 簡單api使用：[link](https://colab.research.google.com/drive/12V2G9VlHoaTjN2LlVzUhNIwh0y0lsp3E?usp=sharing)
- forks 和  stars 數量的比值，可以代表什麼呢？stars算是「覺得這個repo很讚」，來點一下；而fork是想要來操作看看該repo。如果把 forks/stars，代表每1個按star的人，有多少會fork下來操作看看。
    - 是不是可以查看，langChain、LlamaIndex等優秀開源庫，他們的forks/stars的比值，代表優秀項目的 forks/stars 區間？

- 不過，主要是要找開發者，好像不用太糾結這個項目的有趣度有多高？
