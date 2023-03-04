# Lark-ChatGptBot
Build a ChatGpt bot in Lark (飞书) using OpenAI's gpt-3.5-turbo model. The backend is hosted on AWS's serveless, and it is free.
For steps in Lark side, please refer to [develop-a-bot-in-5-minute](https://open.feishu.cn/document/home/develop-a-bot-in-5-minutes/create-an-app)

## Steps   
1. create a `.env` file in folder `cdkstack/`,  add the your actual variables. 
```  
DB_TABLE=lark_messages
LARK_APPID=cli_xxxx
LARK_APP_SECRET=xxxx
LARK_TOKEN=xxxx
OPENAI_API_KEY=sk-MjDVnhmnxxxx
START_CMD=/rs
```   
2. Install the AWS CDK  
`npm install -g aws-cdk`  

3. In folder `cdkstack/`
run `cdk bootstrap`  
run `cdk synth`   
run `cdk deploy`  

4. Once deply success, you can get the api endpoint from the output. 
For example, `Outputs: CdkstackStack.LarkchatApiEndpoint2DAA2EB8 = https://.....`, this is the callback url for lark. 

5. After all dones. congrats