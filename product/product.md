**Products For Autocount**
----
  Returns json data about products with join option name

* **URL**

  index.php?route=extension/api/product
* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `name=[integer]`

* **Data Params**
  | Name|Type|Description|
  |----------|:-------------:|------:|
  |username| string | uniq username use to access api, will be provide|
  |key| string |uniq key  use to access api pair to each username , will be provide|
* **Checking**
  * **Uniq id in order**
  -Product_id  (product id in webstore)
  -Model (model in webstore)
  * **description**
   
  | Name|Type|Description|
  |----------|:-------------:|------:|
  |product_id| integre|uniq product id in websotre|
  |model|string|uniq str in webstore to record product(can use a item code|
  |name| string|name for product, default use same as admin language in webstore for multiple language|
  |price|decimal|not inlcude special price or other price.|
  |option|string|*-dash been use as seperator for join option value in product. Example:Black-Large (L) = *COLOR*-*SIZE*|
  |sku|integer| uniq id to record each variant quantity and price.|

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** {
```
    {
      "products": [
        {
            "product_id": "97",
            "model": "cloths00001",
            "name": " KEEXUENNL SOS Smart Thermal Slimming Top ",
            "price": "89.0000",
            "quantity": "1",
            "option": "Black-Large (L)",
            "sku": "140162"
        }
      ]
    }
```


* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Warning: Incorrect API Key!" }`

* **Sample Call With Python:**

  ```Python
    import requests

    url = 'https://dbpo.shinajii.com/a1/index.php?'

    x = requests.get(url, params = {"route": "extension/api/product","key":"key you get","name": "username"})
  ```
