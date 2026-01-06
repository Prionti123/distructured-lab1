# distructured-lab1

Q1. Create a database named collegeDB and switch to it.
Ans:use collegeDB.


Q2. Create a collection named students in the collegeDB database.
Ams:db.createCollection("students")


Q3. Insert one document into the students collection with the following fields:
• name
• rollNo
• department
• age
Ans:db.students.insertOne({
  name: "Rahul Sharma",
  rollNo: 101,
  department: "CSE",
  age: 20
})

Q4. Insert four more documents into the students collection with different
values.
Ans:```js
db.students.insertMany([
  {
    name: "Anita Das",
    rollNo: 102,
    department: "ECE",
    age: 21
  },
  {
    name: "Sourav Paul",
    rollNo: 103,
    department: "CSE",
    age: 22
  },
  {
    name: "Neha Singh",
    rollNo: 104,
    department: "ME",
    age: 20
  },
  {
    name: "Amit Kumar",
    rollNo: 105,
    department: "CSE",
    age: 23
  }
])
Q5. Display all documents present in the students collection.
Ans:db.students.find()

Q6. Display only those students who belong to the CSE department.
Ans:db.students.find({ department: "CSE" })

Q7. Update the age of one student (any one) to a new value.
Ans:db.students.updateOne(
  { rollNo: 101 },
  { $set: { age: 21 } }
)

Q8. Delete one document from the students collection using any condition.
