# Book by Slot 
![](https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/logo.png)

Book by Slot is a django application developed to book room slots.

## Features
- Authenticated users can sign in
- Two roles are defined- Manager and Customer
- Manager can add, update and delete rooms, slots and advance number of days booking allowed
- Manager can view booking history with details of customer who booked
- Users can update their profile
- Customer can book rooms on given slots only 'x' days before(as defined by the manager)
- Customer can view(past+future) and cancel their bookings
- No two customer can book same slots for rooms

## Technology Stack

 1.  Python 3.10.3
 2.  Django 2.2.26
 4.  HTML, CSS
 5.  JavaScript

### Dependencies

1. date, datetime


## How to Run?
1. Download and install Python 3.10.3
2. Open powershell and navigate to the folder where you want to clone the repo `cd targetFolder`
3. Run `git clone https://github.com/vishalkumar-30/BookBySlot.git`
4. Navigate to the root folder `cd BookBySlot`
5. Install virtualenv `pip install virtualenv`
6. Create a virtual environment `virtualenv env -p python3.10.3`  
7. Activate the env `env/Scripts/activate`
8. Install the requirements: `pip install -r requirements.txt`
9. Change directory `cd BookBySlot`
10. Make migrations `python manage.py makemigrations`
11. Migrate the changes to the database `python manage.py migrate`
12. Create admin(as stated in assumptions) `python manage.py createsuperuser`
13. Run the server `python manage.py runserver`
14. Navigate to http://127.0.0.1:8000/ on any browser

## Assumptions
1.  There is one admin who takes care of users who logs in.
2.  He has a privilege to visit http://127.0.0.1:8000/admin with username, password created in superadmin coommand below and can modify role of any logged in user to manager.
3.  At a particular time only one manager can exit, if admin made another manager at the same time then the first one will become a customer again.
4.  There will not be a case that no manager is present, condion to ensure this is being added already.

## Workflows

### HomePage

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/Homepage.png">

### Admin
Admin has superuser privilege, he will log into `http://127.0.0.1:8000/admin` with the username and password created in the above `step 12`. Then navigate to `/home/profile`.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/adminpanel.png" width="700" height="400">

Now, admin can select any user and promote them as a manager.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/adminrights.png" width="700" height="400">

### Manager

#### Sign up
Sign up to BookBySlot website by entering username, password and confirm that.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managersignup.png" width="700" height="400">

#### Log in
After signing up you will be redirected to update profile page, and if you want to log in again after log out then you can do so by entering your username and password.


<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerlogin.png" width="700" height="400">

#### Manager Home Page
Once you log in this page will show you the rooms, time slots and days allowed to pre book rooms.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerhomepage.png" width="700" height="400">

#### Manage Rooms
In this tab there are three options to manage and add **rooms available**, **time slots** for that and **advance number of days** to pre book.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerooms&options.png" width="700" height="400">

#### Updating time slots
You can add new slots, if any overlapping happens, all such cases are taken care of.

From here you can also delete time slots. If there are no bookings made for the deleted slot, the deletion will take effect from the very next day. Otherwise, the deletion of the slot will take effect from the day next to the day of last Pre-Booking.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managetimeslots.png" width="700" height="400">

#### Booking History
Manager can also see all booked rooms and their status details.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerseebookings.png" width="700" height="400">

The details of customer who booked that room can also be checked here.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerseecustomerdetails.png" width="700" height="400">

#### Update Profile
User can update when they sign up, and also they can navigate to update profile tab as well.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/managerupdateprofile.png" width="700" height="400">

### Customer

#### Sign up
Sign up to BookBySlot website by entering username, password and confirm that.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customersignup.png" width="700" height="400">

#### Log in
After signing up you will be redirected to update profile page, and if you want to log in again after log out then you can do so by entering your username and password.


<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customerlogin.png" width="700" height="400">

#### Customer Home Page
Once you log in as a customer, this page will show you the tab to book rooms and the number of days before which you can book a room.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customehomepage.png" width="700" height="400">

So by selecting slots given by the manager you can also book rooms in below way.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customerbooks.png" width="700" height="400">

#### History of Bookings
Customer can also view all booked rooms and their status details.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customerseebookings.png" width="700" height="400">

The details of manager who provided that room and time slot can also be checked here.

<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customerseemanagerdetails.png" width="700" height="400">

If customer wants to cancel the booking that can also be done.
<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customercancels.png" width="700" height="400">

#### Update Profile
Customer can update when they sign up, and also they can navigate to update profile tab as well.
<img src="https://github.com/vishalkumar-30/BookBySlot/blob/main/Screenshots/customerupdateprofile.png" width="700" height="400">

## How to run tests?
1. Navigate to the project folder `cd BookBySlot`
2. Activate the virtual environment created above `env/Scripts/activate`
3. Run `cd BookBySlot`
4. Run `python manage.py test home`

## Author
- Name: Vishal Kumar
- Email: vishal1924s@gmail.com
