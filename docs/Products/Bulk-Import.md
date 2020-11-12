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

In the type field, enter the Product type. There are 3 options which can be entered:

-   **Simple** - A simple product is a type of product which is a unique (there is only one version), stand-alone, physical product that a customer can add to cart/purchase.
-   **Variable** - A variable product is a type of product which can have multiple options to choose from. For example, a t-shirt available in different colors and/or sizes.
-   **Variation** - These are multiple options available for a Variable product. 

>   **Note** - **Variation rows  should always come below the Simple and Variable rows.** 


Entry in CSV | As updated in Backend
---------|---------
 ![type](Images\Bulk-Import\type.jpg) |![type1](Images\Bulk-Import\type1.jpg)


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



Entry in CSV |  As updated in Backend
---------|---------
 ![published1](Images\Bulk-Import\published1.jpg) | ![published](Images\Bulk-Import\published.jpg)
 ![private1](Images\Bulk-Import\private1.jpg) |  ![private](Images\Bulk-Import\private.jpg)
 

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


Entry in CSV | As updated in Backend
---------|---------
 ![taxstatus](Images\Bulk-Import\taxstatus.jpg) | ![taxstatus1](Images\Bulk-Import\taxstatus1.jpg)

### **Tax Class**

Tax classes are used to apply different tax rates specific to certain types of products. Enter the applicable code in this field.

Tax class is a **mandatory** field and relevant code should be entered.


Entry in CSV |  As updated in Backend
---------|---------
 ![taxclass](Images\Bulk-Import\taxclass.jpg) |   ![taxclass1](Images\Bulk-Import\taxclass1.jpg)


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


Entry in CSV  | As updated in Backend  
---------|----------|
 ![simplebackorder](Images\Bulk-Import\simplebackorder.jpg) | ![simplebackorder1](Images\Bulk-Import\simplebackorder1.jpg) 
 ![variablebackorder](Images\Bulk-Import\variablebackorder.jpg) | ![variablebackorder1](Images\Bulk-Import\variablebackorder1.jpg)  
 ![variationbackorder](Images\Bulk-Import\variationbackorder.jpg) | ![variationbackorder1](Images\Bulk-Import\variationbackorder1.jpg)   

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


### **Categories**

Product categories help in organizing the products. Categories are the primary way to group products with similar features. You can also add sub-categories if desired. We refer to them as levels.

* L1 - Parent Category
* L2 - Sub-category
* L3 - Sub-sub-category

When making an entry in the CSV file a sequence needs to be followed in order to update the backend in the required manner.

The sequence is defined by using a ">" sign between each level and seperated by commas. Let's look at the example below to understand this:

**L1>L2>L3,L1>L2,L1**

OR

**L1,L1>L2,L1>L2>L3**

Here:

L1 = Parent Category
L1>L2 = Sub-category under the Parent category
L1>L2>L3 = Sub-sub-category under the sub-category

The category field is updated only in the **Simple** and **Variable** products. It is not required in the Variations.


Entry in CSV | As updated in Backend
---------|---------
 ![category](Images\Bulk-Import\category.jpg) |  ![category1](Images\Bulk-Import\category1.jpg)
 ![category2](Images\Bulk-Import\category2.jpg) | ![category3](Images\Bulk-Import\category3.jpg)


### **Tags**

Product tags are another way to relate products to each other. These are keywords which can be used in searching products on the website.

In this field enter keywords seperated by commas.


Entry in CSV| As updated in Backend
---------|---------
 ![tags](Images\Bulk-Import\tags.jpg) | ![tags1](Images\Bulk-Import\tags1.jpg)


### **Shipping Class**

Shipping classes are used by certain shipping methods to group similar products. It allows you to control important details about a physical product (weight, dimensions) for shipping.

Only 2 options are available, which should be entered as per product category:

-   Normal
-   Delhivery (Primarily used for Home & Living products)

Shipping class is a mandatory field and one of the above options should be entered.


Entry in CSV | As updated in Backend
---------|---------
 Entry is required for all products | Updations happen as per entry
 ![shippingclass](Images\Bulk-Import\shippingclass.jpg) | ![shippingclass1](Images\Bulk-Import\shippingclass1.jpg)


### **Images**

The Images field refers to the **Product Image** and **Product Gallery Images** on the backend.

Some tips to fill this field:

-   The complete image URL has to be entered. 
-   Multiple URL's can be entered seperated by commas. 
-   the 1st URL entered will represent the Product/featured image.
-   All other URL's represent the Product Gallery images.


Entry in CSV |  As updated in Backend
---------|---------
 ![images](Images\Bulk-Import\images.jpg)| ![images1](Images\Bulk-Import\images1.jpg)
 Entry required only for Simple and Variable products | Updated under respective products


### **Download Limit - NA**

This field is not required and is left blank.

### **Download Expiry Days - NA**

This field is not required and is left blank.


### **Parent**

