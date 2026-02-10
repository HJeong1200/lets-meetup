# Design Spec: Current Meeting Related

## Goal
Provide a clear overview of the user's commitments and the collective progress of their groups.

## Scenarios

### 1. Viewing Currently Joined Meetings (Dashboard)
*   **Actor**: A user logging in to check their day.
*   **Flow**:
    1.  Dashboard displays a grid/list of "Active Meetings".
    2.  Each card shows:
        *   Meeting Title.
        *   **My Status Today**: e.g., "0/30 mins" (Pending) or checkmark (Done).
        *   **Group Status**: Small avatars of who else finished today.

### 2. Viewing a Specific Meeting (Detail View)
*   **Actor**: A user wanting to see who is slacking off or doing well.
*   **Flow**:
    1.  User clicks a meeting card.
    2.  **Leaderboard/Grid**:
        *   Rows: Members.
        *   Columns: Days (Mon, Tue, Wed...).
        *   Cells: Status indicators (Done, Missed, Frozen/Rest).
    3.  **Feed**: "Alice completed 30m just now."

### 3. Viewing My Status
*   **Actor**: The user.
*   **Flow**:
    1.  On the dashboard, the user sees their "Daily Progress".
    2.  Visual feedback (e.g., a filling ring or progress bar) indicates how much is left for the day across all meetings.

### 4. Viewing Other People's Status
*   **Actor**: A user checking on a friend.
*   **Flow**:
    1.  In the Meeting Detail view, user taps on a friend's avatar.
    2.  User sees their streak for this meeting and recent activity logs.

## Key UI Elements
*   **Dashboard Grid**: High-level summary.
*   **Status Indicators**: Clear colors (Green=Done, Grey=Todo, Red=Missed).
*   **Member List**: easy way to see everyone in the group.
