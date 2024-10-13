# UFC-Database
## Team Name: 
  We're Using Chat
## Team Members:
* Benjamin Brown -
* Matthew Burt 
* Jared Eidson - 
* Harrison Mcclure -
* John Overstreet - 
## Scenario Description (Why does this data matter?):
This database models the fighters, events, customers, and employees of the UFC so that the upper level management, like Dana White, can make decisions to drive profit and popularity. It will allow management to schedule marquee fights, improve advertising, and decide fighter bonus pay. By capturing detailed information about fighters’ performance, event scheduling, customer engagement and employee responsibilities, the database that our group has created will support decision making in several areas. In conclusion, this database will be an invaluable tool for UFC management, enabling data-driven decisions that not only optimize operations but also enhance the fan experience, boost fighter performance, and ultimately drive the organization's success.
## Data Model
![Final_Project_Data_Model](https://github.com/user-attachments/assets/58cd714d-ee79-43a2-b7b0-e2c4348b4851)
* The two main entities in our model are the Events and Fighters entities with the rest of of the model revolving around them in some way or another. Fighters contains information about the atheletes who are contracted by the UFC while Events has data on where the fights take place and how they are viewed. 
* Events can have many employees and employees can work many events.  Because this was many to many we created a weak entity that joined events and employees which shows us which employees are working which events.

