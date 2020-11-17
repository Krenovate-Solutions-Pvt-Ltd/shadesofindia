#   **Administrator**

##  **Introduction**

The administrator role is the most powerful role. Users with the administrator role/rights can:

-   add new posts
-   edit any posts
-   delete any posts
-   install, edit, delete plugins and themes
-   add new users
-   edit user information
-   delete any user


This role is basically reserved for site owners and gives them full control of the whole website.

##  **Add a New Admin User**

In this section, we will look at the steps to be followed to add a New user with Admin rights.

1.  Go to <a href="https://shadesofindia.com/wp-admin" target="_blank">**ShadesofIndia**</a>
2.  Login with the credentials, you will reach the admin dashboard
3.  Click -> **Users**
4.  Click -> **Add New**

    ![add new](Administrator\addnew.jpg)

5.  Fill the below form:

    ![form](Administrator\form.jpg)

    -   **User Name** - It is a required field. Add any name you wish. The filed is case sensitive so it is advised not to use capital letters.
    -   **Email** - This is a required field. Enter the email id. The entered email id cannot be used for any other role.
    -   **First Name** - Enter the user's first name
    -   **Last Name** - Enter the user's last name
    -   **Website** - This field is NA. Leave it blank
    -   **Password** - Click -> Show password - it will show a system generated password. It is recommended to use this password only.
    -   **Send User Notification** - Always enable this option -> this will send an email notification to the user
    -   **Role** - From the drop down select the role as **Administrator**

6.  Click -> **Add New User** at the bottom of the form. 

##  **User Verification**

Once the user is created, an email notification is received on the registered email id. This email helps in making the created account active.

![mail recvd](Administrator\mailrecvd.jpg)

Follow the below steps:

1.  Click -> Link in the email

    ![mail link](Administrator\maillink.jpg)

2.  Copy the password shown and save
3.  Click -> Reset the password

    ![password](Administrator\password.jpg)

4.  Once password is rest, login with the Username and password.

    ![password reset](Administrator\passwordreset.jpg)


>   **Note - Never save passwords on the working machine.**

##  **Two Factor Authentication (2FA)**

Two-factor authentication (2FA), sometimes referred to as *two-step verification* or *dual-factor authentication*, is a security process in which users provide two different authentication factors to verify themselves.

Two-factor authentication methods rely on a user providing a password, as well as a second factor, usually either a security token or a biometric factor, such as a fingerprint or facial scan.

Two-factor authentication adds an **additional layer of security** to the authentication process by making it harder for attackers to gain access to a person's devices or online accounts.

### **Download AUTHY**

Authy is the authenticator app that we use to enable the 2FA. Below are the steps to download the app:

1.  Go to -> <a href="https://authy.com/" target="_blank">**Authy Website**</a>
2.  On top right side corner, Click -> **Download**

    ![authy download](Administrator\authydownload.jpg)

3.  Go to -> **Desktop**
4.  Select your operating system - mac/windows

    ![authy desktop](Administrator\authydesktop.jpg)

5.  Run **Setup** to install Authy on your machine.


### **Authy Account Setup**

1.  Run **Setup** to install Authy on your machine.
2.  Select Country -> India (+91)

    ![country](Administrator\country.jpg)

3.  Enter -> Mobile number, Click **Next**

    ![click next](Administrator\clicknext.jpg)

4.  Enter -> email id for notifications

    ![email](Administrator\email.jpg)
    
5.  Select -> SMS - to receive verification code

    ![sms verify](Administrator\smsverify.jpg)

6.  Enter -> Code received on mobile number

    ![enter code](Administrator\entercode.jpg)

Now your Authy setup is complete.


### **Connect Authy to Admin Account**

1.  Click -> "+" sign

    ![click +](Administrator\click+.jpg)

2.  Generate code in the website admin panel. Steps to get code are below:

    -   Go to -> Admin Panel
    -   Go to -> **Wordfence** -> **Login Security**

        ![wordfence](Administrator\wordfence.jpg)

    -   Copy code visible under the Bar code

        ![copy code](Administrator\copycode.jpg)

3.  Paste the code in Authy
4.  Click -> **Add account**

    ![past in authy](Administrator\pasteinauthy.jpg)

5.  Add -> **Account Name**

    ![account name](Administrator\accountname.jpg)

6.  Scroll to the bottom of given list. Select -> **Wordpress**

    ![select wordpress](Administrator\selectwordpress.jpg)

7.  Choose -> **Token Length** - Recommended length is 6 digit

    ![token length](Administrator\tokenlength.jpg)

8.  Click -> **Save** 
9.  Copy the visible code. This code changes every 30 seconds.

    ![copy6digit code](Administrator\copy6digitcode.jpg)

10. Go back to -> Admin Panel
11. Paste code under section 2

    ![pastecode](Administrator\pastecode.jpg)

12. Click -> **Activate**

    ![clickactivate](Administrator\clickactivate.jpg)

### **Recovery Codes**

Once the connection between Authy and Admin account is set up, a pop-up comes up - **Download Recovery Codes**

1.  Click -> **Download** : The text file has 5 extra codes in case the previous code is lost.

    ![download recovery codes](Administrator\downloadrecoverycodes.jpg)

2.  Save for future use.

-   The recovery codes, can be used if you ever lose your authenticator device or if you remove the app or its saved codes by mistake. Make sure you store these codes in a safe place.
-   Because they don’t expire, recovery codes are longer than normal codes — 16 letters and numbers instead of only 6 numbers — but each code can only be used once. 
-   You can generate new recovery codes on the Login Security page of your site.
-   Generating new codes will invalidate the previous codes.



##  **Login with 2 Factor Authentication**

1.  Go to <a href="https://shadesofindia.com/wp-admin" target="_blank">**ShadesofIndia**</a>
2.  Enter Username and Password
3.  Click -> **Log In**

    ![login](Administrator\login.jpg)

4.  When the **2FA Code** prompt appears -> enter the code from the authy app; this code gets updated every 30 seconds
5.  Again Click -> **Log In**

    ![2falogin](Administrator\2falogin.jpg)


##  **Important - Enable 2FA based on Roles**

Once, all the above steps have been followed and the 2FA has been setup, the most **important/mandatory** step to be followed is to **Enable 2FA for the respective roles**. Below are the steps for the same:

1.  Go to -> **Admin Panel**
2.  Go to -> **Wordfence** -> **Login Security**

    ![wordfence](Administrator\wordfence.jpg)

3.  Click -> **Settings**
4.  Tick mark the checkbox -> **Enable 2FA for these roles** - Select the required role

    ![enable2fa](Administrator\enable2fa.jpg)

5.  Click -> **Save settings**

After this, whenever a user of selected role logs in to the WordPress site, user will be asked for two-factor. 

##  **Delete a User**

To delete a user, follow the below steps:

1.  Go to -> **Users** -> **All Users**

    ![allusers](Administrator\allusers.jpg)

2.  Hover over the user you want to delete.
3.  Click -> **Delete**

    ![deleteuser](Administrator\deleteuser.jpg)