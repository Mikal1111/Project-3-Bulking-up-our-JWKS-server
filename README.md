# Project-3-Bulking-up-our-JWKS-server
JWKS Server Enhancement
Objective
The objective of this project is to enhance the security and functionality of your JWKS (JSON Web Key Set) server. This will be achieved by implementing AES encryption for private keys, adding user registration capabilities, logging authentication requests, and optionally introducing a rate limiter to control request frequency.

Features
1. AES Encryption for Private Keys: Implement AES encryption to securely store private keys in the database.
2. User Registration: Allow users to register accounts with the JWKS server, providing a username, password, and optional email.
3. Authentication Request Logging: Log authentication requests, including client IP, timestamp, and user ID.
4. Rate Limiter (Optional): Introduce a rate limiter to control the frequency of requests to the JWKS server, preventing abuse or DoS attacks.

    Implementation Details
AES Encryption for Private Keys
-Use AES encryption to encrypt private keys before storing them in the database.
-Generate a random encryption key and securely store it.
-Encrypt the private keys using the encryption key before insertion into the database.

User Registration
-Implement an endpoint for user registration, allowing users to sign up with a username, password, and optional email.
-Hash the passwords before storing them in the database to enhance security.
-Store user information in a dedicated table in the database.

Authentication Request Logging
-Log each authentication request, capturing the client's IP address, timestamp, and associated user ID (if available).
-Store the logs in a dedicated table in the database for auditing and analysis purposes.

Rate Limiter (Optional)
-Implement a rate limiter to restrict the number of requests a client can make to the JWKS server within a specified time frame.
-Set reasonable limits to prevent abuse while ensuring legitimate users can access the service without interruption.

Usage
1. Installation: Install the necessary dependencies by running pip install -r requirements.txt.
Configuration: Configure the JWKS server by setting up the encryption key, database connection, and any other required parameters.
2. Running the Server: Start the JWKS server by running python main1.py.
3. User Registration: Users can register accounts by accessing the registration endpoint and providing the required information.
4. Authentication: Clients can authenticate by requesting JWT tokens from the /auth endpoint.
5. Logging: Authentication requests and other relevant actions will be logged in the database for auditing purposes.
