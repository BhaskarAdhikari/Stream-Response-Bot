Chatbot using OpenAI API

Overview
This Python project demonstrates how to build a simple chatbot using the OpenAI API. It includes functions for both standard and streaming responses from OpenAI's GPT-4 model. The code uses the openai library to send user prompts and receive responses from the API.

Features
Basic API Setup: Demonstrates how to connect to the OpenAI API using an API key.
Standard Response: A function to send a prompt and receive a full response at once.
Streaming Response: A function to receive responses in chunks, creating a more interactive experience.
Conversation History: Stores the assistant's responses for potential future use.
Requirements
Python 3.12.7 or later
OpenAI Python library
Install the OpenAI library if you haven’t already:

bash
Copy
Edit
pip install openai
Setup
Obtain an API key from OpenAI.
Set your API key as an environment variable:
bash
Copy
Edit
export OPENAI_API_KEY='your_api_key_here'
Ensure that the openai library is installed.
Usage
1. Getting a Standard Response
The get_chat_completion function sends a prompt to the GPT-4 model and returns a single response.

python
Copy
Edit
result = get_chat_completion("Say this is a test")
print(result)
Example Output:

bash
Copy
Edit
This is a test.
2. Getting a Streaming Response
The stream_chat_response function sends a prompt to the GPT-4 model and streams the response back in real-time.

python
Copy
Edit
stream_chat_response("Tell me a joke")
Example Output:

vbnet
Copy
Edit
Why don't skeletons fight each other?
They don't have the guts.
3. Running an Interactive Chat
This code block enables an interactive chat session:

python
Copy
Edit
while True:
    user_input = input("You: ")
    if user_input.lower() == "exit":
        break
    stream_chat_response(user_input)
To exit the chat, type:

bash
Copy
Edit
exit
Customization
Temperature: Controls creativity (0 to 1). Increase for more creative responses.
Model: Change "gpt-4o" to another model if needed.
Error Handling
If an error occurs, the functions will print an error message instead of crashing.

Notes
Make sure your API key is valid and has enough quota.
Use stream=True for real-time response streaming.
This is a simple yet powerful starting point for building chatbots using OpenAI's API. Feel free to expand and customize the code!







