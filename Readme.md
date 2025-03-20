# Important information about API testing

API Testing Project for Google Drive
The goal of this project, for the "IT Factory Manual Testing Course", is to use all the knowledge acquired during the course sessions, and to be able to apply it in a practical way.

Application under test: https://drive.google.com

Tools used: Postman, Newman

Collection link: 

<h2>Execution report for the created API collection</h2>

Below you can find the execution report that was generated through the Postman collection runner:<br>

[Postman](https://github.com/PokaNorbert/GoogleDrive-API_Postman_Newman/blob/main/Postman_collection.json)

The collection was also run through newman directly from the terminal, and the results can be found below:<br>

[Newman](https://github.com/PokaNorbert/GoogleDrive-API_Postman_Newman/blob/main/Executed_by_Newman.md)

<h2>Defects found</h2>

No bugs/defects were identified in this testing session.

<h2>Conclusions</h2>

All requests ran without problems, not taking into account the fact that some of them needed more than 200 ms. The application can be used by any user without any problem. The response times are not high enough to create problems for the user. 

Instead, a risk could represent the downfall of the Google platform, which would guarantee the impact of all requests. I did not send requests based on all types of files, so I recommend that the next tester set a better coverage.
