#   **Add Products**

##  **Introduction**

The Add products section of the Manual will cover steps which are common for all product types. This shows the basic steps to be followed always.

##  **Adding a Product**

Adding a product involves the below steps:

1.  Go to -> https://newwebsite.shadesofindia.com/wp-admin
2.  Login with the credentials
3.  Click on **Products** on the left side panel.
4.  Click -> **Add New**. This opens a new interface, where you can add Product name, description, product image, product category, tags etc. A sample screenshot is below:

    ![add new](Images\Simple-Products\addnewprod.jpg)

Below, we will see how to add/edit each section for a product:

### **Product Name & Description**

The first step is to :

![add name](Images\Simple-Products\addname.jpg)

*   **Add Name** : Provide a title for the product.
*   **Add Descripton** : Provide a detailed description about the product. 

The website look:

![add name1](Images\Simple-Products\addname1.jpg)
    
### **Products Custom Fields**

This section allows you to add customised details about the product. These details can be seen on the single product page on the website. The options available are:

![custom fields](Images\Simple-Products\prodcustomfields.jpg)

*   **Finer Details** - This field may include details related to the fabric used, care instructions, etc. Eg. below:

    ![finer details](Images\Simple-Products\finerdetails.jpg)

*   **Size & Fit** - Any instructions regarding the size and fit can be added here. Eg, below:

    ![size fit](Images\Simple-Products\sizefit.jpg)

*   **Delivery & Exchange** - This field contains information regarding shipping, return of product etc. Eg. below:

    ![del return](Images\Simple-Products\delreturn.jpg)


### **Product Data**

The Product Data box is where the majority of important data is added for the products. Here, you will select the product type and information about pricing, inventory, shipping etc.

Let's look at the options available.

*   Under **Product Data** -> Select **Product Type** from the list.

![prod data](Images\Simple-Products\proddata.jpg)

Once the type of product is selected, information in various tabs needs to be added. We will discuss the tabs one by one:

####   **General** 

The General section is for configuring the regular and sale price and taxes of the product.

![general](Images\Simple-Products\general.jpg)

*   **Price**

    -   **Regular Price** - Item's normal or regular price. This shows along with the product on catalog page as well as the single product page.
    -   **Sale Price** - The sale price is for when you decide to run a discount campaign. Otherwise, shoppers will see the regular price.

*   **Tax**

    -   **Tax status** - Select whether or not the product is taxable.
    -   **Tax class** - Choose the applicable tax class, if product is taxable.

####    **Inventory**

The inventory section allows you to manage stock for the product individually and define whether to allow back orders and more. It enables you to sell products and allow customers to add them to the cart to buy.


-   **SKU** - SKU is a unique identification number available on every product or service which simplifies inventory management. It can be entered manually or generated automatically.
-   **Manage stock?**

    -   **Stock management at product level is disabled** - You are responsible for updating the **Stock Status** manually.

         ![inventory1 disable](Images\Simple-Products\stkmngmtdisable.jpg)

    -   **Stock management at product level is enabled** - Below options need to be updated:

        ![inventory enable](Images\Simple-Products\stkmngmtenable.jpg)

        -   **Stock Quantity** : Enter the number of pieces available, and it will auto update as Stock, Out of Stock or On Backorder.
        -   **Allow Backorders** : Select the required option. 
        -   **Low stock threshold** : Enter a number, which will notify you when the product’s stock goes below the threshold.
        -   **Sold individually** : Tick this box to limit the product to one per order.


####    **Shipping**

The Shipping tab, allows you to control important details about a physical product for shipping. The below fields are required to be filled:

![shipping](Images\Simple-Products\shipping.jpg)

-   **Weight** - Enter the weight of the product.
-   **Dimensions** - Enter the Length, Width and Height of the product.
-   **Shipping Class** - Shipping class is used by certain shipping methods to group similar products. Select the option from the list.

####    **Linked Products**

Linked products are recommendations to cross promote products and improve store revenue. There are two ways to accomplish this:

![linkedprods](Images\Simple-Products\linkedprods.jpg)

-   **Upsells** - Up-sells are displayed on the product details page. These are products that you may wish to encourage users to upgrade, based on the product they are currently viewing. Search and add the relevant product in this field.
-   **Cross-sells** - Cross-sells are products that are displayed with the cart and related to the user’s cart contents.  Search and add the relevant product in this field.

####    **Attributes**

Attributes are descriptors for a product. This tab will help you assign details like color options, sizes, fit and more to the product.

-   Choose the relevant option from the list which provides two options:

    -   **Custom Product attribute** : These are added at the product level and won’t be available in layered navigation or other products.

        :computer:  <a href="https://docs.woocommerce.com/document/managing-product-taxonomies/#add-custom-attributes" target="_blank">**How to add Custom Product Attributes**</a>

    -   **Global attribute sets already created** : These attributes once created will be available  in layered navigation or other products.

        :computer: <a href="https://docs.woocommerce.com/document/managing-product-taxonomies/#add-custom-attributes" target="_blank">**Learn to create Global Attributes**</a>

-   Click on **Add**

    ![attributes](Images\Simple-Products\attributes.jpg)
    
-   Apply the terms/values attached to the attribute. For simple products, mostly a single value is entered.
-   Tick the **Visible on the product page** box - This will show the selected attribute on the product page.

    ![attribute1](Images\Simple-Products\attributes1.jpg)

This is how a selected attribute looks on the product page:

