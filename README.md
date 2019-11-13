# Azure Wars
## THE DATA LAKE STRIKES BACK

### Excersice

#### Goal: Setup a Data Management Platform

Start:
  -	An Azure Resource Group for the Data Management Platform 
  -	An Azure Resource Group for the US BI department 
  -	An Azure Resource Group for the AsiaPacific ML department
  
Requirements:
 -	The files on the Azure Data Lake store has to be time partitioned
 -	The US BI department isn’t allowed to look into the AsiaPacific data, and the other way around
 
 #### Prep Guide:
1.	Create three resource groups, and name them what you want. Keep in mind, it has to be clear which of them is the Data Management         Platform resource group
2.	Within the Data Management Platform resource group, add the following components and give them appropriate names:
a.	Azure Data Lake Storage, for example: ADLS-DMAP 
b.	Azure Data Factory V2, for example: ADF-DMAP
c.	Storage account, for example: STA-DMAP
3.	Within the department resource groups, add the following components:
  a.	Azure Data Factory V2, for example: ADF-USBI / ADF-APML
  b.	SQL Server Database, for example: SSR- USBI / SSR-APML

 #### DMAP Guide:
1.	Within the storage account, create a container. 
2.	Put the files in the DMAP Storage account container.
3.	Create the target folders on the Data Lake
4.	Make an Azure Data Factory pipeline to move the files from Storage Account to the Azure Data Lake Storage.  
5.	Run the pipeline to move the files 

 #### Department Guide:
1.	Connect with the appropriate component to the DMAP Data Lake, where the files reside 
2.	Move the files from the DMAP Data Lake to your own apartment 
3.	Query the data 
4.	Optional: Visualize the data in PowerBI? 
