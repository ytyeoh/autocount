# Sync product quantity & price
---
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
* # sync [product](https://github.com/ytyeoh/autocount/blob/main/product/product.md) first before use this api, because it need product_id
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

* **Checking**
  * **Uniq id in order**
  -Product_id  (product id in webstore)
  -Model (model in webstore)
  * **description**

  | Name|Type|Description|
  |----------|:-------------:|:------|
  |product_id| integre|uniq product id in websotre|
  |quantity|integer|to record product stock availability  |
  |price|decimal|not inlcude special price or other price.|

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** {
```
   Product x,x,x had been update success
```


* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Warning: Incorrect API Key!" }`

* **Sample Call With Python:**

  ```Python
  import requests
  url = "https://dbpo.shinajii.com/a1/index.php?"
    
  data = {"product": [{"product_id": "1","quantity": "13","price": "5.00"},{"product_id": "21","quantity": "53","price": "10.00"}]}

  x = requests.post(url, params = {"route": "extension/api/product/sync","key":"key","username": "username"}, json = data)
  print(x.text)
  ```
