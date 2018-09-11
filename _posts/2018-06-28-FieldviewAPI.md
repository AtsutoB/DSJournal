To address the lack of guidance that exists around the fieldview Application programming inteface (API). I thought i'd write up an article on how to connect and use it for loading the task lists from fieldview. I imagine many in the construction sector using this application have experienced the horrific nature of trying to locate any information that is captured on the system. Hopefully this can end now.

First things first, an API can be thought of as a group of functions that allows one application to interact with another. There are various ways in which one application can transfer information in order to interact with an API. The most common way is through the Hypertext Transfer Protocol (HTTP). We all commonly see part of this acronym when going onto any website. It's within that top bar at the top of your web browser. This protocol is a standard for transferring data in a protocol called Request methods. Using a website as an example, your web browser application  a request with one of these methods, along with a URL and a payload (like a form or query string request) which communicate to the server what action they want performed

Phew so nearly finished with all the explainy bits an getting closer to the 'copy and paste this stuff' bit! Which is where is gets exciting! As your data will start to become more integrated as it omes closer together!

![Screen grab of Postman](/DSJournal/master/assets/photos/PostmanStart.png)
    

We will be calling 2 different API functions in order to get the corrcet information to call the GetprojectTasksList() function which, as the name implies, gets a lists of tasks from a particular project.

The functions you first need to call are the [GetProjectTaskTypes()](https://fvdocs.viewpoint.com/Admin_web_topics/APIs/tasks_services/r_GetProjectTaskTypes.html) and [GetProjectDetails()](https://fvdocs.viewpoint.com/Admin_web_topics/APIs/project_services/r_GetProjectDetails.html)



https://www.priority1.uk.net/FieldViewWebServices/WebServices/JSON/API_ProjectServices.asmx

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetProjectDetails xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">
      <apiToken>ADD_API_TOKEN_HERE</apiToken>
      <startRow>1</startRow>
      <pageSize>500</pageSize>
    </GetProjectDetails>
  </soap:Body>
</soap:Envelope>
```


















POST request to load information from https://www.priority1.uk.net/FieldViewWebServices/WebServices/JSON/API_TasksServices.asmx

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetProjectTasksList xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">     
        <apiToken>Add_API_Token_Here</apiToken>
        <projectId>Add_Project_ID_Here</projectId>   
        <taskTypeLinkIds>ADD_Task_Type_Link_ID_Here</taskTypeLinkIds>
        <createdDateFrom>2018-06-28-02:00</createdDateFrom>    
        <createdDateTo>2018-06-29-01:00</createdDateTo>
    </GetProjectTasksList>
  </soap:Body>
</soap:Envelope>

```
