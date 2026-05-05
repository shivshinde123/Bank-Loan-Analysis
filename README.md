# Bank-Loan-Analysis
Maintain accurate records of store locations, employees, products, and customers. • Track sales transactions, including orders and order items. • Manage inventory levels across multiple store locations. • Enhance data integrity through relational database constraints. • Enable efficient data retrieval and reporting for business insigt
3. Scope
In Scope:
• Store management
• Staff information tracking
• Product catalog management
• Customer data management
• Order processing and tracking
• Inventory management
4. Functional Requirements
4.1 Stores Management
• Maintain a list of store locations.
• Capture store details: Name, phone, email, address, city, state, and zip code.
4.2 Staff Management
• Store employee details, including first name, last name, email, and phone.
• Associate staff with stores.
• Track managers by linking staff to other staff members.
• Maintain active status for employees.
4.3 Product Management
• Maintain product details, including name, brand, category, model year, and list price.
• Categorize products by category and brand.
4.4 Customer Management
• Store customer details such as name, phone, email, and address.
4.5 Order Management
• Capture customer orders with order status, order date, required date, and shipped date.
• Associate orders with customers, staff, and stores.
• Track individual order items, including product, quantity, list price, and discounts.
4.6 Inventory Management
• Maintain stock levels for each product at each store location.
• Track the quantity of products available per store.
5. Data Model
5.1 Tables
Stores Table
• The stores table includes the store’s information. Each store has a store name, contact 
information such as phone and email, and an address including street, city, state, and zip 
code.
Staffs Table
• The staffs table stores the essential information of staffs including first name, last name. 
It also contains the communication information such as email and phone.
• A staff works at a store specified by the value in the store_id column. A store can have 
one or more staffs.
• A staff reports to a store manager specified by the value in the manager_id column. If the 
value in the manager_id is null, then the staff is the top manager.
• If a staff no longer works for any stores, the value in the active column is set to zero.
Categories Table
• The categories table stores the bike’s categories such as children bicycles, comfort 
bicycles, and electric bikes.
Brands Table
• The brands table stores the brand’s information of bikes, for example, Electra, Haro, and 
Heller.
Products Table
• The products table stores the product’s information such as name, brand, category, model 
year, and list price.
• Each product belongs to a brand specified by the brand_id column. Hence, a brand may 
have zero or many products.
• Each product also belongs a category specified by the category_id column. Also, each 
category may have zero or many products.
Customers Table
• The customers table stores customer’s information including first name, last name, 
phone, email, street, city, state and zip code.
Order Table
• The orders table stores the sales order’s header information including customer, order 
status, order date, required date, shipped date.
• It also stores the information on where the sales transaction was created (store) and who 
created it (staff).
• Each sales order has a row in the sales_orders table. A sales order has one or many line 
items stored in the order_items table.
Order_Items Table
• The order_items table stores the line items of a sales order. Each line item belongs to a 
sales order specified by the order_id column.
• A sales order line item includes product, order quantity, list price, and discount.
Stocks Table
• The stocks table stores the inventory information i.e. the quantity of a particular product 
in a specific store.
