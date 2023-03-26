---
layout: post
title: Building a Facebook Messenger Quotebot with Python Flask
---

Facebook Messenger is one of the most popular messaging platforms with millions of active users. In recent years, businesses and individuals have started to use chatbots to automate their communication with customers and friends. Chatbots can help save time and provide quick responses to common questions.

Alfred - the Quotebot is a simple automated bot that can respond with quotes and images to keywords entered by the user. The bot uses the Facebook Send/Receive API to handle incoming messages and Flask to handle web requests.

**Implementation**

The first step in building the Quotebot is to create a Facebook Page and a Facebook App. The Facebook App will be used to access the Send/Receive API. Once the App is created, we need to generate an access token that will be used to authenticate requests to the API.

Next, we will create a Python Flask web application to handle incoming messages from Facebook. We will use the Flask-RESTful library to create a RESTful API endpoint that will handle incoming messages. The endpoint will parse the incoming message and extract any keywords that match the list of quotes we have in our database.

The Quotebot will then use a simple algorithm to select a random quote from a website and send it back to the user along with an image related to the quote.

Finally, we will deploy our Flask application to a hosting service like Heroku.