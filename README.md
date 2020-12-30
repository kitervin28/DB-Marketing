# MARKETING DB
## Database source
![data source](https://user-images.githubusercontent.com/73084975/103285369-ed8c5680-4a18-11eb-9ba7-b3a53dee15a6.png)
This Database is all about the records of the agents anywhere in the country
it defines the items the locations of each agent that has a order.

### AGENTS - this table shows the agent names and its information.
### CUSTOMER - this table shows the country and the balances of each agents.
### ORDERS -  this table shows the amount and other descriptions of the agents.

# Database Dependency Diagram

![3421321-01](https://user-images.githubusercontent.com/73084975/103286969-51644e80-4a1c-11eb-8ae6-e1396dd395f9.jpg)

# Complex Queries
#### Query 1
## SELECT COUNT(DISTINCT agent_code) AS Total_Count_of_Agents FROM agents
![1](https://user-images.githubusercontent.com/73084975/103287672-106d3980-4a1e-11eb-9aa6-633e55e3ad89.png)
this Query counts the all agents from agents table.
#### Query 2
## SELECT agents.agent_code, agents.agentname, customer.working_area FROM agents LEFT JOIN customer ON agents.agent_code = customer.agent_code ORDER BY customer.cust_name
![222](https://user-images.githubusercontent.com/73084975/103288230-65f61600-4a1f-11eb-94b0-26e1d37102d2.png)
this Query combines the table from agents table to connect customers table.
#### Query 3
## SELECT * FROM agents WHERE agentname like'%R'
![33](https://user-images.githubusercontent.com/73084975/103327861-5ca59180-4a91-11eb-88a3-42ccd498633b.png)
this Query gets the names by starting by R.
#### Query 4
## SELECT DISTINCT ord_num,ord_amount from orders a where 3 >= (select count(distinct ord_num,ord_amount) from orders b where a.ord_num <= b.ord_amount) order by a.ord_num desc
![44](https://user-images.githubusercontent.com/73084975/103327972-db9aca00-4a91-11eb-949f-8bd60d29da42.png)
#### Query 5
## SELECT COUNT(ord_num),COUNT(ord_amount) FROM orders
![55](https://user-images.githubusercontent.com/73084975/103328181-b35f9b00-4a92-11eb-9e6c-7447db782c08.png)
this Query counts the order number and the order amount from the order table.
#### Query 6
## SELECT working_area, COUNT(agentname) as working_area FROM agents GROUP BY agentname
![6](https://user-images.githubusercontent.com/73084975/103330156-3edd2a00-4a9b-11eb-838a-69c31fe022c2.png)
this Query counts the agent name and group by working area.
#### Query 7
## SELECT cust_code, cust_name, cust_city, cust_country FROM customer WHERE cust_country IS NOT NULL
![7](https://user-images.githubusercontent.com/73084975/103330284-bf9c2600-4a9b-11eb-96cd-49eee77725d7.png)
this Query select out in customer's country which is not null.
#### Query 8
## SELECT * FROM agents JOIN orders WHERE orders.ord_num = orders.ord_num
![8](https://user-images.githubusercontent.com/73084975/103330462-8fa15280-4a9c-11eb-9fe6-f6d5926090c3.png)
this Query select all from the agents table to join in orders table.
#### Query 9
## SELECT agentname, working_area, phone_no FROM agents WHERE agentname LIKE 'a%';
![9](https://user-images.githubusercontent.com/73084975/103330564-06d6e680-4a9d-11eb-9930-170277fd836d.png)
this Query selects column in agents table which more like a starting letter A in names.
#### Query 10
## SELECT CONCAT( cust_code, ', ' , cust_name, ', ' , cust_city, ', ' , working_area, ', ' , cust_country) AS CompleteInformation FROM customer LIMIT 20;
![10](https://user-images.githubusercontent.com/73084975/103330667-7f3da780-4a9d-11eb-86c6-2026c7d32b12.png)
this Query combines all the complete info in customer's table limited by 20

