## <a name="exchange-rate-currency-pair-to-msdyn_currencyexchangeratepairs"></a>Valutapar for valutakurs til msdyn_currencyexchangeratepairs

Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.

Finance and Operations-felt | Tilordningstype | Annet Dynamics 365-felt | Standardverdi
---|---|---|---
EXCHANGERATEDISPLAYFACTOR | >< | msdyn_displayfactor | 
EXCHANGERATETYPENAME | = | msdyn_currencyexchangeratetypeid.msdyn_name | 
FROMCURRENCYCODE | = | msdyn_fromtransactioncurrencyid.isocurrencycode | 
TOCURRENCYCODE | = | msdyn_totransactioncurrencyid.isocurrencycode | 
