# Warehouse-Management-System
Software designed using java, swing, SQL for management of warehouse

## Description

Ware house management system is designed for managing the items in the warehouse which can be ordered by the dealers or by the customers considering a wholesale scenario. Separate login for owner and each of the dealer/distributor. Owner can update the stocks of certain products as well as can check for quantity available with him. SQL back end to maintain the login details of owner as well as dealers and to maintain the details of the items present in the warehouse. Designed such that on purchase of products by the dealer, warehouse stocks are updated and dealer id, item id, quantity and amount is added automatically into a transactional database to show the order details as per the dealer.

## SQL Tables used 

Database name = `warehouse`

1. `Products` : 

| Field       | Type        | Null | Key | Default 
|:-------------:|:-------------:|:------:|:-----:|:---------:|
| productid   | int(11)     | NO   | PRI | NULL    |     
| price       | double      | NO   |     | NULL    |     
| quantity    | int(11)     | NO   |     | NULL    |     
| productname | varchar(20) | YES  |     | NULL    |     

2. `Distributor` :

| Field           | Type        | Null | Key | Default | 
|-----------------|-------------|------|-----|---------|
| distributorid   | int(11)     | NO   | PRI | NULL    |       
| distributorpass | varchar(20) | NO   |     | NULL    |       
| distributorname | varchar(20) | YES  |     | NULL    |    

3. `Buyers` :

| Field         | Type    | Null | Key | Default | Extra          |
|---------------|---------|------|-----|---------|----------------|
| distributorid | int(11) | NO   | MUL | NULL    |                |
| price         | double  | NO   |     | NULL    |                |
| invoice       | int(11) | NO   | PRI | NULL    | auto_increment |

## ScreenShots 

`Main Login`


![Main Page](https://github.com/hammertime1308/Warehouse-Management-System/blob/master/Images/mainPage.png)


`Owner Operations`


![Owner Operations](https://github.com/hammertime1308/Warehouse-Management-System/blob/master/Images/ownerOperations.png)


`Buyers List Owners profile`


![Buyers List](https://github.com/hammertime1308/Warehouse-Management-System/blob/master/Images/buyersListOwner.png)


`Distributor Operations`


![Distributor operations](https://github.com/hammertime1308/Warehouse-Management-System/blob/master/Images/DistributorOperations.png)


`Buy using Distributor profile`


![Buy example](https://github.com/hammertime1308/Warehouse-Management-System/blob/master/Images/buyDistributor.png)
