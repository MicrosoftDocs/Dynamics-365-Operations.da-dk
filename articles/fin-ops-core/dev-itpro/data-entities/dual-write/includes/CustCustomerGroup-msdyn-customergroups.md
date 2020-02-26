## <a name="customer-groups-to-msdyn_customergroups"></a>Debitorgrupper til msdyn_customergroups

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Common Data Service.

Finance and Operations-felt | Tilknytningstype | Andet Dynamics 365-felt | Standardværdi
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
BESKRIVELSE | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 
