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

@@@@ Generation Of The Qrcode  @@@@@
The user is required to enter the 2-Factor authentication key password. Once the password is correct . A Qrcode is generated. The qrcode contains a time based code that should only be correct once the 2-Factor authentication key password entered is correct. 

@@@@ Authentication @@@@
For the user to access the main password manager he /she must firstly be verified using 2-factor authentication. This requires the user to have the correct master username , password and key password to be correct. Then the user can now access the password manager.

