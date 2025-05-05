# Patient information .csv to .json converter

--
This application takes in a .csv file containing patient information, and converts it to json.

The .csv file is formatted to contain FirstName, LastName, DOB, EmailAddress, Address, SSN, PhoneNumber, InsuranceID, InsuranceCarrier, Symptoms, Diagnosis for each patient.

Example format for csv:
FirstName,LastName,DOB,EmailAddress,Address,SSN,PhoneNumber,InsuranceID,InsuranceCarrier,Symptoms,Diagnosis

Eric,Rose,1989-09-07,eric.rose97@coruscant.space,"954 Hanson Turnpike, Ericafort, VA 19735",710-37-0415,535.250.0117,INS-8990-8170,Aetna,Abdominal Pain; Runny Nose,COVID-19

The application takes .csv files from the inbound directory, and converts them to a JSON file. The JSON file is placed in the outbound directory, while the old .csv file is moved from the inbound directory to the processed directory.

JSON file output example:
{
"FirstName": "Eric",
"LastName": "Rose",
"DOB": "1989-09-07",
"EmailAddress": "eric.rose97@coruscant.space",
"Address": "954 Hanson Turnpike, Ericafort, VA 19735",
"SSN": "710-37-0415",
"PhoneNumber": "535.250.0117",
"InsuranceID": "INS-8990-8170",
"InsuranceCarrier": "Aetna",
"Symptoms": "Abdominal Pain; Runny Nose",
"Diagnosis": "COVID-19"
},

--
Node requirement: v22.15.0

--
Instructions:
"npm i" to get node modules
"docker compose up --build" to build to container
application runs at http://localhost:3000
