---
title: Separert programiverksettingspakke med dobbel skriving
description: Pakke for programiverksetting for dobbel skriving er ikke lenger en enkeltpakke, men er delt inn i mindre pakker. Denne artikkelen beskriver løsninger og kart som hver pakke inneholder, og avhengigheten til andre pakker.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 504939f1f98c18005c092cabc1d040b420402c93
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874819"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Separert programiverksettingspakke med dobbel skriving

[!include [banner](../../includes/banner.md)]



Tidligere var pakken for programiverksetting for dobbel skriving var en enkelt pakke som inneholder følgende løsninger:

- Dynamics 365 Notes
- Dynamics 365 Finance and Operations-fellesanker
- Enhetstilordninger for dobbel skriving for Dynamics 365 Finance and Operations
- Aktivabehandlingsappen for Dynamics 365
- Aktivabehandling for Dynamics 365
- HCM Felles
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations-felles
- Dynamics 365 Company
- Valutakurser
- Field Service Common

Fordi det var en enkelt pakke, opprettet denne pakken en alt eller ingenting-situasjon for kunder. Microsoft har imidlertid nå delt det inn i mindre pakker. Derfor kan kunder bare velge pakkene for løsningene de trenger. Hvis du for eksempel er Microsoft Dynamics 365 Supply Chain Management-kunde og ikke krever integrering med Dynamics 365 Human Resources, notater og aktivabehandling, kan du utelate disse løsningene fra løsningene som er installert. Fordi de underliggende løsningsnavnene, publiserings- og kartversjonene forblir like, er denne endringen ikke-brytende. Eksisterende installasjoner oppgraderes.

![Separat pakke.](media/separated-package-1.png)

Denne artikkelen beskriver løsninger og kart som hver pakke inneholder, og avhengigheten til andre pakker.

## <a name="dual-write-application-core"></a>Programkjerne for dobbel skriving

Med programkjernepakken for dobbel skriving kan brukere installere og konfigurere dobbel skriving uten kundeengasjementsapper. Det inneholder følgende fem løsninger:

| Unikt navn                           | Vis navn                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations-felles |
| CurrencyExchangeRates                 | Valutakurser                    |
| msdyn_DualWriteAppCoreMaps            | Enhetstilordninger for programkjerne for dobbel skriving   |
| msdyn_DualWriteAppCoreAnchor          | Programkjerneanker for dobbel skriving        |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper     | Kundeengasjementsapper                    |
|---------------------------------|---------------------------------------------|
| Driftsenhet                  | msdyn_internalorganizations                 |
| Organisasjonshierarki          | msdyn_internalorganizationhierarchies       |
| Juridiske enheter                  | msdyn_internalorganizations                 |
| Juridiske enheter                  | cdm_companies                               |
| Formål for organisasjonshierarki | msdyn_internalorganizationhierarchypurposes |
| Valutapar for valutakurs     | msdyn_currencyexchangeratepairs             |
| Navnevedlegg                    | msdyn_nameaffixes                           |
| Valutakurstype              | msdyn_exchangeratetypes                     |
| Valutakurser for CDS              | msdyn_currencyexchangerates                 |
| Type organisasjonshierarki     | msdyn_internalorganizationhierarchytypes    |
| Valutaer                      | transactioncurrencies                       |
| Veiledningsenhet for blandet virkelighet     | msmrw_guides                                |

**Avhengighetsinformasjon**

Programkjernepakken for dobbel skriving har ingen avhengighet for andre pakker.

## <a name="dual-write-human-resources"></a>Human Resources for dobbel skriving

Human Resources-pakke for dobbel skriving inneholder løsningene og kartene som kreves for å synkronisere Human Resources-dataene. Det inneholder følgende tre løsninger:

| Unikt navn                | Vis navn                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM Felles                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources-enhetstilordninger |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources-anker      |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper | Kundeengasjementsapper         |
|-----------------------------|----------------------------------|
| Etnisk opprinnelse              | cdm_ethnicorigins                |
| Kompensasjon, jobbfunksjon   | cdm_jobfunctions                 |
| Stillinger V2                | cdm_jobpositions                 |
| Jobber                        | cdm_jobs                         |
| Kompensasjon, jobbtype       | cdm_jobtypes                     |
| Språkkoder              | cdm_languages                    |
| Stillingstype               | cdm_positiontypes                |
| Arbeidertilordninger for stilling | cdm_positionworkerassignmentmaps |
| Veteranstatus              | cdm_veteranstatuses              |
| Worker                      | cdm_workers                      |
| Ansettelse per firma      | cdm_employments                  |

**Avhengighetsinformasjon**

