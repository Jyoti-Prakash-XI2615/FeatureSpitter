# FeatureSpitter

# Challenge Instructions

The purpose of this challenge is to assess your technical experience and your working methodology.

You should create a repository where you periodically commit/push your progress, so later we can have access and perform a **code-review**.

You can put your challenge project code in any public Git repository that allows for code-review with **Pull Requests** or similar (eg.: GitHub, GitLab, etc.), and at the end you provide your interviewer with the link for the PR you created.

There is no need to host/deploy your running project to anywhere, we want to be able to run it directly from its source code in the Git repository.

Your challenge will be evaluated in several aspects such as:

* Architecture
* Code readability and maintainability
* Documentation
* Tests
* Reliability and Error Handling
* Performance
* Design Decision-making

### Data Sources

In this challenge it is requested that you create a small full-stack app.

The idea of this app is to be an aggregator/centralizer of all store related information in the ficticious company called _ACME Corporation_.

The information regarding these stores can be found in 3 different places:

* `GET /v1/stores/` Is the "almost central" API endpoint that contains most data regarding ACME stores.

* `GET /other/stores_and_seasons` A different endpoint which provides a list of the active stores and the season names of which they are operational. ACME divides the year in two halves called seasons, first half (denoted as H1) and second half (H2), followed by the year. For eg.: H2 21 is the second half of year 2021.

* `extra_data.csv` A CSV file containing some extra properties regarding the existing stores.

The documentation regarding these endpoints can be found [here](http://134.209.29.209).

Like in any real-world scenario, beware that these data sources are sometimes faulty in their reliability and data consistency.

Also, all endpoints require a token to be sent in an HTTP header called `apiKey`. You can request this token to your interviewer.

### The App

Given this, your app should provide the following features:

* It should import and centralize all the information from the 3 sources described above, into a single place (a database for eg.)

* It should provide a frontend app that allows the user to efficiently visualize the store information, for eg. using a paginated table.

* The user should be able to edit the store names using the frontend. This is the only editable field.

* The user must be able to search stores by their names (full or partial name search)

**Bonus Features:**

* The frontend must provide a download button that will serve the user a CSV file containing all the stores and their data (basically an export to CSV).

* Make the import happen every hour, so that your app always provides the user with the most up-to-date store data (for all the 3 endpoints)

### Tech Stack

The challenge needs to be implemented using the following technologies if applicable:

**Backend**: Kotlin, Postgres for the DB if needed, and any other libs or frameworks you find necessary

**Frontend**: Vue.js with TS, and any other libs you find necessary

**Tools**: Git (Gitflow), Docker

**Deploy**: The project must be able to fully start at `http://localhost:8080` using the following one-line CLI command:
`docker-compose up`

Depending on the developer's experience, this challenge duration can range from a few hours up until one week.

### Good luck, and have fun! :)
