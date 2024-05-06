Lab 4a - IAM

•	These are the steps to create a IAM user With pasword and Multifactor Authentication.

Firstly, I logged into my AWS account using my main credentials, and once inside, I navigated to the IAM section, where user management and permissions are handled. There, I clicked on "Add user" and gave the new user a name. I then determined the type of access this user should have, whether it's through code or the console. Carefully considering security, I assigned only the necessary permissions, ensuring the user had access to what they needed, but no more.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/af61a918-c94f-45a8-a488-9eab478cfcdf)


Here I had created a new user name IAM_USER and added EC2 permission only so that, this user has permission to create EC2 only.

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/cddb5796-e7b1-4aed-81a8-e5202e60b8c7)

 

Give the User console access and create a password for this user to login with IAM User. As shown in the fig I had given the user and password.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/1b920651-c22d-4abf-960f-3c35ded31683)

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/f0563c6f-23bf-4cb5-bebf-660dcb9d4eda)
 

Now for Multifactor Authentication, I had used Authenticator app in my Android for login with random 6 digit code give by the Authenticator.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/4311c330-b80c-400d-a31a-d4ed4d41fe34)


By scanning the QR code we can connect the IAM user with Authenticator.  It will generate multiple 6 digit code and give to Android devices every minute.

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/7ba1adab-7471-4793-ac0a-6de267d41eb4)
 
Here I successfully assigned MFA to this IAM USER.
![image](https://github.com/sainakka5/IAM-USER/assets/136338958/af66e573-1b33-40b4-bacb-6112ccb0ef44)
 

Now copy the Url of this user and paste in new tab to login into console by IAM user

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/c02debda-5796-414a-85bf-33cb002943ab)

 
https://406316190827.signin.aws.amazon.com/console

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/da3f1de9-336f-4a05-9d1e-3f2a7089b118)
 

After creating the user, I logged out and tested the new user's login credentials. It went smoothly, but there was an extra layer of security - Multi-Factor Authentication (MFA). This required verifying my identity with both a password and a special code from my phone or another device, adding an extra level of protection to my account.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/ee0cf392-c30b-48dc-90c9-55d39e1bc670)


Here I gave the 6 digit Authentication code which I had given as shown in the fig.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/e5ba2f17-72c6-42e2-b8d9-6a22a2a65aad)


After the I had login to the Aws account with limited access of this Aws account, which is only ec2 access.

 ![image](https://github.com/sainakka5/IAM-USER/assets/136338958/89d8a30e-64a6-4569-8739-476c33a8617b)


I had successfully launched EC2 instance form this user, but this user does not have other permissions accept EC2.
 
![image](https://github.com/sainakka5/IAM-USER/assets/136338958/090c417e-7216-4218-b98e-35da75454f6a)


Here I try to create S3 bucket which is not possible from this user, at last it failed to create because of lack of permissions.
 
![image](https://github.com/sainakka5/IAM-USER/assets/136338958/5116ce53-9da4-4a6e-a9ff-3a4fc9853f68)


Everything seemed to be going smoothly until I tried to access a service that I hadn't granted permissions for. I quickly realized that the IAM user didn't have the necessary privileges to use that particular service, and I was promptly denied access.

![image](https://github.com/sainakka5/IAM-USER/assets/136338958/65702e75-cd24-44c9-97dd-96e281e2238b)

 

This experience served as a valuable lesson in the importance of carefully managing permissions within AWS. By granting limited access to only the resources and services needed for each user's role, I was able to enhance the security of my AWS account and protect against unauthorized access to sensitive data and resources.

From this task I ensuring a record of your actions and the security measures implemented. These screenshots, along with explanations detailing the significance of each step, were compiled and submitted according to the assignment instructions, demonstrating your commitment to enhancing the security of your AWS account.
I got some experience in creating the IAM USER with limited access with MFA.
