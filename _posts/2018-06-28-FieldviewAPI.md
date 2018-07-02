To address the lack of guidance that exists around the fieldview API. I thought i'd write up an article on how to connect up to View points fieldview API. I imagine many in the construction sector using this application have experienced the horrific nature of trying to locate any information that is captured on the system.

POST request to load information from https://www.priority1.uk.net/FieldViewWebServices/WebServices/JSON/API_TasksServices.asmx

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetProjectTasksList xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">     
        <apiToken>Add_API_Token</apiToken>
        <projectId>Add_Project_ID</projectId>   
        <taskTypeLinkIds>ADD_Task_Type_Link_ID</taskTypeLinkIds>
        <createdDateFrom>2018-06-28-02:00</createdDateFrom>    
        <createdDateTo>2018-06-29-01:00</createdDateTo>
    </GetProjectTasksList>
  </soap:Body>
</soap:Envelope>

```
