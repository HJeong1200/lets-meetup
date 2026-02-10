# Design Spec: Time-Tracking Related

## Goal
Provide a focused, distraction-free interface for users to perform their committed tasks and log their time accurately.

## Scenarios

### 1. Starting Current Timer
*   **Actor**: A user ready to work.
*   **Flow**:
    1.  From Dashboard or Meeting Detail, user clicks "Start Session".
    2.  App enters **Focus Mode** (overlay or dedicated screen).
    3.  Timer starts counting Up (from 00:00) or Down (from Goal Time).
    4.  UI shows "Focusing on [Meeting Name]".

### 2. Pausing Current Timer
*   **Actor**: A user interrupted by a phone call.
*   **Flow**:
    1.  User clicks the large "Pause" button.
    2.  Timer stops.
    3.  Visual state changes (e.g., dimmed, "Paused" label blinking).
    4.  **Backend Action**: A "Session Segment" is recorded (e.g., Duration: 305 seconds).

### 3. Resuming Timer
*   **Actor**: A user returning to work.
*   **Flow**:
    1.  User clicks "Resume".
    2.  Timer continues from where it left off (visually).
    3.  **Backend Action**: A *new* "Session Segment" begins.

### 4. Finishing the Session
*   **Actor**: A user completing the daily goal.
*   **Flow**:
    1.  Timer reaches goal (e.g., 30 mins) OR User clicks "Finish/Stop".
    2.  App asks for confirmation: "Log 30 minutes?".
    3.  User confirms.
    4.  App shows a celebration animation (Confetti).
    5.  **Logic**: System sums all "Session Segments" for the day. If Sum >= Goal, Status = "Complete".
    6.  User is returned to Dashboard with status updated.

## Key UI Elements
*   **Focus Overlay**: Minimalist design to prevent distractions.
*   **Big Controls**: Large Play/Pause buttons.
*   **Visual Timer**: Digital clock + Progress Circle.
