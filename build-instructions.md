### Build Instructions

1. Go to the following link [Meal Or No Meal](https://github.com/meal-or-no-meal/meal-or-no-meal-android)
2. Click on the green Code button
3. Ensure that Clone with SSH is selected
    * If HTTPS is selected, click on SSH in the upper right-hand corner of dialog box.
4. Click on the clipboard icon next to the SSH key value to copy the key
5. Refer to your IDE and choose to create your project from version control
6. Specify that the Version Control is Git
7. Paste the key into URL field and click open
8. If you are testing app on an emulator on your computer skip to step 14
9. If you are testing on a physical Android device, you will need to find your computer's local IP address
10. Copy the IP address 
11. Navigate to the local.properties file in the project
12. Paste the following value on the last clear line of the file `base_url = {YOUR.IP.VALUE}`
13. Replace `{YOUR.IP.VALUE}` (including the brackets `{}`) with the IP address from your computer 
14. Once fully loaded, click on Play
    * This will build the app and open it in your emulator or attached device