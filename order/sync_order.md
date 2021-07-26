**Orders FOr Autocount**
----
  Returns json data about orders by order status set by client to sync
  **Caution** Kindly sync product before sync order to avoid unneccesary bugs
* **URL**

  index.php?route=api/order

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `name=[integer]`

* **Data Params**
  | Name|Type|Description
  |----------|:-------------:|------:|
  |username| string | uniq username use to access api, will be provide|
  |key| string |uniq key  use to access api pair to each username , will be provide|
* **Checking**
  * **Uniq id in order**
  -RefDocNo (order id in webstore)

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** {
    "invoice": [
        {
            "RefDocNo": "146",
            "Totals": "168.0000",
            "Order_type": "Webstore",
            "PaymentType": "molpay",
            "product": [
                {
                    "DebtorName": "Customer Name",
                    "Description": "Online Order",
                    "DetailDescription": "VT Cica Purifying Mask",
                    "UOM": "PCS",
                    "Location": "HQ",
                    "ItemCode": "MASK00169",
                    "QTY": "1",
                    "UnitPrice": "59.0000",
                    "SubTotal": "59.0000",
                    "Phone1": "01256456748",
                    "InvAddr1": "31 Tiara 28",
                    "InvAddr2": "Pengkalan JJhh",
                    "InvAddr3": "Ipoh 31650",
                    "InvAddr4": "Perak, Malaysia",
                    "ShpAddr1": "31 Jalan 28",
                    "ShpAddr2": "Pengkalan oljdf",
                    "ShpAddr3": "Ipoh 31650",
                    "ShpAddr4": "Perak, Malaysia"
                },
                {
                    "DebtorName": "Customer Name",
                    "Description": "Online Order",
                    "DetailDescription": "LABIOTTE COLLAGEN ESSENCE TONER - PRE ORDER (7-14DAYS)",
                    "UOM": "PCS",
                    "Location": "HQ",
                    "ItemCode": "TN00035",
                    "QTY": "1",
                    "UnitPrice": "99.0000",
                    "SubTotal": "99.0000",
                    "Phone1": "01256456748",
                    "InvAddr1": "31 Tiara 28",
                    "InvAddr2": "Pengkalan JJhh",
                    "InvAddr3": "Ipoh 31650",
                    "InvAddr4": "Perak, Malaysia",
                    "ShpAddr1": "31 Jalan 28",
                    "ShpAddr2": "Pengkalan oljdf",
                    "ShpAddr3": "Ipoh 31650",
                    "ShpAddr4": "Perak, Malaysia"
                }
            ],
            "total": [
                {
                    "order_total_id": "181502",
                    "order_id": "146",
                    "code": "shipping",
                    "title": "West Malaysia  (Weight: 1.30kg)",
                    "value": "10.0000",
                    "sort_order": "3"
                }
            ]
        }


* **Error Response:**

  * **Code:** 404 NOT FOUND <br />
    **Content:** `{ error : "Order doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Warning: Incorrect API Key!" }`

* **Sample Call With Python:**

  ```Python
    import requests

    url = 'https://koreaheaven.asia/index.php?'

    x = requests.get(url, params = {"route": "api/order","key":"key you get","name": "username"})
  ```
