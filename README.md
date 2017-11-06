# TicketService
Reserve tickets.

# Maven Commands:
Assuming current directory is at this repository (where pom.xml is present).
1. mvn clean package assembly:assembly OR mvn clean package assembly:assembly -DskipTests (To skip the test cases) 
2. java -jar target\TicketService-0.0.1-jar-with-dependencies.jar com.walmart.ticket.Start // Program will start. Then follow the command prompt.


# Implementation:
Following data model has been implemented
* Venue: acts like a asset (ie theatre) where it has matrix of seats. each elemenet of matrix represents Seat object. 
* Seat: contains number(in x,y co-ordinates), status (using enum), reservedBy(Customer type)
* Loc: for indexing seat number. i.e. 0th row, 5th seat. 
* Customer: to store customer related information i.e. email.
* SeatHold: works as a separate timed based object where it has user requested information (#seats, email), and where event happened (timestamp). This object depends on the request for hold.
