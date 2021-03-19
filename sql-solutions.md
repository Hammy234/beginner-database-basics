
-----------Tabel person solutions-----------

*PROBLEM ONE

CREATE TABLE Person (
  person_id SERIAL PRIMARY KEY,
  name varchar (255),
  age int,
  height int,
  city varchar(255),
  favorite_color varchar(255)
  )

  *PROBLEM TWO

INSERT INTO Person ( name, age, height, city, favorite_color )
VALUES ( 'Jeremy', 25, 182.88, 'McGill', 'Orange');

INSERT INTO Person ( name, age, height, city, favorite_color )
VALUES ( 'Jake', 26, 182.88, 'Ely', 'Black');

INSERT INTO Person ( name, age, height, city, favorite_color )
VALUES ( 'Brandon', 26, 172.72, 'Las Vegas' , 'Green');

INSERT INTO Person ( name, age, height, city, favorite_color )
VALUES ( 'Jack', 26, 182.84, 'McGill', 'Red');

INSERT INTO Person ( name, age, height, city, favorite_color )
VALUES ( 'Clay', 24, 167.64, 'Ely', 'Silver');


*PROBLEM THREE

SELECT * FROM person ORDER BY height DESC;


*PROBLEM FOUR

SELECT * FROM Person ORDER BY height ASC;


*PROBLEM FIVE

SELECT * FROM Person ORDER BY age DESC;


*PROBLEM SIX

SELECT * FROM person WHERE age > 20;



*PROBLEM SEVEN

SELECT * FROM Person WHERE age = 18;


*PROBLEM EIGHT

SELECT * FROM Person WHERE age < 20 or age > 30;


*PROBLEM NINE

SELECT * FROM Person WHERE age != 27;


*PROBLEM TEN

SELECT * FROM Person WHERE favorite_color != 'red';


*PROBLEM ELEVEN

SELECT * FROM Person WHERE favorite_color != 'red' AND favorite_color != 'blue';


*PROBLEM TWELVE 

SELECT * FROM Person WHERE favorite_color = 'orange' and favorite_color = 'green';


*PROBLEM THIRTEEN 

SELECT * FROM Person WHERE favorite_color IN ( 'orange', 'green', 'blue' );



*PROBLEM FOURTEEN 

SELECT * FROM Person WHERE favorite_color IN ( 'yellow', 'purple' );





-----------Tabel Order solutions-----------

*PROBLEM ONE

CREATE TABLE Orders (
  order_id SERIAL PRIMARY KEY,
  person_id int,
  product_name varchar (250),
  product_price numeric,
  quantity int
  )


*PROBLEM TWO

INSERT INTO Orders ( person_id, product_name, product_price, quantity ) VALUES ( 420, 'play station', 250, 1 ); 

INSERT INTO Orders ( person_id, product_name, product_price, quantity ) VALUES ( 47, 'xbox one', 300, 1 ); 

INSERT INTO Orders ( person_id, product_name, product_price, quantity ) VALUES ( 56, 'nintendo switch', 250, 2 );

INSERT INTO Orders ( person_id, product_name, product_price, quantity ) VALUES ( 78, 'PC', 1400, 1 ); 

INSERT INTO Orders ( person_id, product_name, product_price, quantity ) VALUES ( 100, 'oculus quest', 200, 1 ); 



*PROBLEM THREE

SELECT * FROM Orders 


*PROBLEM FOUR

SELECT SUM(quantity) FROM Orders;


*PROBLEM FIVE

SELECT SUM(quantity * product_price) FROM Orders;


*PROBLEM SIX

SELECT SUM( product_price * quantity) FROM Orders WHERE 56 = 0;




-----------Tabel Invoice solutions-----------


*PROBLEM ONE

SELECT COUNT(*) FROM invoice WHERE billing_country = 'USA';



*PROBLEM TWO 

SELECT MAX(total) FROM invoice;



*PROBLEM THREE

SELECT MIN(total) FROM invoice;


*PROBLEM FOUR

SELECT * FROM invoice WHERE total > 5;


*PROBLEM FIVE

SELECT COUNT(*) FROM invoice WHERE total < 5;


*PROBLEM SIX

SELECT COUNT(*) FROM invoice WHERE total < 5;


*PROBLEM SEVEN

SELECT AVG(total) FROM invoice;
 

*PROBLEM EIGHT 

SELECT SUM(total) FROM invoice;