![attribute2](Images\Simple-Products\attribute2.jpg)



####    **Advanced**

The Advanced tab can be used for adding a purchase note that appears after placing an order. The below fields need to be filled:

![advanced](Images\Simple-Products\advanced.jpg)

-   **Purchase note** - Enter an optional note to send the customer after they purchase the product.
-   **Menu order** - Custom ordering position for this item.
-   **Enable Reviews** - Enable/Disable customer reviews for this item.



### **Product Short Description**

In the short description box, write an engaging short description using the editor.

This is an excerpt which typically appears at a prominent spot next to product imagery on the listing page.

![prodshortdesc](Images\Simple-Products\prodshortdesc.jpg)

### **Right Side Panel - Add some finishing touches**

By following the above steps correctly, the product page is almost ready. Some more tweaks and finishing touches to the right side panel will make the product page more user-friendly. Let's look at the menu options to be updated here:

####    **Product Categories**

Product categories help in organizing the products. Categories are the primary way to group products with similar features. You can also add sub-categories if desired.

Categories can also be **reordered** by dragging and dropping – this order is used by default on the front end whenever the categories are listed. This includes both widgets and the category/subcategory views on product pages.

:computer: <a href="https://docs.woocommerce.com/document/managing-product-taxonomies/#section-1" target="_blank">**How to add categories and sub-categories**</a>

The customers will be able to use the categories on the front-end of the website store in the form of filters to find/shortlist products.

![prodcat2](Images\Simple-Products\prodcat2.jpg)


1.  Go to -> **Product Categories**
2.  Choose from existing categories and sub-categories.
3.  Click -> **Add New Category** to add new names.

This is how the category filter looks on the website:

![cat filter](Images\Simple-Products\catfilter.jpg)

####    **Product Tags**

Product tags are another way to relate products to each other, next to product categories. Contrary to categories, there is no hierarchy in tags; so there are no “subtags.”

The customers will be able to use the tags on the front-end of the website store in the form of filters to find products. Try to make them logical and useful for your target customers.

![prodtags](Images\Simple-Products\prodtags.jpg)

1.  Go to -> **Product Tags**
2.  **Add** keywords seperated with commas
3.  You can also **choose from the most used tags**



####    **Colors**

Colors help in organizing the products on the basis of color category/family. The customers will be able to use this as a color filter on the front-end of the website store to find products.

![colors](Images\Simple-Products\colors.jpg)

1.  Go to -> **Colors**
2.  Select from the existing list
3.  Click -> **Add New Color** to add more choices

The color filter on the website:

![color filter](Images\Simple-Products\colorfilter.jpg)

####    **Materials**

Materials help in organizing the products on the basis of material used (fabric, accessories). The customers will be able to use this as a material filter on the front-end of the website store to find products.

![materials](Images\Simple-Products\materials.jpg)

1.  Go to -> **Materials**
2.  Select from the existing list
3.  Click -> **Add New Material** to add more choices

The material filter looks as below:

![material filter](Images\Simple-Products\materialfilter.jpg)

####    **Product Image**

The Product Image is the main image for your product and is reused in different sizes across your store. This will be the largest image on the single product page and will also appear on the catalog page.

Follow the steps to add image:


1.  Go to -> **Product Image** 
2.  Click -> **Set Product Image**

    ![setprodimage](Images\Simple-Products\setprodimage.jpg)

3.  Select an existing image or upload a new one.
4.  Click -> the image to edit or update

    ![prodimage](Images\Simple-Products\prodimage.jpg)

A snapshot of the product image in the catalog on the website is below:

![prod image1](Images\Simple-Products\prodimage1.jpg)

####    **Product Gallery**

Product galleries display all images attached to a product through the Product Gallery meta box. You can add extra images that appear in the gallery on the single product page.

Follow the below steps to add gallery images:

![prod gallery](Images\Simple-Products\prodgallery.jpg) 

1.  Go to -> **Product Gallery**
2.  Click -> **Add product gallery image**
3.  Select existing images or upload new ones.

>   **Images in the product gallery can be re-ordered easily via drag and drop.**

>   **To remove an image from the product gallery, hover over the image and click on the red “x.”** 

This is how the product gallery appears on the website product page:

![prodgalleryfinal](Images\Simple-Products\prodgallery1.jpg)


>   **Note** - The first image in the Product Gallery is the same as the Product Image. Rest of the images are known as Gallery Images.

####    **Setting catalog visibility options and feature status**

In the Publish panel, you can set Catalog Visibility for your product. The below options are available to choose from:

![catalogvisibility](Images\Simple-Products\catalogvisibility.jpg)

-   **Shop and search** – Visible everywhere, shop pages, category pages and search results.
-   **Shop only** – Visible in shop pages and category pages, but not search results.
-   **Search only** – Visible in search results, but not in the shop page or category pages.
-   **Hidden** – Only visible on the single product page – not on any other pages.



##  **Publish/Update**

Once you double-check that all of the product details are correct, you can:

-   Click on **Publish** button on the right side panel to save a new entry.

    ![publish](Images\Simple-Products\publish.jpg)


    
-   Click on **Update** button on the right side panel to save any edit done on existing entries.

    ![update](Images\Simple-Products\update.jpg)


##  **The Final Product Page**

Once all the above changes are published or updated, the final look of the product page on the website is below:

![simpleprodfinal](Images\Simple-Products\simpleprodfinal.jpg)



