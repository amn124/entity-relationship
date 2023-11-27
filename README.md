task:
You decide to join a very large known gym chain. When you arrive, you go to the reception. You find the owner arguing with a member who wants to attend a session he has not registered for. Your turn finally arrives, the owner apologizes for letting you wait so long. He explains that his employee, in charge of registrations, made a mistake in choosing the member's session.

You are surprised that such a recognized gymnasium still uses the cards to manage its large number of clients. So you're talking to the owner to  fix this problem. Interested in your knowledge, he asks you to find him a solution, in return he will offer you a free 3-months inscription.  

The owner informs you that:

 he has several gymnasiums which are distinguished by their names, addresses and telephone number. 
Members can register at one of these gymnasiums, so they must provide the following information: unique identifier, last name, first name, address, date of birth and gender. 
Each session is characterized by a type of sport and a schedule and can accommodate a maximum of 20 members. 
The sessions are led by a maximum of two coaches who have a last name, first name, age and specialty.Given the above mentioned text, try to create the according Entity relationship model.
solution:
To create an Entity-Relationship (ER) model based on the information provided, we can identify the following entities and their relationships:

Entities:

Gymnasium:

Attributes: GymnasiumID (unique identifier), Name, Address, TelephoneNumber
Member:

Attributes: MemberID (unique identifier), LastName, FirstName, Address, DateOfBirth, Gender
Relationships: Registers at Gymnasium (Many-to-One, as one gym can have many members)
Session:

Attributes: SessionID (unique identifier), SportType, Schedule
Relationships: Takes Place at Gymnasium (Many-to-One, as one gymnasium can host many sessions)
Coach:

Attributes: CoachID (unique identifier), LastName, FirstName, Age, Specialty
Relationships: Leads Session (Many-to-One, as one session can be led by many coaches)
Relationships:

Registration:

Connects Member to Gymnasium (Many-to-One, as one member registers at one gym)
Participation:

Connects Member to Session (Many-to-Many, as one member can participate in many sessions, and one session can have many members)
Assignment:

Connects Coach to Session (Many-to-Many, as one coach can lead many sessions, and one session can have many coaches)


