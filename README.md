### VOCAL QUERY

This application provides an API for transcribing audio and converting spoken commands into SQL queries using Google APIs and a generative AI model. It first transcribes real time audio submitted by users via Google’s Speech-to-Text API. Then, using the transcribed text, it generates a SQL query in PostgreSQL syntax with the help of the Google Gemini AI model. The generated query is cleaned, executed in a PostgreSQL database. 

### How to run
Setup the Server:

Navigate to the server folder:
'''
cd server
'''
Place your Google Speech-to-Text API credentials in a .json file (e.g., Google-SpeechToText-API-Credentials.json).
Create a .env file in the same directory and add the following:
plaintext
Copy code
GOOGLE_API_KEY=YOUR_GOOGLE_GEMINI_API_KEY
Set the path to the Google Speech-to-Text JSON credentials:
plaintext
Copy code
GOOGLE_APPLICATION_CREDENTIALS=Google-SpeechToText-API-Credentials.json
Update the PostgreSQL password in app.py:
python
Copy code
password="YOUR-PASSWORD"  # Replace with your actual PostgreSQL password
Run the Flask app:
bash
Copy code
python app.py
Setup the Client:

Navigate to the client folder:
bash
Copy code
cd client
Install the dependencies:
bash
Copy code
npm install
Start the client:
bash
Copy code
npm start
After completing these steps, the server should be running on the specified port, and the client application will start in development mode on a local port.

### Frontend

![Architecture of Vocal Query](Images/Frontend.png)

### Postgresql Table Creation/Automation
![Architecture of Vocal Query](Images/Tables.png)





