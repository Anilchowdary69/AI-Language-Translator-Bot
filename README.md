# 🤖 AI-Language-Translator-Bot

A conversational chatbot built with **Amazon Lex V2** that detects user input and provides real-time translations using **Amazon Translate**.

## ☁️ Architecture Overview


1. **User Interface**: Amazon Lex handles the conversation and slot elicitation.
2. **Logic Layer**: AWS Lambda processes the intent and extracts slot data.
3. **AI Service**: Amazon Translate performs the language conversion.
4. **Security**: IAM Role with 'Least Privilege' permissions for `translate:TranslateText`.

## 🛠️ Features
- **Auto-Language Detection**: Users can type in any supported language.
- **Dynamic Slot Filling**: Lex ensures both the target language and the phrase are collected before fulfillment.
- **Serverless Scaling**: Built entirely on AWS Lambda and Lex for zero-server maintenance.

## 🚀 How to Deploy
1. **Lambda**: Create a function with the code in `src/` and attach the policy in `iam/`.
2. **Lex**: Import or create a bot with a `TranslateIntent`.
3. **Fulfillment**: Link the Lambda function to the Lex Bot alias.