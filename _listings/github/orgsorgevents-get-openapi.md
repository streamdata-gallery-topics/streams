---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Get Orgs Org Events
  description: List public events for an organization.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{username}/orgs:
    get:
      summary: Get Users Username Orgs
      description: List all public organizations for a user.
      operationId: list-all-public-organizations-for-a-user
      x-api-path-slug: usersusernameorgs-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: username
        description: Name of user
      responses:
        200:
          description: OK
      tags:
      - Users
      - Username
      - Orgs
  /user/orgs:
    get:
      summary: Get User Orgs
      description: List public and private organizations for the authenticated user.
      operationId: list-public-and-private-organizations-for-the-authenticated-user
      x-api-path-slug: userorgs-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      responses:
        200:
          description: OK
      tags:
      - User
      - Orgs
  /search/code:
    get:
      summary: Get Search Code
      description: Search code.
      operationId: search-code
      x-api-path-slug: searchcode-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: The search terms
      - in: query
        name: sort
        description: Can only be indexed, which indicates how recently a file has
          been indexedby the GitHub search infrastructure
      responses:
        200:
          description: OK
      tags:
      - Search
      - Code
  /events:
    get:
      summary: Get Events
      description: List public events.
      operationId: list-public-events
      x-api-path-slug: events-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      responses:
        200:
          description: OK
      tags:
      - Events
  /search/issues:
    get:
      summary: Get Search Issues
      description: Find issues by state and keyword. (This method returns up to 100
        results per page.)
      operationId: find-issues-by-state-and-keyword-this-method-returns-up-to-100-results-per-page
      x-api-path-slug: searchissues-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: 'The q search term can also contain any combination of the supported
          issue search qualifiers:'
      - in: query
        name: sort
        description: The sort field
      responses:
        200:
          description: OK
      tags:
      - Search
      - Issues
  /search/repositories:
    get:
      summary: Get Search Repositories
      description: Search repositories.
      operationId: search-repositories
      x-api-path-slug: searchrepositories-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: The search terms
      - in: query
        name: sort
        description: If not provided, results are sorted by best match
      responses:
        200:
          description: OK
      tags:
      - Search
      - Repositories
  /search/users:
    get:
      summary: Get Search Users
      description: Search users.
      operationId: search-users
      x-api-path-slug: searchusers-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: The search terms
      - in: query
        name: sort
        description: If not provided, results are sorted by best match
      responses:
        200:
          description: OK
      tags:
      - Search
      - Users
  /orgs/{org}/events:
    get:
      summary: Get Orgs Org Events
      description: List public events for an organization.
      operationId: list-public-events-for-an-organization
      x-api-path-slug: orgsorgevents-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Events
x-streamrank:
  polling_total_time_average: "0.2"
  polling_size_download_average: "34762.27"
  streaming_total_time_average: "0.11"
  streaming_size_download_average: "17390.83"
  change_yes: "1027"
  change_no: "1313"
  time_percentage: "44"
  size_percentage: "50"
  change_percentage: "44"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---