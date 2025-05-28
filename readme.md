# Nationality Predictor Web App

This is a simple web application that predicts the likely nationality (country of origin) of a given name using an external API. Built with basic HTML, CSS, and JavaScript, this project demonstrates how to interact with third-party APIs, process JSON responses, and dynamically update the user interface.

## Features

- User inputs any name into the form.
- The app fetches data from the [Nationalize.io API](https://nationalize.io/).
- Displays a list of countries with associated probabilities indicating the likelihood of the name being from that nationality.
- Handles user input and displays errors gracefully.

---

##JavaScript Functionality (Core Logic)

The JavaScript logic (script.js) is the core component that powers the app's interaction with the *Nationalize.io API*.

### Workflow:

1. *Form Submission Handling:*
   - An event listener is added to capture the submit event on the form.
   - event.preventDefault() is used to stop the default form submission behavior (i.e., page reload).

2. *API Request:*
   - It sends a GET request to https://api.nationalize.io?name=<entered_name>.
   - The name entered by the user is appended as a query parameter.

3. *Data Processing:*
   - The response from the API is in JSON format.
   - It contains an array of country codes and associated probabilities.

4. *Dynamic DOM Manipulation:*
   - The script dynamically creates and inserts HTML elements into the #nationality-results div.
   - If an error occurs or no data is found, a user-friendly message is shown.

5. *Error Handling:*
   - Network or API errors are caught using try...catch and displayed in the #error-message section.

---

## Technologies Used

- *HTML5* – Page structure and input form
- *CSS3* – External stylesheet for styling (style.css)
- *JavaScript (Vanilla)* – Core logic and API interaction

---

## API Used

- *[Nationalize.io](https://nationalize.io/)*  
  A free API that predicts the nationality of a name based on a large dataset of name occurrences per country.

---

## Getting Started

1. Clone this repository:
   ```bash
   git clone https://github.com/Angie-commits/name-analyzer.git