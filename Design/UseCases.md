# Actors
* User: The customers that regularly use the system to find clothes through the goodwill API.
* Admin: The client that will be maintaining the website post launch.
# Use Cases
* UC1 : User Survey
  * Explanation: This use case allows for the website to work how it was intended to work. This use case has the users fill out a survey that helps the AI find what clothing the user would be interested in. This is one of the most important use cases because everything starts here and without it, you would not be able to navigate through the website.
  * Actor: User
  * Flow:
    * 1.1 A Survey is displayed with 60 data points that must be answered fully before clothing is displayed.
    * 1.2 A collection of clothing is displayed based off of how the survey was answered.
  * Business Requirement: BR1
* UC2 : User Registration
    * Explanation: This case enables the users to register or to log in on the website. It's very important to have this as a use case because, this is a website that's used for online shopping. Protection of the user and it's data such as credit information is top priority.
    * Actor: User
    * Flow:
        * 2.1 User navigates to the registration or login page.
        * 2.2 User provides their email and password.
        * 2.3 User submits the registration form or login form.
        * 2.4 User is prompted to check email for verification.
    * Business Requirement: BR1
* UC3 : User Cart Management
    * Explanation: This case enables the user to remove or add a piece of clothing to their cart. It's important to have this as a use case because, their can be multiple users on the website at a time searching for the same piece of clothing. Having a cart management system can help users checkout easier or remove clothes form their cart. This is important to have as a use case because it could prevent issues when browsing the website. 
    * Actor: User
    * Flow:
        * 3.1 User navigates through the website after answering the 60 data point survey viewing clothing.
        * 3.2 User clicks "Add To Cart" on clothing.
        * 3.3 User navigates to cart screen.
        * 3.4 User decides they do not want the piece of clothing anymore and clicks "Remove From Cart" button.
        * 3.5 User navigates to checkout.
    * Business Requirement: BR1
* UC4 : Admin Management
    * Explanation: This case enables the admin to be able to update the website easily. This use case is important to have because it allows for regular maintenance of the website. 
    * Actor: Admin
    * Flow:
        * 4.1 Administrator logs into the admin account.
        * 4.2 Access the content from the admin view.
        * 4.3 Add or remove content if it is available or not.
        * 4.4 The system updates after edits is made.
    * Business Requirement: BR2


