# to be update
autocount can set price and quantity  to sync up to webstore
**Products For Autocount**
----
  Returns json data about products with join option name

* **URL**

  index.php?route=extension/api/product/sync
* **Method:**

  `POST`
  
*  **URL Params**

   **Required:**
 
   `name=[integer]`

* **Body JSON**
  ```{
    "product": [
        {
            "product_id": "1",
            "quantity": "13",
            "price": "5.00"
        },
        {
            "product_id": "21",
            "quantity": "53",
            "price": "10.00"
        }
    ]
```
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

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** {
```
   success
```


* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Warning: Incorrect API Key!" }`

* **Sample Call With Python:**

  ```Python
    import requests

    url = 'https://koreaheaven.asia/index.php?'

    x = requests.get(url, params = {"route": "extension/api/product/sync","key":"key you get","name": "username"})
  ```
