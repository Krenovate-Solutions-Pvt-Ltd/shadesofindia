#   **Bulk Import**

##  **Introduction**

The Import feature in the Admin panel, allows the administrator to create/upload bulk products in one go.

To do a bulk import, an excel file ".csv" is created. All the required data is populated in this CSV file in a pre-defined format.  The file has columns dedicated to each field corresponding to the fields in the backend.

Maintaining the format of all columns is of utmost importance in order import all data correctly.

A sample CSV file is below:

![sample](Images\Bulk-Import\sample.jpg)



##  **Column Fields**

In this section of the manual, we will discuss all the columns fields one by one:

### **ID**

Once a new product is created in the system, a Product Id is generated automatically. This Product Id is unique to each product.

![prod id](Images\Bulk-Import\prodid.jpg)


### **Type**

In the type field, enter the Product type. There are 3 options to which can be entered:

-   **Simple** - A simple product is a type of product which is a unique (there is only one version), stand-alone, physical product that a customer can add to cart/purchase.
-   **Variable** - A variable product is a type of product which can have multiple options to choose from. For example, a t-shirt available in different colors and/or sizes.
-   **Variation** - These are multiple options available for a Variable product. 

>   **Note** - **Variation rows  should always come below the Simple and Variable rows.** 


Entry in CSV | As updated in Backend |
---------|----------|---------
 ![type](Images\Bulk-Import\type.jpg) | ![type1](Images\Bulk-Import\type1.jpg)| 


### **SKU** 

SKU refers to a Stock-keeping unit, a unique identifier for each distinct product and service that can be purchased.


Simple | Variable | Variation
---------|----------|---------
 Enter the Product SKU here | This is known as a Parent SKU | Here enter the Variation SKU which gets uploaded in the Variation data
 ![simplesku1](Images\Bulk-Import\simplesku1.jpg)| ![variablesku1](Images\Bulk-Import\variablesku1.jpg) | ![variationsku1](Images\Bulk-Import\variationsku1.jpg)
 ![simplesku](Images\Bulk-Import\simplesku.jpg)| ![variablesku](Images\Bulk-Import\variablesku.jpg)| ![variationsku](Images\Bulk-Import\variationsku.jpg)

### **Name**

In the name field,  product name to be displayed on the website product pages is to be entered.


Simple | Variable | Variation
---------|----------|---------
 The name should be as to be shown on the website | The name should be as to be shown on the website | The name along with the variation name should be entered
 ![simplename](Images\Bulk-Import\simplename.jpg) |![variablename](Images\Bulk-Import\variablename.jpg) | ![variationname](Images\Bulk-Import\variationname.jpg)
 ![simplename1](Images\Bulk-Import\simplename1.jpg) | ![variablename1](Images\Bulk-Import\variablename1.jpg) | 


### **Published**

Publishing a product means that it will be visible on the website. Till the time it is not published, the product status remains private.

In the CSV file, only 2 values can be entered:

-   **0** = Not published (private)
-   **1** = Published



Entry in CSV | Appears on Backend | 
---------|----------|---------
 ![published1](Images\Bulk-Import\published1.jpg) | ![published](Images\Bulk-Import\published.jpg) | 
 ![private1](Images\Bulk-Import\private1.jpg) | ![private](Images\Bulk-Import\private.jpg) | 
 

### **Featured**

Featured field is used for marking products on homepage or any particular page in a featured category.

In the CSV file, only 2 values can be entered:

-   **0** = Not Featured
-   **1** = Featured

![featured](Images\Bulk-Import\featured.jpg)

**By default, the entry = "0" for all products as at SOI this functionality is not required.**


### **Visibility in Catalog**

This setting determines which shop pages products will be listed on.

By default, the entry on CSV = "visible"

![catalogvisibility](Images\Bulk-Import\catalogvisibility.jpg)


### **Short Description**

The short description is not required so this field is left blank for all products.

### **Description**

In this field text describing the product is added. This is applicable to all **Simple** and **Variable** products.

At variation level, this description is not required.


Simple | Variable | Variation
---------|----------|---------
 Required | Required | Not Required 

Few points to remember while adding text:

-   The description text appears in the "Text" tab on the backend.
-   Use "br in <>" once to go to next line; twice to insert a line space.
-   To mark any text bold, add "strong in <>" at the beginning and end of the text.

On the backend, text shows as below:

![desc](Images\Bulk-Import\desc.jpg)


### **Date Sale price starts/ends**

The Date Sale price starts and Date Sale price ends fields help in setting the schedule for any sale if applicable.


Simple | Variable | Variation
---------|----------|---------
 The schedule is set in the General tab | The sale schedule is set at Variation level | The schedule is set in the variation data section
 ![simple schedule](Images\Bulk-Import\simplesaleschedule.jpg) |  | ![variation schedule](Images\Bulk-Import\variationsaleschedule.jpg)
<br>

>   **Note** - **The date format to be followed always = "yyyy-mm-dd"**

>   **NEVER USE WRONG DATE FORMAT**

### **Tax Status**

The tax status field defines whether or not the entire product is taxable.

By default, all products at SOI are taxable. Always enter "taxable" in this field.


Entry in CSV | Updated at Backend | 
---------|----------|---------
 ![taxstatus](Images\Bulk-Import\taxstatus.jpg) | ![taxstatus1](Images\Bulk-Import\taxstatus1.jpg) |

### **Tax Class**

Tax classes are used to apply different tax rates specific to certain types of products. Enter the applicable code in this field.

Tax class is a **mandatory** field and relevant code should be entered.


Entry in CSV | Updated at Backend | 
---------|----------|---------
 ![taxclass](Images\Bulk-Import\taxclass.jpg) | ![taxclass1](Images\Bulk-Import\taxclass1.jpg) | 


