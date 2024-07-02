# Project. Hotel Management System

### Idea: Hotel Reservation System

#### Business Requirements 

We want to create a database for a hotel. It should contain information about guests (name, surname, date of birth, contact information) and employees (name, surname, date of employment, date of dismissal (if the employee is no longer employed)). An employee can be either a manager, receptionist, cleaner, maintenance staff, or other staff members. 

For the manager, we need to store an email, phone number, and biography as well. In addition, we want to store information about the departments they oversee. 

Our system should have the ability to manage our room inventory. We need to know what types of rooms we have (e.g., single, double, suite), room numbers, and the number of each type available. Each room should also have details such as price per night, amenities, and current status (available, occupied, under maintenance). 

Each guest of the hotel can make reservations. We need to remember the reservation details such as check-in date, check-out date, room type, and status (confirmed, canceled, checked-in, checked-out). A guest can also have multiple reservations over time. 

To generate revenue, guests should pay for their reservations, so we want to store information about all payments including the date, type of payment (cash, card, online, etc.), and amount of each payment (payments for a reservation can be split into several transactions). 

We also want to manage services provided to guests such as room service, laundry, spa, and dining. For each service, we need to store information about the type of service, date and time of service, charges, and the employee who provided the service. 

Additionally, we want to store feedback and ratings from guests about their stay, including comments and ratings for specific services or facilities. 
  
#### Entities and Attributes 

1. **Guests** 

   - ID 

   - Name 

   - Surname 

   - Date of Birth 

   - Contact Information (Email, Phone Number, Address) 

   - Membership Status (Regular, VIP, etc.) 

  

2. **Employees** 

   - ID 

   - Name 

   - Surname 

   - Date of Employment 

   - Date of Dismissal (if applicable) 

   - Role (Manager, Receptionist, Cleaner, etc.) 

   - Contact Information (Email, Phone Number) 

   - Biography (for Managers) 

  

3. **Rooms** 

   - Room Number 

   - Room Type (Single, Double, Suite, etc.) 

   - Price Per Night 

   - Amenities (WiFi, TV, Minibar, etc.) 

   - Status (Available, Occupied, Under Maintenance) 

  

4. **Reservations** 

   - Reservation ID 

   - Guest ID 

   - Room Number 

   - Check-in Date 

   - Check-out Date 

   - Status (Confirmed, Canceled, Checked-in, Checked-out) 

  

5. **Payments** 

   - Payment ID 

   - Guest ID 

   - Reservation ID 

   - Date 

   - Type of Payment (Cash, Card, Online, etc.) 

   - Amount 

  

6. **Services** 

   - Service ID 

   - Service Type (Room Service, Laundry, Spa, Dining, etc.) 

   - Date and Time 

   - Charge 

   - Employee ID (who provided the service) 

  

7. **Feedback** 

   - Feedback ID 

   - Guest ID 

   - Date 

   - Comments 

   - Ratings (for services or facilities) 

  

#### Example Scenarios 

  

1. **Guest Check-In/Check-Out**: Track the check-in and check-out dates for guests, including room assignments and payment processing. 

2. **Room Management**: Monitor room availability, maintenance schedules, and occupancy. 

3. **Service Provision**: Record details of additional services used by guests, including charges and employee assignments. 

4. **Payment Tracking**: Maintain detailed records of all payments made by guests, including payment types and amounts. 

5. **Guest Feedback**: Collect and analyze guest feedback to improve services and facilities. 

 

 

 

Functional Requirements for the Hotel Reservation System 

  

1. **Find All Reservations for a Particular Guest** 

  

   - **Description**: Retrieve a list of all reservations made by a specific guest, including details like check-in date, check-out date, room type, and reservation status. 

   - **Query Example**: Find all reservations and associated details for a guest with a specific ID or name. 

  

2. **Show All Services Utilized by a Specific Guest** 

  

   - **Description**: Display a detailed list of all services (e.g., room service, laundry, spa) utilized by a particular guest during their stay. 

   - **Query Example**: Show all services used and their details (type, date, charges) for a guest with a specific ID. 

  

3. **Calculate Total Revenue Generated from a Specific Room Type** 

  

   - **Description**: Calculate the total amount of revenue generated from reservations for a particular type of room (e.g., single, double, suite) over a given period. 

   - **Query Example**: Find the total revenue earned from reservations for the "Suite" room type during the last month. 

  

