**Function**
----
- Orders
  1. [Get Orders](/order/sync_order.md)
- Product
  1. [Get Products](/product/product.md)

* **Featured**

  * Sync order form webstore to autocount
  * Sync products form autocount to webstore

* **Format Return**
All return is json format

* **plugin check**
  - Check duplicate order before insert autocount via order id.
  - Api return might return previous order which can cause duplicate order id.
  - Take note on product quantity deduct if apply stock control.
  - Can autocount store product_id in item? Thie will be use to sync back product in webstore.
  - advise use option name + model to generate uniq item code  or UOM in autocount.
  


* **Explanitation**
  ### product_variant

  Order been create, API will return uniq model and product_id advise use product_id to sync back item in autocount.
 

