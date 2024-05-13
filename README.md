 How to use the tool:
        
	(1)Install mysql; Then create a Database.

        (2)Install the following modules in python:
            mysql.connector
            os
            cryptography
	    Os 
 	    Base64
 	    Binascii
 	    Mysql.connector
 	    Time
 	    Pyotp
 	    Qrcode
	    PIL  Image

        (3)Replace the password and user for the connection to server i.e cnx = mysql.connector.connect( user = 'Your username',password = 'Your_password',host= 'Your_host',database = 'mydatabase')
	
	(4)Install google authenticator on your phone. This is for 2-Factor-Authetication purposes for maximum security.
############################################################################################################################    
After completing the tasks above you can now store your passwords successfully. Good luck

Remember Do Not Repeat The Same Username or Account or Site for the Same Password!!! For if you do that the previous password will be replaced.





########### Developed by Pow3r T3am A.K.A  Rob-DuckSec #############################

This tool is used to store passwords securely. The tool uses python modules:

######Cryptography######
This module plays an important role in the encryption and decryption of passwords used in the tool.

#### MYSQL CONNECTOR ######
This module helps store the user credentials without revealing the location of the database. It also plays a role of user interaction with the user to the database.

#### PYOTP #############
This module helps in generating time based codes that are used for two factor authentication.

##### QRCODE ###########
This module helps in Qrcode generation for authentication purposes.

Other modules are usually prebuilt in python. The rest of the unnamed help in the basic functionality of the tool.

#######################################################################################################################################################################

####### THE MECHANISM BEHIND THE WORK ################
@@@@@ Register @@@@@@
The user has to set the master username and password. Using cryptography, fernet will generate a key that will encrypt the master password and username. Additionally, the master key password will be set  the so as to encrypt key that encrypts the master username and password before storing it in a files with the extension ".key". 
We use password based encryption for key management.

@@@@ Set the 2 Factor Authentication @@@@@@@@
The user will set the 2 Factor-Authentication key password so as to encrypt the key that generates the code which is later embedded as a Qrcode.

 #####Generation Of The Qrcode #####
The user is required to enter the 2-Factor authentication key password. Once the password is correct . A Qrcode is generated. The qrcode contains a time based code that should only be correct once the 2-Factor authentication key password entered is correct. 

##### Authentication #####
For the user to access the main password manager he /she must firstly be verified using 2-factor authentication. This requires the user to have the correct master username , password and key password to be correct. Then the user can now access the password manager.

