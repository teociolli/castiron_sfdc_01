Updating the CDK connector with newer version connector . 

1)If version of connector is minimum three digits (for example. 1.0.1 ) skip step I and proceed directly to step II.
2)If version is less then digits (example 1.0) please first follow the steps in section I to update to to minimum three digits before moving to step II.


I .Update the project connector version to minimum three digits to be able to cleanly updated connector in project :

	NOTE : Make sure to backup the project before making any changes .
	1) Close the Studio .
	1) Go to folder where the project is located on disk .
	2) Inside the project folder find the ".connectors/<connector>" folder 
	3) Under that folder find and open the <connector>-config.xml file and update the version from two digits to minimum three digits . 
	  example:
	    <con:connectorConfiguration xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	      xsi:schemaLocation="http://www.approuter.com/schemas/cdk/config/ ci-connector-config.xsd"
	      xmlns:con="http://www.approuter.com/schemas/cdk/config/"
	      category="CRM"
	      name="ForceBulkAPIConnector"
	      label="Force.com Bulk API"
	      version="1.0"  <--- update this version to version="1.0.0" 
	      ....
	      ....

	   this should now look like 
	    <con:connectorConfiguration xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	      xsi:schemaLocation="http://www.approuter.com/schemas/cdk/config/ ci-connector-config.xsd"
	      xmlns:con="http://www.approuter.com/schemas/cdk/config/"
	      category="CRM"
	      name="ForceBulkAPIConnector"
	      label="Force.com Bulk API"
	      version="1.0.0"   <-- updated three digit version . 
	      .....
	      ....
      	  4) Repeat this steps for all the connectors used by project .
      	  5) Save the file and proceed to Step II .

II .Updating the CDK connector version( Connector version minimum three digits (for example. 1.0.1 ) ):

	1) Close all the projects in Studio  . 
	2) From top menu select Solutions->Plugin Connectors ->Choose "Installed" connectors tab. 
	3) Select the connector and install the connector first . 
	4) Now  restart the Studio .
	5) Again From top menu select Solutions->Plugin Connectors ->Choose "Available" connectors tab. 
	6) Choose and install the connector . 
	7) Now open your project . The Studio must prompt a dialogue asking to update the project with  new version of avaliable connector.
	8) Select update the project . 



   
   
   