## <a name="currencies-to-transactioncurrencies"></a>Valutaer til transactioncurrencies

Denne skabelon synkroniserer data mellem Finance and Operations-apps og Common Data Service.

Kildefilter: ((CURRENCYCODE != "999"))

Finance and Operations-felt | Tilknytningstype | Andet Dynamics 365-felt | Standardværdi
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAVN | = | currencyname | 
SYMBOL | = | currencysymbol | 
ingen | >> | exchangerate | 1
