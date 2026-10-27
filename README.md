# MyAccountApp - Practical Tutorial 04

## Overview
This mobile application was developed as part of **Practical Tutorial 04: Data Transfer Between Screens and Form Handling** for the Mobile Application Development module. The application demonstrates form handling, state management, screen navigation, data passing between screens, and conditional logic using React Native and Expo Router.

---

## Features Implemented

1. **User Registration Form (`app/index.js`)**:
   - Captures user input (Username, Email, Phone Number, Year of Birth, Password, and Confirm Password) using React Native's `TextInput` and `useState` hooks.
   - Validates that all fields are filled before submitting.
   - Checks if passwords match[cite: 2].
   - Calculates the user's age dynamically based on the provided year of birth.
   - Navigates to the Review screen while passing user data using `router.push()` with `params`.

2. **Review Screen (`app/review.js`)**:
   - Retrieves parameters passed from the registration screen using `useLocalSearchParams()`.
   - Displays the captured details: Username, Email, Phone Number, and calculated Age.
   - Includes an **"Edit Info"** button utilizing `router.back()` to navigate back while preserving previous state.
   - Implements **Conditional Navigation**: Validates if the user is 18 years or older[cite: 5]. If under 18, shows an alert preventing submission[cite: 5]. Otherwise, routes to the success screen.

3. **Success Screen (`app/success.js`)**:
   - Extracts the `userName` parameter.
   - Greets the user with a confirmation screen confirming successful account creation.

---