**Points to remember:**

-   Pre-defined HSN Codes are entered in the tax class field.
-   HSN Code to be used should be already added in the system.

    ![taxrates](Images\Bulk-Import\taxrate.jpg)

-   If HSN code not added, follow the **Tax Rate Setup**

### **In stock?**

This field allows to let the system know, if the product is available or out of stock.

By default, for all products of SOI, the In stock field has value as "1"

In the CSV file, only 2 values can be entered:

-   **0** = No (out of stock)
-   **1** = Yes (In stock)

>   **Note** - **If marking "1", make sure the Stock Value is greater than 1**

### **Stock**

Stock field refers to the stock quantity available for each product.

"In case of a variable product this value will be used to control stock for all variations, unless you define stock at variation level."


Simple | Variable | Variation
---------|----------|---------
 Stock quantity is set in the Inventory section | Do not enter value for variable here | Stock quantity is defined at the variation level 
![simplestock1](Images\Bulk-Import\simplestock1.jpg) |  |![variationstock1](Images\Bulk-Import\variationstock1.jpg)
![simplestock](Images\Bulk-Import\simplestock.jpg) ||![variationstock](Images\Bulk-Import\variationstock.jpg)


### **Low Stock Amount**

This refers to the threshold, which, when the product stock reaches this amount you will be notified by email.


Simple | Variable | Variation
---------|----------|---------
 This value is updated in the Inventory section | This value is updated in the Inventory section | Value is updated at variable level only
 ![simplelowstock](Images\Bulk-Import\simplelowstock.jpg) | ![variablelowstock](Images\Bulk-Import\variablelowstock.jpg) | 



### **Backorders Allowed?**

This field controls whether or not backorders (No stock but still taking orders) are allowed. It means, if enabled, stock quantity can go below 0.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**For all products of SOI, by default the value is "0"**


CSV File | Backend | 
---------|----------|
 ![simplebackorder](Images\Bulk-Import\simplebackorder.jpg) | ![simplebackorder1](Images\Bulk-Import\simplebackorder1.jpg) | 
 ![variablebackorder](Images\Bulk-Import\variablebackorder.jpg) | ![variablebackorder1](Images\Bulk-Import\variablebackorder1.jpg) |  
 ![variationbackorder](Images\Bulk-Import\variationbackorder.jpg) | ![variationbackorder1](Images\Bulk-Import\variationbackorder1.jpg) |  

### **Sold Individually**

If this field is enabled, it would mean that the customer would be allowed to add only one product in the cart.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**Since this functionality is not required for all SOI products, by default the value remains "0"**

### **Weight**

Weight is part of the shipping details of all products. Entering a value to this field is mandatory.

Weight should be entered in "kgs"


Simple| Variable | Variation
---------|----------|---------
 The value is updated in the shipping section | The value is set at variation level | The value is set in the respective variation data
 ![simpleweight1](Images\Bulk-Import\simpleweight1.jpg) |  | ![variaitonweight1](Images\Bulk-Import\variationweight1.jpg)
 ![simpleweight](Images\Bulk-Import\simpleweight.jpg) | ![variableweight](Images\Bulk-Import\variableweight.jpg) | ![variaitonweight](Images\Bulk-Import\variationweight.jpg)


### **Length**

Length is part of the dimensions for  shipping details of all products. Entering a value to this field is mandatory.

Length should be entered in "inches"

### **Width**

Width is part of the dimensions for  shipping details of all products. Entering a value to this field is mandatory.

Width should be entered in "inches"

### **Height**

Height is part of the dimensions for  shipping details of all products. Entering a value to this field is mandatory.

Height should be entered in "inches"

The dimensions are updated as below:


Simple| Variable | Variation
---------|----------|---------
 The value is updated in the shipping section | The value is set at variation level | The value is set in the respective variation data
 ![simpledimension](Images\Bulk-Import\simpledimensions.jpg) | | ![variationdimension](Images\Bulk-Import\variationdimensions.jpg)
 ![simplemeasurement](Images\Bulk-Import\simplemeasurement.jpg) | ![variablemeasurement](Images\Bulk-Import\variablemeasurement.jpg) | ![variaitonmeasurement](Images\Bulk-Import\variationmeasurement.jpg)




### **Allow Customer Reviews?** - **NA**

If enabled, this field allows the customers to leave reviews on the product pages.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**Since this functionality is not required for all SOI products, by default the value remains "0"**


### **Purchase Note** - **NA**

This function is not required for all SOI products, so it will be left blank.

### **Sale Price**

Sale price is the value which is updated if and when a product goes on sale.


Simple | Variable | Variation
---------|----------|---------
 Value is updated in the General section | Value is updated at variaiton level | Value updated in respective variations data
 ![simplesale](Images\Bulk-Import\simplesaleprice.jpg) | ![variablesale](Images\Bulk-Import\variablesaleprice.jpg) | ![variationsale](Images\Bulk-Import\variationsaleprice.jpg)


### **Regular Price**

Regular price is the amount the customer pays for any product. 

This is a mandatory field and a value has to be entered for each product.

Simple | Variable | Variation
---------|----------|---------
 Value is updated in the General section | Value is updated at variaiton level | Value updated in respective variations data
 ![simpleregular](Images\Bulk-Import\simpleregular.jpg) | ![variableregular](Images\Bulk-Import\variableregular.jpg) | ![variationregular](Images\Bulk-Import\variationregular.jpg)
 ![simpleregularprice](Images\Bulk-Import\simpleregularprice.jpg) | ![variableregularprice](Images\Bulk-Import\variableregularprice.jpg) | ![variationregularprice](Images\Bulk-Import\variationregularprice.jpg)   









