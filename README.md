# CORS Problem Solving in Flutter Web

A step-by-step guide to solving **CORS (Cross-Origin Resource Sharing)** issues when loading images from **Firebase Storage** in Flutter Web applications.

---

## 📌 What is a CORS Issue?

**CORS (Cross-Origin Resource Sharing)** is a browser security mechanism that controls whether a website is allowed to access resources from another domain.

When a **Flutter Web** application tries to load an image from **Firebase Storage**, the browser checks whether Firebase Storage allows the website to access that resource.

If the required permission is not configured, the browser blocks the request and displays a **CORS error**.

---

# 🚀 Step-by-Step Guide

## Step 1 — Open Google Cloud Console

Open the **Google Cloud Console**:

👉 [Open Google Cloud Console](https://console.cloud.google.com/)

Make sure that the logged-in Google account has access to the Firebase/Google Cloud project you want to configure.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/761e4c8fe9fc0478a4db6471b339f2f5f67d55fa/CORS%20problem%20solving/1.GoogleClodeConsole.png?raw=true" width="800">
</p>

---

## Step 2 — Select Your Project

In the Google Cloud Console, click the **Project Selector** at the top of the page.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/640afeba6841e2f6a925c8e9f6edf4107264c6b0/CORS%20problem%20solving/2.ViewProject.png?raw=true" width="800">
</p>

Select the project associated with your Firebase application.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/66de92f5847e03756e05d6c2c52a947f683e8492/CORS%20problem%20solving/3.SelectProject.png?raw=true" width="800">
</p>

---

## Step 3 — Open Cloud Storage

After selecting the project:

1. Open the **Navigation Menu**.
2. Select **Cloud Storage**.
3. Select **Buckets**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac905c/CORS%20problem%20solving/4.Selected%20Project%20Console.png?raw=true" width="800">
</p>

Select **Buckets**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac905c/CORS%20problem%20solving/5.TakeCloudeBucket.png?raw=true" width="800">
</p>

---

## Step 4 — Select Your Storage Bucket

In the **Buckets** section, find the Cloud Storage bucket associated with your Firebase project.

Click the bucket.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/6.SelectProjectStorage.png?raw=true" width="800">
</p>

Then select **Configuration**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/7.SelectConfiguration.png?raw=true" width="800">
</p>

---

## Step 5 — Open CORS Configuration

Inside the bucket configuration, select:

**Cross-Origin Resource Sharing (CORS)**

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/84a90bdf79826a51a34139945150c6a2c8bb48f5/CORS%20problem%20solving/8.SelectCORS.png?raw=true" width="800">
</p>

Then select **Allow Cross-Origin Resource Sharing**.

An **Add a configuration** button will appear.

Click **Add a configuration**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/be52261b4c2b67d3a927d728ef521c055ac79567/CORS%20problem%20solving/9.AddConfiguration.png?raw=true" width="800">
</p>

---

## Step 6 — Configure CORS

In the configuration:

### Allowed Origins

Enter:

```text
*


