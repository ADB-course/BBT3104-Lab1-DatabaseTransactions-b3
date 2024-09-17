[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r-tQZu0l)
# BBT3104-Lab1of6-DatabaseTransactions


| **Key**                                                               | Value                                                                                                                                                                              |
|---------------|---------------------------------------------------------|
| **Group Name**                                                               | B3 |
| **Semester Duration**                                                 | 19<sup>th</sup> August - 25<sup>th</sup> November 2024                                                                                                                       |

## Flowchart

![flowchart](Flowchart.png)
## Pseudocode
PSUEDOCODE. 
Step1: 	Begin Transaction; 
Step2: Use classicmodels;
Step3: START transaction;
Step4: set orderNumber = (SELECT MAX (orderNumber)+1 FROM orders); 
Step5: INSERT
 into oder in Ordernumber,orderdate,requiredDate,ShipmentDate ,insert VALUES(@OrderNumber,DATE(now()),DATE(addDATE),ADD(NOW(),INTERVAL 3 DAY),DATE(DATE(DATE_ADD(NOW)INTERVAL 2DAY)),'in process,145);
Step6: SAVEPOINT before_product_1; 
Step7: INSERT 
-INTO orderdetails(ordernumber,productcode,quantityOrdered,priceEach,OrderLineNumber);
VALUES(@OrderNumber,'s18_1749',2724,'136',1);
Step8: set quantityinstock = (SELECT quantityInStock  FROM products WHERE productCode = ‘S18_1749’);
Step9: UPDATE products SET quantirtyInStock = (quantityInstock -540  WHERE productCode  = ‘S18_2248’);
Step10: SET @quantityInStock TO the current stock of product ‘s18_2248’; 
Step11: Error with Product 2?;
Step12: SAVEPOINT before_product 3; 
Step13: INSERT a new order detail for  product ‘s18_1749’ with: 
                -quantityOrdered:68 
              -priceEach: 95.34 
             -orderLineNumber: 3 
Step15: SET @quantityInStock TO the current stock of product ‘s12_1099’; 
Step16: UPDATE product 'S12_1099' to reduce stock by 68 units; 
Step17: INSERT a payment record with: 
  customerNumber: 145  
 checkNumber: 'JM555210'  
 paymentDate: current date  
 amount: 12000 
  
Step17: COMMIT Transaction; 
Step18: SELECT * FROM classicmodels.orderdetails WHERE orderNumber = 10426;
Step 19: End/Stop transaction

## Support for the Sales Departments' Report
For the sales department to be able to track and generate a report on unpaid orders they need to create a database that will be able to accommodate tracking payment towards each order made by a customer and they can do this by first creating a payments table which is going to record all the payment transactions which can include a payment Id ,OrderId ,paymentAmount ‘amount paid in each installment’ ,paymentDate ‘contains date of payment’ and paymentMethod ‘Information about how payment was made. In the orders table they can add the paidAmount column which is going to store the amount paid.They can also use the SQL queries to calculate the outstanding balances for each order, hence to enable them identify and track down orders which are not fully paid. A column for paymentStatus can also be added which will store information such as is the amount paid in full ,partially or unpaid.

