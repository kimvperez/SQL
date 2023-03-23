Grocery Store Database

--Create a grocery store database

CREATE TABLE groceries (id INTEGER PRIMARY KEY, item TEXT, section TEXT, price INTEGER, popularity INTEGER);

INSERT INTO groceries VALUES (1, "Bananas", "fresh", 4, 6);
INSERT INTO groceries VALUES (2, "Apples", "fresh", 3, 5);
INSERT INTO groceries VALUES (3, "Plums", "fresh", 2, 5); 
INSERT INTO groceries VALUES (4, "Peaches", "fresh", 2, 8);
INSERT INTO groceries VALUES (5, "Raspberries", "frozen", 5, 2);
INSERT INTO groceries VALUES (6, "Tomatoes", "fresh", 1, 10);
INSERT INTO groceries VALUES (7, "Broccoli", "frozen", 5, 10);
INSERT INTO groceries VALUES (8, "Cauliflower", "frozen", 3, 4);

--display the database ordered by price. 
SELECT * FROM groceries
ORDER BY price desc; 

--what is the avg price of items in the frozen section? 
SELECT AVG(price) "avg frozen item price"
FROM groceries
where section='frozen'; 

--what are the most 5 popular items? 
SELECT item, price, popularity
FROM groceries
order by popularity desc
limit 5; 
