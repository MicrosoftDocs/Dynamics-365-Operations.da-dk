## <a name="cds-contacts-v2-to-contacts"></a>CDS kontakter V2 til kontakter

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Common Data Service.

Kildefilter: (AssociatedContactType = 1)

Tilbageført kildefilter: msdyn_contactforvendor eq true og msdyn_sellable eq false og msdyn_contactpersonid ne ''

Finance and Operations-felt | Tilknytningstype | Andet Dynamics 365-felt | Standardværdi
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | ingen | Leverandør
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | afdeling | 
KOMMENTARER | = | beskrivelse | 
KØN | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
ingen | >> | msdyn_contactforvendor | Sand
CONTACTPERSONID | = | msdyn_contactpersonid | 
