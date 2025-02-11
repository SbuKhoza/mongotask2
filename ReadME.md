Codetribe MongoDB Setup

This repository contains MongoDB shell (Mongosh) commands to set up the Codetribe database, with three collections: `Facilitators`, `Trainees`, and `Projects`.

Prerequisites

- MongoDB must be installed on your system.
- MongoDB shell (`mongosh`) should be available.

 Starting the MongoDB Shell (Mongosh)

To start the MongoDB shell, follow these steps:

1. Open your terminal.
2. Type the following command to connect to the local MongoDB instance:

   ```bash
   mongosh
This will launch the MongoDB shell.

To verify if you're connected, type:

bash
Copy code
show dbs
This will show all the existing databases.

Steps to Create the Database and Collections
1. Create the Codetribe Database
To create and use a new database named Codetribe, run:

bash
Copy code
use Codetribe
2. Create the Collections
Facilitators Collection
To create the Facilitators collection and insert a document with the required fields, run:

bash
Copy code
db.Facilitators.insertOne({
  "Name": "Mahlatse Serathi",
  "Location": "Soweto",
  "Course": "Web Development"
})
Trainees Collection
To create the Trainees collection and insert a document with the required fields, run:

bash
Copy code
db.Trainees.insertOne({
  "Name": "Sibusiso Khoza",
  "Location": "Soweto",
  "Facilitator": "Mahlatse Serathi"
})
Projects Collection
To create the Projects collection and insert a document with the required fields, run:

bash
Copy code
db.Projects.insertOne({
  "Name": "Portfolio Website",
  "Course": "Web Development",
  "Lesson": "HTML and CSS Basics"
})
Viewing Data in the Collections
To view all the documents in any of the collections, use the find() method.

For the Facilitators collection:

bash
Copy code
db.Facilitators.find().pretty()
For the Trainees collection:

bash
Copy code
db.Trainees.find().pretty()
For the Projects collection:

bash
Copy code
db.Projects.find().pretty()
The .pretty() method formats the output in a readable format.

Additional MongoDB Commands
To list all collections in the Codetribe database:

bash
Copy code
show collections
To drop a collection (if needed):

bash
Copy code
db.<collection_name>.drop()
To exit the MongoDB shell, type:

bash
Copy code
exit
Conclusion
This README provides a step-by-step guide to create the Codetribe database, set up collections, insert documents, and interact with the MongoDB database using Mongosh.

python
Copy code

The facilitator's name has been updated to "Mahlatse Serathi," and the location to "Soweto." Similarly, the trainee's name has been updated to "Sibusiso Khoza," with the location also set to "Soweto."
