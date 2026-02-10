# Design Spec: Sign Up and Log In

## Goal
Enable users to securely access the platform and identify themselves to their groups.

## Scenarios

### 1. New User Sign Up
*   **Actor**: A new user invited by a friend or discovering the app.
*   **Flow**:
    1.  User lands on the Welcome Page.
    2.  User chooses "Get Started".
    3.  User enters Email/Password.
    4.  System creates a new account.
    5.  System prompts for a "Display Name" (this is how they will appear in meetings).
    6.  User is redirected to the Dashboard.

### 2. Returning User Log In
*   **Actor**: A registered user.
*   **Flow**:
    1.  User lands on the Welcome Page.
    2.  User selects "Log In".
    3.  User authenticates.
    4.  User is redirected to the Dashboard.

### 3. Password Recovery
*   **Actor**: A user who forgot their password.
*   **Flow**:
    1.  User clicks "Forgot Password".
    2.  System sends a magic link or reset token to email.
    3.  User sets a new password.

## Key UI Elements
*   **Welcome Screen**: Branding, Value Prop, "Get Started" / "Login" buttons.
*   **Auth Forms**: Clean input fields, error handling (e.g., "Email already taken").
*   **Onboarding Modal**: A simple popup after first signup to set the Display Name.
