### NOTE: This is quite an outdated (and questionable) approach to building an application and was used primarily for learning. Please keep your code decoupled and DRY.

Experimenting with object-oriented JavaScript to create a multi-layered API. Use multiple data stores, interchangeable ORM, environment-specific configuration settings, etc. Still a WIP.

Order of communication: `api/controller > service layer > repository layer > models`

`/src/`:
- `/api`: Used to route requests, currently using ExpressJS as an example, but is not necessary. These can be thought of as controllers. Instantiates models as necessary.
-  `/models`: Define schemas for multiple data stores, with interchangeable ORMs, for each model. This section needs to be improved to be more adaptable across each ORM. Still a work-in-progress.
- `/repositories`: A repository layer! Not usually seen or used in node.js, but it's a very useful abstraction layer to allow for multiple data stores. This is often used for large-scale applications, especially those that have to deal with integration of third-party or legacy software.
- `/services`: Services, which can be created for working specifically with third-party applications or APIs, such as Facebook. This data is not usually stored so wouldn't need to have a repository or model.
- `/utils`: A convenience utility, not really used much in this application except for containing additional authentication processing. This should be moved elsewhere, or maybe omitted completely.


If you'd like to contribute, feel free to open a PR.

Available under the MIT license.

