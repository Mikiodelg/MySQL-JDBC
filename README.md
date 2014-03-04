Ejercicio 1 MySQL) 


Desde la linea de comandos de MySQL (DB1.sql contenida en la carpeta raiz del proyecto), con la base de datos creada y seleccionada:


	1) SELECT * FROM RODUCTS;

	2) SELECT Name, PRICE FROM PRODUCTS;

	3) SELECT NAME FROM PRODUCTS WHERE PRICE <=200;

	4) SELECT NAME, PRICE FROM PRODUCTS WHERE PRICE <= 120 AND PRICE >=60;

	5) SELECT NAME, PRICE*100 FROM PRODUCTS;

	6) SELECT AVG(PRICE) FROM PRODUCTS;

	7) SELECT AVG(PRICE) FROM PRODUCTS WHERE MANUFACTURER=2;

	8) SELECT COUNT(*) FROM PRODUCTS WHERE PRICE >=180;

	9) SELECT NAME,PRICE FROM PRODUCTS WHERE PRICE>=180 ORDER BY PRICE DESC,NAME;

	10) SELECT * FROM PRODUCTS INNER JOIN MANUFACTURERS ON PRODUCTS.MANUFACTURER=MANUFACTURERS.CODE;

	11) SELECT PRODUCTS.NAME, PRICE, MANUFACTURERS.NAME FROM PRODUCTS INNER JOIN MANUFACTURERS ON PRODUCTS.MANUFACTURER = MANUFACTURERS.CODE;

	12) SELECT AVG(PRICE), MANUFACTURER FROM PRODUCTS GROUP BY MANUFACTURER;

	13) SELECT AVG(PRICE),MANUFACTURERS.NAME FROM PRODUCTS INNER JOIN MANUFACTURERS ON PRODUCTS.MANUFACTURER = MANUFACTURERS.CODE GROUP BY MANUFACTURERS.NAME;

	14) SELECT AVG(PRICE),MANUFACTURERS.NAME FROM PRODUCTS INNER JOIN MANUFACTURERS ON PRODUCTS.MANUFACTURER = MANUFACTURERS.CODE GROUP BY MANUFACTURERS.NAME HAVING AVG(PRICE) >=150;

	15) SELECT NAME,PRICE FROM PRODUCTS WHERE PRICE = (SELECT MIN(PRICE) FROM PRODUCTS);

	16) SELECT MANUFACTURERS.NAME, PRODUCTS.NAME, PRICE FROM PRODUCTS INNER JOIN MANUFACTURERS ON PRODUCTS.MANUFACTURER = MANUFACTURERS.CODE AND PRICE = (SELECT MAX(PRICE) FROM PRODUCTS WHERE PRODUCTS.MANUFACTURER = MANUFACTURERS.CODE);

	17) INSERT INTO PRODUCTS (NAME,PRICE,MANUFACTURER) VALUES ('Loudspeaker',70,2);

	18) UPDATE PRODUCTS SET NAME='Laser Printer' WHERE CODE = 8;

	19) UPDATE PRODUCTS SET PRICE = PRICE*0.9;

	20) UPDATE PRODUCTS SET PRICE = PRICE*0.9 WHERE PRICE >=120;


-------------

Ejercicio 2 JDBC) 

Desde la linea de comandos de Mysql:

Mysql - >
	
create database feedback;
	
use feedback;
	
CREATE USER sqluser IDENTIFIED BY 'sqluserpw'; 
	

grant usage on *.* to sqluser@localhost identified by 'sqluserpw'; 
	
grant all privileges on feedback.* to sqluser@localhost;

	CREATE TABLE COMMENTS (id INT NOT NULL AUTO_INCREMENT, 

    MYUSER VARCHAR(30) NOT NULL,
    
    EMAIL VARCHAR(30), 
    
    WEBPAGE VARCHAR(100) NOT NULL, 
    
    DATUM DATE NOT NULL, 
  
    SUMMARY VARCHAR(40) NOT NULL,
  
    COMMENTS VARCHAR(400) NOT NULL,
  
    PRIMARY KEY (ID));

INSERT INTO COMMENTS values (default, 'lars', 'myemail@gmail.com','http://www.vogella.com', '2009-09-14 10:33:11', 'Summary','My first comment');

SELECT * FROM COMMENTS;  


Eclipse ->

Run as -> Java Aplication.