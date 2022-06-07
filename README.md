# mixer

Use "Postman" application for POST, PUT, and DELETE operations.

Install PostgreSQL. Create database and connect it to project. 

Create 2 tables with names "people" and "docs" with this options:

CREATE TABLE DOCS(
id bigserial not null primary key,
number numeric,
type varchar(30),
name_of_issuing_authority varchar(30),
date_of_issuing date,
date_of_expiry date);

CREATE TABLE Person(
id bigserial not null primary key,
name varchar(30),
age numeric,
email varchar(30),
date_of_birth date,
created_at date);

Create foreign key:
in postgresql shell write this:
ALTER TABLE people add docs_id bigint references docs (id);

Run Application.

Note: method with getting person with getting by date doesnt work... cant resolve why...