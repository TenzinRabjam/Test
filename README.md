README v1.0 / 19 DECEMBER 2019

# Medical Administration Record

## Introduction

Medical Administration Record's purpose is to store the medication records for the residential clients at Valley Behavioral Health. It is using a .NET API and ASP.NET Page with a simple API tool named SWAGGER IO.        


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

Medication recieved by Valley Users, more specifically by Nurse Robin currently at Valley CORE 1 Residential. 

Medication distributed to the Clients with their initials as the signature.

## Contributing

Valley Behavioral Health
Cerenimbus.inc

## Help

Communication channels are available to request help by Tenzin, .Net Developer at Valley Behavioral Health. Communication channels with a proven track record are outlook mailing lists, IRC, and .net forums. Users can submit bugs or feature requests on slack to me(Slack username: tenzinr).

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

Visual Studio 2019 Enterprise
Nuget: Entity Core Framework 
Swagger IO API
SSMS: ValleyCareProd DB

### Installation

1. There are two projects on the server: VBHServer01 via Cisco AnyConnect or Remote Desktop
2. In the users section, pick TENZINR or Kirby.Glad
3. You will find, three projects named MedicationAdministrationRecord, MarAPI and MarAPIDebug
      3a. MedicationAdministrationRecord is the frontend for the project
      3b.  MarAPI and MarAPIDebug are the backend where MarAPI is in production and MarAPIDebug is in debug mode.
4. You would need to enable COR if there is ECor issue.

### Configuration

1. Run both the projects in ADMIN Mode.
2. Server path should be configured with the default user pool.

## Credits

Kirby Glad at Cerenimbus.inc

## Contact

Mail: tenzinr@valleycares.com
Slack username: tenzinr
Phone: 3854446917

## License

This project is licensed under Valley Behavioral Health. 

