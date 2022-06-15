# Friends
Creating my own friends table, then add/delete from it

#1. I'm creating a table named 'Friends' with 3 columns
CREATE TABLE friends
(id INTEGER, name TEXT, birthday DATE);

#2. Adding my first friend to the table
INSERT INTO friends (id, name, birthday)
VALUES (1, 'Cyndi McCynderson', '1974-01-28');

#3. Now making sure that Cyndi has been added to the database
SELECT *
FROM friends;

#4. Going to add 2 more friends to the table
INSERT INTO friends (id, name, birthday)
VALUES (2, 'Bobby McBobberson', '1978-12-18');

INSERT INTO friends (id, name, birthday)
VALUES (3, 'Mayra McMayrason', '1984-05-29');

#5. Cyndi McCynderson just realized that she can control the weather and decided to change her name to "Storm"
UPDATE friends
SET name = 'Storm'
WHERE id = 1

#6. Adding a new column named 'email'
ALTER TABLE friends
ADD COLUMN email TEXT;

#7. Updating the email address for everyone in the table
UPDATE friends
SET email = 'storm@McEmail.com'
WHERE id = 1;

UPDATE friends
SET email = 'Bobby@McEmail.com'
WHERE id = 2;

UPDATE friends
SET email = 'Mayra@McEmail.com'
WHERE id = 3;

#8. Wait! Storm is fictional, I'll remove her from the table
DELETE FROM friends
WHERE id = 1;

#9. Now looking at the results one last time
SELECT *
FROM friends;
