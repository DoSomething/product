# Let's Do This

A DoSomething.org native app.

## User Registration

Following fields are required:
* First Name
* Email
* Password
    * Must be at least 6 characters

Not required:
* Mobile number

## Social Integration  

We will create accounts through FB and G+ logins. The back-end schema hasn't been worked out yet, but we can create DS accounts and attach tokens to them to access social graphs for friend lists.

## Campaigns

Campaigns to be included in the app are found by querying the Campaigns endpoint where `mobile_app=true`.

### Main Feed

Campaigns displayed in the Main Feed should be sorted alphabetically.
There are two states of campaign activity. No activity and signed up/completed reportback. Small visual differences accompany each state. 

- No activity: Normal visuals
- Signed up/completed: Yellow bar on left side, button says "More Info"

### Reportbacks

Reportback Items which have been `promoted` should be displayed first, then `approved`.

Tapping on a Reportback Item should display the Reportback Detail view of the selected item.

## User Profile (Hub)

On all screens, if a user avatar/name is tapped, the user's profile is displayed.

Pre-reportback, a upload photo option is shown in place of photo.
Post-reportback, tapping this photo will take you to the reportback detail screen.

### Reportbacks

All of a User's non-`flagged` Reportback Items of current Campaigns are displayed.

## Reportback Detail

Displays:
* Reportback Item image (does not link out)
* User avatar (links to User Profile)
* Campaign Title (links to Campaign Detail)
* Kudos Drawer


### Kudos Drawer

Displays number of Kudos by Kudos Type for a Reportback Item, in descending order of Kudos count.

*e.g. 7 Hearts, 5 Hot Dogs, 3 Stars, 2 Bowling Pins, 0 Rabbits*

If no Kudos exist for a Reportback Item, the Kudos Types are displayed in random order.

Tapping on a Kudos Type will allow the User to submit a Kudos of that Kudos Type.

For v1:
* A user may only submit one Kudos Type
* A user is not able to delete a Kudos Type

# Offline Mode
If the device loses connection, the user is unable to perform any tasks, and a "Fail Whale" screen is displayed.

## Restoring Connection / After Force Quit
Upon restoring connection or upon opening the app after forcing Quit, the User is directed to the Main Feed if a signed in session has been saved.

If a signed in session has not been saved, the user is directed to the User Connect screen (https://github.com/DoSomething/product/blob/master/LetsDoThis/Screens/Onboarding/Log%20In*.png)

