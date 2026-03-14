# Application Analysis

The lab provides a vulnerable web login page which interacts with a MongoDB database.

Unlike traditional relational databases, MongoDB stores data in documents instead of tables.

Example document:

{
 "username": "admin",
 "password": "secret123",
 "email": "[email protected]"
}

The backend query used by the application looks similar to:

db.users.find({
 username: input_username,
 password: input_password
})

If user input is not sanitized properly, attackers can inject malicious operators into the query.
