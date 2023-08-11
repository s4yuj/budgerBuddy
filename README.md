# BudgetBuddy
### A Smart Finance Tracker

## About
BudgetBuddy is a personal finance tracker app designed to help 
users stay on top of their expenses and reach their financial goals. 
The app features an easy-to-use interface that allows users to track 
their income and expenses, set budgets, and see where their money 
is going.

In addition to budgeting, BudgetBuddy also 
offers a comprehensive financial tracking feature. 
Users can save up for an emergency fund and track bill payments so that
no bill is left unpaid.


Saving and planning for the future is also a priority for BudgetBuddy, 
with features that enable users to set savings goals and 
track progress towards those goals. 
With BudgetBuddy, users have the ability to see how much they are 
saving and how close they are to reaching their goals.

BudgetBuddy's goal is to make the process of taking control of 
finances as easy and stress-free as possible, by providing tools to 
help users understand their spending habits and make smarter financial
decisions. 

## Inspiration
Effectively tracking your budget and knowing where your money is going
is a skill that can take a lifetime to perfect.
Even then, one has to juggle in their mind how much they should be spending
and how much they should be saving.

In today's day and age, it is imperative to have a
"second brain" or personal assistant take care of your expenses
and budget so that you can focus your attention on things that 
actually matter.

## Technologies used
- Java 19.0.2

## Additional Help Received
- Used code very similar to the TellerApp ui to create a general structure for BudgetBuddy's ui. 

## User Stories
- As a user I want to be able to add my current monthly incoming salary.
- As a user I want to be able to set a strict budget for myself for the month.
- As a user I want to be able to track where I spend money from my budget and 
know how much of my monthly budget I have remaining. (Add multiple expenses into the app)
- As a user I want that the app notifies me when I am about to go over budget.
- As a user I want to have the option to save my budget and expenses data.
- As a user I want to have the option to load my budget and expenses data. 

# Instructions for Grader   
- You can add expenses to the budget by clicking the 
"track new expenses" button. This button allows you to input a new expense amount and what it is towards and saves it
to the JSON file.
- You can generate the first required action related to this by clicking the "print all expenses" button.
This prints all the expenses that have been incurred so far.
- You can generate the second required action related to this by clicking the "save more money" button. This button
allocates some more of your spending money for the month towards your savings. Your current budget state
  (i.e your remaining budget for the month and the amount you've saved so far) can also be viewed by clicking the
  "View Balance & Savings" button.
- You can locate my visual component on the main menu page (the image icon of a money face).
There is another visual component in the message box that confirms the saving of an additional sum (thumbs up emoji).
Finally, you can click the "view credits" button to see a picture of me (the creator).
- You can save the state of the application by clicking the "save state" button"
- You get prompted to load state or start afresh when you first run the application.


# Phase 4 - Task 2
Here is a representative sample of what an Event Log would look like when the user exits the application:

Wed Apr 12 00:41:35 PDT 2023
New budget created for Sayuj

Wed Apr 12 00:41:46 PDT 2023
Tracked 600.0$ towards Rent

Wed Apr 12 00:41:53 PDT 2023
30.0$ saved!

Wed Apr 12 00:42:04 PDT 2023
Tracked 50.0$ towards Groceries

Wed Apr 12 00:42:27 PDT 2023
Tracked 300.0$ towards Pit Night

Wed Apr 12 00:42:48 PDT 2023
Tracked 5000.0$ towards New Car

Wed Apr 12 00:42:49 PDT 2023
75% Budget used.

Wed Apr 12 00:42:53 PDT 2023
2.0$ saved!

# Phase 4 - Task 3
One of the ways in which my design could be refactored and thus improved is if i changed 
the expenses class to a more general name and used the same design that I used for tracking 
expenses to track savings. This would essentially mean creating an interface for a datatype that stores
(amount + towards) and then have 2 arrays that store savings and expenses.
In this way I can abstract out the savings expenses feature and use the same code for savings as well.

An advantage of this refactoring would be a reduction in the amount of code as well as code duplication, 
however, it also means carrying out some unnecessary computation which could lead to slower runtime.

Another opportunity for refactoring can be found in the MainMenu and BudgetBuddyUI classes. 
At present, most of the methods in my ui are located in the BudgetBuddyUI class. 
This means that class has very low cohesion.
This can be greatly improved by refactoring the relationship between MainMenu and BudgetBuddy and sending 
all MainMenu related methods (like what the ui needs to call when a button is pressed) to MainMenu.

This would help increase cohesion according to the Single Responsibility Principle but it 
might affect processing times slightly as a disadvantage.
