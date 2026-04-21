# flaskvue
Custom template for a Lightweight web stack employing [Flask](https://flask.palletsprojects.com/en/stable/) to serve a [REST API](https://developer.mozilla.org/en-US/docs/Glossary/REST) and a [Vue 3](https://vuejs.org/guide/introduction.html) front end. The Vue app consumes the API in order to communicate asychronously with the backend.

### Flask
The Flask app uses [Flask-RESTX](https://flask-restx.readthedocs.io/en/latest/) to build the API and API documentation. Flask-RESTX and [Pydantic](https://pydantic.dev/docs/) are used to validate input and return data. User authorization and session management are handled by [Flask-Login](https://flask-login.readthedocs.io/en/latest/).

In addition to the API, the Flask app serves an HTML file that contains the Vue app. The HTML file is rendered with the URL of the API, which the Vue app uses to make API requests. [TODO] The app also serves a login page. A user must be logged for the Vue app to make authorized API requests.

### Vue
The Vue app is static JavaScript that is deployed directly to the frontend without a build step. [Pinia](https://pinia.vuejs.org/introduction.html) is used for reactive state management. The Vue components call the API using `fetch` requests to interact with the backend. Flask-Login handles authorizing the API requests

The Vue app is intended to be a [single-page application (SPA)](https://developer.mozilla.org/en-US/docs/Glossary/SPA). The app loads one "main" component, and all the other components that make up the app are expected to be children of the main component. This template provides three pre-built components for page header, sidebar, and content. Components can share reactive data using Pinia. A generic Pinia data store is pre-built into this template.
