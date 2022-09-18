# User in jenkins

### Add User in jenkins
1. Step 1) 
   - Login to Jenkins Dashboard
   - Login to your Jenkins dashboard by visiting http://localhost:8080/
   - If you haven’t installed Jenkins in your local server, go to the appropriate URL and access your dashboard by using your login credentials.
   - ![Jenkins Login Page](https://www.guru99.com/images/1/091318_0444_HowtoCreate1.png)

2. Step 2) 
   - Choose the option
   - You will now see options to create and add user in Jenkins and manage current users.

3. Step 3) 
   - Create a new User
   - Under Manage Jenkins, Click Create User
   - Enter Jenkins add user details like password, name, email etc.
   - Click Create User
   - ![create user in jenkins](https://www.guru99.com/images/1/091318_0444_HowtoCreate2.png)

4. Step 4) 
   - User is created
   - You will see on the dashboard that a new Jenkins create user as per the details entered.
   - ![Users in Jenkins](https://www.guru99.com/images/1/091318_0444_HowtoCreate3.png)

### How to Install Role Strategy Plugin in Jenkins
There are two methods for installing plugins in Jenkins:
1. Installing it through your Jenkins dashboard
2. Downloading the plugin from Jenkins website and installing it manually.
---
1. Step 1)
   1. Go to Manage Jenkins
   2. Click on the Manage Plugins option
   ![Manage Jenkins](https://www.guru99.com/images/1/091318_0444_HowtoCreate4.png)
2. Step 2)
   1. In available section, screen Search for “role”.
   2. Select Role-based Authorization Strategy plugin
   3. Click on “Install without restart” (make sure you have an active internet connection)
   ![Role-based Authorization Strategy plugin](https://www.guru99.com/images/1/091318_0444_HowtoCreate5.png)
3. Step 3)
   1. Once the plugin is installed, a “success” status will be displayed.
   ![Installing plugin](https://www.guru99.com/images/1/091318_0444_HowtoCreate6.png)
4. Step 4)
   1. Go to Manage Jenkins -> Configure Global Security -> Under Authorization, select Role Based Strategy. Click on Save.
   ![Configure Global Security](https://www.guru99.com/images/1/091318_0444_HowtoCreate7.png)

### How to Manage Users and Roles in Jenkins
Following are the steps on how to manage and assign roles in Jenkins:

Step 1)
1. Go to Manage Jenkins
2. Select Manage and Assign Roles
![Manage and assign Roles Dashboard](https://www.guru99.com/images/1/091318_0444_HowtoCreate8.png)
>Note: that the Manage and Assign Roles option will only be visible if you’ve installed the role strategy plugin.

Step 2) Click on Manage Roles to add new roles based on your organization.
![](https://www.guru99.com/images/1/091318_0444_HowtoCreate9.png)

Step 3) To create a new role called “developer”,
![Developer Role](https://www.guru99.com/images/1/091318_0444_HowtoCreate10.png)

```
Type “developer” under “role”.
Click on “Add” to create a new role.
Now, select the Jenkins user permissions you want to assign to the “Developer” role.
Click Save
```

### How to Assign Roles in Jenkins
Step 1) Now that you have created roles, let us assign them to specific users.
1. Go to Manage Jenkins
2. Select Manage and Assign Roles

Step 2) We shall add the new role “developer” to user “guru99”
1. Selector developer role checkbox
2. Click Save


References:
- https://www.guru99.com/create-users-manage-permissions.html