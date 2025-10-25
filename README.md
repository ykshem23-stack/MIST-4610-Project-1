# MIST-4610-Project-1

## Team Members
- Yesha Ghandi
- Bradley Guy
- Ivan Jaiwant
- Yusuf Kshem

## Problem Description
This project presents a comprehensive relational database model that organizes and connects key social, economic, environmental, and cultural data across global regions and their respective countries. The model is built around a hierarchical structure linking regions, countries, and cities, allowing for an integrated view of global relationships. Each country serves as the central entity in the schema and is connected through one-to-one relationships to detailed national-level tables, including Economy, Education, Health, Demographics, Environment, and Labor Force. These tables store critical indicators such as GDP, education enrollment rates, population density, and mortality statistics, enabling multidimensional analysis of development and performance across nations. In addition, the model incorporates many-to-many relationships with Language and Currency entities, reflecting the cultural and financial interconnections between countries. Through a set of analytical SQL queries, the project enables exploration of relationships between key factors such as education and wages, GDP and environmental efficiency, tax rates and economic growth, and population density and productivity. Overall, this database provides a powerful framework for global data analysis, supporting insights into economic trends, sustainability efforts, and cross-regional development patterns.
## Data Model
Our hospital management system is designed to optimize hospital operations and facilitate the efficient delivery of patient care. The model emphasizes the management of staff, patient records, departments, appointments, lab tests, and billing processes.

Patients are at the heart of the system's design. The Patient entity stores key information about individuals receiving care, including their emergency contact details. Each patient is assigned to a Ward, forming a one-to-many relationship since a ward can accommodate multiple patients. Patients may also have multiple Appointments with doctors, represented by a one-to-many relationship between the Patient and Appointment entities. Each appointment record includes details about the attending doctor, as well as the date and time of the consultation. Additionally, each patient can undergo one or more Lab Tests, represented by a one-to-many relationship with the Lab_Tests entity, which records tests performed in a specific laboratory.

Doctors are integral to delivering patient care. The Doctor entity captures essential information about the hospital's medical staff. Each doctor may report to a Senior Doctor, establishing a recursive one-to-many relationship within the Doctor table. Furthermore, each doctor is associated with a specific Department, such as cardiology, surgery, or pediatrics, forming a one-to-many relationship between the Department and Doctor entities. This structure effectively represents the organization of the hospital's medical staff.

Doctors manage appointments with multiple patients, represented by a one-to-many relationship between the Doctor and Appointment entities. During these appointments, doctors may prescribe treatments or medications, which are documented in the Prescription entity. A one-to-many relationship exists between Doctor and Prescription, as a doctor can issue multiple prescriptions, and also between Patient and Prescription, since a patient may receive several prescriptions over time. Each prescription record includes details such as the medication name, dosage, and specific instructions for use. To ensure proper organization, the Pharmacy entity has been added which is represented by a one-to-many relationship with Prescription. This keeps track of which pharmacy each precription was written at, the pharmacy name, location, and the contact number for the pharmacy.

The Nurse entity represents all nurses within the hospital. To reflect the hierarchy, a recursive one-to-many relationship exists within the Nurse table, allowing each nurse to report to a Head Nurse. Additionally, we introduced an associative entity called NurseWardAssignment to manage the assignments of nurses to various wards. This entity models the many-to-many relationship between Nurses and Wards, as a nurse can be assigned to multiple wards, and each ward can have several nurses working in it.

The Ward entity represents various sections within the hospital, such as ICU, Pediatrics, or General Surgery. Each ward is overseen by a Head Nurse, which is captured through a one-to-one relationship between the Ward and Nurse entities for the head nurse role.

The hospital's Medical_Record entity collaborates with the Diseases entity to ensure each patient's information is properly organized and correctly assigned to the patient. A one-to-many relationship exists between Diseases and Medical_Record, as well as between Patient and Medical_Record, since patients may have multiple records for different visits. Each instance of the Diseases entity includes details about the disease, symptoms, duration, severity, and recommended treatment.

In addition to medical care, the hospital management system tracks financial information through the Billing entity. Each Billing record is connected to a Patient and an Insurance provider. The Billing table captures the total amount, the insurance-covered portion, and payment details, ensuring a comprehensive record of the patient's financial obligations. A one-to-one relationship exists between Billing and Insurance, with each billing record linked to a specific insurance policy.

Lastly, the Insurance entity stores information about insurance providers, policies, and coverage periods. This entity helps the hospital manage insurance claims and coverage for patients' medical expenses.