The Parent field refers to the Parent SKU as entered in all variable products.

The parent field is required only for **variation** rows. Each variation of a particular variable product is linked to the parent product through this field.

It is mandatory to enter the correct corresponding Parent SKu against the variations, in order to update the backend and frontend correctly.

The below example explains this:

![parent](Images\Bulk-Import\parent.jpg)


### **Grouped Products - NA**

This field is not required and is left blank.

### **Upsells**

Up-sells are displayed on the product details page. These are products that are displayed to encourage users to upgrade, based on the product they are currently viewing. 

This field will include the Product Id of products to be shown and should be seperated by a comma.


### **Cross-Sells - NA**

This field is not required and is left blank.

### **External URL**

### **Button Text**

### **Position**

The number entered in the Position field, defines the position of the variations of a variable product. It decides the sequence in which the variations will show on the front-end/website product page.


Simple | Variable | Variation
---------|----------|---------
 Not required | Not required | Required - Mandatory

<br>

Entry in CSV | As Updated in Backend | As appears on Frontend
---------|----------|---------
 ![position](Images\Bulk-Import\position.jpg) | ![position1](Images\Bulk-Import\position1.jpg) | ![position2](Images\Bulk-Import\position2.jpg)


### **Color Taxonomy**

Colors help in organizing, searching the products on the basis of color category/family.

In the color taxonomy field, all the product related colors should be entered seperated by a comma.

This field should be updated only for **Simple** and **Variable** rows.


Entry in CSV | As updated in Backend
---------|----------
 ![colors](Images\Bulk-Import\color.jpg) | ![colors1](Images\Bulk-Import\colors1.jpg)| 


### **Material Taxonomy**

Materials help in organizing the products on the basis of material used (fabric, accessories).

In the material taxonomy field, all the product related materials should be entered seperated by a comma.

This field should be updated only for **Simple** and **Variable** rows.

Entry in CSV | As updated in Backend
---------|----------
 ![material](Images\Bulk-Import\material.jpg) | ![materials1](Images\Bulk-Import\materials1.jpg) | 


### **Attribute Color**

The attribute color field is applicable only to **Variable** and **variation** rows for products which have color variations.

This field defines the color tone for each variation. These color tones are visible on the product page.

Entry to be done = Color name|Corresponding color code


Product Type | Entry In CSV | As updated in Backend | As appears on Frontend 
-------|---------|----------|---------
Variable |![variableattributecolor](Images\Bulk-Import\variableattributecolor.jpg) | ![variableattributecolor1](Images\Bulk-Import\variableattributecolor1.jpg) | ![attributecolor2](Images\Bulk-Import\attributecolor2.jpg) 
Variation |![attributecolor](Images\Bulk-Import\attributecolor.jpg) | ![variationattributecolor](Images\Bulk-Import\variationattributecolor.jpg) | ![attributecolor2](Images\Bulk-Import\attributecolor2.jpg) 


### **Attribute 1 name**

In this field, name of the required attribute is added. This column field is dedicated to the **size** attribute.

For all products, the entry remains same.


Simple | Variable | Variation
---------|----------|---------
 Required - Size | Required - Size | Required - Size


### **Attribute 1 Value(s)**

In this field, all values associated with Attribute 1 should be entered.

This is a required field for all rows - Simple, Variable, Variation


Simple | Variable | Variation
---------|----------|---------
 This will have a single entry (could be a measurement or size) | Here all possible variation values to be entered | Enter only variation specific value
 ![simpleattribute1value](Images\Bulk-Import\simpleattribute1value.jpg) | ![variableattribute1value](Images\Bulk-Import\variableattribute1value.jpg) | ![variationattribute1value](Images\Bulk-Import\variationattribute1value.jpg)
 

### **Attribute 1 visible**

Attribute to be visible means that it appears on the product page.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated only for **Simple** and **Variable** rows. The value should always be "1" 



Entry in CSV | As updated in Backend
---------|---------
 ![attribute1visible](Images\Bulk-Import\attribute1visible.jpg) | ![attribute1visible1](Images\Bulk-Import\attribute1visible1.jpg)


### **Attribute 1 global**

Attribute to be global means that the attributes are available to choose from.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated for all rows - Simple, Variable, Variation. The value should always be "1" 

### **Meta: _wpv_contains_gutenberg_views - NA**

This field is not required/not applicable and is left blank.

### **Meta: Shoulder**

This field consists of the Shoulder measurement for all products in the **Uppers** (blouses, dresses, kurtas) category.

-   This field is only required for **Variation** rows.
-   The shoulder measurement helps in differentiating between variations sizes.
-   Measurement unit to be used is "inch".


Entry in CSV | As updated in Backend 
---------|----------
 ![shoulder](Images\Bulk-Import\shoulder.jpg) | ![shoulder1](Images\Bulk-Import\shoulder1.jpg) 


### **Meta: Bust**

This field consists of the Bust/chest measurement for all products in the **Uppers** (blouses, dresses, kurtas) category.

