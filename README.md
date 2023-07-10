## gpt-3.5-turbo_OpenAI API Request
 Originally designed for discord bot. An OpenAI API Requesting mode. For gpt-3.5-turbo model.

### Function
`AIChat(fileName_GPT_APIdata,fileName_context,user_name,user_msg)`  
> 每個參數都是必要的

`fileName_GPT_APIdata` 傳入存放API的檔案，已將範例文件置於本專案目錄下。  
`fileName_context` 傳入存放上下文的檔案，已將範例文件置於本專案目錄下。  
`user_name` 傳入使用者名稱  
`user_msg` 傳入使用者輸入的訊息  

### Output
```python
    {
        "content" : str(completion['choices'][0]['message']["content"]),
        "finish_reason" : str({completion['choices'][0]['finish_reason']})[2:-2]
    }
```
> type: <class 'dict'>  
  
`"finish_reason"`: 根據官方文件說明如下：  
  
Every response will include a finish_reason. The possible values for finish_reason are:  
  
**stop**: API returned complete message, or a message terminated by one of the stop sequences provided via the stop parameter  
**length**: Incomplete model output due to max_tokens parameter or token limit  
**function_call**: The model decided to call a function  
**content_filter**: Omitted content due to a flag from our content filters  
**null**: API response still in progress or incomplete  
  
詳見：<https://platform.openai.com/docs/guides/gpt/chat-completions-api>
 
