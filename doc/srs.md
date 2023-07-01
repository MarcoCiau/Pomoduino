
# Pomoduino Documentation

## Description

Pomoduino combines the Pomodoro time management technique with the flexibility and interactivity of Arduino. The Pomodoro technique is a productivity technique based on dividing time into work and rest intervals to maximize concentration and efficiency. The goal of this project is to create a Pomodoro timer using the Arduino microcontroller and other electronic components.

The Pomoduino will use an Arduino with an ESP32 to control the timer. It will integrate WS2812B LEDs to provide visual feedback, navigation buttons to adjust settings, and a 128x64 I2C OLED display to show information to the user. The Pomoduino software will allow the user to configure the work duration, rest duration, and the number of work-rest cycles before a long break.

During the operation of the Pomoduino, the OLED display will show the remaining time in each interval, while the WS2812B LEDs will provide visual feedback to indicate the timer's status and progress. Additionally, audio notifications will be generated at the end of each interval, helping the user stay focused and take appropriate breaks.

The Pomoduino will offer an intuitive and user-friendly interface, allowing the user to adjust times and navigate between settings using the navigation buttons. The combination of hardware and software will enable effective time management and improve productivity during work sessions.

With the Pomoduino project, users will be able to implement the Pomodoro technique in an interactive and personalized way, maximizing their focus and achieving higher performance in their daily activities.


## Software Requirements Specifications (SRS)

### Introduction
   - Purpose: The purpose of this document is to describe the software requirements for the Pomodoro timer project with Arduino.
   - Scope: The software should control the Pomodoro timer, allow configuration settings, and provide visual and audio feedback to the user.
   - Definitions, Acronyms, and Abbreviations: N/A

### General Description
   - The software will control the Pomodoro timer using an Arduino with an ESP32, WS2812B LEDs, navigation buttons, and a 128x64 I2C OLED display.
   - Users will be able to configure the work and rest duration, as well as the number of cycles before a long break.
   - The software will provide visual feedback through the WS2812B LEDs and display information on the OLED display.
   - Audio notifications will be generated at the end of each work cycle, rest cycle, and complete work-rest cycle before a long break.

### Functional Requirements
   - R1: Timer Configuration
     - R1.1: The software will allow the user to set the work duration in minutes.
     - R1.2: The software will allow the user to set the rest duration in minutes.
     - R1.3: The software will allow the user to set the number of work-rest cycles before a long break.

   - R2: Start the Timer
     - R2.1: The software will allow the user to start the timer from zero.
     - R2.2: The software will provide visual feedback through the WS2812B LEDs to indicate the timer's status.
     - R2.3: The software will provide visual feedback through the WS2812B LEDs to show the progress of the timer.
     - R2.4: The software will display the remaining time on the OLED display during the timer.

   - R3: Navigation and Settings
     - R3.1: The software will allow the user to use the navigation buttons to move between timer settings.
     - R3.2: The software will allow the user to use the navigation buttons to increase or decrease the values of the settings.
     - R3.3: The software will allow the user to save the changes made in the settings.

   - R4: Audio Notifications
     - R4.1: The software will generate a notification sound at the end of each work cycle.
     - R4.2: The software will generate a notification sound at the end of each rest cycle.
     - R4.3: The software will generate a notification sound at the end of a complete work-rest cycle before a long break.

### Non-Functional Requirements
   - RNF1: Intuitive User Interface: The software should have an intuitive and user-friendly interface.
   - RNF2: Resource Efficiency: The software should use Arduino resources efficiently to ensure optimal performance.
   - RNF3: Stability and Reliability: The software should be stable and reliable during the operation of the Pomodoro timer.

### Graphical Interface
   - The software will use a 128x64 I2C OLED display to show information to the user.
   - The following mocks will be displayed on the OLED display:
   #### Home Screen
   In the Home screen, it displays the remaining time for the current session (e.g., 25 minutes for work) and the session type (e.g., "WORK").

    ``` 
    -----------------------------------
    |              HOME                |
    -----------------------------------
    |             WORK                 |
    |                                  |
    |              25                  |
    -----------------------------------
    
    ```

  #### Settings 
  In the Settings screen, the user can adjust the work duration, rest duration, and the number of cycles. The current values are displayed, and the user can make changes as needed.

    ```
    -----------------------------------
    |             SETTINGS            |
    -----------------------------------
    | > Work Duration:       25 min   |
    |   Rest Duration:       5 min    |
    |   Cycles before Long Break:   4 |
    |                                 |
    -----------------------------------

    ```  
## System Requirements

| ID  | Requirement Description                                                                                  |
|-----|---------------------------------------------------------------------------------------------------------|
| RS1 | The system must allow the user to configure the work duration in minutes.                                |
| RS2 | The system must allow the user to configure the rest duration in minutes.                                |
| RS3 | The system must allow the user to configure the number of work-rest cycles before a long break.          |
| RS4 | The system must allow the user to start the timer from zero.                                             |
| RS5 | The system must provide visual feedback through the WS2812B LEDs to indicate the timer's status.        |
| RS6 | The system must provide visual feedback through the WS2812B LEDs to display the timer's progress.       |
| RS7 | The system must display the remaining time on the OLED screen during the timer.                         |
| RS8 | The system must allow the user to navigate between timer settings using navigation buttons.              |
| RS9 | The system must allow the user to increase or decrease the values of the timer settings using buttons.    |
| RS10 | The system must allow the user to save the changes made to the timer settings.                           |
| RS11 | The system must generate a notification sound at the end of each work cycle.                             |
| RS12 | The system must generate a notification sound at the end of each rest cycle.                             |
| RS13 | The system must generate a notification sound at the end of a complete work-rest cycle before a long break. |

## User Stories vs System Requirements

| User Story           | System Requirements       |
|----------------------|---------------------------|
| User Story 1         | RS1, RS2, RS3             |
| User Story 2         | RS4, RS5, RS6, RS7        |
| User Story 3         | RS8, RS9, RS10            |
| User Story 4         | RS11, RS12, RS13          |

### System Requirements vs SRS

Now a clear traceability is established between the system requirements and the corresponding functional requirements. The system requirements provide a high-level overview of the desired features, and the functional requirements specify the specific functions and actions needed to meet those system requirements.

| System Requirement | Functional Requirement |
| --- | --- |
| RS1 | R1.1 |
| RS2 | R1.2 |
| RS3 | R1.3 |
| RS4 | R2.1 |
| RS5 | R2.2 |
| RS6 | R2.3 |
| RS7 | R2.4 |
| RS8 | R3.1 |
| RS9 | R3.2 |
| RS10 | R3.3 |
| RS11 | R4.1 |
| RS12 | R4.2 |
| RS13 | R4.3 |
