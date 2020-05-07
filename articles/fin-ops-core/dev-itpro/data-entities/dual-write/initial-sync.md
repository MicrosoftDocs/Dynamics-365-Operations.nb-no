---
title: Enhetsavhengighetskjede (synkroniseringsrekkefølge)
description: Dette emnet angir rekkefølgen for synkroniseringen du må følge for å opprette de opprinnelige dataene.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275493"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Enhetsavhengighetskjede (synkroniseringsrekkefølge)

[!include [banner](../../includes/banner.md)]

Dette emnet angir synkroniseringsrekkefølgen du må følge for å opprette de opprinnelige dataene hvis du ikke bruker enhetsavhengighetene som leveres av funksjonen **innledende synkronisering**. Hvis du ikke bruker **innledende synkronisering**, må du kjøre hver enhetstilordning hver for seg.

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management-enheter

Følgende enheter for Supply Chain Management er oppført i den rekkefølgen du skal aktivere dem.

| Tilordningsnavn på siden Dobbel skriving | Enhetsmetadatanavn i Supply Chain Management | Enhetsmetadatanavn i Common Data Service | Notater |
|---|---|---|---|
| Enheter ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Enhetskonverteringer ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Alle produkter ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Produktdimensjonsgrupper ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Lagringsdimensjonsgrupper ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Sporingsdimensjonsgrupper ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Farger ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Størrelser ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Stiler ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigurasjoner ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Frigitte produkter V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service-frigitte spesifikke produkter ... produkter                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | produkt                                      | |
| Strekkode for produktnummeridentifikasjon ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Standard ordreinnstillinger ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Innstillinger for produktstandardordre V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Produktspesifikke enhetskonverteringer ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Områder ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Lagre ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Se [merknad 1](#scm-notes). |
| Produktstandardfarger ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Produktstandardstørrelser ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Produktstandardstiler ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Produktstandardkonfigurasjoner ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Produktkategorier ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Se [merknad 2](#scm-notes). |
| Produktkategoritilordninger ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Produktkategorihierarkier ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Roller for produktkategorihierarki ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Lagergang ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Lagersoner ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Lagersonegrupper ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Lagerlokasjoner ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Se [merknad 3](#scm-notes). |
| Lagerarbeidshoder ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Lagerarbeidslinjer ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Se [merknad 4](#scm-notes). |
| Leveringsmåter ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Leveringsbetingelser ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Koder for salgsordregrunnlag ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service-salgsordrehoder ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service-salgsordrelinjer ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service-salgstilbudshode ... tilbud                               | SalesQuotationHeaderCommon Data ServiceEntity          | tilbud                                        | |
| Common Data Service-salgstilbudslinjer ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Salgsfakturahoder V2 ... fakturaer                                               | SalesInvoiceHeaderV2Entity                             | faktura                                      | |
| Salgsfakturalinjer V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Tilordningsspesifikke merknader

1. På grunn av selvavhengighet kan det hende at du må kjøre den innledende synkroniseringen to ganger.
2. Som standard er innledende synkronisering slått av på grunn av relasjonen overordnet/underordnet ("smart" bestilling håndteres ikke av plattformen). De eksisterende produktkategoriene må derfor synkroniseres manuelt (for eksempel ved å oppdatere beskrivelsen av kategorien) i riktig rekkefølge (rotkategori først, deretter underordnede, og deretter underordnede til underordnede). Gå til **Behandling av produktinformasjon \> Oppsett \> Kategorier og attributter \> Kategorihierarkier**. På **Kategorihierarkier**-siden kan du velge hvert hierarki og se produktkategoriene i det.
3. Tilordning av tomme **ItemNumberInLocation**-oppslagsfelt og de første, andre og tredje ekstra lagersonene vil føre til at innledende synkronisering mislykkes. Derfor er disse tilordningene fjernet for øyeblikket.
4. Tilordningen av det tomme **CaptureWeight**-feltet vil føre til at innledende synkronisering mislykkes. Derfor er denne tilordningen fjernet for øyeblikket.

### <a name="setup-related-information"></a>Oppsettsrelatert informasjon

+ Når poster opprettes for første gang i **Produkter**-enheten i modelldrevne apper i Dynamics 365, har de statusen **Utkast**. Hvis du vil endre statusen til **Aktiv**, går du til **Innstillinger \> Administrasjon \> Systeminnstillinger \> Salg** i den modelldrevne appen og setter alternativet **Opprett produkter i aktiv tilstand** til **Ja**.
+ Hvis du oppretter poster i **Produkter**-enheten i modelldrevne apper i Dynamics 365 eller i Common Data Service før du aktiverer dobbel skriving, blir disse postene bare oppdatert hvis hele nøkkelen, inkludert **Firma**, samsvarer med data i Finance and Operations-appen.
+ Synkronisering av **Produkter**-enheten er enveis, fra Finance and Operations-apper til Common Data Service. Hvis et tilordnet felt i **Produkter**-enheten i modelldrevne apper i Dynamics 365 oppdateres, vil oppdateringen bli overskrevet under neste synkronisering fra Finance and Operations-appen.

### <a name="known-issues"></a>Kjente problemer

- Det oppstår en feil når en enhet slettes i en Finance and Operations-app. Når måleenheter synkroniseres fra Finance and Operations-appen til Common Data Service, opprettes den første enheten for en bestemt klasse som primær enhet, og vil forhindre sletting.

    **Reduksjon:** Slett først enheten i Common Data Service. Den kan deretter slettes i Finance and Operations-appen.

- Det oppstår en feil når et driftssted slettes i Common Data Service. Feilmeldingen angir "Infologg: Advarsel: Primær adresse kan ikke slettes.; Advarsel: Enhetsposten kan ikke slettes fordi valideringen mislyktes for følgende datakilde: InventSiteLogisticsLocation (InventSiteLogisticsLocation)." Denne feilen skyldes et problem i dataenheten i Finance and Operations-appen.

    **Reduksjon:** Du kan slette området i Finance and Operations-appen. Området blir deretter slettet i Common Data Service hvis tilsvarende tilordning for dobbel skriving kjører.

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance-enheter

Følgende enheter for Dynamics 365 Finance er oppført i den rekkefølgen du skal aktivere dem.

| Tilordningsnavn på siden Dobbel skriving | Enhetsmetadatanavn i Finance | Enhetsmetadatanavn i Common Data Service | Notater |
|---|---|---|---|
| Valutaer ... transactioncurrencies                                            | CurrencyEntity                              | Valuta.                                   | |
| Valutakurstype ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Valutapar for valutakurs ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service-valutakurser ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Se [merknad 1](#fin-notes). |
| Integreringsenhet for regnskapskalender ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Integreringsenhet for regnskapskalenderår ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Regnskapskalenderperiode ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Type organisasjonshierarki ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Se [merknad 1](#fin-notes). |
| Formål for organisasjonshierarki ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Se [merknad 1](#fin-notes). |
| Juridiske enheter ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Se [merknad 1](#fin-notes). |
| Juridiske enheter ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Driftsenhet ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Se [merknad 1](#fin-notes). |
| Organisasjonshierarki – publisert ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Se [merknad 1](#fin-notes). |
| Navnevedlegg ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Common Data Service for betalingsdager ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Common Data Service for betalingsdagslinjer V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Betalingsplan ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Betalingsplanlinjer ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Betalingsbetingelser ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Kundebetalingsmåte ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Leverandørbetalingsmåte ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Kundegrupper ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Leverandørgrupper ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Mva-grupper ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Varens mva-grupper ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Finansposteringsgrupper for mva V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Mva-fritakskode for Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Skattemyndigheter ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Mva-kode ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Se [merknad 1](#fin-notes). |
| Finansdimensjonsformat ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finansdimensjoner ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Kildeskattgrupper ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Kildeskattkoder ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Kontoplan ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Finans ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Se [merknad 1](#fin-notes). |
| Hovedkontokategorier ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Hovedkonto ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Kunder V3 ... kontoer                                                       | CustCustomerV3Entity                        | konto                                    | Se [merknad 2](#fin-notes). |
| Kunder V3 ... kontakter                                                       | CustCustomerV3Entity                        | kontakte                                    | Se [merknad 3](#fin-notes). |
| Leverandører V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Se [merknad 2](#fin-notes). |
| Common Data Service-kontakter V2 ... kontakter                                    | smmContactPersonCommon Data ServiceV2Entity | kontakte                                    | Se [merknad 4](#fin-notes). |
| Common Data Service-kontakter V2 ... kontakter                                    | smmContactPersonCommon Data ServiceV2Entity | kontakte                                    | Se [merknad 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Tilordningsspesifikke merknader

1. Enveis synkronisering skjer fra Finance and Operations-apper til Common Data Service.
2. På grunn av selvavhengighet kan det hende at du må kjøre den innledende synkroniseringen mer enn én gang. Pass på at du velger **Kunde** som relasjonstype når du oppretter en konto ved hjelp av **Kontoer**-siden i Common Data Service. Hvis det oppstår problemer med **Hovedkontakt**-feltet under den innledende synkroniseringen, fjerner du dette feltet fra tilordningen og kjører deretter den innledende synkroniseringen på nytt. Når den innledende synkroniseringen er fullført, stopper du tilordningen og legger til **Hovedkontakt**-feltet i den på nytt. Start deretter tilordningen, men hopp over den innledende synkroniseringen. Verdien i **Hovedkontakt**-feltet vil ikke bli inkludert i den innledende synkroniseringen, og du må manuelt overføre verdiene.
3. Pass på at du setter alternativet **Salgbar** til **Ja** på **Kontakter**-siden i Common Data Service når du prøver å opprette en kunde av typen **Person**.
4. Denne tilordningen har et filter på begge sider for å koble kundekontakter. Åpne tilordningsdetaljene, velg filterknappen (traktsymbolet) ved siden av **Sales.Contact**-enhetsnavnet, og kontroller at filterkriteriene inneholder **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Denne tilordningen har et filter på begge sider for å koble leverandørkontakter. Åpne tilordningsdetaljene, velg filterknappen (traktsymbolet) ved siden av **Sales.Contact**-enhetsnavnet, og kontroller at filterkriteriene inneholder **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources-enheter

Følgende enheter for Dynamics 365 Human Resources er oppført i den rekkefølgen du skal aktivere dem.

| Tilordningsnavn på siden Dobbel skriving | Enhetsmetadatanavn i Human Resources | Enhetsmetadatanavn i Common Data Service | Notater |
|---|---|---|---|
| cdm_jobfunction - Jobbfunksjon                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Jobbtyper                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Jobber                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Jobbdetaljer                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Basisstilling                              | HcmPositionBaseEntity             | cdm_jobposition                  | Se [merknad 1](#hr-notes). |
| cdm_jobposition - Stillingsdetaljer                            | HcmPositionDetailEntity           | cdm_jobposition                  | Se [merknad 1](#hr-notes). |
| cdm_jobposition - Stillingsvarighet                           | HcmPositionDurationEntity         | cdm_jobposition                  | Se [merknad 1](#hr-notes). |
| cdm_jobposition - Stillingshierarkier                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Se [merknad 1](#hr-notes). |
| cdm_veteranstatus - Veteranstatus                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Etnisk opprinnelse                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Språkkode                              |                                   | cdm_languagecode                 | |
| cdm_worker - Arbeider                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Ansettelser                                 |                                   | cdm_employments                  | |
| cdm_employments - Ansettelsesdetalj                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Stillingstilordning | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Se [merknad 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Tilordningsspesifikke merknader

1. Én Common Data Service-enhet tilordnes til flere Finance and Operations-appenheter.
2. Denne tilordningen har en selvreferanse.

## <a name="asset-management-entities"></a>Enheter for aktivumbehandling

Følgende enheter for aktivumbehandling for Dynamics 365 Supply Chain Management er oppført i den rekkefølgen du skal aktivere dem.

| Tilordningsnavn på siden Dobbel skriving | Enhetsmetadatanavn i Aktivumbehandling | Enhetsmetadatanavn i Common Data Service | Notater |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Aktivabehandling, livsløpstilstander for aktiva               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Aktivabehandling, livsløpsmodeller for aktiva               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Aktivabehandling, livsløpsmodeller for arbeidssted | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Aktivabehandling, livsløpstilstander for arbeidssted | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Aktivabehandling, aktivatyper                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Aktivabehandling, arbeidsstedstyper            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Aktivabehandling, arbeidssteder                 | msdyn_functionallocations                | Se [merknaden](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Aktivabehandling, aktiva                               | msdyn_customerassets                     | Se [merknaden](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Aktivabehandling, produsenter                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Aktivabehandling, modeller                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Aktivabehandling, garanti                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Tilordningsspesifikke merknader

- På grunn av selvavhengighet kan det hende at du må kjøre den innledende synkroniseringen mer enn én gang.
