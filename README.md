# USA-Real-Estate-Database-System-Postgres-Power-BI
**Project Overview: USA Real Estate Database System**

**Objective:**
Design and implement a comprehensive real estate database system utilizing PostgreSQL, integrated with Power BI for data visualization.

**Database Architecture:**
- **Properties Table:**
  - Defined real estate property attributes (status, bed, bath, acre_lot, city, state, zip_code, house_size, prev_sold_date, price).
  - Implemented a primary key (PropertyID) and a foreign key (BuyerID) referencing the DimBuyer table.

- **DimBuyer Table:**
  - Captured buyer details (BuyerID, Email_Id, Prefix, Name, Birth_Date, Phone_Number, Additional_Email_Id, Address, Zip_Code, City, State, Country, Link, Text).
  - Established BuyerID as the primary key.

- **DimProp Table:**
  - Extracted relevant property details (PropertyID, status, city, state, prev_sold_date) from the Staging table.
  - Employed PropertyID as the primary key.

- **Fact Table:**
  - Created a central fact table (FactID, bed, bath, acre_lot, zip_Code, house_size, price, Year, Time, SSN, BuyerID, PropertyID).
  - Integrated foreign keys referencing DimBuyer and DimProp tables.

- **Staging Table:**
  - Temporary storage for incoming data.
  - Populated using data from the Properties and Buyers tables.

**Workflow:**
1. **Data Extraction:**
   - Loaded raw data into the Staging table from the Properties and Buyers tables.

2. **Dimension Tables:**
   - Transferred data from the Staging table into DimProp and DimBuyer tables.
   - Ensured data integrity by applying constraints and primary keys.

3. **Data Transformation:**
   - Utilized SQL queries to link Staging data with DimProp and DimBuyer tables.
   - Conducted updates and transformations to enhance data accuracy.

4. **Fact Table Population:**
   - Integrated data from Staging into the central Fact table, considering key references to DimBuyer and DimProp.

**Performance Tuning:**
- Conducted performance tuning on the database, ensuring optimal query execution.

**Power BI Integration:**
- Crafted a Power BI dashboard for insightful data visualization, emphasizing critical metrics like premiums, claims ratio, and policy formulations.

This project showcases expertise in database design, SQL programming, and data visualization, particularly tailored for the intricacies of usa real estate datasets. The GitHub repository includes SQL scripts, database schema, and relevant documentation for comprehensive understanding and replication.
