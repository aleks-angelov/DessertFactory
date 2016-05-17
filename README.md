# Dessert Factory

### Group class project for INF 280 - Database Systems (Fall 2015)

##### Description:
The goal of our project is to create a database that facilitates the operation of a dessert factory. 

##### Data entities and attributes:
The current model of our database has thirteen entities, four of which are subclass entities:

1.	Name: Department  
  Attributes: number (key), name, location, manager
  
2. Name: Item  
Attributes: name (key), expiration_date

 * Name: Desserts  
Attributes: dessert_id (key), daily_production

 * Name: Ingredients  
Attributes: ingredient_id (key), storage_conditions

3. Name: Employee  
Attributes: SSN (key), first name, last name, address, phone, birth_year

 * Name: White-collared  
Attributes: salary, bonus, payment_year

 * Name: Blue-collared  
Attributes: wage, hours, payment_day

4. Name: Dependent  
Attributes: name (key), relationship

5. Name: Facility  
Attributes: facility_id (key), type, location

6. Name: Equipment  
Attributes: equipment_id (key), type, year_bought, electricity_consumption

7. Name: Supplier  
Attributes: supplier_id (key), name, location, phone

8. Name: Customer  
Attributes: customer_id (key), name, address, phone, volume, discount

9. Name: Expense  
Attributes: expense_id (key), name, regularity, amount

##### Data relations:
The current model of our database has eleven relations:

1. Orders from – Department 1:N Supplier  
Attributes: order_date, quantity, price, delivery_date

2. Housed by – Department M:N Facility

3. Incurs – Department M:N Expenses

4. Sold to – Dessert M:N Customer  
Attributes: order_date, quantity, price, vehicle_id, delivery_date

5. Supplied by – Ingredient M:N Supplier  
Attributes: order_date, price, quantity, delivery_date

6. Works in – Employee N:1 Department

7. Manages – Employee 1:1 Department

8. Works on – Employee N:1 Dessert

9. Depends on – Dependent N:1 Employee

10. Stored in – Facility M:N Item  
Attributes: arrival_date, quantity

11. Located in – Equipment N:1 Facility

##### Constraints and assumptions:
For the purposes of the project, we have decided to include entities and relations only for the fundamental components of a typical dessert factory.

##### Selected DBMS:
We have selected MySQL 5 as our Database Management system.

