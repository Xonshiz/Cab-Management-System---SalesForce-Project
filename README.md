# Cab-Management-System---SalesForce-Project

This is a very basic `Cab Management System` made for SalesForce Platform as our Summer Training Project. 
We developed it within 1 week, while learning SalesForce side by side, so it's not going to be the BEST logic or cleanest work/project you've ever seen.
This project was developed with the mindset of "Using SalesForce without letting the users know about it". What does that even mean?
We wanted to create a website where users can book a cab, get the cab assigned and then get the bills on their registered E-Mail IDs.All this on SalesForce platform, but the user won't see anything related to SalesForce. They should simply see the website, do their work and be done with it. That's it.


#The Team

Team had 6 members, and here are their names :

1.) [Dhruv Kanojia](https://github.com/Xonshiz)

2.) [Hinshu Jain](https://github.com/CrackedLearner)

3.) [Ankit Passi](https://github.com/ankitpassi141)

4.) [Devesh Shyngle](https://github.com/deveshyngle)

5.) [Raghav Sharma](https://github.com/dkrsharma73)

6.)  Rasil Banga

We're all in our 3rd year of college and are pursuing "C.S.E" from Northern India Engineering College (N.I.E.C).
Not sure why, but we decided to go with the name "Cab Job" as our project name. Maybe because of some dirty reference lol.

#Limitations

1.) There's no `Driver` access currently.

2.) No real time tracking. Hence, the distance calculated in Bill is the `Straight Path` to destination from pickup.

3.) Poorly written VisualPage Code.

4.) User Passwords saved in Object's field as simple text.

#Strong Points

There aren't a lot of strong points for this project, but I'll list some of them anyway :

1.) Since the project is hosted on SalesForce, the data is being transmitted via HTTPS. So, data is somewhat safe

2.) Based on triggers and classes. So, no `major` relationship is needed among various objects.

3.) Proper Errors are generated on wrong data.

4.) Real Time validation of input on Sign Up page.

5.) Highly Customizable

#How to Use

Using this is pretty simple. You'll need to make 4 objects from your side and make some fields in all the objects (would hardly take an hour).
Since this project heavily uses Standard Objects from SalesForce, you won't have to specify objects on each and every page. Most of the work is being done on `Account` Object.
I'll post an image to all the objects and their fields in description as soon as I get the time, so everyone knows which object is being used.
All you need to do is, copy the codes from respective folders and just make some little changes here and there (if you want).

#File Naming
I've organised all the pages, classes and triggers in respective folders with proper extension. The code is well indented, it won't be highlighted on GitHub, because it doesn't support this SalesForce yet, I guess.
File Naming is pretty simple and straightforward, so there shouldn't be a problem. However, in trigger, I followed a special naming pattern.
For example : `Lead_To_Customers (Lead)`

This says that name of trigger is "`Lead_To_Customers`" and it is being activated on "`Lead`".

Anything with the `(Inactive)` tag in it means that it is not being used anywhere. It is not properly working and might be used in future with some updation.

Rest is self-explanatory!

#How does this work?

First, you'll need to update the source code of the VisualForce Pages and Classes, because I did not use partial links when I wrote this. So, update the links in classes as well, because of the PageReference method for page redirection.

Anyways, the basic working of this project is that :

The user will sign up from the sign up page and that data will be saved in a custom object with API name "`Customer__c`". Now, if the data is valid, it'll redirect the user to `Booking Page`, otherwise, it'll refresh the page and show the respective error. The `Email Address` field is Unique, so no repeated records for an email ID. Now, whatever you enter in booking page, it'll go and save in `Account`, a standard object. and a trigger will be activated when this runs, which will check the entered phone number and fetch the related email ID from the `Customer__c` into `Account`. And another trigger will be fired after insertion, that will copy the Phone Number from Ph_Num field of account an add it into the `Name` field of `Account` Object.
Now, after Booking, you'll see a thank you page and an email will be sent to the registered email ID with the billing details.


There's no driver's scenario, that is why the trip ends as soon as it starts. We'll probably work on this and make something out of it for driver, so the driver can end the trip status and some other things happen and it gets the job done.

Anyway, the project is very basic and does what it is intereded to do without any kind of problem(s).

Btw, there's a login functionality and password reset functionality, which is done via apex class. Look for it in the code itself ;)


#Notes

Special thanks to our trainer `Mr. Shiv Shankar` for his help in writing some of these triggers and classes.

The website's layout was ripped off of a template designed by `W3layouts`. You can find it [HERE](https://w3layouts.com/city-taxi-taxi-services-mobile-website-template/).

I had to keep all the CSS, JS and jQuery in the VisualForce pages because it wasn't accepting the external file for some reason.


