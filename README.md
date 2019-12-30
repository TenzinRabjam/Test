README v1.0 / 19 DECEMBER 2019

# Medical Administration Record

## Introduction
Medical Administration Record's purpose is to store the medication records for the residential clients at Valley Behavioral Health. It is using a .NET API and ASP.NET Page with a simple API tool named SWAGGER.  Front     



Give your users an overview of the purpose and function of your project in a paragraph or two (at most). Because sometimes a picture is worth a thousand words, include screenshots when appropriate.


## Changes
Keyword: User - Person accessing MAR, Client: Clients at Valley Residential
Note: 1. All the headers are the cshtml pages in this project(13 pages - 6 in Distribution and 7 in Reciever)
      2. We have added few functionalities storing the log with no deletions at all in the entire project
      3. Recording is taking place in Custom_MarUserLog table in ValleySmartCareProd Database.
      4. In the MAR Backend, only user controller has been changed and every other controllers are unchanged.
      
Mar User tracking records in following pages:
  
  Front End: Medical Administration Record
   
    MobileApp directory: MAR Distribution Section
      
      Choose-Distribution-Date:
          (line 75): CSS Changes for making a uniform look for the login page as the reciever login page.
      
      Client:
          (line 433 - 449): Recording the user log, if they viewed the distributed client lists.
          (line 480 - 497): Recording the user log, if they viewed the undistributed client lists.
          (line 588 - 605): Recording the user log, if they viewed the all the client lists.
          (line 954 - 971): Recording the user activity, and client ID, when they use the deliver ordered page.
          (line 1057 - 1074): Recording the user activity, if they view deliver PRN page for a specific client.
          (line 1098 - 1112): Recording the user state when they logout and also clearing the session.
          
      Deliver-Ordered:
          (line 284 - 302): Recording the user log and client ID, when they have submitted orders.
      
      Deliver-PRN:
          (line 278 - 296): Recording the user log and client ID, when they have submitted PRN.
          
      Display-Clientlist:
          (line 73): CSS changes for padding to make the page broad.
          (line 83- 85): CSS changes for styling the margin and screen-content.
          
      Index:
          (line 286 - 312): Setting the user's current session, and recording their log. 
      
    Pages directory: MAR Reciever Section.
      
      Medication-Add-Medication: 
          (line 486 - 506): Recording the user log, when they have changed multiple client's medication.
          
      Medication-Delivery:
          (line 171 - 187): Recording the user name, and using the password as a page name holder.
          (line 204 - 218): Recording the logging out action of the user.
      
      Medication-Reciept-Verification-login:
          (line 100 - 102): CSS Changes for adding and submitting medication.
      
      Medication-Recieved-Per-Client:
          (line 509 - 526): Recording the user log and client's ID and program, when they delete a client's medication.
      
      Medication-Remove-Medication:
          (line 381 - 401): Recording the whole detail of a client if the user viewed the remove medication page.
      
      Medication-Report:
          none-changed
      
      Index:
          (line 142 - 158): Setting the user's current session, and recording their log.        
    
    
  Back End: Mar API
  
    Controllers directory: UserController      
       (line 134 - 232): Added for Recording each user activity with 13 routings(5 in Reciever and 8 in Distribution Section):
          MAR Distribution Section      
              1. LoginUserDistributor
              2. LogoutUserDistributor
              3. ClientDistributor
              4. ViewClientListDistributor
              5. DeliverOrderedDistributor
              6. DeliverPrnDistributor
              7. SubmitDeliverOrderedDistributor
              8. SubmitDeliverPrnDistributor
        
         MAR Reciever Section:
              1. LoginUserReciever
              2. LogoutUserReciever
              3. MedicationPerClientUserReciever
              4. RemoveClientUserReciever
              5. ChangedClientUserReciever
              
## Usage
Medication recieved from the page: 

Medication distributed:

## Contributing
Cerenimbus.inc

## Help
Explain which communication channels are available to request help. Communication channels with a proven track record are mailing lists, IRC channels, and forums. Also be sure to tell your more experienced users how and where to submit bugs or feature requests, possibly turning them into project participants.

