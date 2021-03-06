# TITLE: Multithread_Chat

# Final project for Operative Systems - Sapienza University of Rome
# Professors: Giorgio Grisetti and Irvin Aloise

- - - -

## Description:
The project consists in the development of a private chat environment 
to exchange text messages between hosts. 

***The project is composed by two main modules:***

## Server: 
* Receives and does not store messages
* Previews messages sent between users and READ notification
* Once a user logs in, the server will clean the log and show the new list of connected users
* Forwards the messages from client to client
* Notifies to the Sender Client, Delivered and Read status in their respective cases once they occur

## Client: 
* Provides a very simple interface to login or register a new user
* Once successfully logged in the Client will show a menu with 3 options:
  * Send a message
    * Deliver a message in the following format -> *USERNAME_OF_THE_RECIEVER:MESSAGE*  
  * Check Inbox
    * Shows incoming messages
    * Incoming notifications
    * In case of empty Inbox, given the NON-Blocking Recv implementation will print ("Empty Inbox, press a key to continue")
  * Exit

- - - -

## Common errors handled:
* Incorrect credentials during login
* Connection error, when connecting from the Client when the Server is not online
* User Offline notification, when sending a message to an offline user

- - - -

## How-to-run:
Compile the project using the Makefile


**Run in different terminals:**
* First the server, ./server_multithread
* Then run the clients, ./client


You could either register a new user, or login with one of the 3 default accounts.


**Default Accounts:**
* Account #1
  * Username: A 
  * Password: a
* Account #2
  * Username: B 
  * Password: b
* Account #3
  * Username: C 
  * Password: c


Remeber the format to send a message:
***USERNAME_DESTINATARIO:Messaggio***


*The project has been tested with 3 users and by default could support until 5 users as specified in common.h in the constant MAX_USERS*
