# Secret-Message 
[![PyPI](https://img.shields.io/pypi/v/secret-message?color=blueviolet&label=Web-version%20&logo=appveyor&style=plastic)](https://secret-msg.onrender.com/)

[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/PurpleBird7613/secret_msg?color=inactive&label=GitHub)](https://github.com/PurpleBird7613/secret_msg)

[![PyPI](https://img.shields.io/pypi/v/secret-message?color=blue&label=python-package&style=plastic)](https://pypi.org/project/secret-message/)

Create and share Messages in a  **Secret** way.

This WebApp allows users to create and share various types of messages, including text, images, videos, files, and documents, with the added option to protect them with a password. It offers features of message sharing with a unique link for a message. This WebApp is user-friendly and accessible from any device with an internet connection, making it easy and convenient to use.

## Install
```python
pip install secret-message
```

## Import the package
```python
import secret_message

# ------OR------

#from secret_message import create,show,history
```

## Create a Message:
```python
import secret_message as message 

message.create("<USERNAME>","<YOUR_MESSAGE>","<Image_Path(Only Image)>" or None,"<PASSWORD_FOR_THE_MESSAGE>")
```
For creating a message it takes only 4 parameters:
```
1. Username - Just add your name as username(No registration stuff is required.)
	
2. Text Message - You can add your message

3. Image - You can add image as a message, just add image path here or just add None if you don't want to add an image
	
4. Message Password = Create a password of your choice for the message you are creating 
```

• Output:
```python
{
  "id": <YOUR_MESSAGE_ID>,
  "text_message": "<YOUR_MESSAGE>",
  "image": "<YOUR_IMAGE>",
  "password": "<YOUR_MESSAGE_PASSWORD>",
  "web_msg_link": "<YOUR_MESSAGE_LINK_FOR_WEB>",
  "api_msg_link": "<YOUR_MESSAGE_LINK_FOR_API_CALL>"  
}
```
```
web_message_link - Using this link anyone will be able to access your message from web[Any web browser].

api_msg_link - Using this link anyone will be able to access your message by api call 

image - Can only be seen from web_message_link
```

## Show/Read Message
```python
import secret_message as message

message.show("<USERNAME>","<MESSAGE_LINK>","<PASSWORD_OF_THE_MESSAGE>")
```
For showing or reading someone else's messages,it takes only 3 parameters:
```
1. Username - Just add your name as username(No registration stuff is required.)
	
2. Message Link - This link must the "api_msg_link" in order to read or view the message.
	
3. Password - This must be the exact password for the message created by other user.
```
	
• Output:
```python
{
  "text_message" : "<USER'S_MESSAGE>",
  "image" : "<USER'S_IMAGE>",
  "web_msg_link" : "<USER'S_MESSAGE_LINK_FFOR_WEB>"
}
```

## Message History 
```python
import secret_message as message

message.history("<Username>")
```
For getting history of your messages,it takes only 1 parameter:
```
1. Username - Just add your name as username(No registration stuff is required.)
```

• Output:
```python
{
  "Messages": [
  	{
  	   "id": "<YOUR_MESSAGE_ID>",
  	   "text_message": "<YOUR_MESSAGE>",
  	   "image": "<YOUR_IMAGE>",
  	   "password": "<YOUR_MESSAGE_PASSWORD>",
  	   "web_msg_link": "<YOUR_MESSAGE_LINK_FOR_WEB>",
  	   "api_msg_link": "<YOUR_MESSAGE_LINK_FOR_API_CALL>" 
  	},
  	........,
  ]
}
```
