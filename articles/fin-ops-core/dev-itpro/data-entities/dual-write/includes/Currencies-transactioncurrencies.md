## <a name="currencies-to-transactioncurrencies"></a>Valutaer til transactioncurrencies

Denne malen synkroniserer data mellom Finance and Operations-apper og Common Data Service.

Kildefilter: ((CURRENCYCODE != "999"))

Finance and Operations-felt | Tilordningstype | Annet Dynamics 365-felt | Standardverdi
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
none | >> | exchangerate | 1
