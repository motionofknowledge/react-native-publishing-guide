# EAS Setup Guide

## 1. Sign Up for EAS
- Go to the EAS portal and sign up for an account.
- Create a project and copy the **Project ID**.
- Set up the **Project ID** and **Slug** in your `app.json`.

### Example `app.json` Structure
```json
{
  "expo": {
    "slug": "your-app-slug",
    "eas": {
      "projectId": "your-project-id"
    }
  }
}
```

---

## 2. Login to EAS
- Run the following command to log in:
```bash
eas login
```
- Enter your **user ID** or **email** and password.

### Logout of EAS
If needed, logout of your existing session:
```bash
eas logout
```

### Verify Login Status
To check the currently logged-in user:
```bash
eas whoami
```

---

## 3. Configure EAS Build
Run the configuration command:
```bash
eas build:configure
```
- Select "All" or a specific platform during setup.

---

## 4. Build EAS for Specific Platforms
- For iOS:
```bash
eas build --platform ios
```
- For Android:
```bash
eas build --platform android
```

---

## 5. Apple Developer Account Setup
### Sign Up for an Apple Developer Account
1. Create an Apple ID:
   - Go to [Apple ID Creation](https://account.apple.com/account).

2. Enroll in the Apple Developer Program:
   - Visit [Apple Developer Enrollment](https://developer.apple.com/programs/enroll/).

3. Download the **Developer App**:
   - Install the "Developer" app from the App Store on your MacBook.
   - Sign in with your Apple ID.

4. Complete Enrollment:
   - Fill out all required details in the Developer app.
   - Wait 24-48 hours to complete the process.
   - Submit the enrollment payment ($99).

---

## 6. Create App Identifiers
1. Login to your [Apple Developer Account](https://developer.apple.com/account).
2. Under **Program Resources**, click on **Identifiers**.
3. Create a new Identifier:
   - Select **App IDs**.
   - Choose **App** as the type.
   - Enter a description (e.g., your app name).
   - Enter a Bundle ID (e.g., `com.motionofknowledge.app`).

4. Go to **Apps** and create a new app:
   - Enter all required details.
   - Choose the Bundle ID created earlier.
   - Enter a unique SKU (e.g., `com.motionofknowledge.app`).

---

## 7. Update App Store Information
1. Navigate to the newly created app in your Apple Developer account.
2. Update the following:
   - Privacy Policy
   - App Information
   - Pricing & Availability
   - App Screenshots, Metadata, Promotional Text, Description, Developer Notes, and App Credentials (if required).
3. Ensure the app passes the App Store testing process.

---

## 8. Log In for iOS Build
1. Enter your Apple ID and password.
2. If Two-Factor Authentication is enabled, enter the OTP sent to your device.

---

## 9. Generate Certificates and Profiles
1. Generate a new Apple Distribution Certificate: **Yes**.
2. Generate a new Apple Provisioning Profile: **Yes**.

---

## 10. Build Upload
- Your build will automatically be uploaded to EAS.
- **Congratulations!**

### Submit the Build to the App Store
1. After the build is finished, submit it:
```bash
eas submit -p ios --latest
```
2. Open your Apple Developer account and navigate to **Apps** > **Your App**.
3. Under the **App Version**, select the uploaded build.
4. Update any missing policies or details in TestFlight.
5. Submit your app for review.

---

### Recommended Resources
For a detailed video tutorial, check out this [YouTube Guide](https://youtu.be/LE4Mgkrf7Sk?si=RVzFTTrq21a8cj-5).

