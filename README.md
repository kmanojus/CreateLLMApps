# langchain-falcon-chainlit
Simple Chat UI using Falcon model, LangChain and Chainlit


### Open Source in Action 🚀
- [Falcon](https://falconllm.tii.ae/) as Large Language model
- [LangChain](https://python.langchain.com/en/latest/modules/models/llms/integrations/huggingface_hub.html) as a Framework for LLM
- [Falcon model](https://huggingface.co/tiiuae/falcon-7b-instruct) from Huggingface Website
- [Chainlit](https://docs.chainlit.io/langchain) for deploying.

## System Requirements

You must have Python 3.10 or later installed. Earlier versions of python may not compile.

Create a virtualenv and activate it
   ```
   python3 -m venv .venv && source .venv/bin/activate
   ```

## Steps to Replicate 

1.  Input the huggingfacehub api token as follows. Get Huggingfacehub api token from this [URL](https://huggingface.co/settings/tokens). You need to create an account in Huggingface if you haven't already.
   ```
   HUGGINGFACEHUB_API_TOKEN=your_huggingface_token
   ```

   OPTIONAL - If you want to use LangSmith. Get this [URL](https://smith.langchain.com/). You need to create an account in LangSmith website if you haven't already. 
      ```
      LANGCHAIN_TRACING_V2=true
      LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
      LANGCHAIN_API_KEY="your-api-key"
      LANGCHAIN_PROJECT="your-project"
      ```

3. Run the following command in the terminal to install necessary python packages:
   ```
   pip install -r requirements.txt
   ```

4. Run the following command in your terminal to start the chat UI:
   ```
   chainlit run langchain_falcon.py --no-cache -w
   chainlit run langchain_falcon_langsmith.py --no-cache -w
   ```


