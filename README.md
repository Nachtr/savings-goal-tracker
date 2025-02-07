# savings-goal-tracker
This is an assignment for my Flatiron x SMU AI bootcamp. The goal of this assignment is to complete the following scenario:

-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-
Imagine you are a junior developer working for a financial technology company. Your team is 
tasked with developing a new feature for the company’s mobile banking app that enables users 
to set and track their savings goals.

Your specific responsibility is to develop the functionality for the savings goal tracking system. 
This system should be able to set new savings goals based on specific users and set dates to achieve
said goals, as well as update the savings progress towards the goals. It should also include a user 
notification when a goal date is approaching and the savings has not been met.
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

Requirements Analysis:
- Lets identify the main functionalities of the system.
    - Savings Goal
        - The user should be able to create, and store savings goal targets with a targeted date
    - Savings Progress
        - The user should be able to successfully edit/update the amount saved
    - Savings Goal Status
        - The system should retrieve the current status of the goal and determine how much has been saved vs the targeted goal.
    - Savings Goal Notification
        - If the target date is approaching and the goal has not been fulfilled, the system should send an alert to the user.

Variables:
UserID
TargetAmount
TargetDate
TotalAmountSaved


Inputs and Outputs: # I know this isnt how this was supposed to be interpreted in the instructions, but I wanted to define the verbs anyways!
  Create:
    - Input
      - UserID
      - TargetAmount
      - TargetDate
    - Output
      - Print a message confirming that the users goal has successfully been set!
  Store:
    - Input:
      - UserID
      - TargetAmount
      - TargetDate
      - AmountSaved
    - Process: # Im defining a process to explain why this is important
      - Saves the goal information in the system.
    - Output:
      - Data is stored (consider no visible outputs...)
      - Error Statement should display as: "An error has occured while trying to save your goal. Please try again!"
  Retrieve:
    - Input:
      - UserID
    - Output:
      - Display the stored data for the user:
        - "Savings Goal: $1000 | Deadline: 2025-06-01 | Current Savings: $200 | 20% Complete!"
  Update:
    - Input:
      - UserID
      - DepositAmount (new amount to add to savings)
    - Output:
      - "Savings Updated! New balance: $500" or some sort of message similar. 
  Return:
    - Input:
      - UserID
    - Output:
      - "You have saved $X amount of your $X goal. You are X% complete!"
  Composing
    - Input:
      - UserID
      - TargetDate
      - TargetAmount
      - AmountSaved
      - CurrentDate
    - Output:
      - "Reminder: Your savings goal deadline is in X days! You have saved $X out of $X."
