# DigiBahi
Secure and reliable Digital Bahi khata using cryptography. Frontend is built using flutter and backend using rust and actix web.
It project provides both mobile and pc application.

Front design is located [here](https://www.figma.com/file/RpDGO53QxgctvM8j772krq/DigiBahi?type=design&node-id=0%3A1&mode=design&t=Z3IJA8DOBTNRJjmq-1).

# Working
It will work like other blockchain systems. Backend server will be built using actix web and MySQL(for database). Frontend will work like non-custodial blockchain wallet.
## Working of Backend
Backend will be built using actix web and MySQL. DigiBahi database will have two tables for storing data.
1. Transactions table which will have columns Id(Serial number of transaction), Sender, Receiver, Amount and Timestamp.
1. Blockchain table which will have columns Id(Serial number of block), Start(starting transaction id), End(last transaction id), Hash(previous block hash)
   Selected transaction will be converted to csv then hash will be calculated.
1. Users table which will have columns Id, Username, Public-Key, Email-Id, Token, time joined
## Here is step by step process starting from account creation:
### 1. Account creation
User account will be created using user Email-id and private-public key pair will be generated. User details will be securely stored on backend server. Private key will be encrypted and stored securely on client device using various technologies like android keystore and PKCS12.

### 2. User login
User will login using username and password after successful login. A token will be generated and will be sent to client device to keep session alive.

### 3. Creating records
User will sign and send request for records to the server. Server will then verify using public key and record will added to the database.

# Exporting data
Data can be exported to PDF or JSON files for external use.

# Importing data
Data can be imported from JSON files
