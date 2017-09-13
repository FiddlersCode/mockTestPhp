# mockTestPhp

This was a training exercise at work.  

### Versions
PHP 7.1.8

PHPUnit 6.3.0

#### Mock   Workshop
A   new   service   is   being   created   to   return   details   on   Products   and   alongside   this   a   Stock
service   is   being   created   to   check   the   amount   of   stock   left   for   a   product.

The   services   have   been   specced   but   development   has   yet   to   start.   The   service   returns   the
following   fields:
- ID
- Name
- Description
- Price
- VAT
- Date   Created   (a   Unix   Timestamp)

When   written   the   service   will   have   a   getter   for   each   method   for   example   there   will   be   a `getPrice()`   method   that   returns   the   price   field.

The   stock   service   will   get   the   amount   of   stock   for   product   when   supplied   a   product   id: 

`getStock($productId)`   returns   int

We   need   to   build   a   Product   class   that   takes   the   services   as   a   constructor   arguments   and does   the   following:

#### Requirement   1
Write   a   method   that   gets   the   total   price   for   a   product,   this   is   the   product   price   plus   the   VAT.

#### Requirement   2
Write   a   method   that   gets   the   product   description   from   the   price   service.   If   there   is   no   product
description   then   return   the   product   name. 

#### Requirement   3
Write   a   method   that   takes   a   product   id   as   an   argument   and   gets   the   stock   remaining   for   that product   and   returns   the   following   message:

- When   >   5   in   stock   return   “In   Stock”
- When   <   5   but   >   1   in   stock   return   “Warning   very   low   stock!”
- When   1   left   in   stock   return   “Hurry   only   one   left   in   stock!”

#### Requirement   4
Create   a   new   class   called   “DateHelper”   with   the   method   formatTimestamp.   This   method must   receive   a   Unix   timestamp   as   an   argument   and   return   a   date   in   the   following   format   “DD -   MM   -   YYYY”

#### Requirement   5
Write   a   method   in   the   product   class   that   gets   the   date   the   product   was   created,   formats   it   in our   time format   and   returns   the   product   description   with   “Date   added:   productCreationDate” appended   to   it.

#### Requirement   6
Write   a   method   which   returns
- “offer   price”   if   today's   day   is   a   Monday,   Friday   or   Sunday   then
the   method   will   return   the   products   total   price   -   25%   else   it   returns   the   total   price. 

#### Requirement   7
Add   to   the   `offerPrice`   method   the   following:   if   the   date   today   is   Christmas   day   return   the   total price   -   85%.
