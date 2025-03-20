# Important information about API testing

API Testing Project for Google Drive
The goal of this project, for the "IT Factory Manual Testing Course", is to use all the knowledge acquired during the course sessions, and to be able to apply it in a practical way.

**Application** under test: https://drive.google.com

**Tools** used: Postman, Newman

**Collection** link: [tap here](https://github.com/PokaNorbert/GoogleDrive-API_Postman_Newman/blob/main/Postman/Postman_collection.json)

<h2>Requests</h2>

![Postman-Collection](https://github.com/user-attachments/assets/5963ae6d-2fa5-4bd8-99ba-0dc52287a3ba)

<h2>Execution report for the created API collection</h2>

Below you can find the execution report that was generated through the Postman collection runner:<br>

[Postman](

The collection was also run through newman directly from the terminal, and the results can be found below:<br>

[Newman](https://github.com/PokaNorbert/GoogleDrive-API_Postman_Newman/blob/main/Newman/Executed_by_Newman.md)

<h2>Defects found</h2>

No defects/bugs were identified in this testing session.

<h2>Conclusions</h2>

The conclusions of the testing carried out are the following:
<ul>
<li>All requests ran without problems, not taking into account the fact that some of them needed more than 200 ms;</li>
<li>The response times are not high enough to create problems for the use;</li>
<li>The application can be used by any user without no problems at first glance;</li>
<li>Instead, a risk could be the downfall of the Google platform, which could no longer guarantee the successful completion of requests;</li>
<li>I did not send requests based on all types of files, so I recommend that the next tester set a better coverage.</li>
</ul>
