**Orders FOr Autocount**
----
  Returns json data about order by order status set by client to sync

* **URL**

  index.php?route=api/order/autocount

* **Method:**

  `GET`
  
*  **URL Params**

   **Required:**
 
   `name=[integer]`

* **Data Params**

  username = will be assign
  key = will be assign 

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** {
    "invoice": [
        {
            "RefDocNo": "146",
            "Totals": "168.0000",
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
    **Content:** `{ error : "User doesn't exist" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Warning: Incorrect API Key!" }`

* **Sample Call With Python:**

  ```Python
    import requests

    url = 'https://koreaheaven.asia/index.php?'

    x = requests.get(url, params = {"route": "api/order","key":"key you get","name": "username"})
  ```
