## Shop Application

- This purpose of this app is to define *models* for **products** and **product catagories** and use them in proper *views* to display them on the webpage.

#### Models

##### Catagory

- This model has only two fields, **name** and **slug**.
  - The **name** field is used to store the name of the category and is used to define and **index** to make data **retrival faster**.
  - The slug field is a unique field (unique implies an automatic creation of index) and is used to make Canonical URLs from the catagories.
- In the **Admin** page both fields are displayed and **slug** is *prepoulated* with the **name** (See *admin.py* file).

##### Products

- This model have multiple fields to store relevant data for a product.
  - It have a **ForeignKey** field **category** which create a *one-to-many relationship* with the **Category** model.*(One product belongs to one categroy and one category contains multiple products.)*
  - A **name** and **slug** fields.
  - **image**, **description** and **price** fields for additional product info.
  - A boolean field to see if product is **avaliable** and
  - Two datetime fields to store **created** date **updated** date of products. *(For control purposes.)*