# 🔧 CORS Problem Solving — Firebase Storage & Flutter Web

A step-by-step guide to fixing **CORS (Cross-Origin Resource Sharing)** errors when loading images from **Firebase Storage** in **Flutter Web** applications.

---

## 📖 What is a CORS Issue?

**CORS** is a browser security rule that controls whether a website is allowed to access resources hosted on a different domain.

When a Flutter Web app tries to load an image from Firebase Storage, the browser checks whether Firebase Storage permits your website to access that image.

> ⚠️ If permission is not granted, the browser **blocks the image** and throws a CORS error in the console.

This guide walks you through configuring your Firebase Storage bucket's CORS policy via **Google Cloud Console** so your Flutter Web app can load images without issues.

---

## 🗂️ Table of Contents

- [Step 1 — Open Google Cloud Console](#step-1--open-google-cloud-console)
- [Step 2 — Select Your Project](#step-2--select-your-project)
- [Step 3 — Navigate to Cloud Storage Buckets](#step-3--navigate-to-cloud-storage-buckets)
- [Step 4 — Open Bucket Configuration](#step-4--open-bucket-configuration)
- [Step 5 — Enable CORS](#step-5--enable-cors)
- [Step 6 — Add CORS Configuration](#step-6--add-cors-configuration)

---

## Step 1 — Open Google Cloud Console

👉 [Click here to open Google Cloud Console](https://console.cloud.google.com/welcome?project=quran-academy-b27b5)

> ✅ Make sure the **logged-in Google account** matches the account that owns your **Firebase project**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/761e4c8fe9fc0478a4db6471b339f2f5f67d55fa/CORS%20problem%20solving/1.GoogleClodeConsole.png" alt="Google Cloud Console" width="700">
</p>

---

## Step 2 — Select Your Project

In the Google Cloud Console, click on the **project selection area** at the top to view your available projects.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/640afeba6841e2f6a925c8e9f6edf4107264c6b0/CORS%20problem%20solving/2.ViewProject.png" alt="View Project Selector" width="700">
</p>

Then select the correct project from the list.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/66de92f5847e03756e05d6c2c52a947f683e8492/CORS%20problem%20solving/3.SelectProject.png" alt="Select Project" width="700">
</p>

---

## Step 3 — Navigate to Cloud Storage Buckets

Once the console switches to your selected project, open the sidebar menu, go to **Cloud Storage**, and select **Buckets**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac9053/CORS%20problem%20solving/4.Selected%20Project%20Console.png" alt="Selected Project Console" width="700">
</p>

Go to **Cloud Storage** → **Buckets**:

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/8298abe3f75410416b7314f25ea385ed52ac9053/CORS%20problem%20solving/5.TakeCloudeBucket.png" alt="Cloud Storage Buckets" width="700">
</p>

---

## Step 4 — Open Bucket Configuration

In the **Buckets** section, click on your project's storage bucket, then select the **Configuration** tab.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/6.SelectProjectStorage.png" alt="Select Project Storage Bucket" width="700">
</p>

Select **Configuration**:

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/43f3306fb15e6e588a77c4e1777dc9f057f28640/CORS%20problem%20solving/7.SelectConfiguration.png" alt="Select Configuration Tab" width="700">
</p>

---

## Step 5 — Enable CORS

Scroll to the **Cross-Origin Resource Sharing (CORS)** section.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/84a90bdf79826a51a34139945150c6a2c8bb48f5/CORS%20problem%20solving/8.SelectCORS.png" alt="Select CORS Section" width="700">
</p>

Toggle **Allow Cross-Origin Resource Sharing**, then click **Add a configuration**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/be52261b4c2b67d3a927d728ef521c055ac79567/CORS%20problem%20solving/9.AddConfiguration.png" alt="Add CORS Configuration" width="700">
</p>

---

## Step 6 — Add CORS Configuration

In the configuration form, enter the following values:

| Field | Value |
|---|---|
| **List of Allowed Origins** | `*` |
| **Specify Methods** | `HEAD`, `GET` |
| Everything else | Leave empty |

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/c83e71298c9204eaade241f4b5e49e83416eb67e/CORS%20problem%20solving/10.Configuring.png" alt="Configuring CORS Fields" width="700">
</p>

Leave the remaining fields empty, then click **Save**.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/c83e71298c9204eaade241f4b5e49e83416eb67e/CORS%20problem%20solving/11.balanceConfig.png" alt="Save CORS Configuration" width="700">
</p>

✅ After saving, you'll see your changes reflected here and across your project.

<p align="center">
  <img src="https://github.com/ihsan7770/CORS-problem-solving/blob/907b6acc57ff706637d89ca85c00d5ce707f711c/CORS%20problem%20solving/12.See%20Configured.png" alt="Configured CORS Confirmation" width="700">
</p>

---

## ✅ Result

Your Firebase Storage bucket now allows cross-origin requests, so your Flutter Web app can load images from Firebase Storage without CORS errors. 🎉

---

## 📌 Notes

- Using `*` for allowed origins permits **any** domain to access the bucket's resources via `GET`/`HEAD`. For production apps, consider restricting this to your app's specific domain(s) for better security.
- Changes to bucket CORS configuration may take a few minutes to propagate.

---

<p align="center">Made with ❤️ for Flutter Web + Firebase developers</p>
