# OPENAI-ChatGPT

Step:1 Start shape: configured with No Data. 
Help: https://help.boomi.com/bundle/integration/page/r-atm-Start_shape.html

Step:2 Message shape: holds the request payload for the ChatGPT API.    
Help: https://help.boomi.com/bundle/integration/page/r-atm-Message_shape.html

{
  "model": "text-davinci-003",
  "prompt": "Say this is a test",
  "max_tokens": 7,
  "temperature": 0,
  "top_p": 1,
  "n": 1,
  "stream": false,
  "logprobs": null,
  "stop": "\n"
}

<img width="570" alt="image" src="https://user-images.githubusercontent.com/123489168/214572542-d203869c-6f83-4200-8aa8-5036c79c4194.png">


3. HTTP Client Connector shape:  configured to send request to OpenAI.
The Connector has two components, the Connection and the Operation
	Connection: This is configured with the OpenAI URL and the API Key for the password for authentication. 

URL: https://api.openai.com/v1/completions
For Token you need to generate new token using below link and check the screenshot for reference.
https://beta.openai.com/account/api-keys

![image](https://user-images.githubusercontent.com/123489168/214614708-e2ce1d68-134f-4de8-ac7f-62db40b9fa50.png)


	Operation: This is configured with JSON request and response profiles.  Content Type = application/json, HTTP Method = POST, Resource Path set to completions.

Help: https://help.boomi.com/bundle/connectors/page/r-atm-HTTP_Client_connector.html

<img width="721" alt="image" src="https://user-images.githubusercontent.com/123489168/214614941-e56ad700-6fad-44b3-8e2b-2ffd35302de0.png">

