## <a name="cds-contacts-v2-to-contacts"></a>CDS-kontakter V2 til kontakter

Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.

Kildefilter: (AssociatedContactType = 1)

Filter for reversert kilde: msdyn_contactforvendor eq true and msdyn_sellable eq false and msdyn_contactpersonid ne ''

Finance and Operations-felt | Tilordningstype | Annet Dynamics 365-felt | Standardverdi
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | none | Vendor
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
EMPLOYMENTDEPARTMENT | = | department | 
NOTES | = | description | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
none | >> | msdyn_contactforvendor | True
CONTACTPERSONID | = | msdyn_contactpersonid | 
