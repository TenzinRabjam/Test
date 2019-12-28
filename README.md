README v1.0 / 19 DECEMBER 2019

# Medical Administration Record

## Introduction
Medical Administration Record's purpose is to store the medication records for the residential clients at Valley Behavioral Health. It is using a .NET API and ASP.NET Page with a simple API tool named SWAGGER.  Front     



Give your users an overview of the purpose and function of your project in a paragraph or two (at most). Because sometimes a picture is worth a thousand words, include screenshots when appropriate.

## Changes
Mar User tracking records in following pages:
  Client Page(line:) 

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
