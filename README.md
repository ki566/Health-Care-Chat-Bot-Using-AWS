## Problem Statement

The main goal of the creation of Chatbots was to resemble a human being in the way they perform said interaction, trying to make the user think writing to another human being. 
This chatbot uses Amazon lex to build a text-based conversational interface for web applications. 
AWS lambda function is used to validate user’s response and perform initialization and fulfilment in lex intent configuration. This chatbot uses AWS DynamoDB to control and stores the resources. The bot is deployed onAWS Cloud Formation. 
The application architecture uses AWS Lambda, Amazon Lex, Amazon DynamoDB, to communicate with the application deployed.
The chatbot is built to provide customer support 24x7, especially in the health domain web applications. This will help the user to interact with doctors at any time online and to search for the doctor’s availability and book Appointment etc.This type of chatbot can be deployed in any application by using AWS tools.


![image](https://user-images.githubusercontent.com/53647653/180603130-4e9f4113-16cf-4a60-9c59-aa6af91cd2d1.png)


##  AWS LEX

# Intents used:

**1. Greetings:** The main purpose of this intent is to know the details of the patient and refer to the medical Department that the user needs to baseon the answers given by the user.

**2.BookAnAppointment:** The use of this intent is to select the day for the appointment.

**3.Confirm:** The use of this intent is to Book the appointment for the user after the user has choose the doctor they want to see

![image](https://user-images.githubusercontent.com/53647653/180604245-f4be8a71-990d-4be2-ace3-ec616d0872ad.png)


# Slot Types used:
**1. Greetings:**

The slots and slotypes in this intent used are:

**FirstName:** This is the slot that asks and stores the first name of the patient. The SlotType used here is amazon.us_first_name which is a built-in slot type in amazon lex.


**AgeGroups:** This stores the age of the patient and uses a custom SlotTypeAge Groups.

**Pincode:** This stores the area chosen by the patient and uses a custom SlotTypePincode.

**Department:** This stores the type of treatment chosen by the patient and uses a custom SlotType Department.

**2.BookAnAppointment:**

**Doctor_Name:** This slot is in capable of waiting for the doctor to be chosen and saving the doctor's name for later usage in the current Intent. It uses a custom- builtslotTypeDoctor_Name.

**OPD_days:** This contains the user-selected day in relation to the doctor's OPD Days. This uses a custom built slotType called OPD_Days.

**3.Confirm:**

**User_time:** This slot is in capable of enabling patient to schedule a time for booking appointment. It uses a custom-builtslot Type User_time.

**Check_Mail:** This contains the email ID of the patient in order to send appointment confirmation response to the patient. This uses a custom built slotType called Check_Mail.


![image](https://user-images.githubusercontent.com/53647653/180604469-f9aafb9f-f8df-4614-be57-19d71e6adabc.png)




## AWS Lambda

some sample code snippets of Lambda function.

![image](https://user-images.githubusercontent.com/53647653/180604112-5382a6a8-9bb2-4d2f-9e9c-86264afe0e72.png)


**Dynamo DB**

It is the database that is used to store the information about the doctors and which area are they based in.
There are three main regions are Vizag, Khammam, Nalgonda. There are 3 medical departments which are:

![image](https://user-images.githubusercontent.com/53647653/180604499-11230787-43e7-4ed8-9773-0f96e931faba.png)


Two GSI indexes are created for fetching data from DynamoDB:

![image](https://user-images.githubusercontent.com/53647653/180604517-2d576249-ae2f-458b-a234-27a9e672d0bc.png)


## AWS CloudFormation Deployment

Deployed Using CloudFormation Deployment
Refer Below Link  for more information 


https://aws.amazon.com/blogs/machine-learning/deploy-a-web-ui-for-your-chatbot/

## Sample Outputs

# Successful Case:

![image](https://user-images.githubusercontent.com/53647653/180604583-2c777b35-30f7-433d-810a-346b2f0d7860.png)

![image](https://user-images.githubusercontent.com/53647653/180604588-97eefbd5-70db-44cf-9769-8a29bd80acdc.png)

![image](https://user-images.githubusercontent.com/53647653/180604592-7ed11548-5854-48e3-a944-23be397d8cab.png)

# Unsuccessful Case:

![image](https://user-images.githubusercontent.com/53647653/180604629-e367f495-91d1-4e8a-8499-172bbaddd1bf.png)


## Future Scope:
* This chat bot allows you to effortlessly access multiple hospitals in various places and arrange an appointment.

* This chat bot allows you to verify the availability of doctors at various hospitals.

* Chat bot keep patients engaged 24/7. Can make it user-friendly using AI/ML Algorithms.

* This Chat bot helps to place an order for medicines as well as andelivery assistance.


