#   **Tax Rate Setup**

##  **How to access Tax rates**

Tax classes are displayed at the top of the tax screen. 

1.  Go to: **WooCommerce** -> **Settings** -> **Tax**

    ![woosettings](images\woosettings.jpg)

    ![woo tax](images\wootax.jpg)

2.  Click one to view tax rates for the class.

    ![taxclass](images\taxclass.jpg)

### **Tax Rate Attributes**

Each tax rate has these attributes:

![tax rate](images\taxrate.jpg)

1.  **Country Code** – 2 digit country code for the rate. Use ISO 3166-1 alpha-2 codes. Leave blank (*) to apply to all countries. Eg: IN = India
2.  **State Code** – 2 digit state code for the rate. See i18n/states/COUNTRYCODE.php for supported states. Use a 2 digit abbreviation e.g. UP = Uttar Pradesh. Leave blank (*) to apply to all states.
3.  **ZIP/Postcode** – Enter postcodes for the rate. You may separate multiple values with a semi-colon, use wildcards to match several postcodes (e.g. PE* would match all postcodes starting with PE), and use numeric ranges (e.g. 2000…3000). Leave blank (*) to apply to all postcodes.
4.  **City** – Semi-colon separated list of cities for the rate. Leave blank (*) to apply to all cities.
5.  **Rate %** – Enter the tax rate, for example, 20.000 for a tax rate of 20%.
6.  **Tax Name** – Name your tax, e.g. VAT
7.  **Priority** – Choose a priority for this tax rate. Only 1 matching rate per priority will be used. To define multiple tax rates for a single area you need to specify a different priority per rate.
8.  **Compound** – If this rate is compound (applied on top of all prior taxes) check this box.
9.  **Shipping** – If this rate also applies to shipping, check this box.


### **Tax Import/Export CSV**

In order to add/edit tax rates, there is option of Import CSv and Export CSV.

-   **Multiple HSN Codes** (Tax rates) can be imported in one CSV file.

-   The CSV file for importing requires 10 columns:

    -   **country code** 
    -   **state code**
    -   **postcodes**
    -   **cities**
    -   **rate**
    -   **tax name**
    -   **priority**
    -   **compound**
    -   **shipping**
    -   **tax class**

-   In the CSV file, 3 rows are required to be filled for each tax rate.

Below is a sample tax rate CSV with multiple tax classes to import based on state tax only:

![sample CSV](images\samplecsv.jpg)


<a href="https://docs.google.com/spreadsheets/d/1JERXphaep4o5AZ7WdbYgk0B6VW2Y2GHLx2i4DZ9NeOc/edit?usp=sharing" target="_blank">**Sample Import CSV**</a>