#   **Import/Export CSV Format**


##  **Introduction**

The Import/Export feature in the Admin panel, allows the administrator to create/upload/edit bulk products in one go.

To do a bulk import/export, an excel file ".CSV" is created. All the required data is populated in this CSV file in a pre-defined format.  The file has columns dedicated to each field corresponding to the fields in the backend.

**Maintaining the format of all columns is of utmost importance in order import all data correctly.**

A sample CSV file is below:

![sample](Images\Bulk-Import\sample.jpg)

:bookmark: <a href="https://docs.google.com/spreadsheets/d/1ntkeiv7Bbo0iwmXxi-bWLJkwDmcTQwXbizK9bbg1F6Q/edit?usp=sharing" target="_blank">**Sample CSV**</a> 

##  **CSV columns and formatting**

The below table gives a brief description of all the column fields of a CSV file:

>   :memo: **Note** - It is important to maintain the correct column names in the CSV file in order to map to the respective fields while importing. The table below provides the formats and names to be followed.

CSV Column Name | Maps to Product Property | Example | Notes
---------|----------|---------|-------
 [**ID**](#id) | Product Id | 100 | Defining this will overwrite data for that ID on Import  
 [**Type**](#type) | type | simple,variable,variation | Product Type. Valid values: simple, variable, variation 
 [**SKU**](#sku) | sku | my-sku | Required. Auto-generated if missing. 
 [**Name**](#name) | name | My Product Name | Required  
 [**Published**](#published) | status | 1 | 1 = published, 0 = private, 
 [**Is featured?**](#featured) | featured | 1 | 1 or 0
 [**Visibility in Catalog**](#visibility-in-catalog) | catalog_visibility | visible | Supported values: visible, catalog, search, hidden  
 [**Short Description**](#short-description) | short_description | NA | NA 
 [**Description**](#description) |description | This is more information about a product | D3
 [**Date sale price starts**](#date-sale-price-starts-ends) | date_on_sale_from | yyyy-mm-dd ;hh:mm:ss | Date or leave blank  
 [**Date sale price ends**](#date-sale-price-starts-ends) | date_on_sale_to | yyyy-mm-dd ;hh:mm:ss | Date or leave blank 
 [**Tax Status**](#tax-status) | tax_status | taxable | Supported values: taxable, shipping, none
 [**Tax class**](#tax-class) | tax_class | HSN Code | Can use any existing tax class.  
 [**In stock?**](#in-stock?) | stock_status | 1 | 1 or 0
 [**Stock**](#stock) | manage_stock/stock_quantity | 20 | Numeric stock level enables stock management. parent can be used for variations. Blank = no stock management.
 [**Low stock amount**](#low-stock-amount) | low_stock_amount | 3 | Any number or blank  
 [**Backorders allowed?**](#backorders-allowed-?) | backorders | 0 | 0 or 1 
 [**Sold individually?**](#sold-individually-?) | sold_individually | 0 | 1 or 0
 [**Weight**](#weight) (unit) | weight | 100 | Only numbers; Unit = kgs  
 [**Length**](#length) (unit) | length | 20 | Only numbers; Unit = inch 
 [**Width**](#width) (unit) | width | 20 | Only numbers; Unit = inch 
 [**Height**](#height) (unit) | Heigth | 20 | Only numbers; Unit = inch   
 [**Allow customer reviews-?**](#allow-customer-reviews?) | reviews_allowed | 0 | 1 or 0 ; NA 
 [**Purchase Note**](#purchase-note) | purchase_note | NA | NA - Leave blank
 [**Sale price**](#sale-price) | sale_price | 1000 | Any number or blank; Unit = INR  
 [**Regular price**](#regular-price) | regular_price | 1000 | Mandatory - Any number; Unit = INR  
 [**Categories**](#categories) | category_ids | Category 1, Category 1 > Category 2  | CSV list of categories. ">" used for hierarchy.
 [**Tags**](#tags) | tag_ids | Tag 1, Tag 2 | CSV list of tags.
 [**Shipping class**](#shipping-class) | shipping_class_id | Name | Name of shipping class - Normal, Delhivery
 [**Images**](#images) | image_id/gallery_image_ids | Image url, image id, image name | First is featured image
 [**Download Limit**](#download-limit) | download_limit | NA | NA - Leave blank
 [**Download expiry days**](#download-expiry-days) | download_expiry | NA | NA - Leave blank
 [**Parent**](#parent) | parent_id | id:100, SKU-1 | Set parent ID. Used for variations. Can be just a numeric ID e.g. id:100 or a SKU. Export will use SKU when possible.
 [**Grouped products**](#grouped-products) | children | NA | NA - Leave blank
 [**Upsells**](#upsells) | upsell_ids | id:100, id:101, SKU-1, SKU-2 | List of IDs. Can be just a numeric ID e.g. id:100 or a SKU. Export will use SKU when possible.
 [**Cross-sells**](#cross-sells) | cross_sell_ids | NA | NA - Leave blank
 [**External URL**](external-url) | product_url | NA | NA - Leave blank
 [**Button Text**](#button-text) | button_text | NA | NA - Leave blank
 [**Position**](#position) | menu_order | 1/2/3 | Menu order, used for sorting - enter a number
 [**Color taxonomy**](#color-taxonomy) | color_taxonomy | Red,blue,multi | Enter all colors seperated by comma
 [**Material taxonomy**](#material-taxonomy) | material_taxonomy | cotton, linen, silk | Enter all materials seperated by comma
 [**Attribute Color**](#attribute-color) | color | color|color code | Enter only for variable & variations; Color code = #alpha-number
 [**Attribute 1 name**](#attribute-1-name) | attributes | size | Looks for global attribute or uses text if not found. Include as many as needed. "Used for variations" is set automatically.
 [**Attribute 1 value**](#attribute-1-value) | attributes | S, M, L, XL | List of values. Variations only need 1 value. First is used if multiple get provided.
 [**Attribute 1 visible**](#attribute-1-visible) | attributes | 1 | 1 or 0. Mapping screen labels this as "Attribute Visibility"
 [**Attribute 1 global**](#attribute-1-global) | attributes | 1 | 1 or 0. Mapping screen labels this as "Is a global attribute?"
 [**Meta: Shoulder**](#meta-shoulder) | shoulder | 10 | Enter any number; Unit = inch
 [**Meta: Bust**](#meta-bust) | bust | 10 | Enter any number; Unit = inch
 [**Meta: Waist**](#meta-waist) | waist | 10 | Enter any number; Unit = inch
 [**Meta: Hip**](#meta-hip) | hip | 10 | Enter any number; Unit = inch
 [**Meta: Length**](#meta-length) | length | 10 | Enter any number; Unit = inch
 [**Meta: _wc_additional_variation_images**](#meta-wc-additional-variation-images) | additional_images | 1234, 6538,2878 | Only Color attribute variations; enter numeric code
 [**Meta: wpcf-finer-details**](#meta-wpcf-finer-details) | finer_details | This is text related to a product | Enter text
 [**Meta: wpcf-delivery-exchange**](#meta-wpcf-delivery-exchange) | delivery_exchange | This is text related to a products delivery/exchange/return | Enter text
 [**Meta: wpcf-size-fit**](#meta-wpcf-size-fit) | size_fit | This is text related to a products size/fit | Enter text
 [**Attribute 2 name**](#attribute-2-name) | attributes | color | Looks for global attribute or uses text if not found. Include as many as needed. "Used for variations" is set automatically.
 [**Attribute 2 value**](#attribute-2-value) | attributes | red, yellow, blue | List of values. Variations only need 1 value. First is used if multiple get provided.
 [**Attribute 2 visible**](#attribute-2-visible) | attributes | 1 | 1 or 0. Mapping screen labels this as "Attribute Visibility"
 [**Attribute 2 global**](#attribute-2-global) | attributes | 1 | 1 or 0. Mapping screen labels this as "Is a global attribute?"

 

##  **Column Fields**

In this section of the manual, we will discuss all the columns fields one by one:

### **ID**

Once a new product is created in the system, a Product Id is generated automatically. This Product Id is unique to each product.

![prod id](Images\Bulk-Import\prodid.jpg)


[**Back to Table**](#csv-columns-and-formatting)

### **Type**

In the type field, enter the Product type. There are 3 options which can be entered:

-   **Simple** - A simple product is a type of product which is a unique (there is only one version), stand-alone, physical product that a customer can add to cart/purchase.
-   **Variable** - A variable product is a type of product which can have multiple options to choose from. For example, a t-shirt available in different colors and/or sizes.
-   **Variation** - These are multiple options available for a Variable product. 

>   **Note** - **Variation rows  should always come below the Simple and Variable rows.** 


Entry in CSV | As updated in Backend
---------|---------
 ![type](Images\Bulk-Import\type.jpg) |![type1](Images\Bulk-Import\type1.jpg)


[**Back to Table**](#csv-columns-and-formatting)

### **SKU** 

SKU refers to a Stock-keeping unit, a unique identifier for each distinct product and service that can be purchased.


Simple | Variable | Variation
---------|----------|---------
 Enter the Product SKU here | This is known as a Parent SKU | Here enter the Variation SKU which gets uploaded in the Variation data
 ![simplesku1](Images\Bulk-Import\simplesku1.jpg)| ![variablesku1](Images\Bulk-Import\variablesku1.jpg) | ![variationsku1](Images\Bulk-Import\variationsku1.jpg)
 ![simplesku](Images\Bulk-Import\simplesku.jpg)| ![variablesku](Images\Bulk-Import\variablesku.jpg)| ![variationsku](Images\Bulk-Import\variationsku.jpg)

[**Back to Table**](#csv-columns-and-formatting)

### **Name**

In the name field,  product name to be displayed on the website product pages is to be entered.


Simple | Variable | Variation
---------|----------|---------
 The name should be as to be shown on the website | The name should be as to be shown on the website | The name along with the variation name should be entered
 ![simplename](Images\Bulk-Import\simplename.jpg) |![variablename](Images\Bulk-Import\variablename.jpg) | ![variationname](Images\Bulk-Import\variationname.jpg)
 ![simplename1](Images\Bulk-Import\simplename1.jpg) | ![variablename1](Images\Bulk-Import\variablename1.jpg) | 

[**Back to Table**](#csv-columns-and-formatting)

### **Published**

Publishing a product means that it will be visible on the website. Till the time it is not published, the product status remains private.

In the CSV file, only 2 values can be entered:

-   **0** = Not published (private)
-   **1** = Published



Entry in CSV |  As updated in Backend
---------|---------
 ![published1](Images\Bulk-Import\published1.jpg) | ![published](Images\Bulk-Import\published.jpg)
 ![private1](Images\Bulk-Import\private1.jpg) |  ![private](Images\Bulk-Import\private.jpg)
 
[**Back to Table**](#csv-columns-and-formatting)

### **Featured**

Featured field is used for marking products on homepage or any particular page in a featured category.

In the CSV file, only 2 values can be entered:

-   **0** = Not Featured
-   **1** = Featured

![featured](Images\Bulk-Import\featured.jpg)

**By default, the entry = "0" for all products as at SOI this functionality is not required.**

[**Back to Table**](#csv-columns-and-formatting)


### **Visibility in Catalog**

This setting determines which shop pages products will be listed on.

By default, the entry on CSV = "visible"

![catalogvisibility](Images\Bulk-Import\catalogvisibility.jpg)

[**Back to Table**](#csv-columns-and-formatting)

### **Short Description**

**NA**

The short description is not required so this field is left blank for all products.

[**Back to Table**](#csv-columns-and-formatting)

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

[**Back to Table**](#csv-columns-and-formatting)

### **Date Sale price starts/ends**

The Date Sale price starts and Date Sale price ends fields help in setting the schedule for any sale if applicable.


Simple | Variable | Variation
---------|----------|---------
 The schedule is set in the General tab | The sale schedule is set at Variation level | The schedule is set in the variation data section
 ![simple schedule](Images\Bulk-Import\simplesaleschedule.jpg) |  | ![variation schedule](Images\Bulk-Import\variationsaleschedule.jpg)
<br>

>   **Note** - **The date format to be followed always = "yyyy-mm-dd;hh:mm:ss"**

>   **NEVER USE WRONG DATE FORMAT**

[**Back to Table**](#csv-columns-and-formatting)

### **Tax Status**

The tax status field defines whether or not the entire product is taxable.

By default, all products at SOI are taxable. Always enter "taxable" in this field.


Entry in CSV | As updated in Backend
---------|---------
 ![taxstatus](Images\Bulk-Import\taxstatus.jpg) | ![taxstatus1](Images\Bulk-Import\taxstatus1.jpg)

[**Back to Table**](#csv-columns-and-formatting)

### **Tax Class**

Tax classes are used to apply different tax rates specific to certain types of products. Enter the applicable code in this field.

Tax class is a **mandatory** field and relevant code should be entered.


Entry in CSV |  As updated in Backend
---------|---------
 ![taxclass](Images\Bulk-Import\taxclass.jpg) |   ![taxclass1](Images\Bulk-Import\taxclass1.jpg)


**Points to Remember:**

-   Pre-defined HSN Codes are entered in the tax class field.
-   HSN Code to be used should be already added in the system.

    ![taxrates](Images\Bulk-Import\taxrate.jpg)


-   If HSN code not added, follow the [**Tax Rate Setup**](../WooCommerce-Settings/Tax-Rate-Setup.md)

[**Back to Table**](#csv-columns-and-formatting)

### **In stock?**

This field allows to let the system know, if the product is available or out of stock.

By default, for all products of SOI, the In stock field has value as "1"

In the CSV file, only 2 values can be entered:

-   **0** = No (out of stock)
-   **1** = Yes (In stock)

>   **Note** - **If marking "1", make sure the Stock Value is greater than 1**

[**Back to Table**](#csv-columns-and-formatting)

### **Stock**

Stock field refers to the stock quantity available for each product.

"In case of a variable product this value will be used to control stock for all variations, unless you define stock at variation level."


Simple | Variable | Variation
---------|----------|---------
 Stock quantity is set in the Inventory section | Do not enter value for variable here | Stock quantity is defined at the variation level 
![simplestock1](Images\Bulk-Import\simplestock1.jpg) |  |![variationstock1](Images\Bulk-Import\variationstock1.jpg)
![simplestock](Images\Bulk-Import\simplestock.jpg) ||![variationstock](Images\Bulk-Import\variationstock.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Low Stock Amount**

This refers to the threshold, which, when the product stock reaches this amount you will be notified by email.


Simple | Variable | Variation
---------|----------|---------
 This value is updated in the Inventory section | This value is updated in the Inventory section | Value is updated at variable level only
 ![simplelowstock](Images\Bulk-Import\simplelowstock.jpg) | ![variablelowstock](Images\Bulk-Import\variablelowstock.jpg) | 

[**Back to Table**](#csv-columns-and-formatting)

### **Backorders Allowed?**

This field controls whether or not backorders (No stock but still taking orders) are allowed. It means, if enabled, stock quantity can go below 0.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**For all products of SOI, by default the value is "0"**


Entry in CSV  | As updated in Backend  
---------|----------
 ![simplebackorder](Images\Bulk-Import\simplebackorder.jpg) | ![simplebackorder1](Images\Bulk-Import\simplebackorder1.jpg) 
 ![variablebackorder](Images\Bulk-Import\variablebackorder.jpg) | ![variablebackorder1](Images\Bulk-Import\variablebackorder1.jpg)  
 ![variationbackorder](Images\Bulk-Import\variationbackorder.jpg) | ![variationbackorder1](Images\Bulk-Import\variationbackorder1.jpg)   

[**Back to Table**](#csv-columns-and-formatting)

### **Sold Individually**

If this field is enabled, it would mean that the customer would be allowed to add only one product in the cart.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**Since this functionality is not required for all SOI products, by default the value remains "0"**

[**Back to Table**](#csv-columns-and-formatting)

### **Weight**

Weight is part of the shipping details of all products. Entering a value to this field is mandatory.

Weight should be entered in "kgs"


Simple| Variable | Variation
---------|----------|---------
 The value is updated in the shipping section | The value is set at variation level | The value is set in the respective variation data
 ![simpleweight1](Images\Bulk-Import\simpleweight1.jpg) |  | ![variaitonweight1](Images\Bulk-Import\variationweight1.jpg)
 ![simpleweight](Images\Bulk-Import\simpleweight.jpg) | ![variableweight](Images\Bulk-Import\variableweight.jpg) | ![variaitonweight](Images\Bulk-Import\variationweight.jpg)

[**Back to Table**](#csv-columns-and-formatting)

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


[**Back to Table**](#csv-columns-and-formatting)

### **Allow Customer Reviews?** 

**NA**

If enabled, this field allows the customers to leave reviews on the product pages.

In the CSV file, only 2 values can be entered:

-   **0** = No (Do not allow)
-   **1** = Yes (Allow)

**Since this functionality is not required for all SOI products, by default the value remains "0"**

[**Back to Table**](#csv-columns-and-formatting)


### **Purchase Note**

**NA**

This function is not required for all SOI products, so it will be left blank.

### **Sale Price**

Sale price is the value which is updated if and when a product goes on sale.


Simple | Variable | Variation
---------|----------|---------
 Value is updated in the General section | Value is updated at variaiton level | Value updated in respective variations data
 ![simplesale](Images\Bulk-Import\simplesaleprice.jpg) | ![variablesale](Images\Bulk-Import\variablesaleprice.jpg) | ![variationsale](Images\Bulk-Import\variationsaleprice.jpg)

[**Back to Table**](#csv-columns-and-formatting)

### **Regular Price**

Regular price is the amount the customer pays for any product. 

This is a mandatory field and a value has to be entered for each product.

Simple | Variable | Variation
---------|----------|---------
 Value is updated in the General section | Value is updated at variaiton level | Value updated in respective variations data
 ![simpleregular](Images\Bulk-Import\simpleregular.jpg) | ![variableregular](Images\Bulk-Import\variableregular.jpg) | ![variationregular](Images\Bulk-Import\variationregular.jpg)
 ![simpleregularprice](Images\Bulk-Import\simpleregularprice.jpg) | ![variableregularprice](Images\Bulk-Import\variableregularprice.jpg) | ![variationregularprice](Images\Bulk-Import\variationregularprice.jpg)   

[**Back to Table**](#csv-columns-and-formatting)

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


[**Back to Table**](#csv-columns-and-formatting)


### **Tags**

Product tags are another way to relate products to each other. These are keywords which can be used in searching products on the website.

In this field enter keywords seperated by commas.


Entry in CSV| As updated in Backend
---------|---------
 ![tags](Images\Bulk-Import\tags.jpg) | ![tags1](Images\Bulk-Import\tags1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


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

[**Back to Table**](#csv-columns-and-formatting)

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


[**Back to Table**](#csv-columns-and-formatting)


### **Download Limit** 

**NA**

This field is not required and is left blank.

### **Download Expiry Days**  

**NA**

This field is not required and is left blank.


### **Parent**

The Parent field refers to the Parent SKU as entered in all variable products.

The parent field is required only for **variation** rows. Each variation of a particular variable product is linked to the parent product through this field.

It is mandatory to enter the correct corresponding Parent SKu against the variations, in order to update the backend and frontend correctly.

The below example explains this:

![parent](Images\Bulk-Import\parent.jpg)

[**Back to Table**](#csv-columns-and-formatting)

### **Grouped Products** 

**NA**

This field is not required and is left blank.

### **Upsells**

Up-sells are displayed on the product details page. These are products that are displayed to encourage users to upgrade, based on the product they are currently viewing. 

This field will include the **Product Id** or **Parent SKU** of products to be shown and should be seperated by a comma. 

To enter data, follow below format:

-   To enter a Product Id - ID:number
-   To enter SKU : sku-number

**A maximum of 3 products can be added.**

[**Back to Table**](#csv-columns-and-formatting)


### **Cross-Sells**  

**NA**

This field is not required and is left blank.

### **External URL**  

**NA**

This field is not required and is left blank.

### **Button Text - NA**

This field is not required and is left blank.

### **Position**

The number entered in the Position field, helps decide the order of products on the PLP. 

-   If position = number value : the product will be listed on that position.
-   If position = 0 : the product will be randomly listed.

Simple | Variable | Variation
---------|----------|---------
 Optional | Optional | Not required

<br>

Entry in CSV | As appears on Frontend
---------|----------
 ![position](Images\Bulk-Import\position.jpg) | ![position2](Images\Bulk-Import\position2.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Color Taxonomy**

Colors help in organizing, searching the products on the basis of color category/family.

On the front-end these colors are available as color filters to select from.

In the color taxonomy field, all the product related colors should be entered seperated by a comma.

This field should be updated only for **Simple** and **Variable** rows.


Entry in CSV | As updated in Backend | As appears on Frontend
---------|----------|--------
 ![colors](Images\Bulk-Import\color.jpg) | ![colors1](Images\Bulk-Import\colors1.jpg)| ![colorfilter](Images\Bulk-Import\colorfilter.jpg) 

[**Back to Table**](#csv-columns-and-formatting)


### **Material Taxonomy**

Materials help in organizing the products on the basis of material used (fabric, accessories).

On the front-end these materials are available as material filters to select from.

In the material taxonomy field, all the product related materials should be entered seperated by a comma.

This field should be updated only for **Simple** and **Variable** rows.

Entry in CSV | As updated in Backend| As appears on Frontend
---------|----------|-------
 ![material](Images\Bulk-Import\material.jpg) | ![materials1](Images\Bulk-Import\materials1.jpg) | ![materialfilter](Images\Bulk-Import\materialfilter.jpg) 

[**Back to Table**](#csv-columns-and-formatting)


### **Attribute Color**

The attribute color field is applicable only to **Variable** and **variation** rows for products which have only color variations.

This field defines the color tone for each variation. These color tones are visible on the product page.

Entry to be done = Color name|Corresponding color code (The color code is designated by "#' and a alpha-number, eg. #ebf9ff)


Product Type | Entry In CSV |  As appears on Frontend 
-------|---------|---------
Variable |![variableattributecolor](Images\Bulk-Import\variableattributecolor.jpg) | ![attributecolor2](Images\Bulk-Import\attributecolor2.jpg) 
Variation |![attributecolor](Images\Bulk-Import\attributecolor.jpg) | ![attributecolor2](Images\Bulk-Import\attributecolor2.jpg) 

[**Back to Table**](#csv-columns-and-formatting)


### **Attribute 1 name**

In this field, name of the required attribute is added. This column field is dedicated to the **size** attribute.

For all products, the entry remains same.


Simple | Variable | Variation
---------|----------|---------
 Required - Size | Required - Size | Required - Size

[**Back to Table**](#csv-columns-and-formatting)

### **Attribute 1 Value(s)**

In this field, all values associated with Attribute 1 should be entered.

This is a required field for all rows - Simple, Variable, Variation


Simple | Variable | Variation
---------|----------|---------
 This will have a single entry (could be a measurement or size) | Here all possible variation values to be entered | Enter only variation specific value
 ![simpleattribute1value](Images\Bulk-Import\simpleattribute1value.jpg) | ![variableattribute1value](Images\Bulk-Import\variableattribute1value.jpg) | ![variationattribute1value](Images\Bulk-Import\variationattribute1value.jpg)
 
[**Back to Table**](#csv-columns-and-formatting)


### **Attribute 1 visible**

Attribute to be visible means that it appears on the product page.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated only for **Simple** and **Variable** rows. The value should always be "1" 



Entry in CSV | As updated in Backend
---------|---------
 ![attribute1visible](Images\Bulk-Import\attribute1visible.jpg) | ![attribute1visible1](Images\Bulk-Import\attribute1visible1.jpg)


[**Back to Table**](#csv-columns-and-formatting)

### **Attribute 1 global**

Attribute to be global means that the attributes are available to choose from.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated for all rows - Simple, Variable, Variation. The value should always be "1" 

[**Back to Table**](#csv-columns-and-formatting)

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

[**Back to Table**](#csv-columns-and-formatting)

### **Meta: Bust**

This field consists of the Bust/chest measurement for all products in the **Uppers** (blouses, dresses, kurtas) category.

-   This field is only required for **Variation** rows.
-   The bust measurement helps in differentiating between variation sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![bust](Images\Bulk-Import\bust.jpg) | ![bust1](Images\Bulk-Import\bust1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Meta: Waist**

This field consists of the waist measurement for all products in the **Lowers** (skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The waist measurement helps in differentiating between variation sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![waist](Images\Bulk-Import\waist.jpg) | ![waist1](Images\Bulk-Import\waist1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Meta: Hip**

This field consists of the hip measurement for all products in the **Lowers** (skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The hip measurement helps in differentiating between variation sizes.
-   Measurement unit to be used is "inch".

[**Back to Table**](#csv-columns-and-formatting)


### **Meta: Length**

This field consists of the length measurement for all products in the **Lowers** & **Uppers** (Shirts, blouses, kurtas, skirts, pyjamas, salwars, trousers) category.

-   This field is only required for **Variation** rows.
-   The Length measurement helps in differentiating between variation sizes.
-   Measurement unit to be used is "inch".

Entry in CSV | As updated in Backend 
---------|----------
 ![length](Images\Bulk-Import\length.jpg) | ![length1](Images\Bulk-Import\length1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Meta: _wc_additional_variation_images**

For every product with a color variation, more images related only to that variation can be added as additional images. On the Front-end, these images with each color of the product.

-   This field is updated only for the **Variation** rows.
-   Multiple additional images can be uploaded for each color variation.
-   Each image is assigned with a numeric code. These codes, seperated by comma are entered in this field.

Entry in CSV | As updated in Backend 
---------|----------
 ![additionalimages](Images\Bulk-Import\additionalimages.jpg) | ![additionalimages1](Images\Bulk-Import\additionalimages1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


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

[**Back to Table**](#csv-columns-and-formatting)


### **Meta: wpcf-delivery-exchange**

The delivery/ exchange field contains information regarding shipping, return of product etc. 

Points of consideration while entering text in this field:

-   This field can be upated for **Simple** and **Variable** rows.
-   The text entered will be updated in the **Text** tab.
-   To give line break : add "br in <>" at end of line twice. This will insert a blank line and take you to the next line.
-   To make text bold : add "strong in <>" at the start and end of text.

[**Back to Table**](#csv-columns-and-formatting)


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


[**Back to Table**](#csv-columns-and-formatting)


### **Meta: _views_template - NA**

This field is not required and is left blank.

### **Attribute 2 name**

In this field, name of the required attribute is added. This column field is dedicated to the **color** attribute.

For all products, the entry remains same.


Simple | Variable | Variation
---------|----------|---------
 Required - Color | Required - Color | Required - Color

[**Back to Table**](#csv-columns-and-formatting)


### **Attribute 2 Value**

In this field, all values associated with Attribute 2 should be entered.

This is a required field for all rows - Simple, Variable, Variation


Simple | Variable | Variation
---------|----------|---------
 This will have a single entry (only 1 color) | Here all possible variation values to be entered | Enter only variation specific value
 ![simpleattribute2value](Images\Bulk-Import\simpleattribute2value.jpg) | ![variableattribute2value](Images\Bulk-Import\variableattribute2value.jpg) | ![variationattribute2value](Images\Bulk-Import\variationattribute2value.jpg)
 
[**Back to Table**](#csv-columns-and-formatting)


### **Attribute 2 visible**

Attribute to be visible means that it appears on the product page.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated only for **Simple** and **Variable** rows. The value should always be "1" 



Entry in CSV | As updated in Backend
---------|---------
 ![attribute2visible](Images\Bulk-Import\attribute2visible.jpg) | ![attribute2visible1](Images\Bulk-Import\attribute2visible1.jpg)

[**Back to Table**](#csv-columns-and-formatting)


### **Attribute 2 global**

Attribute to be global means that the attributes are available to choose from.

In the CSV file, only 2 values can be entered:

-   **0** = No (Not visible)
-   **1** = Yes (Visible)

This field is updated for all rows - Simple, Variable, Variation. The value should always be "1" 

[**Back to Table**](#csv-columns-and-formatting)




