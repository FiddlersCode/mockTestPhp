# mockTestPhp

This was a training exercise at work.  

### Versions
PHP 7.1.8

PHPUnit 6.3.0

### Mock Workshop

#### Background
This exercise takes a `Product` class (which you will build) and mocks calls to a non-existent `ProductService` class, which returns   details   on   members of the `Products` class, and a non-existent `StockService` class, which checks the amount of stock left for a product.

The   `ProductService` class   returns   the following   fields:
- ID
- Name
- Description
- Price
- VAT (20% of Price)
- Date   Created   (a   Unix   Timestamp)

The `ProductService` class  will   have   a   getter   for   each   method (for   example   there   will   be   a `getPrice()`   method   that   returns   the   price   field).

The   stock   service   will   get   the   amount   of   stock as an integer  for   product   when   supplied   a   product   id: 
`getStock($productId)`

#### Task
Build   a   `Product`   class   that   takes   the   `ProductService`   as   a   constructor   argument   and does   the   following:

#### Requirement   1
Write   a   method   that   gets   the   total   price   for   a   product (price +  VAT).

#### Requirement   2
Write   a   method   that   gets   the   product   description   from   `ProductService`.   If   there   is   no   product
description   then   return   the   product   name. 

#### Requirement   3
Add the `StockService` to the `Product` class's constructor arguments.  Write   a   `getStock()` method   that   takes   a   product   id   as   an   argument   and   gets   the   stock   remaining   for   that product   and   returns   the   following   message:

- When   >   5   in   stock   return   “In   Stock”
- When   <   5   but   >   1   in   stock   return   “Warning   very   low   stock!”
- When   1   left   in   stock   return   “Hurry   only   one   left   in   stock!”

#### Requirement   4
Create   a   new   class   called   `DateHelper`   with   the   method   `formatTimestamp()`.   This   method must   receive   a   Unix   timestamp   as   an   argument   and   return   a   date   in   the   following   format   “DD -   MM   -   YYYY”

#### Requirement   5
Write   a   method   in   the   product   class   that   gets   the   date   the   product   was   created,   formats   it   in our   time format   and   returns   the   product   description   with   “Date   added:   productCreationDate” appended   to   it.

#### Requirement   6
Write   an `offerPrice` method:
- if   today's   day   is   a   Monday,   Friday   or   Sunday   return  "offer price:   total   price   -   25%"
- else  return   the   total   price. 

#### Requirement   7
Add   to   the   `offerPrice`   method   the   following:   if   the   date   today   is   Christmas   day   return   the   total price   -   85%.
