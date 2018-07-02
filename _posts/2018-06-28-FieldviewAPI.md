The following article details how to set up the fieldview API to retrive task information:

```xml

<?xml version="1.0" encoding="utf-8"?>



<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">



  <soap:Body>



    <GetProjectTasksList xmlns="https://localhost.priority1.uk.net/Priority1WebServices/JSON">     
<apiToken>Add_API_Token</apiToken>
     
<projectId>Add_Project_ID</projectId>



     
<taskTypeLinkIds>ADD_Task_Type_Link_ID</taskTypeLinkIds>
      
<taskTypeLinkIds>157</taskTypeLinkIds>

      
<taskTypeLinkIds>156</taskTypeLinkIds>

       
<taskTypeLinkIds>1719</taskTypeLinkId>


      <createdDateFrom>2018-06-28-02:00</createdDateFrom>



     
<createdDateTo>2018-06-29-01:00</createdDateTo>



    </GetProjectTasksList>



  </soap:Body>



</soap:Envelope>

```
