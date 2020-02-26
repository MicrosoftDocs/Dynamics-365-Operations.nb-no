## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Produktkategoritilordninger til msdyn_productcategoryassignments

Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.

Finance and Operations-felt | Tilordningstype | Annet Dynamics 365-felt | Standardverdi
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
