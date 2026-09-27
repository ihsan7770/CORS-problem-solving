# CORS-problem-solving
A step-by-step guide to solve CORS issues when loading Firebase Storage images in Flutter Web applications



**Step 1**
Open Google Cloud Console [Click here](https://console.cloud.google.com/welcome?_gl=1*1k3ttpn*_up*MQ..*_gs*MQ..&gclid=CjwKCAjw_eLVBhBEEiwAeaYZfIW_6roEfZyucTVzlot4C-0q5-ve_AaT_XrxXEgCFfAjCumqXfcGURoCwtkQAvD_BwE&gclsrc=aw.ds&project=quran-academy-b27b5)

Make sure that the logged-in email account and the Firestore project account are the same.

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/761e4c8fe9fc0478a4db6471b339f2f5f67d55fa/CORS%20problem%20solving/1.GoogleClodeConsole.png)


**Step 2**
In the Google Cloud Console, you can see the project selection area. Click on it to view the available projects.

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/640afeba6841e2f6a925c8e9f6edf4107264c6b0/CORS%20problem%20solving/2.ViewProject.png)
Select the project from here

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/66de92f5847e03756e05d6c2c52a947f683e8492/CORS%20problem%20solving/3.SelectProject.png)
**Step 3** 
The console will switch to the selected project. Go to the menu, select **Cloud Storage**, and then select **Buckets**.

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac9053/CORS%20problem%20solving/4.Selected%20Project%20Console.png)
Go to Cloude Storage and then select Buckets
![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac9053/CORS%20problem%20solving/5.TakeCloudeBucket.png)

**Step 3** 

In the Buckets section, you will see the storage bucket for your project. Click on the bucket, then select Configuration
![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/6.SelectProjectStorage.png)

Select Configuration
![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/7.SelectConfiguration.png)

**Step 4**
Select Cross-Origin Resource Sharing (CORS)

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/84a90bdf79826a51a34139945150c6a2c8bb48f5/CORS%20problem%20solving/8.SelectCORS.png)

Then select Allow Cross-Origin Resource Sharing. An Add a configuration button will appear. Click on it.

![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/be52261b4c2b67d3a927d728ef521c055ac79567/CORS%20problem%20solving/9.AddConfiguration.png)

**Step 5**

In the configuration, enter `*` in the List of  **List of Allowed Origins** field. Under **Specify Methods**, select **HEAD** and **GET**. Leave the remaining fields empty, and click **Save**.

 ![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/c83e71298c9204eaade241f4b5e49e83416eb67e/CORS%20problem%20solving/10.Configuring.png)

 Leave the remaining fields empty, and click **Save**. 
 ![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/c83e71298c9204eaade241f4b5e49e83416eb67e/CORS%20problem%20solving/11.balanceConfig.png)

 After saving, you can see the changes here and in Your Project .
  ![App Screenshot](https://github.com/ihsan7770/CORS-problem-solving/blob/907b6acc57ff706637d89ca85c00d5ce707f711c/CORS%20problem%20solving/12.See%20Configured.png)



