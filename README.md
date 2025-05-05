This flow reads incoming emails, extracts the required data from the email body, and sends that data to the target system via an API call.

*****Project Overview***
    This Power Automate flow is designed to streamline manual data entry by automatically processing incoming emails. It reads specific values from the email body, parses the required information, and sends it to an external system using an authenticated API call.

*****Use Case*******
    Businesses often receive structured email notifications containing crucial transactional data. Manually copying this data into internal systems is time-consuming and error-prone. This flow automates that task by:

Monitoring your mailbox
  1 - Extracting key fields from the email content
  2 - Making a secure POST request, with a token key to your system's API
  3 - Passing the extracted values in the correct format

*****Key Features*****
  1 - Triggered on new incoming email
  2 - Parses data using HTML to Text and Substring functions
  3 - Dynamically constructs the API request body, by parsing to the right data type
  4 - Handles headers and authorization tokens securely
  5 - Includes error handling and logging steps

*****Technologies Used*****
  1 - Power Automate (Cloud Flow)
  2 - Microsoft Outlook connector
  3 - HTTP connector
  4 - API (REST, JSON)
  5 - Optional: SharePoint or Excel integration for logging

******Screenshots*****
  1- Trigger: [image](https://github.com/user-attachments/assets/203c3d9d-08b7-43ff-850a-5209a3cd7104)

  2 - Parsing Logic: Parse Html to Text - [image](https://github.com/user-attachments/assets/9c812eed-8690-46d6-852f-28d6c4958111)

  3 - compose/parse to specific data type - [image](https://github.com/user-attachments/assets/a2044b6f-f1c7-4a31-8ca3-b543027d2f23)

  4 - HTTP Requests: API connections - [image](https://github.com/user-attachments/assets/48c6db3e-1078-4e8a-9934-803f62fdefd4)

*****Outcome*****
  This automation reduces manual effort, minimizes errors, and speeds up data transmission across systems — all without writing a single line of code.

*****How to Use*****
  step1 - Create a new flow in Power Automate
  step2 - Set the trigger: When a new email arrives
  step3 - Initialize all the necessary variables
  step4 - Add logic to parse your email content (using substring or regex)
  step6 - Configure the HTTP action:
  step7 - Method: POST
  step8 - URI: https://api.targetsystem.com/endpoint
        Headers: Content-Type: application/json + Authorization
        Body: Insert parsed data
  step9 - Save and test the flow with a sample email


