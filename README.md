# Spring-Boot-Microservices-With-JPA
Spring Boot Microservices with JPA Communicate two microservices


# SQL data

use mydb;

create table product(
id int AUTO_INCREMENT PRIMARY KEY,
name varchar(20),
description varchar(100),
price decimal(8,3) 
);
<br>
create table coupon(
id int AUTO_INCREMENT PRIMARY KEY,
code varchar(20) UNIQUE,
discount decimal(8,3),
exp_date varchar(100) 
);


# Server port
 for couponservice = 9091<br>
#for productservice = 9090

# url for fetch discount from couponservice
http://localhost:9090/productapi/products

try JSON:
      {
   "name":"MAC",
    "description":"Cool",
    "price":  "2000",
    "couponCode":"SUPERSALE"
}

for couponservice itself
http://localhost:9091/couponapi/coupons

try JSON for inserting data into database
  {
  "code":SUPERSALE",
  "discount:10
  
}
