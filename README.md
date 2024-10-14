# UFC-Database
## Team Name: 
  We're Using Chat
## Team Members:
* Benjamin Brown - https://github.com/bdb12838
* Matthew Burt 
* Jared Eidson - https://github.com/jke99240
* Harrison Mcclure - https://github.com/Harrison-mcclure
* John Overstreet - 
## Scenario Description (Why does this data matter?):
This database models the fighters, events, customers, and employees of the UFC so that the upper level management, like Dana White, can make decisions to drive profit and popularity. It will allow management to schedule marquee fights, improve advertising, and decide fighter bonus pay. By capturing detailed information about fighters’ performance, event scheduling, customer engagement and employee responsibilities, the database that our group has created will support decision making in several areas. In conclusion, this database will be an invaluable tool for UFC management, enabling data-driven decisions that not only optimize operations but also enhance the fan experience, boost fighter performance, and ultimately drive the organization's success.
## Data Model
![Final_Project_Data_Model](https://github.com/user-attachments/assets/707d361c-da7d-4d36-8a17-c5bbf0654716)

The two main entities in our model are the Events and Fighters entities with the rest of of the model revolving around them in some way or another. Fighters contains information about the atheletes who are contracted by the UFC while Events has data on where the fights take place and how they are viewed. Fighters can fight in many Events and Events have many Fighters. Since this is a many to many relationship we created a weak entity Event Statistics which contains information about a fighter at an event. This entity also holds attributes like payment and fight statistics that are vary depending on the fighter and event.

Another entity that relates to both Fighters and Events is Country which has a one to many relationship with both entities. A country can have many fighters but a fighter can only be from one Country. Along the same lines, a country can host many events but a given event can only happen in one Country. Country stores a country's code (USA), which is the primary key, and a country's name (Canada).

Two entities that have relationships with Fighters is WeightClasses and Belts. WeightClasses stores data on the name of the weightclass and the maximum weight at which fighters can compete at said weightclass. It has a one to many relationship with Fighters as a weightclass has many fighters competing in it but a fighter can only belong to one weightclass at a given time. Belts contains information on the current champions of each weightclass and when they won their belts. Belts has a one to many relationship with Fighters because a Fighter can have multiple belts (if they won the belt of one weightclass and then changed weightclasses and won another one) but a belt can only be held by one fighter. Belts and WeightClasses has a one to one relationship as each weightclass has one belt and each belt belongs to one weightclass.

Another entity in our data model is Employees which stores information on the people who work for the UFC. This data includes their full name, job title, the date they were hired, and the ID of their boss. Employees has a many to many relationship with Events as an event can be worked by many employees and an employee can work many events. Since this is a many to many relationship we created a weak entity called EmployeesWorkingEvent. This new entity shows us which employees are working which events. Employees also has a one to many recursive relationship which is where a boss (who is stored in Employees) has many workers reporting to them but a worker only reports to one boss.

Customers is the last entity in our model and it contains the names, emails, and ages of people who purchase tickets to a UFC event. Customers has a many to many relationship with Events as an event is viewed by many customers and a customer can view many events. Because this is a many to many relationship we created a weak entity that shows which customers are viewing which event, called CustomersViewingEvent. This entity also stores data on the ticket price and the ticket type (PayPerView or inPerson).
## Data Dictionary
![Table 1](https://github.com/user-attachments/assets/126dfa33-6ca3-4b1c-83f1-9b83c53a694f)

![Table 2](https://github.com/user-attachments/assets/2a429eaa-e27d-4fe1-bfb4-d70eed9ac10d)

![Table 3](https://github.com/user-attachments/assets/849f34e9-734e-4ff4-bb3d-3d29f4bb5a98)

![Table 4](https://github.com/user-attachments/assets/a12f879b-b975-438f-a5c2-17e266b0b1b1)

![Table 5](https://github.com/user-attachments/assets/5fd19713-3b88-4e1c-b070-657635c0b142)

![Table 6](https://github.com/user-attachments/assets/4f993c6c-aa1c-4db7-b4db-a3d61b7918b1)

![Table 7](https://github.com/user-attachments/assets/f9d7376d-82d1-4976-86b3-f2412483460a)

![Table 8](https://github.com/user-attachments/assets/1a544895-9794-4c3b-8fd4-208226921f83)

![Table 9](https://github.com/user-attachments/assets/a767978a-46f1-4fb6-b1b9-aaeeb23bb7ab)

![Table 10](https://github.com/user-attachments/assets/3a11517b-a9c9-4bc7-9a1f-4861a33d108f)

## Ten Queries
1. Query 1 is a subquery designed to return the name, ticket type, and ticket price, from customers who paid more than the average price for a ticket. The marketing department can use this complex query to figure out which customers spend more on average. With this, we can send them loyalty program promotions or other enticements to keep them as loyal customers.

![Screenshot 2024-10-13 at 3 12 47 PM](https://github.com/user-attachments/assets/584d72c0-8dae-4096-adfc-840fc33fd17d)

2. Query 2 is a query designed to find the win ratio of all fighters and return that statistic along with the fighters name and weight. This query is also only searching within the lightweight fighter class. Managers scheduling the next lightweight fight can use this query to make competitive future fights. 

![Screenshot 2024-10-13 at 3 18 50 PM](https://github.com/user-attachments/assets/2e77bedb-e299-41eb-84ab-1284281a016a)

3. Query 3 is a query that counts all the fighters that have a championship belt and groups them by what country they are from. This query helps managers assess which countries produce the most successful fighters based on which country has the most champions.

![Screenshot 2024-10-13 at 3 25 02 PM](https://github.com/user-attachments/assets/2c6d6e1e-5439-48fd-a37f-8ca0786b2b91)

4. Query 4 is a query that searches for a specific fighter by their last name and outputs that fighters full name, wins, loses, and draws. In this example we are searching for one of the most iconic and successful fighters in the UFC, Conor Mcgregor. Managers in the UFC can use this query to search for important statistics of individual fighters by changing the regexp.

![Screenshot 2024-10-13 at 3 27 51 PM](https://github.com/user-attachments/assets/24341e5e-92c1-4bf2-8cd0-c4f2141c3a21)

5. Query 5 is a subquery that returns the city, venue, and viewership from the event in the database which had the hightest viewership. This query can be useful to managers by showing the venue that resulted in the most viewers, so they can plan on scheduling another event there. This can also be used to see where the UFC may want to put more effort in building hyp earound the smaller venues not shown in the list. 

![Screenshot 2024-10-13 at 3 33 30 PM](https://github.com/user-attachments/assets/7116aa86-c85a-4979-9d69-ceac0ddbecc4)

6. Query 6 is a query designed to show which contracted fighters have not currently fought at an event. Managers can then use this query to make sure their fighters are active in the UFC. This can also help the UFC to see which fighters are maybe looking for a fight or mainly who to schedule that the public may have not seen fight yet. This will help bring more publicity to newer fighters and large events. 

![Screenshot 2024-10-13 at 3 39 02 PM](https://github.com/user-attachments/assets/e71aff5f-6748-4ad6-aecc-65f988bfd6c9)

7. Query 7 is a query that returns a fighter's full name, height, and weight class, given that they are from the US and are taller than 70 inches. The social media team for the UFC could make an engaging graphic with this information that targets US viewers. 

![Q7](https://github.com/user-attachments/assets/3a2eab72-5255-4828-8aae-c206ad5465a1)

8. Query 8 is a query that sums all the wins of fighters from their country of origin and groups these wins by country. The result is then ordered by the number of wins a country has descending from highest to lowest. Fight planners and advertisers at UFC can use this query and target the countries with the most wins to host more events with fighters from said country.

![image](https://github.com/user-attachments/assets/4a982c36-52a9-4285-9649-3f93237bf136)

9. Query 9 is a query that joins the Employees, EmployeesWorkingEvent, and Events entities to find all the employees that worked in Las Vegas and who work in security. Managers can use this query to find specialized employees to work the next event located in Las Vegas. 

![Screenshot 2024-10-13 at 7 48 19 PM](https://github.com/user-attachments/assets/701de781-4f94-435e-aa5f-4749c6bb2228)

10. Query 10 is a simple query that list all the venues along with their attendances then ordering the results by the highest attendance to the lowest attendance. Upper level management at the UFC will find this list useful as higher attendance equates to more ticket sales which translates to higher revenue.

![Screenshot 2024-10-13 at 8 06 59 PM](https://github.com/user-attachments/assets/92d668da-7120-4f42-ae40-84f83241a70b)
## Database Information 
![Screenshot 2024-10-13 at 8 19 02 PM](https://github.com/user-attachments/assets/37375783-fa85-4c46-8ded-5f6559ff340e)

Name of the database: cs_meb61924

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
