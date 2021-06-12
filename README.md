**Function**
----
- Orders
  1. [Get Orders](/order/sync_order.md)
- Product

* **Featured**

  * Sync order form webstore to autocount
  * Sync products form autocount to webstore

* **Format Return**
All return is json format

* **plugin check**
  - Check duplicate order before insert autocount via order id.
  - Api return might return previous order which can cause duplicate order id.
  - Take note on product quantity deduct if apply stock control.
  - Item code in autocout will be use as product model during sync.
  - Products with variants via OUM sync to autocount will not have uniq model. [MORE](#product_variant)


* **Explanitation**
  ### product_variant

  Order been create, API will return uniq model as item code in below format `0001-12-32` 
  | model | option 1|option 2|
  |----------|:-------------:|------:|
  | 0001  | -12 | -32|
  | product uniq model / item code| - as seperator 12 is uniq option id in w ebstore | - as seperator 12 is uniq option id in w ebstore|

