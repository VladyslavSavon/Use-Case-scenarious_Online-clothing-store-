# Use-Case-scenarious_Online-clothing-store-
Use Case scenarious for the Online clothing store include 4 Use cases: UC-1 Register User, UC-2 Log-in User, UC-3 User's product search using the catalog menu, UC-4 User's product search using the search field

##

UC-1 | Register User 
--- | --- 
Goal | In order to buy a product on the website, a new user must register a customer profile in the system.
Actors | User — customer
Preconditions | The user added a product to the cart
Trigger | The user initiates a purchasing process
Flow of Events | User Registration
1 | The system requests a username and password
2 | The user enters a username and password
3 | The system checks that the username does not duplicate any existing registered usernames.
4 | The system requests a name, surname, phone number, and email address. All fields are obligate. 
5 | The user enters the information.
6 | The system accepts the information.
7 | The system displays the user a message asking the user to check the user's email box. 
8 | The system sends a confirmation email to the user's email address entered into the system.
9 | The user receives the confirmation email at the email address entered into the system.
10 | The user opens the confirmation email. 
11 | The confirmation email asks the user to follow the link to confirm the registration in the system.
12 | The user follows the link to confirm the registration in the system. 
13 | The user confirmed the registration.
14 | The system starts a login session and displays a welcome message based on the user's information. 
Alternative Flow of Events | 3a. The username duplicates an existing username. 
1 | The system displays an error message 
2 | The use case goes back to step 1.
Alternative Flow of Events | 5a. The user does not fill in all fields. 
1 | The system marks empty fields in red. 
2 | The use case goes to step 5. 
Alternative Flow of Events | 9a. The user doesn't receive the confirmation email at the email address entered into the system.
1 | In 90 seconds after sending the confirmation email to the user's email address entered into the system, the system displays a message prompting the user to confirm sending another email.
2 | The user case goes back to step 7.
Alternative Flow of Events | 14a. The system failed to start a login session. 
1 | The system displays a message with an error asking the user to click the confirmation link again. 
2 | The use case goes back to step 12. 
Post-conditions | The user can now continue the purchasing process in the system. 

##

UC-2 | Log-in User
--- | --- 
Goal | In order to buy a product on the website, a registered user must log in to the system.
Actors | User — customer
Preconditions | The user added a product to the cart.
Trigger | The user initiates a purchasing process
Flow of Events | User log-in
1 | The system requests an email and password
2 | The user enters an email and password
3 | The system identifies the email.
4 | The system validates the password.
5 | The system authorizes the user.
6 | The system starts a login session and displays a welcome message based on the user's information.
Alternative Flow of Events | 3a. The system doesn't identify the user's email.
1 | The system displays a message to check the correctness of the email address and to reenter it.
2 | The system marks the field in red.
3 | The use case goes back to step 2.
Alternative Flow of Events 4a. | The system doesn't validate the user's password.
1 | The system displays a message to check the correctness of the password and to reenter the password.
2 | The system marks the field in red.
3 | The use case goes back to step 2.
Alternative Flow of Events 6а. | The system failed to start a login session.
1 | The system displays a message with an error asking the user to enter the email and password again.
2 | The use case goes back to step 1
Post-conditions | The user can now continue the purchasing process in the system.

##

UC-3 | User's product search using the catalog menu
--- | --- 
Goal | In order to find a desired product, the user must search for it in the system.
Actors | User — customer
Preconditions | none
Trigger | The user visits the website
Flow of Events | Search for a product using the catalog menu
1 | On the start page, the system displays a catalog menu, a search field, personalized recommendations, and discount products.
2 | The user clicks on the catalog menu button.
3 | The system displays the catalog menu. The catalog menu contains categories of products.
4 | The user clicks on a selected category in the catalog menu.
5 | The system displays subcategories of the selected category.
6 | The user clicks on a subcategory of the selected category.
7 | The system displays names and images of products, their short descriptions, and product sorting filters.
8 | The user clicks on a product name or image.
9 | The system displays a product page with information about the product and a button “buy”.
10 | The user clicks the button “buy”.
11 | The system adds the product to the cart
Alternative Flow of Events | None
Post-conditions | The user can now continue to search for a desired product (UC-3 or UC-4) or to start UC-1 or UC-2.

##

UC-4 | User's product search using the search field
--- | --- 
Goal | In order to find a desired product, the user must search for it in the system.
Actors | User — customer
Preconditions | none
Trigger | The user visits the website
Flow of Events | Search for a product using the search field
1 | The system displays a catalog menu, a search field, personalized recommendations, and discount products.
2 | The user clicks on the search field.
3 | The system activates the search field.
4 | The user enters the name of the desired product in the search field.
5 | The user clicks the button “Search”.
6 | The system finds relevant names of the user's search request in the product database and displays their names and images of products, their short descriptions, and product sorting filters.
7 | The user clicks on a product name or image.
8 | The system displays information about the product and a button “buy”.
9 | The user clicks the button “buy”.
10 | The system adds the product to the cart
Alternative Flow of Events | 6a. The system didn't find relevant names of the user's search request in the product database.
1 | The system displays a message, that it didn't find the relevant products.
2 | The use case goes back to step 4.
Post-conditions | The user can now continue to search for a desired product (UC-3 or UC-4) or to start UC-1 or UC-2.
