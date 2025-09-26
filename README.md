School Student Information
This is a single-page web application designed to display student information by pulling data from a Google Sheet. It features a responsive design, a searchable student list, and dedicated pages for individual student details.

Features
Live Data: Fetches student information in real-time from a Google Sheet via a Google Apps Script API.

Search Functionality: Filter students by name or ID using a dynamic search bar.

Individual Student Pages: Click on a student's name to view their full details.

Single-Page Application (SPA): The entire application is contained within a single index.html file, making it easy to deploy on platforms like GitHub Pages.

Modern UI: Styled using Tailwind CSS for a clean and responsive look.

Setup & Deployment
To get this application running, you need to set up a Google Sheet and a Google Apps Script to act as your data API.

1. Prepare Your Google Sheet
Create a new Google Sheet and name it Sheet1. The first row must contain the following headers exactly as written:

id

name

grade

email

phone

address

major

imageUrl

Populate the rows below with your student data. The imageUrl can be a link to a profile picture or a placeholder image URL.

2. Set Up the Google Apps Script
Go to the Google Apps Script dashboard and create a new project.

Copy the Apps Script code from the previous instructions into the Code.gs file.

Save the script and then click Deploy > New deployment.

Choose Web app as the type.

Set "Who has access" to "Anyone".

Click Deploy and copy the provided URL. This is your API endpoint.

3. Update the Website File
Open the index.html file in a text editor and find the following line:

const GOOGLE_APPS_SCRIPT_URL = 'YOUR_GOOGLE_APPS_SCRIPT_URL_HERE';

Replace the placeholder URL with the URL you copied from your Google Apps Script deployment.

4. Deploy to GitHub Pages
Create a new public repository on GitHub.

Upload the updated index.html file to the root of your repository.

Go to your repository's settings, navigate to the Pages section, and select the main branch as your source.

Your website will be live at https://<your-username>.github.io/<your-repo-name>/.

Technologies Used
HTML5: For the page structure.

Tailwind CSS: For all styling and responsive design.

JavaScript (ES6+): To handle data fetching, search functionality, and page rendering.

Google Apps Script: As a serverless backend to serve data from the Google Sheet.
