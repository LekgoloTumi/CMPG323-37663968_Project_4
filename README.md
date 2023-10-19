# CMPG323-37663968_Project_4

# A brief explanation of how the UiPath works:

# Gather user credentials:

Uses an "Input Dialog" activity to prompt the user for their email address and password.
Displays a message like "Please enter your email address:" and stores the input in a variable.
Displays a message like "Please enter your password:" and stores the input in a variable.

# Navigate to the login page:

Uses an "Open Browser" activity to open the web application URL.
Specify the web application URL in the "URL" property of the "Open Browser" activity.
Uses a "Navigate To" activity to navigate to the login page.
Specify the relative path or full URL of the login page in the "URL" property of the "Navigate To" activity.

# Enter login credentials:

Uses "Type Into" activities to enter the email address and password into the corresponding input fields on the login page.

For the email input field, use a "Type Into" activity with the following properties:
Selector: Identify the UI element selector for the email input field.
Text: Assign the userEmail variable to the "Text" property.

For the password input field, use a "Type Into" activity with the following properties:
Selector: Identify the UI element selector for the password input field.
Text: Assign the userPassword variable to the "Text" property.

# Submit login form:

Uses a "Click" activity to click the "login" button on the login page.
Identify the UI element selector for the "login" button and assign it to the "Selector" property of the "Click" activity.
Verify successful login:

For example, checks for a specific element on the homepage or a successful status message.
It uses an "Element Exists" activity to check for the presence of a specific element that indicates a successful login.
Uses an "If" activity to evaluate the result of the "Element Exists" activity and proceed with data operations if login is successful.

# Proceed with data operations:

Once successful login is confirmed, proceed with the data operations based on the user's selections (add, edit, or delete) and the data category (Customers, Orders, Products, or Order Details).
Uses conditional logic to determine the specific actions to perform based on the user's selections.
Implement specific logic for each operation (add, edit, or delete) and data category.
Use UI automation activities to interact with the web application and perform the desired actions on the selected data.