-   This field is only required for **Variation** rows.
-   The bust measurement helps in differentiating between variations sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![bust](Images\Bulk-Import\bust.jpg) | ![bust1](Images\Bulk-Import\bust1.jpg)


### **Meta: Waist**

This field consists of the waist measurement for all products in the **Lowers** (skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The waist measurement helps in differentiating between variations sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![waist](Images\Bulk-Import\waist.jpg) | ![waist1](Images\Bulk-Import\waist1.jpg)


### **Meta: Hip**

This field consists of the hip measurement for all products in the **Lowers** (skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The hip measurement helps in differentiating between variations sizes.
-   Measurement unit to be used is "inch".


### **Meta: _wc_additional_variation_images**

For every variation more images related only to that variation can be added as additional images.

-   This field is updated only for the **Variation** rows.
-   Multiple additional images can be uploaded for each variation.
-   Each image is assigned with a 4-digit code. These codes seperated by comma are entered in this field.

Entry in CSV | As updated in Backend 
---------|----------
 ![additionalimages](Images\Bulk-Import\additionalimages.jpg) | ![additionalimages1](Images\Bulk-Import\additionalimages1.jpg)


### **Meta: _wp_old_date - NA**

This field is not required and is left blank.

### **Meta: _layouts_template - NA**

This field is not required and is left blank.

### **Meta: _wp_page_template - NA**

This field is not required and is left blank.

### **Meta: views_woo_price - NA**

This field is not required and is left blank.

### **Meta: views_woo_in_stock - NA**

This field is not required and is left blank.

### **Meta: wpcf-finer-details**

The finer details field may include details related to the fabric used, care instructions, etc.

Points of consideration while entering text in this field:

-   This field can be upated for **Simple** and **Variable** rows.
-   The text entered will be updated in the **Text** tab.
-   To give line break : add "br in <>" at end of line twice. This will insert a blank line and take you to the next line.
-   To make text bold : add "strong in <>" at the start and end of text. 


### **Meta: wpcf-delivery-exchange**

The delivery/ exchange field contains information regarding shipping, return of product etc. 

Points of consideration while entering text in this field:

-   This field can be upated for **Simple** and **Variable** rows.
-   The text entered will be updated in the **Text** tab.
-   To give line break : add "br in <>" at end of line twice. This will insert a blank line and take you to the next line.
-   To make text bold : add "strong in <>" at the start and end of text.


### **Meta: wpcf-size-fit** 

Any instructions regarding the size and fit can be added here. 

Points of consideration while entering text in this field:

-   This field can be upated for **Simple** and **Variable** rows.
-   The text entered will be updated in the **Text** tab.
-   To give line break : add "br in <>" at end of line twice. This will insert a blank line and take you to the next line.
-   To make text bold : add "strong in <>" at the start and end of text.

Below is an example of how text is updated in the abpve fields: 

Entry in CSV | As update in Backend | As appears on Frontend
---------|----------|---------
 ![delexc1](Images\Bulk-Import\deliveryexchange1.jpg) | ![delexc](Images\Bulk-Import\delexc.jpg) | ![delexc2](Images\Bulk-Import\deliveryexchange2.jpg)



### **Meta: _views_template - NA**

This field is not required and is left blank.

### **Attribute 2 name**

In this field, name of the required attribute is added. This column field is dedicated to the **color** attribute.

For all products, the entry remains same.


Simple | Variable | Variation
---------|----------|---------
 Required - Color | Required - Color | Required - Color


### **Attribute 2 Value(s)**

In this field, all values associated with Attribute 2 should be entered.

This is a required field for all rows - Simple, Variable, Variation


Simple | Variable | Variation
---------|----------|---------
 This will have a single entry (only 1 color) | Here all possible variation values to be entered | Enter only variation specific value
 ![simpleattribute2value](Images\Bulk-Import\simpleattribute2value.jpg) | ![variableattribute2value](Images\Bulk-Import\variableattribute2value.jpg) | ![variationattribute2value](Images\Bulk-Import\variationattribute2value.jpg)
 

### **Attribute 2 visible**

Attribute to be visible means that it appears on the product page.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated only for **Simple** and **Variable** rows. The value should always be "1" 



Entry in CSV | As updated in Backend
---------|---------
 ![attribute2visible](Images\Bulk-Import\attribute2visible.jpg) | ![attribute2visible1](Images\Bulk-Import\attribute2visible1.jpg)


### **Attribute 2 global**

Attribute to be global means that the attributes are available to choose from.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated for all rows - Simple, Variable, Variation. The value should always be "1" 

### **Meta: Length**

This field consists of the length measurement for all products in the **Lowers** & **Uppers** (Shirts, blouses, kurtas, skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The Length measurement helps in differentiating between variations sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![length](Images\Bulk-Import\length.jpg) | ![length1](Images\Bulk-Import\length1.jpg)
