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
#### Query 2
## SELECT agents.agent_code, agents.agentname, customer.working_area FROM agents 
## LEFT JOIN customer ON agents.agent_code = customer.agent_code ORDER BY customer.cust_name
![222](https://user-images.githubusercontent.com/73084975/103288230-65f61600-4a1f-11eb-94b0-26e1d37102d2.png)
#### Query 3
#### Query 4
#### Query 5
#### Query 6
#### Query 7
#### Query 8
#### Query 9
#### Query 10
