# jpa03-dscpsyl

Running at: <https://jpa03-dscpsyl.dokku-07.cs.ucsb.edu>


# Accessing swagger

Swagger is a tool that allows you to work directly with the RESTful API endpoints of the backend.
It is similar to the tool Postman, but more convenient because it is built directly into the application.

To access the Swagger API endpoints, use:

* <http://localhost:8080/swagger-ui/index.html>

You can also append `/swagger-ui/index.html` to the URL manually when running on Dokku.

# To run React Storybook locally (for development)

* cd into frontend
* use: `npm run storybook`
* This should put the storybook on http://localhost:6006
* Additional stories are added under frontend/src/stories

You can also see the storybook for the main branch and all open pull requests on the 
github pages site associated with the repo; see [/docs/github-pages.md](/docs/github-pages.md) for more info.

* For documentation on React Storybook, see: <https://storybook.js.org/>

# To generate javadoc (locally, for development)

* cd to top level of repo
* use: `mvn javadoc:javadoc`
* open in a web browser: `target/site/apidocs/index.html`

You can also see the javadoc for the main branch and all open pull requests on the 
github pages site associated with the repo; see [/docs/github-pages.md](/docs/github-pages.md) for more info.

* For documentation on Javadoc, see: <https://www.oracle.com/java/technologies/javase/javadoc-tool.html>

# SQL Database access

On localhost:
* The SQL database is an H2 database and the data is stored in a file under `target`
* Each time you do `mvn clean` the database is completely rebuilt from scratch
* You can access the database console via a special route, <http://localhost:8080/h2-console>
* For more info, see [docs/h2-database.md](/docs/h2-database.md)

On Dokku:
* The SQL database is a postgres database provisioned automatically by Dokku
* More info and instructions for accessing the SQL prompt are at [docs/postgres-database.md](/docs/postgres-database.md)
