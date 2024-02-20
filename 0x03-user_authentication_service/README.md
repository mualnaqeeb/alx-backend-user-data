# User Authentication Service Project Overview

This project is designed to guide you through the process of building a user authentication service. It covers the fundamentals of creating secure and efficient authentication mechanisms using various Python libraries and tools.

## Prerequisites

Before starting, ensure you have the following software installed:
- SQLAlchemy version 1.3.x
- pycodestyle version 2.5
- bcrypt for password hashing
- Python version 3.7

## Project Objectives

Complete the following tasks to build a comprehensive user authentication service:

1. **User Model**: Implement a SQLAlchemy model named `User` in [user.py](user.py). This model should represent a `users` database table and include attributes for user ID, email, hashed password, session ID, and reset token.

2. **User Creation**: Enhance the `DB` class in [db.py](db.py) by adding an `add_user` method. This method should accept email and hashed password as parameters, create a new `User` object, and save it to the database.

3. **User Lookup**: Add a `find_user_by` method to the `DB` class. This method should allow finding a user by various attributes and handle exceptions appropriately.

4. **User Update**: Implement an `update_user` method in the `DB` class to modify user attributes based on provided keyword arguments.

5. **Password Hashing**: Create a `_hash_password` method in [auth.py](auth.py) that generates a salted hash of a password using `bcrypt`.

6. **User Registration**: In the `Auth` class within [auth.py](auth.py), implement a `register_user` method that registers a new user with an email and password.

7. **Basic Flask Application**: Develop a basic Flask application in [app.py](app.py) that returns a welcome message.

8. **User Registration Endpoint**: Add an endpoint to the Flask app to handle user registration.

9. **Login Validation**: Implement a `valid_login` method in the `Auth` class to verify user credentials.

10. **Session ID Generation**: Add a `create_session` method in the `Auth` class to generate and store a session ID for logged-in users.

11. **Login Endpoint**: Create a login endpoint in the Flask app to authenticate users and initiate a session.

12. **Session Retrieval**: Implement a `get_user_from_session_id` method in the `Auth` class to retrieve user details from a session ID.

13. **Session Destruction**: Add a `destroy_session` method to the `Auth` class to invalidate a user session.

14. **Logout Endpoint**: Create a logout endpoint in the Flask app to end user sessions.

15. **User Profile Endpoint**: Implement a profile endpoint to display user details to logged-in users.

16. **Password Reset Token Generation**: Add a `get_reset_password_token` method in the `Auth` class for generating password reset tokens.

17. **Password Reset Token Endpoint**: Implement an endpoint in the Flask app to issue password reset tokens.

18. **Password Update**: Create an `update_password` method in the `Auth` class to allow users to change their password using a reset token.

19. **Password Update Endpoint**: Add an endpoint to the Flask app for users to update their passwords with the reset token.

20. **Integration Testing**: Perform end-to-end integration testing using a separate [main.py](main.py) module to ensure all components work together seamlessly.

## Resources

- [Flask Documentation](https://flask.palletsprojects.com/)
- [Requests Module](https://requests.readthedocs.io/)
- [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)

This project will help you learn the intricacies of user authentication, including password hashing, session management, and handling user data securely.