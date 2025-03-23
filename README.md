# Web Application with Routing and Form Handling

This web application uses Python to create a server that handles routes for two HTML pages: `index.html` and `message.html`, processes forms, and stores data in a JSON format.

## Main Requirements

# Routing

Two HTML pages have been created: index.html and message.html.
Static resource handling is included (file style.css, image logo.png).
The web application runs on port 3000.

# Form Handling

The form on the message.html page works correctly, sending data (username and message).
The form data is converted into a dictionary and written to the data.json file in the following format:

json
Копировать
Редактировать
{
  "%timestamp%": {
    "username": "example",
    "message": "example message"
  }
}

# Template Page

When accessing the /read route, a Jinja2 template page is returned that displays all saved messages from the data.json file.

# 404 Error Page

In case of a 404 error, the error.html page is returned.

# Storing Messages

Messages are stored in the storage/data.json file in JSON format, where the key is the timestamp of when the message was received.

### Installation

1. Clone the repository or copy the project files.

2. Ensure that Python 3.x is installed.

3. Install the necessary dependencies:

   ```bash
   pip install jinja2
