## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Kildeskattkoder til msdyn_withholdingtaxcodes

Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.

Finance and Operations-felt | Tilordningstype | Annet Dynamics 365-felt | Standardverdi
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
