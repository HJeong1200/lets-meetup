# Design Spec: New Meeting Related

## Goal
Facilitate the formation of "Meetings" (Groups) where users commit to shared goals.

## Scenarios

### 1. Creating a New Meeting (Group)
*   **Actor**: A user who wants to lead a challenge (e.g., "Morning Jog").
*   **Flow**:
    1.  User clicks "Create New Meeting" on the dashboard.
    2.  User inputs:
        *   **Title**: e.g., "5AM Club".
        *   **Description**: Purpose of the meeting.
        *   **Target Goal**: e.g., "Jog for 30 mins".
        *   **Frequency**: e.g., "5 days / week".
        *   **Schedule**: Start Date and End Date (or "Forever").
        *   **Privacy**: Public (searchable) or Private (invite only).
        *   **Max Participants**: e.g., 4 people (to keep it intimate, or unlimited).
    3.  System creates the meeting and assigns the user as "Host".
    4.  System generates a **Shareable Invite Link**.

### 2. Joining a Meeting via Link
*   **Actor**: A user who received a link (e.g., via WhatsApp).
*   **Flow**:
    1.  User clicks the link.
    2.  App opens a "Join Meeting" preview card showing Title, Host, and Goal.
    3.  User confirms "Join".
    4.  Meeting is added to their Dashboard list.

### 3. Searching for an Active Meeting
*   **Actor**: A user looking for a community.
*   **Flow**:
    1.  User navigates to "Explore" or "Search".
    2.  User types keywords (e.g., "Reading", "Code").
    3.  App displays a list of *Public* meetings.
    4.  User views details and clicks "Join".

## Key UI Elements
*   **Create Modal/Page**: distinct steps for setup vs. goal definition.
*   **Invite Card**: A visually appealing summary to confirm joining.
*   **Search Bar & Filters**: To find relevant public groups.
