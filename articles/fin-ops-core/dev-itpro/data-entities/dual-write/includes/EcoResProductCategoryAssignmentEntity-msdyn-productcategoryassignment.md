## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Tildelinger af produktkategori til msdyn_productcategoryassignments

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Common Data Service.

Finance and Operations-felt | Tilknytningstype | Andet Dynamics 365-felt | Standardværdi
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
