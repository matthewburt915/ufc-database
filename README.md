# UFC-Database
## Team Name: 
  We're Using Chat
## Team Members:
* Benjamin Brown - https://github.com/bdb12838
* Matthew Burt 
* Jared Eidson - 
* Harrison Mcclure -
* John Overstreet - 
## Scenario Description (Why does this data matter?):
This database models the fighters, events, customers, and employees of the UFC so that the upper level management, like Dana White, can make decisions to drive profit and popularity. It will allow management to schedule marquee fights, improve advertising, and decide fighter bonus pay. By capturing detailed information about fighters’ performance, event scheduling, customer engagement and employee responsibilities, the database that our group has created will support decision making in several areas. In conclusion, this database will be an invaluable tool for UFC management, enabling data-driven decisions that not only optimize operations but also enhance the fan experience, boost fighter performance, and ultimately drive the organization's success.
## Data Model
![Final_Project_Data_Model](https://github.com/user-attachments/assets/58cd714d-ee79-43a2-b7b0-e2c4348b4851)
The two main entities in our model are the Events and Fighters entities with the rest of of the model revolving around them in some way or another. Fighters contains information about the atheletes who are contracted by the UFC while Events has data on where the fights take place and how they are viewed. 

Events can have many employees and employees can work many events.  Because this was many to many we created a weak entity that joined events and employees which shows us which employees are working which events.

Weight classes can have many Fighters but Fighters can only have one Weight Class. Fighters can have many Belts but Belts can only belong to one fighter. Weight Classes belong to one Belt but a Belt can only belong to one Weight Class.

Many customers can view  many events and events can have many customers.  Because this is a many to many relationship we created a weak entity that shows which customers are viewing which  event.

Fighters can fight in many Events and Events has many Fighters because this is a many to many relationship it creates the weak entity Event Statistics which contains information about about each fighter for that event.

Country can have many Fighters but Fighters can only belong to one Country.

A Country can have many Events but Events can only happen in one Country.
## Data Dictionary
## Ten Queries
1. Query 1 is a subquery designed to return the name, ticket type, and ticket price, from customers who paid more than the average price for a ticket. The marketing department can use this complex query to figure out which customers spend more on average. With this, we can send them loyalty program promotions or other enticements to keep them as loyal customers.

![Screenshot 2024-10-13 at 3 12 47 PM](https://github.com/user-attachments/assets/584d72c0-8dae-4096-adfc-840fc33fd17d)

2. Query 2 is a query designed to find the win ratio of all fighters and return that statistic along with the fighters name and weight. This query is also only searching within the lightweight fighter class. Managers scheduling the next lightweight fight can use this query to make competitive future fights. 

![Screenshot 2024-10-13 at 3 18 50 PM](https://github.com/user-attachments/assets/2e77bedb-e299-41eb-84ab-1284281a016a)

3. Query 3 is a query that counts all the fighters that have a championship belt and groups them by what country they are from. This query helps managers assess which countries produce the most successful fighters based on which country has the most champions.

![Screenshot 2024-10-13 at 3 25 02 PM](https://github.com/user-attachments/assets/2c6d6e1e-5439-48fd-a37f-8ca0786b2b91)

4. Query 4 is a query that searches for a specific fighter by their last name and outputs that fighters full name, wins, loses, and draws. In this example we are searching for one of the most iconic and successful fighters in the UFC, Conor Mcgregor. Managers in the UFC can use this query to search for important statistics of individual fighters by changing the regexp.

![Screenshot 2024-10-13 at 3 27 51 PM](https://github.com/user-attachments/assets/24341e5e-92c1-4bf2-8cd0-c4f2141c3a21)

5. Query 5 is a subquery that returns the city, venue, and viewership from the event in the database which had the hightest viewership. This query can be useful to managers by showing the venue that resulted in the most viewers, so they can plan on scheduling another event there.

![Screenshot 2024-10-13 at 3 33 30 PM](https://github.com/user-attachments/assets/7116aa86-c85a-4979-9d69-ceac0ddbecc4)

6. query 6 is a query designed to show which contracted fighters have not currently fought at an event. Managers can then use this query to make sure their fighters are active in the UFC.

![Screenshot 2024-10-13 at 3 39 02 PM](https://github.com/user-attachments/assets/e71aff5f-6748-4ad6-aecc-65f988bfd6c9)








## Database Information 
