# Dimensional Modeling

This project has as main goal the practising of data modeling techniques based on [Kimball design techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/).

## **Fundamental Concepts**

The four key decisions made during the design of a dimensional model include:

1. Select the business process
2. Declare the grain
3. Identify the dimensions
4. Identify the facts.

Following the business process, grain, dimension, and fact declarations, the design team determines the table and column names, sample domain values, and business rules.

### **Business Processes**
Business processes are the operational activities performed by the organization. 
Business process events generate or capture performance metrics that translate into facts in a fact table. 
Most fact tables focus on the results of a single business process. 
Each business process corresponds to a row in the data warehouse. 

### **Grain**
The grain establishes exactly what a single fact table row represents. The grain must be declared before choosing dimensions or facts because every candidate dimension or fact must be consistent with the grain.
Atomic grain refers to the lowest level at which data is captured by a given business process. 
Eachg proposed fact table grain results in a separate physical table; different grains must not be mixed in the same table.

### **Dimensions for descriptive context**
Dimensions provide the *who, what, where, when, why, and how* context surrounding a business process event. 
Dimension tables contain the descriptive attributes used by BI applications for filtering and grouping the facts. With the grain of a fact table firmly in mind, all the possible dimensions can be identified.

### **Facts for measurements**
Facts are the measurements that result from a business process event and are almost always numeric. A single fact table row has a one-to-one relationship to a measurement event as described by the fact table's grain.