Pakke for Human Resources for dobbel skriving er avhengig av programkjernepakken for dobbel skriving. Derfor bør du installere programkjernepakken for dobbel skriving før du installerer Human Resources-pakken for dobbel skriving.

## <a name="dual-write-supply-chain"></a>Forsyningskjede for dobbel skriving

Forsyningskjedepakke for dobbel skriving inneholder løsningene og kartene som kreves for å synkronisere Supply Chain Management-dataene. Det inneholder følgende tre løsninger:

| Unikt navn                                | Vis navn                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Utvidede enhetstilordninger for Dynamics 365 Supply Chain Management |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Utvidet anker for Dynamics 365 Supply Chain Management      |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper                 | Kundeengasjementsapper                      |
|---------------------------------------------|-----------------------------------------------|
| Enheter                                       | uoms                                          |
| CDS-salgsordrehoder                     | salesorders                                   |
| CDS-salgsordrelinjer                       | salesorderdetails                             |
| CDS-salgstilbudshode                  | tilbud                                        |
| CDS-salgstilbudslinjer                   | quotedetails                                  |
| Frigitte spesifikke produkter for CDS              | produkter                                      |
| Lagersoner                             | msdyn_warehousezones                          |
| Lagersonegrupper                       | msdyn_warehousezonegroups                     |
| Arbeidslinjer for lager                        | msdyn_warehouseworklines                      |
| Arbeidshoder for lager                      | msdyn_warehouseworkheaders                    |
| Lagre                                  | msdyn_warehouses                              |
| Lagergang                             | msdyn_warehouseaisles                         |
| Enhetsomregninger                            | msdyn_unitofmeasureconversions                |
| Leveringsbetingelser                           | msdyn_termsofdeliveries                       |
| Leveringsmåter                           | msdyn_shipvias                                |
| Produktstandardstiler                       | msdyn_sharedproductstyles                     |
| Salgsfakturalinjer V2                      | invoicedetails                                |
| Salgsfakturahoder V2                    | fakturaer                                      |
| Produktstandardstørrelser                        | msdyn_sharedproductsizes                      |
| Frigitte produkter V2                        | msdyn_sharedproductdetails                    |
| Produktstandardkonfigurasjoner               | msdyn_sharedproductconfigurations             |
| Produktstandardfarger                       | msdyn_sharedproductcolors                     |
| Koder for salgsordregrunnlag                    | msdyn_salesorderorigins                       |
| Mottaksseddelhode                      | msdyn_purchaseorderreceipts                   |
| Mottaksseddellinje                        | msdyn_purchaseorderreceiptproducts            |
| Bestillingshoder V2                   | msdyn_purchaseorders                          |
| Myk sletting av enhet for CDS-bestillingslinje | msdyn_purchaseorderproducts                   |
| Bestillingslinjeenhet for CDS              | msdyn_purchaseorderproducts                   |
| Sporingsdimensjonsgrupper                   | msdyn_producttrackingdimensiongroups          |
| Stiler                                      | msdyn_productstyles                           |
| Lagringsdimensjonsgrupper                    | msdyn_productstoragedimensiongroups           |
| Produktspesifikke enhetsomregninger           | msdyn_productspecificunitofmeasureconversions |
| Innstillinger for produktstandardordre V2           | msdyn_productspecificdefaultordersettings     |
| Størrelser                                       | msdyn_productsizes                            |
| Produktdimensjonsgrupper                    | msdyn_productdimensiongroups                  |
| Standard ordreinnstillinger                      | msdyn_productdefaultordersettings             |
| Konfigurasjoner                              | msdyn_productconfigurations                   |
| Alle produkter                                | msdyn_globalproducts                          |
| Farger                                      | msdyn_productcolors                           |
| Roller for produktkategorihierarki            | msdyn_productcategoryhierarchyroles           |
| Produktkategorihierarkier                | msdyn_productcategoryhierarchies              |
| Produktkategoritilordninger                | msdyn_productcategoryassignments              |
| Produktkategorier                          | msdyn_productcategories                       |
| Lagerlokasjoner                         | msdyn_inventorylocations                      |
| CDS-beholdning på                            | msdyn_inventoryonhandentries                  |
| Produktkategorier                          | msdyn_productcategories                       |
| CDS-beholdning på                            | msdyn_inventoryonhandrequests                 |
| Strekkode identifisert med produktnummer           | msdyn_productbarcodes                         |
| Fordelskort                                | msdyn_loyaltycards                            |
| Fordelspoeng                       | msdyn_loyaltyrewardpoints                     |
| Priskundegrupper                       | msdyn_pricecustomergroups                     |
| Siter                                       | msdyn_operationalsites                        |
| CDS-salgstilbudslinjer                   | quotedetails                                  |
| CDS-salgsordrelinjer                       | salesorderdetails                             |