![image](https://github.com/user-attachments/assets/9cddd960-842f-4584-9e81-f882e12f6774)



## Data Dictionary

![image](https://github.com/user-attachments/assets/77082899-0cd4-4fa7-b887-50f2ce4e7e11)

![image](https://github.com/user-attachments/assets/70e782e5-5ba9-4582-b6e0-8b90d30e6424)
![image](https://github.com/user-attachments/assets/48042ac0-eb53-4642-9528-30efe598082d)
![image](https://github.com/user-attachments/assets/3b414ac8-28c1-47b6-a326-0280653a2753)
![image](https://github.com/user-attachments/assets/661972d7-e242-41a3-90df-f1c3f408b0dd)
![image](https://github.com/user-attachments/assets/35a6efea-1f4b-4bed-9507-636ce7d7b7cb)


![image](https://github.com/user-attachments/assets/0513c62f-020a-4631-8dbd-a79af9e15102)

![image](https://github.com/user-attachments/assets/cf2b9ebc-4290-40fc-b703-9a766ff0084c)
![image](https://github.com/user-attachments/assets/3e9b52db-123e-4e0b-b9e6-586d384c3b07)
![image](https://github.com/user-attachments/assets/3891f6b1-3fbd-4759-88eb-4d3cf1b24e6f)
![image](https://github.com/user-attachments/assets/24c5d775-f0cc-474d-98ee-d0dd3faa0c95)




![image](https://github.com/user-attachments/assets/3e1d6b17-d6d4-4889-9ed6-a9e5b76de202)

![image](https://github.com/user-attachments/assets/33873034-7f12-4b0f-afea-2628afea47b2)

![image](https://github.com/user-attachments/assets/b39ad5c3-a99d-4561-8163-a515c005c881)

![image](https://github.com/user-attachments/assets/91cc84d8-db37-449b-a2f8-5230aa22be41)

![image](https://github.com/user-attachments/assets/4aba44b2-1cdc-4213-baf8-1e0151a735ae)

![image](https://github.com/user-attachments/assets/bf41fc0f-3f90-42ff-961f-920be66adfab)

![image](https://github.com/user-attachments/assets/603ebf4c-6cb9-4ee9-83bd-ca1eb8abd1f1)


![image](https://github.com/user-attachments/assets/dfbea109-de5b-47c0-8f9a-6093e42c0019)

![image](https://github.com/user-attachments/assets/ccbaa1f7-a78b-4470-9984-5cbed9c21750)

![image](https://github.com/user-attachments/assets/c17e2d28-03d9-4c57-93d9-d43997721629)

![image](https://github.com/user-attachments/assets/a8c0e567-2286-44a0-a28b-7275968dbeee)

![image](https://github.com/user-attachments/assets/576c6bf2-5d2f-4f8f-b30f-f69fc1b5baef)


![image](https://github.com/user-attachments/assets/fa46e752-0a7e-4d97-a6de-af3b01d07c96)

![image](https://github.com/user-attachments/assets/4632bbe2-62aa-45fa-9dce-b04a8851e451)

![image](https://github.com/user-attachments/assets/376a813b-12a3-409a-a5ae-7b57981d40d0)

![image](https://github.com/user-attachments/assets/9a37b809-e6a0-4dcd-90f1-a775170f3c3f)


![image](https://github.com/user-attachments/assets/39a24778-beff-4773-a75a-2f030f2bf61e)

![image](https://github.com/user-attachments/assets/d2aa703f-10e9-4b87-849e-7b2ad869b6ae)



![image](https://github.com/user-attachments/assets/ee0eb7db-d25a-421b-b88d-e7fbb3b22099)

![image](https://github.com/user-attachments/assets/5e4be7dd-c107-4564-95d6-218d0efd96c0)



![image](https://github.com/user-attachments/assets/2d638cc3-471c-470d-8a06-c82ae9df2a08)

![image](https://github.com/user-attachments/assets/c9015e89-7abb-42db-9db3-40f9383921ad)



![image](https://github.com/user-attachments/assets/4aa035d9-5420-4b5b-9ef5-e8629904a8e4)

![image](https://github.com/user-attachments/assets/987327dd-58f6-48dd-9c13-1dca1754d993)



![image](https://github.com/user-attachments/assets/d460eb26-072b-4ae6-b6c1-b8fa4048af6a)

![image](https://github.com/user-attachments/assets/e576cea4-a51b-4c6a-b70f-0d6578a12f33)

![image](https://github.com/user-attachments/assets/be725c37-47bf-4ae0-970e-c71cd6eba28d)



![image](https://github.com/user-attachments/assets/12f540ba-5479-4a64-a7e4-76858f305848)

![image](https://github.com/user-attachments/assets/02c13a1b-c41d-4512-81ae-22bbdc33d40a)



![image](https://github.com/user-attachments/assets/568cf800-28d9-4544-87d5-1817b4f43c5b)

![image](https://github.com/user-attachments/assets/7d14ca9f-503e-4092-851b-b56f31b6169f)



![image](https://github.com/user-attachments/assets/abe39511-f7cf-4742-99e9-7c42fd07fb30)

![image](https://github.com/user-attachments/assets/128f507f-b34d-450e-9b4c-7ca793013b07)



![image](https://github.com/user-attachments/assets/77925230-86aa-48a4-9bca-17dcedbd19de)

![image](https://github.com/user-attachments/assets/3917b7bc-6e5d-41f2-937d-23dec5e4cbd1)



![image](https://github.com/user-attachments/assets/afe99142-21c4-4a8e-aff9-22628a346576)

![image](https://github.com/user-attachments/assets/7043f0ba-b9c7-4cfc-9c51-149d902b9249)

![image](https://github.com/user-attachments/assets/d6305188-2705-4afa-ac2a-fc7a926171db)

![image](https://github.com/user-attachments/assets/149181f2-6c5c-4921-b96b-e9eb830b4a89)



## Queries

Query 1: 
Query: Return the senior doctor(s) with the highest amount of subordinate doctors

Why? This query is useful to determine which senior doctors carry the heaviest workload in the supervision of subordinate doctors. A hospital may want to run this query and determine
this information for a number of reasons such as determining which senior doctors are the strongest leaders or to try to create even distribution of subordinates to senior doctors. 
![image](https://github.com/user-attachments/assets/7990fce9-28c4-47a8-a190-fe4734712a5a)

Query 2:
Query: Show how many appointments each doctor had per year

Why?: A hospital with this database would want to run this query mainly as a measure of productivity, as it can demonstrate which doctors are doing the most work and are managing their time
most effectively. In addition, a hospital may waant to be able to use this query to determine which doctors the patients have the most demand for. Overall, determining how many appointments 
each specific doctor had per year would be vital to a hospital determining where their resources should be allocated.

![image](https://github.com/user-attachments/assets/2e274af7-6078-43bf-aede-fbaa87e20903)

Query 3:
Query: View with limited patient and billing info

Why?: Creating a view of this nature would allow a finance team in the hospital to work on data involving how much money they are still expecting to recieve.
Creating a view with limited patient information will ensure that access to sensitive personal patient information like name and SSN are restricted only to those that need it. This will ensure the hospital is 
complying with privacy regulations while also maintaining productivity for those that need this information.

![image](https://github.com/user-attachments/assets/1e2b583d-d751-4b2b-a6cb-aaa82cd09183)

![image](https://github.com/user-attachments/assets/b5b2bdf2-1bcc-4f00-b2f1-a2dfd5f6a33b)

![image](https://github.com/user-attachments/assets/206d729e-c2c4-460c-9aa8-ce8a81ac36f7)

![image](https://github.com/user-attachments/assets/69bf8889-fbcf-4c2d-a649-c86080845749)

![image](https://github.com/user-attachments/assets/b9ae6e2d-3276-458d-87e5-0a4a76a94938)

Query 4:
Query: Shows financial and appointment info for any given doctor after inputting first and last name

Why?: A query of this nature would be useful in order to assess doctor productivity on an individual level. A hospital may want this for a number of reasons such as being able to benchmark performance between
doctors for promotions by seeing the financial value added by a given doctor. In addition, a query of this nature could help the hospital ensure that resources are being allocated to the right doctors in the right
departments, such as additional nurses or equipment that is being purchased. 

![image](https://github.com/user-attachments/assets/ca737d96-e58c-4afe-a40a-599e72aa966d)

![image](https://github.com/user-attachments/assets/2582bb8f-827f-4a0d-a2f4-b9f3b69cf241)

![image](https://github.com/user-attachments/assets/ead0ac73-6eb2-406d-bcf0-4583a8be39a3)

![image](https://github.com/user-attachments/assets/e7b12897-bff9-44fb-a7e9-57fab19fc546)

Query 5: Provide a list of patients have have recieved a prescription but have not been billed because they do not have an insurance provider on file

Why?: This query would be useful to the hospital by being able to address potential gaps in revenue they can follow up on. It would be a mechanism for the hospital to check with compliance issues and to identify gaps 
in the billing data. 

<img width="637" alt="Screenshot 2024-12-03 at 3 43 11 PM" src="https://github.com/user-attachments/assets/b93ea8de-586a-48df-9c11-bee0ee9f54af">
<img width="469" alt="Screenshot 2024-12-03 at 3 43 38 PM" src="https://github.com/user-attachments/assets/aabbffa3-ad03-4c98-b5f8-ff2b0a5bd874">

## Visualizations

<img width="804" alt="image" src="https://github.com/user-attachments/assets/5e20648a-ac64-47cf-9656-b01dc455e868">

### Nurses and Patients per Ward
- This chart shows the number of nurses and patients assigned to each ward, which provides insight into the hospital's nurse to patient ratios. It helps the hospital ensure that each ward has adequate staffing, which improves patient care and efficiency.

### Appointments and Revenue by Year
- This time series compares the number of appointments to total revenue over the years, which reveals trends in hospital activity and financial performance. It is very important for identifying times of high demand and evaluating how effectively revenue aligns with appointment volume.

### Lab Tests and Results
- This bar chart breaks down the number of lab tests conducted for each test type and their results, showing trends in diagnostics. This is very beneficial in tracking abnormalities and identifying which tests are the most common.

## Database Info
Database name: cs_jac29684

Queries 1,2,4,5 can be called using CALL Team5_Qx() where x is the query number<br/>

Query 2 requires a year as input and query 4 requires first and last name

Since Query 3 is a view, it can be called using select * from patientFinancialInfo
