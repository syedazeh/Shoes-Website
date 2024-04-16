Full-stack website created using PHP, MyPHPadmin, HTML 5, and CSS 3. 

Project description can be read below.

Project Description
You will create a full stack web application for a fictional organization or a company that sells products
(e.g. toys, electronics, cloths, cars, etc.) or provides services (e.g. fitness club, automobile maintenance,
carpet cleaning, etc.).
The website must provide site visitors with the ability to purchase items and view their order history.
The basic style of the website is up to you, but it must follow a fluid layout, be visually appealing, and
appropriate for the purpose and audience.

Project Requirements
Part 1
1. Decide what company/products your website will be about and get your instructor's approval.
2. Determine and create the parts that are common across all pages such as the header, the footer, etc.
3. The navigational links must contain links to 6 pages: Home, Products, Orders, Subscribe, and Log in.
4. Create the Home page of the website. This page must be enriched with images (a slider or an image
album in addition to bulk images such as the logo, etc.). Use images from the Internet or create your
own. This page must also contain:
a. An introduction about the company and its products/services.
b. In addition to links in the navigation menu, you need to add two links in the body of this page that
will be styled to look like buttons:
i. The first button takes the user to the login page.
ii. The second button takes the user to the registration page (Subscribe).
5. Add different styles to this web page for printing.
6. Use responsive design techniques to apply different style rules when the page is viewed on mobile
devices with different screen sizes.

Part 2
Due date: Mon 16 Mar
1. Create the Subscribe page (HTML code only). This page contains a form that collects information from
the user which will be submitted to the server for user registration (you will complete the registration
process on the server side later). The registration form must contain at least:
a. A field for user name.
b. A field for password.
c. A field to confirm the password.
d. A field for email address.
e. Inputs for shipping address, including:
i. Building number.
ii. Street name.
iii. City name from a dropdown list containing major cities.
f. A field for phone number.
g. Radio buttons to denote the preferred method of contact (phone call, email, etc.).
h. Any additional fields you feel needed for your web app.
2. Add code to validate the user input using JavaScript or jQuery (you shouldn't rely here on the browser
to perform validation such as using the required attribute). Your validation must include:
a. All text fields cannot be empty.
b. The two password fields cannot be empty and the password must be the same in both.
c. Email address must contain the @ character, followed by at least three other characters, followed
by .com at the end (Hint: you may need to use string methods such as indexOf(), charAt(),
lastIndexOf(), substring(), etc.)
d. The phone number cannot be empty and must contain digits only (exactly 8 digits).
e. Building number must be a number between 1 and 9999.
f. A city name has been chosen by the user.
g. A preferred method of contact is chosen by the user.
h. Display suitable error messages for each validation, and prevent the browser from submitting the
form if it doesn't pass the validation process.
3. Create the Log in page (HTML code only). This page contains a form that collects information from the
user which will be submitted to the server for logging in (you will complete the login process on the
server side later). The form in this page must contain:
a. A field for user name.
b. A field for password.

Part 3
1. Design the database tables for your web application. Use MySQL to create and set the relationship
between them. Depending on your design, your database may include at least the following three
tables:
a. A table containing information about users. This table will be used to register users in the system
and verify users when logging in.
b. A table containing information about products/services such as item name, item price, item
description, image file name, and any other information you feel related to products.
c. A table containing information about orders made by the user such as, quantity, total amount,
order date, delivery method (shipped or picked up), etc.
d. Add some experimental data to the tables and test your database with different queries to make
sure that everything works correctly. In particular, you may need to test joining tables to get the
order history of a user. You shouldn't go further with your project if the database doesn't work
correctly.
2. Create a PHP file subscribe.php that receives the input from the user registration page and adds the
user to the database. This page responds back with a message informing the user if the registration
was unsuccessful with a link to the original registration page subscribe.html. Otherwise, if the
registration was successful, it redirects the user to the login page.
3. Create another PHP file login.php that receives the input from the user login.html page and verifies
whether the user is registered or not. This page responds back with a message informing the user if
the login was unsuccessful with a link back to login.html. Otherwise, if the login process was successful,
it redirects the user to the Products page.
4. Create a third PHP page products.php that displays a table showing all the items available for purchase
on the website. This page must connect to the database and get the data from the products table.
However, the table displayed in this web page contains three columns only:
a. The first column shows the name of the item.
b. The second column shows the price.
c. The third column displays a button that submits the item ID to the details.php page (more info
about this page in the next part).
d. Remember to link this page to the navigational menu in your application.

Part 4
1. Create an additional PHP page details.php which displays more information about an item in the
catalog. This page receives the item ID from the products.php page, connects to the database and
displays all information related to this item including: its image, name, description, and price.
Additionally, this page displays:
a. A numeric input field that allows the user to specify the quantity needed.
b. A button that enables the user to submit to the purchase.php page.
c. Create an additional PHP page purchase.php that can be used to complete the purchase process.
The page receives the input from products.php and completes the purchase process by:
i. Updating the available quantity for that product in the database/products table.
ii. Adding an order record in the database/orders table.
iii. Displaying a message showing the completion of purchase.
2. Create the PHP page orders.php and link it to the navigation menu. This page displays a table
containing the history of all purchase orders. Information must be pulled from the database