**Avhengighetsinformasjon**

Forsyningskjedepakken for dobbel skriving kan være avhengig av følgende tre pakker. Derfor bør du installere disse pakkene før du installerer forsyningskjedepakken for dobbel skriving.

- Programkjernepakke for dobbel skriving
- Finanspakke for dobbel skriving
- Human Resources-pakke for dobbel skriving

## <a name="dual-write-finance"></a>Finans for dobbel skriving

Finanspakke for dobbel skriving inneholder løsningene og tilordningene som kreves for å synkronisere Dynamics 365 Finance-dataene. Det inneholder følgende fire løsninger:

| Unikt navn                            | Vis navn                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance-utvidede enhetstilordninger |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance-utvidet anker      |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper             | Kundeengasjementsapper        |
|-----------------------------------------|---------------------------------|
| Kildeskattgrupper                  | msdyn_withholdingtaxgroups      |
| CDS-kontakter V2 (kunde)              | kontakter                        |
| CDS-kontakter V2 (leverandør)                | kontakter                        |
| Kunder V3                            | kontakter                        |
| Kildeskattkoder                   | msdyn_withholdingtaxcodes       |
| Leverandører V2                              | msdyn_vendors                   |
| Betalingsmåte for leverandør                   | msdyn_vendorpaymentmethods      |
| Leverandørgrupper                           | msdyn_vendorgroups              |
| Kontoplan                       | msdyn_chartofaccountses         |
| Finansposteringsgrupper for mva V2      | msdyn_taxpostinggroups          |
| Varens mva-gruppe                    | msdyn_taxitemgroups             |
| Mva-grupper                        | msdyn_taxgroups                 |
| Enhet for mva-fritakskoder for CDS        | msdyn_taxexemptcodes            |
| Kundegrupper                         | msdyn_customergroups            |
| Kundebetalingsmåte                 | msdyn_customerpaymentmethods    |
| Finansdimensjoner                    | msdyn_dimensionattributes       |
| Skattemyndigheter                   | msdyn_taxauthorities            |
| Format for finansdimensjon              | msdyn_financialdimensionformats |
| Økonomisk kalenderperiode                  | msdyn_fiscalcalendarperiods     |
| Enhet for integrering av regnskapskalender      | msdyn_fiscalcalendars           |
| Enhet for årsintegrering av regnskapskalender | msdyn_fiscalcalendaryears       |
| Betalingsbetingelser                        | msdyn_paymentterms              |
| Betalingsplan                        | msdyn_paymentschedules          |
| Linjer i betalingsplan                  | msdyn_paymentschedulelines      |
| Betalingsdager, CDS                        | msdyn_paymentdays               |
| Betalingsdagslinjer, CDS V2                | msdyn_paymentdaylines           |
| Hovedkonto                            | msdyn_mainaccounts              |
| Hovedkontokategorier                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Kunder V3                            | kontoer                        |

**Avhengighetsinformasjon**

Finanspakke for dobbel skriving er avhengig av programkjernepakken for dobbel skriving. Derfor bør du installere programkjernepakken for dobbel skriving før du installerer finanspakken for dobbel skriving.

## <a name="dual-write-notes"></a>Notater for dobbel skriving

Notatpakke for dobbel skriving inneholder løsningene og kartene som kreves for å synkronisere notat- eller merknadsdata. Det inneholder følgende fire løsninger:

| Unikt navn                  | Vis navn                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Utvidede notater for Dynamics 365    |
| msdyn_Dynamics365NotesMaps   | Enhetstilordninger for notater for Dynamics 365 |
| msdyn_Dynamics365NotesAnchor | Notatanker for Dynamics 365      |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Dokumentvedlegg for topptekst i salgsordre    | merknader         |
| Kundevedlegg                       | merknader         |
| Vedlegg for leverandørdokument                | merknader         |
| Dokumentvedlegg for topptekst i bestilling | merknader         |

**Avhengighetsinformasjon**

Notatpakken for dobbel skriving kan være avhengig av følgende to pakker. Derfor bør du installere disse pakkene før du installerer notatpakken for dobbel skriving.

- Programkjernepakke for dobbel skriving
- Finanspakke for dobbel skriving

## <a name="dual-write-asset-management"></a>Aktivabehandling for dobbel skriving

Aktivabehandlingspakke for dobbel skriving inneholder løsningene og kartene som kreves for å synkronisere aktivadata fra Supply Chain Management eller Dynamics 365 Field Service. Det inneholder følgende fire løsninger:

| Unikt navn                          | Vis navn                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Aktivabehandling for Dynamics 365             |
| Dynamics365AssetManagementApp        | Aktivabehandlingsapp for Dynamics365          |
| msdyn_DualWriteAssetManagementMaps   | Enhetstilordninger for aktivabehandling for Dynamics 365 |
| msdyn_DualWriteAssetManagementAnchor | Aktivabehandlingsanker for Dynamics 365      |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper                           | Kundeengasjementsapper                |
|-------------------------------------------------------|-----------------------------------------|
| Aktivabehandling, garanti                             | msdyn_warranties                        |
| Aktivabehandling, modeller                               | msdyn_models                            |
| Aktivabehandling, produsenter                        | msdyn_manufacturers                     |
| Aktivabehandling, arbeidsstedstyper            | msdyn_functionallocationtypes           |
| Aktivabehandling, arbeidssteder                 | msdyn_functionallocations               |
| Aktivabehandling, livsløpstilstander for arbeidssted | msdyn_functionallocationlifecyclestates |
| Aktivabehandling, livsløpsmodeller for arbeidssted | msdyn_functionallocationlifecyclemodels |
| Aktivabehandling, aktiva                               | msdyn_customerassets                    |
| Aktivabehandling, aktivatyper                          | msdyn_customerassetcategories           |
| Aktivabehandling, livsløpstilstander for aktiva               | msdyn_assetlifecyclestates              |
| Aktivabehandling, livsløpsmodeller for aktiva               | msdyn_assetlifecyclemodels              |

**Avhengighetsinformasjon**

Aktivabehandlingspakke for dobbel skriving er avhengig av programkjernepakken for dobbel skriving. Derfor bør du installere programkjernepakken for dobbel skriving før du installerer aktivabehandlingspakken for dobbel skriving.

## <a name="packages-required-for-project-operations"></a>Pakker som kreves for Project Operations
Project Operations avhenger av følgende pakker. Derfor bør du installere disse pakkene før du installerer Project Operations.

- Programkjernepakke for dobbel skriving
- Finanspakke for dobbel skriving
- Forsyningskjedepakke for dobbel skriving
- Aktivabehandlingspakke for dobbel skriving
- Human Resources-pakke for dobbel skriving

## <a name="dual-write-party-and-global-address-book-solutions"></a>Løsninger for part med dobbel skriving og global adressebok

Pakken med part med dobbel skriving og global adressebok inneholder følgende løsninger og tilordninger som kreves for å synkronisere data for part og for global adressebok. 

| Unikt navn                       | Visningsnavn                            |
|-----------------------------------|-----------------------------------------|
| Part                             | Part                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB Extended               |
| Dynamics365GABDualWriteEntityMaps | Enhetstilordninger for dobbel skriving for Dynamics 365 GAB |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB og part              |

Følgende kart er tilgjengelige i denne pakken:

| Finance and Operations-apper | Kundeengasjementsapper | 
|-----------------------------|--------------------------|
| CDS-parter | msdyn_parties | 
| Postadressesteder for CDS | msdyn_postaladdresscollections | 
| Historikk for CDS-postadresse V2 | msdyn_postaladdresses | 
| Postadressesteder for CDS-part | msdyn_partypostaladdresses | 
| Partskontakter V3 | msdyn_partyelectronicaddresses | 
| Kunder V3 | kontoer | 
| Kunder V3 | kontakter | 
| Leverandører V2 | msdyn_vendors | 
| Kontaktpersontitler | msdyn_salescontactpersontitles | 
| Avsluttende hilsener | msdyn_complimentaryclosings | 
| Hilsener | msdyn_salutations | 
| Roller for beslutningstaking | msdyn_decisionmakingroles | 
| Jobbfunksjoner for ansettelse | msdyn_employmentjobfunctions | 
| Fordelsnivåer | msdyn_loyaltylevels | 
| Typer personlige tegn | msdyn_personalcharactertypes | 
| Kontakter V2 | msdyn_contactforparties | 
| CDS-salgstilbudshode | tilbud | 
| CDS-salgsordrehoder | salesorders | 
| Salgsfakturahoder V2 | fakturaer | 
| CDS-adresseroller | msdyn_addressroles |

**Avhengighetsinformasjon**

Løsningene for part med dobbel skriving og global adressebok er avhengige av følgende tre pakker. Derfor bør du installere disse pakkene før du installerer pakken med løsninger for part med dobbel skriving og global adressebok.

- Programkjernepakke for dobbel skriving
- Finanspakke for dobbel skriving
- Forsyningskjedepakke for dobbel skriving