## Installation
This project is built on two tiers:  
                                     
                                     Front End: Medical Administration Record
                                              1. MobileApp directory: MAR Distribution Section.
                                              2. Pages directory: MAR Reciever Section.
                                     
                                     Back End: Mar API
                                              Client:  
                                              GET /api/client/GetClientListByProgram    
                                              POST /api/client
                                              DELETE /api/client/{id}
                                              PUT /api/client/{id}     
                                              
                                              CustomBlacklist:
                                              GET /GetCustomBlacklistBySlug       
                                              
                                              Delivery:
                                              GET /api/delivery/GetMedicationDelivered                                                  
                                              PUT /api/delivery/UpdateMedicationDelivery/{id}                                          
                                              POST /api/delivery/SaveMedicationDelivery 
                                              POST /api/delivery/SaveMedicationDeliveredByList
                                              DELETE /api/delivery/{id}       
                                              
                                              Medication:
                                              GET /api/medication/GetMedicationList 
                                              GET /api/medication/GetMedicationListByName  
                                              GET /api/medication/SearchMedicationListByName
                                              GET /api/medication/GetMedicationListByClient 
                                              GET /api/medication/GetMedicationListCount
                                              GET /api/medication/GetTimePeriodList
                                              GET /api/medication/GetMedicationScheduleList
                                              GET /api/medication/GetMedicationReceived 
                                              
                                              POST /api/medication/SaveMedicationReceived
                                              POST /api/medication/SaveMedicationReceivedByList
                                              POST /api/medication/SaveMedicationByList 
                                              POST /api/medication
                                              
                                              DELETE /api/medication/{id}  
                                             
                                              PUT /api/medication/UpdateMedicationSchedule/{id}                                         
                                              PUT /api/medication/{id}
                                              PUT /api/medication/DeleteMedicationReceived/{medicationId}/{clientId}  
                                              PUT /api/medication/RestoreMedicationReceived/{medicationId}/{clientId}
                                              PUT /api/medication/UpdateMedicationReceivedErrorEntry/{medicationId}/{clientId}
                                              PUT /api/medication/UpdateMedicationReceived        
                                              
                                              Programs: 
                                              GET /api/program/GetUnitList  
                                              GET /api/program/{id}
                                              DELETE /api/program/{id} 
                                              PUT /api/program/{id}  
                                              POST /api/program     
                                              
                                              User:
                                              POST /api/user/AuthorizeUser  
                                              POST /api/user/LoginUserReciever  
                                              POST /api/user/LogoutUserReciever
                                              POST /api/user/MedicationDeliveryReciever 
                                              POST /api/user/MedicationPerClientUserReciever 
                                              POST /api/user/LoginUserDistributor  
                                              POST /api/user/LogoutUserDistributor
                                              POST /api/user/ClientDistributor
                                              
       
### Requirements

List anything your project requires in order to work as expected.

### Installation

Describe how to install your program. Be precise and give examples. Don't assume your users know how to clone from my github repo. Keep in mind that some of your users may be completely unskilled in system administration or software development.

### Configuration

After having installed the software, the user may need to configure it. List configuration options and explain how and where to set them.

## Credits

Sometimes also called Authors, this is the list of project contributors.

## Contact

People may want to reach out to you for various reasons, ranging from DCMA take down notices to questions about how to donate to your project. Provide contact information, such as an email address, and keep in mind that some countries may require certain information by law, such as a full postal address, website URL, and company name.

## License

This project is licensed under Valley Behavioral Health. 

Sometimes including a Table of Contents (TOC) at the beginning of the documentation makes sense, especially when your README file is more than a few paragraphs. If you think that the README file has grown too large, put some of the more detailed parts, such as installation or configuration sections, into their own files.

## Conclusion
Writing your first documentation doesn't seem as hard or or time-consuming as you initially thought, does it? Now you have a starting point on which you can build. Don't forget to update your README to keep it current with your project's development and new releases.
