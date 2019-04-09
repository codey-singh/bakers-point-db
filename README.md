# bakers-point-db

# Project Details

The project is a database for business management for a bakery. The system will be mainly used for order management. SQL server is used as the database engine for the project. Details regarding the products, customers and employees will be stored in the database. We have used different SQL queries for getting our requirements. Here, we have stored the data values and requirements as stored procedures. The database developed is suitable for a store where several customization options are available for their products. Also new products and different customization options can be added as per requirements.

The database stores details of all the customers including name, contact and address. Orders made by each customer is stored in the database each linked to the customer. Invoice of the order made can be retrieved from the database using the stored procedure for the same. The database has stored procedure to retrieve the total sales during a period entered.

The database includes stored procedures having insert queries required to enter data to all the tables intended. This ensures that the sql file can be run in any system and successfully prove its purpose. Our goal for this project is to create a complete backend system for a bakery.

# Team Members

AJ
BS

# Database tables

| Table Name | Keys &amp; Columns | Details |
| --- | --- | --- |
| Order | PrimaryKey > id   
ForeignKey > customer\_id  order\_date  delivery\_date   delivery\_address   
order\_type | This table keep the details regarding the orders made by the customers. |
| Customer | PrimaryKey > idfnamelnameimageemailphoneaddress | This table keep information regarding the customers. |
| Employee | PrimaryKey > idfnamelnameimageemailphoneaddressForeignKey > job\_id | The employee details are stored in this table. |
| JobRole | PrimaryKey > idtitleResponsibilities | This table keeps information regarding the various job roles. |
| Product | PrimaryKey > idtitlesizeimageshapepriceavailabilityeta | This table keeps details about the various products available in the bakery. |
| OrderStatus | PrimaryKey > idorder\_idstatusupdated\_atForeignKey > updated\_by | This table keeps the status of the orders. |
| OrderLine | PrimaryKey > idForeignKey > product\_idquantitygift\_wrapForeignKey > order\_iddetails | This table keeps the details regarding the price and quantity of the orders. |
| OrderLineCustomization | PrimaryKey > idForeignKey > criteria\_idForeignKey > orderline\_id | This table saves customization criteria. |
| OrderCustomizationCriteria | PrimaryKey > idForeignKey > product\_idcustomization\_nameprice | This table saves customization details. |
| Feedback | PrimaryKey > idForeignKey > customer\_idForeignKey > order\_line\_idfeedback\_textrating | This table stores feedbacks given by the customers. |

# Requirement List

1. Status of each order.
2. Add new products. > Add new products and customizations and its cost.
3. Money Made. > money made between a date range.
4. Average rating for each product.
5. Most sold product.
6. Order invoice.

# Stored Procedure

List of all the stored procedure with details

Example:

| Procedure Name | Input Output Parameters | Details | Team Member worked on it |
| --- | --- | --- | --- |
| insertCustomerData |   |   |  AJ |
| insertEmployeeData |   |   |  AJ |
| insertFeedback |   |   |  AJ |
| insertJobRole |   |   |  AJ |
| insertMasterData |   |   |  AJ |
| insertOLCriteria |   |   |  AJ |
| insertOLCustomizationCriteria |   |   |  BS |
| insertOrderData |   |   |  BS |
| insertOrderLineData |   |   |  BS |
| insertOrderStatusData |   |   |  BS |
| insertProductData |   |   |  BS |
| sp\_createInvoice |  orderId |   |  BS |
| sp\_getMoneyMadeInDateRange |  Start date/ end date |   |  BS |
| sp\_getAverageRatingForAProduct |  productId |   |  BS |
| sp\_MostSoldProduct |   |   |  AJ |
| sp\_getCurrentStatusForAnOrder |  orderId |   |  AJ |
