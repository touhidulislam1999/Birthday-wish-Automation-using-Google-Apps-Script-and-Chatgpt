# Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt

![image](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/480b13cb-6a9d-4c31-9fd9-91553be8fa1c)


# DESCIPTION:

In backend there is a google sheet which contain certain information of users google contact.
The birthday wishes are randomized using chatgpt api.

# Fethcher.gs:


![image](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/eef9cdb9-9127-4b41-9262-2310b3eb8e0c)



**Purpose:** Import contacts from the user's Google Contacts into a Google Sheets spreadsheet.

**Steps:**

1. Open the current spreadsheet.

2. Clear existing data in the sheet.

3. Retrieve the user's contacts using ContactsApp.

4. Write headers (Name, Email 1, Email 2, Email 3, Birthdate) to the sheet.

5. Iterate through each contact:

    i) Get the full name and emails of the contact.

    ii) If the full name is empty, skip the contact.

    iii) Write the contact's name to the sheet.

    iv) Write up to 3 email addresses to the sheet.

    v) Write the birthdate to the sheet if available.

    vi) The data will be imported in the sheet if only both the email and the date of birth are present.
    
    vii) The initial birth year given is 1900 and if the birhtyear of that person is present, 1900 will be replaced. Its because sometimes data might not contain birth year, but it doesn't matter as we need only which day of which month to wish.
  
6. Increment the row count for writing to the sheet.

7. There is a time driven trigger which automatically updates the google sheet from 11pm to 12am.

# Sender.gs :

![image](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/a14014a4-4265-4faf-a683-60e9ba1dda64)


**Purpose:** Send birthday greetings via email to contacts whose birthday matches the current date.

**Steps:**

1. Open the current spreadsheet.
2. Get today's date (month and day).
3. Iterate through each contact in the sheet:

    - Get the contact's name and birthdate from corresponding cells.
   
    - If the birthdate is not empty, check if it matches today's date.
   
    - If it's the contact's birthday : 
   
        - Get the email addresses from columns B, C, D.
   
        - Iterate through each email address:
   
            - Compose a birthday greeting email with a personalized message using the message function.
   
            - Send the email using MailApp.sendEmail.
            
4. There is a time driven trigger which automatically run the code file (sender.gs) within 12am to 1am.
   
         


   
**Additional Notes:**

- The message function utilizes the OpenAI GPT-3.5-turbo model to generate a short birthday wish.
  
- The email body includes HTML formatting for styling.
  
- Two parts of the email body (body and body_2) are concatenated to create the final HTML body.
  
- The message function fetches a short birthday wish from the OpenAI API using an API key.
  
- The email is sent with the subject "Happy Birthday!".
  
- The script uses the MailApp service to send emails.

- If you don't want to use api for randomized the birthday wishes, then there is a commented code part (in sender.gs) that will give same birthday wish for everyone.

![image](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/aca4d5db-86fc-44fc-b94d-ab3975506a9f)


![image](https://github.com/touhidulislam1999/Birthday-wish-Automation-using-Google-Apps-Script-and-Chatgpt/assets/97190512/4d7188cf-d3c1-441c-82f5-c164fd991f03)



 


