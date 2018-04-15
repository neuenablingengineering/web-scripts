Note: all scripts are saved within barebones HTML files for ease of testing during development. To install on our website, some minor modifications need to be made. Start by navigating to the script injection interface in SquareSpace:
    1. Login to our SquareSpace account and open up enablingengineering.org 
    2. Find the target page in the sidebar
    2. Open the page's settings (gear icon appears on hover)
    3. Click "Advanced"
The text box in this window is where you paste the script. To go from the HTML files in this repository to a functional script that's installed on the page of enablingengineering.org you're targeting:
    1. Copy the relevant part of the HTML file, starting with the first <script> tag and ending with the last </script> tag.
    2. Change the line "<script src="airtable.browser.js"></script>" to "<script src="/s/airtablebrowser.js"></script>" 
        (airtablebrowser.js is uploaded as a file in our SquareSpace account, and the /s/ points it there for the source)

jQuery Fundamentals: http://jqfundamentals.com/chapter/jquery-basics

The goal of this project is to display dashboard-style information about Enabling Engineering by accessing our data with the Airtable API. To get started, it will be structured like this: 

STATS INDEX
    - a list of the dashboard pages available

ACTIVITY
    - total number of active projects (number)
    - total number of students participating 

NEEDS
    - list of current project needs (defined by field in Reports)

STUDENTS (all excluding students that have graduated)
    - total number of people in database
    - labeled pie chart of majors
    - labeled pie chart of ages 
    - bar chart showing new submissions by month
    - line plot showing cumulative registrations over time


    - total amount spent on active projects
    - reports submitted in last week
    - reports submitted to date per project

<!-- 
    the two script lines came from: http://stackoverflow.com/questions/7496789/how-to-include-jquery-in-another-javascript-file 
    which says to use the first line to pull in the jquery library from Google, which hosts it. 
    It sounds like that should expose it to the second script line.

    another documentation source here: https://www.w3schools.com/jquery/jquery_get_started.asp

    added line for airtable as source after seeing: https://github.com/kasrak/airtable-api-guide/blob/master/index.html
-->