4. **Show the Most Frequent Room Service Request** 

  

   - **Description**: Identify the most frequently requested room service items or types over a specified period. 

   - **Query Example**: Find the most popular room service requests based on the number of times each service was requested. 

  

5. **List All Employees Working on a Specific Date** 

  

   - **Description**: Retrieve a list of all employees who were scheduled to work on a specific date, including their roles. 

   - **Query Example**: Show all employees and their roles working on the date "YYYY-MM-DD." 

  

6. **Find All Guests Who Have Made More Than Five Reservations** 

  

   - **Description**: List guests who have made more than five reservations at the hotel. 

   - **Query Example**: Show guests who have made more than five reservations, including their names and the number of reservations. 

  

7. **Show All Payments Made by a Guest During a Specific Stay** 

  

   - **Description**: Retrieve a list of all payments made by a guest during a particular stay, including payment dates, types, and amounts. 

   - **Query Example**: Find all payments made by a guest during their stay with a specific reservation ID. 

  

8. **Find the Employee with the Highest Number of Services Provided in the Last Month** 

  

   - **Description**: Identify the employee who provided the highest number of services (e.g., room service, laundry) in the past month. 

   - **Query Example**: Show the employee who provided the most services in the last month. 

  

9. **Show the Average Length of Stay for Guests** 

  

   - **Description**: Calculate the average length of stay for all guests over a specified period. 

   - **Query Example**: Find the average number of nights stayed by guests over the last three months. 

  

10. **List All Rooms Under Maintenance** 

  

    - **Description**: Retrieve a list of all rooms that are currently under maintenance, including room numbers and the start date of maintenance. 

    - **Query Example**: Show all rooms with the status "Under Maintenance" and their maintenance start dates. 

  

11. **Show All Guests Who Have Stayed in a Specific Room Type** 

  

    - **Description**: Display a list of all guests who have stayed in a particular type of room (e.g., suite), including the dates of their stays. 

    - **Query Example**: Find all guests who stayed in "Double" rooms, including the stay dates. 

  

12. **Show All Reservations with Pending Payments** 

  

    - **Description**: Retrieve a list of all reservations that have pending payments, including the guest name, reservation details, and the outstanding amount. 

    - **Query Example**: Find all reservations with pending payments and show the guest's name and the outstanding amount. 

  

13. **Find the Room Type with the Highest Occupancy Rate** 

  

    - **Description**: Determine which room type has the highest occupancy rate over a specified period. 

    - **Query Example**: Show which room type had the highest occupancy rate in the last quarter. 

  

14. **Show the Total Revenue from a Specific Service Type** 

  

    - **Description**: Calculate the total revenue generated from a specific type of service (e.g., spa, dining) during a given time frame. 

    - **Query Example**: Find the total revenue from "Spa" services in the last month. 

  

15. **Identify Guests Who Have Provided Feedback** 

  

    - **Description**: List all guests who have submitted feedback, including the feedback details and the date it was given. 

    - **Query Example**: Find all guests who have provided feedback and show their comments and ratings. 

  

### Example Queries 

  

Here are example SQL queries for a few of the functional requirements: 

  

1. **Find All Reservations for a Particular Guest** 

   ```sql 

   SELECT * FROM Reservations WHERE GuestID = ? 

   ``` 

  

2. **Show All Services Utilized by a Specific Guest** 

   ```sql 

   SELECT * FROM Services WHERE GuestID = ? 

   ``` 

  

3. **Calculate Total Revenue Generated from a Specific Room Type** 

   ```sql 

   SELECT SUM(Amount) FROM Payments JOIN Reservations ON Payments.ReservationID = Reservations.ReservationID WHERE RoomType = ? AND ReservationDate BETWEEN ? AND ? 

   ``` 

  

4. **Show the Most Frequent Room Service Request** 

   ```sql 

   SELECT ServiceType, COUNT(*) as Frequency FROM Services GROUP BY ServiceType ORDER BY Frequency DESC LIMIT 1 

   ``` 

  

5. **Find All Guests Who Have Made More Than Five Reservations** 

   ```sql 

   SELECT GuestID, COUNT(*) as ReservationCount FROM Reservations GROUP BY GuestID HAVING COUNT(*) > 5 

   ``` 
 
