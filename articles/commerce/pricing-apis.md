---
title: API-er for Commerce-priser
description: Denne artikkelen beskriver forskjellige pris-API-er som tilbys av Microsoft Dynamics 365 Commerce-prissettingsmotoren.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294121"
---
# <a name="commerce-pricing-apis"></a>API-er for Commerce-priser

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver forskjellige pris-API-er som tilbys av Microsoft Dynamics 365 Commerce-prissettingsmotoren.

Dynamics 365 Commerce-prissettingsmotoren gir følgende API-er for Retail Server som kan brukes av eksterne programmer for å støtte ulike prissettingsscenarioer:

- **GetActivePrices** – Denne API-en får den beregnede prisen for et produkt, inkludert enkle rabatter.
- **CalculateSalesDocument** – Denne API-en beregner priser og rabatter for produkter til gitte antall hvis de kjøpes sammen.
- **GetAvailablePromotions** – Denne API-en får gjeldende rabatter for produkter i handlekurven. 
- **AddCoupons** – Denne API-en legger til kuponger i en handlekurv.
- **RemoveCoupons** – Denne API fjerner kuponger fra en handlekurv.

Hvis du vil ha mer informasjon om hvordan du forbruker Retail Server-API-er i eksterne programmer, kan du se [Bruk Retail Server-API-er i eksterne programmer](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

API-en *GetActivePrices* ble lansert i Commerce-versjonen 10.0.4. Denne API-en får den beregnede prisen for et produkt, inkludert enkle rabatter. Den beregner ikke rabatter med flere linjer, og det forutsetter at hvert produkt i en API-forespørsel har et antall på 1. Denne API-en kan også ta en liste over produkter som inndata og spørre på prisen på enkeltprodukter samlet.

API-en *GetActivePrices* støtter Commerce-rollene **ansatt**, **kunde**, **anonym** og **program**.

Hovedbrukstilfellet for API-en *GetActivePrices* er siden med produktdetaljer (PDP) der forhandlere ønsker å gi et produkt den beste prisen, inkludert eventuelle effektive rabatter.

Følgende tabell viser inndataparameterne for API-en *GetActivePrices*.

| Navn                                    | Undernavn | Type | Obligatorisk/valgfri | Beskrivelse |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Obligatorisk | |
|                                         | ChannelId | lang | Obligatorisk | |
|                                         | CatalogId | lang | Obligatorisk | |
| productIds                              | | IEnumerable\<long\> | Obligatorisk | Listen over produkter det skal beregnes priser for. |
| activeDate                              | | DateTimeOffset | Obligatorisk | Datoen når prisene beregnes. |
| customerId                              | | streng | Valgfri | Kundekontonummeret. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Valgfri | Tilknytnings- og fordelslag. |
|                                         | AffiliationId | lang | Obligatorisk | Tilknytnings-ID-en. |
|                                         | LoyaltyTierId | lang | Valgfri | Fordelslag-ID-en. |
| includeSimpleDiscountsInContextualPrice | | bool | Valgfri | Angi denne parameteren til **true** slik at den skal inkludere enkle rabatter i prissettingsberegningen. Standardverdien er **usann**. |
| includeVariantPriceRange                | | bool | Valgfri | Sett denne parameteren til **sann** for å få minimums- og maksimumsprisene blant alle varianter for et hovedprodukt. Standardverdien er **usann**. |
| includeAttainablePricesAndDiscounts     | | bool | Valgfri | Sett denne parameteren til **sann** for å oppnå priser og rabatter. Standardverdien er **usann**. |

**Eksempelforespørselstekst**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Eksempelsvartekst**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

API-en *CalculateSalesDocument* ble lansert i Commerce-versjonen 10.0.25. Denne API-en beregner priser og rabatter for produkter til gitte antall hvis de kjøpes sammen i en bestilling. Prissettingsberegningen bak API-en *CalculateSalesDocument* vurderer både enkeltlinjerabatter og flerlinjerabatter.

Det viktigste bruksmåten for API-en *CalculateSalesDocument* er prissettingsberegningen i scenarioer der hele handlekurvkonteksten ikke fastholdes (for eksempel salgstilbud). Scenarioer i salgsstedet og Commerce-netthandel kan også dra nytte av denne bruken. En lavere totalpris når handlekurvvarer beregnes som et sett (for eksempel atskilte grupper, koblede eller anbefalte produkter eller produkter som allerede er lagt til i handlekurven), kan overtale kunder til å legge til produkter i handlekurven.

Datamodellen for både forespørselen og svaret på API-en *CalculateSalesDocument* er **Handlekurv**. I denne API-en kalles imidlertid datamodellen **SalesDocument**. Fordi de fleste egenskapene er valgfrie, og bare noen få påvirker prissettingsberegningen, vises bare prissettingsrelaterte felter i tabellen nedenfor. Vi anbefaler ikke at noen andre felter er involvert i API-forespørselen.

Området for API-en *CalculateSalesDocument* er bare beregningen av priser og rabatter. Avgifter og gebyrer er ikke involvert.

Følgende tabell viser inndataparameterne i objektet som kalles **salesDocument**.

| Navn             | Undernavn | Type | Obligatorisk/valgfri | Beskrivelse |
|------------------|----------|------|-------------------|-------------|
| ID               | | streng | Obligatorisk | Identifikatoren for salgsdokumentet. |
| CartLines        | | IList\<CartLine\> | Valgfri | Listen over linjer det skal beregnes priser og rabatter for. |
|                  | Produkt-ID | lang | Obligatorisk i området for CartLine | Post-ID for produktet. |
|                  | ItemId | streng | Valgfri | Vareidentifikatoren. Hvis det angis en verdi, må den samsvare med verdien for **ProductId**-parameteren. |
|                  | InventoryDimensionId | streng | Valgfri | Identifikatoren for lagerdimensjonen. Hvis det angis en verdi, må kombinasjonen av verdiene **ItemId** og **InventoryDimensionId** samsvare med verdien for **ProductId**-parameteren. |
|                  | Antall | desimal | Obligatorisk i området for CartLine | Antallet for produktet. |
|                  | UnitOfMeasureSymbol | streng | Valgfri | Enheten for produktet. Hvis det ikke er oppgitt en verdiforsyning, bruker API-en som standard salgsenheten for produktet. |
| CustomerId       | | streng | Valgfri | Kundekontonummeret. |
| LoyaltyCardId    | | streng | Valgfri | Identifikatoren for fordelskortet. Alle kundekontoer som er knyttet til fordelskortet , må samsvare med verdien i **CustomerId**-parameteren (hvis den finnes). Det tas ikke hensyn til fordelskortet hvis statusen er **blokkert**. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Valgfri | Tilknytningslinjer for fordelskort. Hvis det finnes verdier for **CustomerId** eller **LoyaltyCardId**, vil de tilsvarende fordelslagslinjene i ansettelsesforholdet bli flettet med linjer som finnes i **AffiliationLines**-verdien. |
|                  | AffiliationId | lang | Obligatorisk i området for AffiliationLoyaltyTier | Tilknytningspost-ID-en. |
|                  | LoyaltyTierId | lang | Obligatorisk i området for AffiliationLoyaltyTier | Fordelslagspost-ID-en. |
|                  | AffiliationTypeValue | int | Obligatorisk i området for AffiliationLoyaltyTier | En verdi som angir om ansettelseslinjen er av typen **Generelt** (**0**)eller **Fordelstype** (**1**). Hvis denne parameteren er satt til **0**, tar API verdien for **AffiliationId** som identifikator, og ignorerer **LoyaltyTierId**-verdien. Hvis den er satt til **1**, tar API verdien for **LoyaltyTierId** som identifikator, og ignorerer **AffiliationId**-verdien. |
|                  | ReasonCodeLines | Kolleksjon\<ReasonCodeLine\> | Obligatorisk i området for AffiliationLoyaltyTier | Årsakskodelinjer. Denne parameteren har ingen innvirkning på prissettingsberegningen, men er nødvendig som en del av objektet **AffiliationLoyaltyTier**. |
|                  | CustomerId | streng | Obligatorisk i området for AffiliationLoyaltyTier | Kundekontonummeret. |
| Kuponger          | | IList\<Coupon\> | Valgfri | Kuponger som ikke gjelder (inaktiv, utløpt eller ikke funnet) blir ikke tatt hensyn til i prissettingsberegningen. |
|                  | Kode | streng | Obligatorisk i området for kupong | Kupongkoden. |
|                  | CodeId | streng | Valgfri | Kupongkodeidentifikatoren. Hvis det angis en verdi, må den samsvare med verdien for **Code**-parameteren. |
|                  | DiscountOfferId | streng | Valgfri | Rabattidentifikatoren. Hvis det angis en verdi, må den samsvare med verdien for **Code**-parameteren. |

**Eksempelforespørselstekst**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Hele handlekurvobjektet returneres som svartekst. Hvis du vil kontrollere priser og rabatter, bør du fokusere på feltene i følgende tabell.

| Navn           | Undernavn | Type | Beskrivelse |
|----------------|----------|------|--------------|
| NetPrice       | | desimal | Nettoprisen for hele salgsdokumentet før rabatter brukes. |
| DiscountAmount | | desimal | Totalt rabattbeløp for hele salgsdokumentet. |
| TotalAmount    | | desimal | Totalt beløp for hele salgsdokumentet. |
| CartLines      | | IList\<CartLine\> | Beregnede linjer som inneholder pris- og rabattdetaljer. |
|                | Pris | desimal | Enhetsprisen for produktet. |
|                | NetPrice | desimal | Nettoprisen for linjen før rabatter brukes (= *Pris* &times; *Antall*). |
|                | DiscountAmount | desimal | Rabattbeløpet. |
|                | TotalAmount | desimal | Det endelige totale prissettingsresultatet for linjen. |
|                | PriceLines | IList\<PriceLine\> | Prisdetaljer, inkludert kilden til prisen (basispris, prisjustering eller handelsavtale) og beløpet. |
|                | DiscountLines | IList\<DiscountLine\> | Rabattdetaljer. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Gitt en handlekurv som har flere handlekurvlinjer, returnerer API-en *GetAvailablePromotions* alle gjeldende rabatter for handlekurvlinjene. 

Det viktigste bruks tilfellet for API-en *GetAvailablePromotions* er handlekurvsiden, der forhandlere ønsker å legge inn rabatter eller tilgjengelige kuponger for den gjeldende handlekurven.

Følgende tabell viser inndataparameterne for API-en *GetAvailablePromotions*.

| Navn        | Type | Obligatorisk/valgfri | Beskrivelse |
|-------------|------|-------------------|-------------|
| nøkkel         | streng | Obligatorisk | Handlekurv-ID-en. |
| cartLineIds | IEnumerable\<string\> | Valgfri | Angi denne parameteren for å returnere rabatter bare for valgte handlekurvlinjer. |

**Eksempelsvartekst**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

API-en *AddCoupons* støtter det å legge til en liste over kuponger i en handlekurv. Returnerer handlekurvobjektet etter at kupongene er lagt til.

Følgende tabell viser inndataparameterne for API-en *AddCoupons*.

| Navn                 | Type | Obligatorisk/valgfri | Beskrivelse |
|----------------------|------|-------------------|-------------|
| nøkkel                  | streng | Obligatorisk | Handlekurv-ID-en. |
| couponCodes          | IEnumerable\<string\> | Obligatorisk | Kupongkodene som skal legges til i handlekurven. |
| isLegacyDiscountCode | bool | Valgfri | Sett denne parameteren til **sann** for å angi at kupongen er en eldre rabattkode. Standardverdien er **usann**. |

## <a name="removecoupons"></a>RemoveCoupons

API-en *RemoveCoupons* støtter fjerning av en liste over kuponger fra en handlekurv. Returnerer handlekurvobjektet etter at kupongene er fjernet.

Følgende tabell viser inndataparameterne for API-en *RemoveCoupons*.

| Navn        | Type | Obligatorisk/valgfri | Beskrivelse |
|-------------|------|-------------------|-------------|
| nøkkel         | streng | Obligatorisk | Handlekurv-ID-en. |
| couponCodes | IEnumerable\<string\> | Obligatorisk | Kupongkodene som skal fjernes fra handlekurven. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
