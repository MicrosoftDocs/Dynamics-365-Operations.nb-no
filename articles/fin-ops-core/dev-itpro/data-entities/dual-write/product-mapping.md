---
title: Ensartet produktopplevelse
description: Dette emnet beskriver integreringen av produktdata mellom Finance and Operations-apper og Dataverse.
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6941a38e96520befd3bdba65956d45a6bbaee4be
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306395"
---
# <a name="unified-product-experience"></a>Samlet produktopplevelse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Når et forretningsøkosystem består av Dynamics 365-programmer, for eksempel Finance, Supply Chain Management og Sales, bruker bedrifter ofte disse programmene for produktdata. Dette er fordi disse appene tilbyr en robust produktinfrastruktur som er komplettert med avanserte prissettingskonsepter og nøyaktige lagerbeholdningsdata. Bedrifter som bruker et eksternt PLM-system (Product Lifecycle Management ) for produktdata, kan kanalisere produkter fra Finance and Operations-apper til andre Dynamics 365-apper. Den enhetlige produktopplevelsen bringer i den integrerte produktdatamodellen til Dataverse, slik at alle programbrukere, inkludert Power Platform-brukere, kan dra nytte av de rike produktdataene som kommer fra Finance and Operations-apper.

Her er produktdatamodellen fra Sales.

![Datamodell for produkter i CE](media/dual-write-product-4.jpg)

Her er produktdatamodellen fra Finance and Operations-apper.

![Datamodell for produkter i Finance and Operations](media/dual-write-products-5.jpg)

Disse to produktdatamodellene er integrert i Dataverse, som vist nedenfor.

![Datamodell for produkter i Dynamics 365-apper](media/dual-write-products-6.jpg)

Tabelltilordningene for dobbel skriving for produkter er utformet for dataflyt én vei, i nær sanntidsopplevelse fra Finance and Operations-apper til Dataverse. Produktinfrastrukturen er imidlertid gjort åpen for å gjøre den toveis om nødvendig. Selv om du kan tilpasse den, skjer det på eget ansvar fordi Microsoft ikke anbefaler denne fremgangsåten.

## <a name="templates"></a>Maler

Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene. Som følgende tabell viser opprettes en samling tabelltilordning for å synkronisere produkter og beslektet informasjon.

Finance and Operations-apper | Andre Dynamics 365-apper | beskrivelse
-----------------------|--------------------------------|---
Frigitte produkter V2 | msdyn\_sharedproductdetails | Tabellen **msdyn\_sharedproductdetails** inneholder kolonnene fra Finance and Operations-apper som definerer produktet og inneholder informasjon om produktets økonomi og administrasjon. 
Dataverse frigitte spesifikke produkter | Produkt | **Produkt**-tabellen inneholder kolonnene som definerer produktet. Den omfatter enkeltprodukter (produkter med undertypeprodukt) og produktvariantene. Tabellen nedenfor viser tilordningene.
Strekkode identifisert med produktnummer | msdyn\_productbarcodes | Produktstrekkoder brukes til entydig identifikasjon av produkter.
Standard ordreinnstillinger | msdyn\_productdefaultordersettings
Innstillinger for produktspesifikk standardordre | msdyn_productdefaultordersettings
Produktdimensjonsgrupper | msdyn\_productdimensiongroups | Produktdimensjonsgruppen definerer hvilke produktdimensjoner som definerer produktet. 
Lagringsdimensjonsgrupper | msdyn\_productstoragedimensiongroups | Produktlagringsdimensjonsgruppen representerer metoden som brukes til å definere plasseringen av produktet i lageret.
Sporingsdimensjonsgrupper | msdyn\_producttrackingdimensiongroups | Produktsporingsdimensjonsgruppen representerer metoden som brukes til å spore produktet i beholdningen.
Farger | msdyn\_productcolors
Størrelser | msdyn\_productsizes
Stiler | msdyn\_productsytles
Konfigurasjoner | msdyn\_productconfigurations
Produktstandardfarger | msdyn_sharedproductcolors | Tabellen **Delt produktfarge** angir fargene som en bestemt produktstandard kan ha. Dette konseptet er overført til Dataverse for å holde dataene konsekvente.
Produktstandardstørrelser | msdyn_sharedproductsizes | Tabellen **Delt produktstørrelse** angir størrelsene som en bestemt produktstandard kan ha. Dette konseptet er overført til Dataverse for å holde dataene konsekvente.
Produktstandardstiler | msdyn_sharedproductstyles | Tabellen **Delt produktstil** angir stilene som en bestemt produktstandard kan ha. Dette konseptet er overført til Dataverse for å holde dataene konsekvente.
Produktstandardkonfigurasjoner | msdyn_sharedproductconfigurations | Tabellen **Delt produktkonfigurasjon** angir konfigurasjonene som en bestemt produktstandard kan ha. Dette konseptet er overført til Dataverse for å holde dataene konsekvente.
Alle produkter | msdyn_globalproducts | Tabellen for alle produkter inneholder alle produktene som er tilgjengelige i Finance and Operations-apper, både frigitte produkter og produkter som ikke er frigitt.
Enhet | uoms
Enhetsomregninger | msdyn_ unitofmeasureconversions
Konvertering av produktspesifikk måleenhet | msdyn_productspecificunitofmeasureconversion
Produktkategorier | msdyn_productcategories | Hver av produktkategoriene og informasjonen om strukturen og kjennetegnene finnes i produktkategoritabellen. 
Produktkategorihierarkier | msdyn_productcategoryhierarhies | Du bruker produkthierarkier til å kategorisere eller gruppere produkter. Kategorihierarkiene er tilgjengelige i Dataverse ved bruk av tabellen for produktkategorihierarki. 
Roller for produktkategorihierarki | msdyn_productcategoryhierarchies | Produkthierarkier kan brukes til forskjellige roller i D365 Finance and Operations. De angir hvilken kategori som brukes i hver rolle som tabellen for produktkategori brukes i. 
Produktkategoritilordninger | msdyn_productcategoryassignments | Hvis du vil tilordne et produkt til en kategori, kan du bruke tabellen for produktkategoritilordninger.

## <a name="integration-of-products"></a>Integrering av produkter

I denne modellen representeres produktet av kombinasjonen av to tabeller i Dataverse: **Produkt** og **msdyn\_sharedproductdetails**. Mens den første tabellen inneholder definisjonen av et produkt (den unike ID-en for produktet, produktnavnet og beskrivelsen), inneholder den andre tabellen kolonnene som er lagret på produktnivå. Kombinasjonen av disse to tabellene brukes til å definere produktet i henhold til konseptet lagerenhet (SKU). Hvert frigitt produkt har informasjonen sin i de nevnte tabellene (Produkt og delt produktinformasjon). For å holde orden på alle produkter (frigitte og ikke frigitte) brukes tabellen **Globale produkter**. 

Fordi produktet er representert som en SKU, kan begrepene for spesifikke produkter, produktstandarder og produktvarianter registreres i Dataverse på følgende måte:

- **Produkter med undertypeprodukt** er produkter som defineres av seg selv. Ingen dimensjoner må defineres. Et eksempel er en bestemt bok. For disse produktene opprettes det én rad i **Produkt**-tabellen og én rad i tabellen **msdyn\_sharedproductdetails**. Ingen rad for produktfamilie opprettes.
- **Produktstandarder** brukes som generelle produkter som inneholder definisjonen og reglene som bestemmer virkemåten i forretningsprosesser. Basert på disse definisjonene kan det genereres spesifikke produkter som er kalles produktvarianter. T-skjorte er for eksempel produktstandarden, og den kan ha Farge og Størrelse som dimensjoner. Varianter kan frigis med ulike kombinasjoner av disse dimensjonene, for eksempel en liten, blå T-skjorte eller en medium grønn T-skjorte. I integrasjonen blir det opprettet én rad per variant i produkttabellen. Denne raden inneholder variantspesifikk informasjon, for eksempel de ulike dimensjonene. Den generelle informasjonen for produktet er lagret i tabellen **msdyn\_sharedproductdetails**. (Denne generelle informasjonen finnes i produktstandarden.) Informasjonen om produktstandarden synkroniseres med Dataverse så snart den frigitte produktstandarden blir opprettet (men før variantene blir frigitt).
- **Spesifikke produkter** refererer til alle produkter med undertypeprodukter og alle produktvariantene. 

![Datamodell for produkter](media/dual-write-product.png)

Når funksjonen for dobbel skriving er aktivert, vil produkter fra Finance and Operations bli synkronisert i andre Dynamics 365-produkter i **Utkast**-tilstand. De blir lagt til den første prislisten med samme valuta. De legges med andre ord til i den første prislisten i en Dynamics 365-app som samsvarer med valutaen til den juridiske tabellen der produktet frigis i en Finance and Operations-app. Hvis ingen prisliste finnes for den angitte valutaen, opprettes det automatisk en prisliste, og produktet tilordnes til den. 

Den gjeldende implementeringen av plugin-modulene for dobbel skriving som knytter standard prisliste til enheten, slår opp valutaen som er knyttet til Finance and Operations-appen, og finner den første prislisten i kundeavtaleappen ved hjelp av alfabetisk sortering i prislistenavnet. Hvis du vil definere en standard prisliste for en bestemt valuta når du har flere prislister for den valutaen, må du oppdatere prislistenavnet til et navn som er tidligere i alfabetisk rekkefølge enn noen andre prislister for den samme valutaen.

Som standard synkroniseres produkter fra Finance and Operations-apper til andre Dynamics 365-apper i **Utkast**-status. Hvis du vil synkronisere produktet med tilstanden **Aktiv**, slik at du for eksempel kan bruke det direkte i salgsordretilbud, må følgende innstilling velges: Under **System > Administrasjon > Systemadministrasjon > Systeminnstillinger > Salg** velger du **Opprett produkter i aktiv tilstand = ja**. 

Når produkter synkroniseres, må du angi en verdi for **Salgsenhet**-feltet i Finance and Operations-appen siden dette er et obligatorisk felt i Sales.

Opprettingen av produktserier fra Dynamics 365 Sales støttes ikke med synkronisering av dobbel skriving for produkter.

Synkroniseringen av produkter skjer fra Finance and Operations-appen til Dataverse. Dette betyr at verdiene i kolonnene for produkttabellen kan endres i Dataverse, men når synkroniseringen utløses (når en produktkolonne endres i en Finance and Operations-app), vil dette overskrive verdiene i Dataverse. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Produktdimensjoner 

Produktdimensjoner er egenskaper som identifiserer en produktvariant. De fire produktdimensjonene (Farge, Størrelse, Stil og Konfigurasjon) blir også tilordnet til Dataverse for å definere produktvariantene. Illustrasjonen nedenfor viser datamodellen for produktdimensjonen Farge. Den samme modellen brukes for Størrelser, Stiler og Konfigurasjoner. 

![Datamodell for produktdimensjoner](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Når et produkt har forskjellige produktdimensjoner (en produktstandard har for eksempel Størrelse og Farge som produktdimensjoner), vil hvert enkelt produkt (det vil si hver produktvariant) defineres som en kombinasjon av disse produktdimensjonene. Produktnummer B0001 er for eksempel en ekstra liten svart T-skjorte, og produktnummer B0002 er en liten svart T-skjorte. I dette tilfellet er de eksisterende kombinasjonene av produktdimensjoner definert. T-skjorten fra det foregående eksemplet kan for eksempel være ekstra liten og svart, liten og svart, medium og svart, eller stor og svart, men den kan ikke være ekstra stor og svart. Det vil si at produktdimensjonene for en produktstandard blir angitt, og varianter kan frigis basert på disse verdiene.

For å holde orden på produktdimensjonene som en produktstandard kan ha, blir følgende tabeller opprettet og tilordnet i Dataverse for hver produktdimensjon. Hvis du vil ha mer informasjon, kan du se [Oversikt over produktinformasjon](../../../../supply-chain/pim/product-information.md). 

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Standard ordreinnstillinger og produktspesifikke standard ordreinnstillinger

Standard ordreinnstillinger definerer området og lageret der varene hentes fra eller lagres, minimumsantall, maksimumsantall, flere og standardantall som skal brukes for handel, eller lagerstyring, leveringstider, stoppflagget og metoden for ordrebekreftelsen. Denne informasjonen er tilgjengelige i Dataverse ved hjelp av standard ordreinnstillinger og produktspesifikke standard ordreinnstillinger. Du finner mer informasjon om funksjonene i [emnet Standard ordreinnstillinger](../../../../supply-chain/production-control/default-order-settings.md).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Måleenhet og konvertering av måleenhet

Måleenhetene og de tilsvarende konverteringene er tilgjengelige i Dataverse etter datamodellen som vises i diagrammet.

![Datamodell for måleenhet](media/dual-write-product-three.png)

Begrepet måleenhet er integrert mellom Finance and Operations-apper og andre Dynamics 365-apper. For hver enhetsklasse i en Finance and Operations-app opprettes en enhetsgruppe i en Dynamics 365-app, som inneholder enhetene som tilhører enhetsklassen. En standard basisenhet opprettes også for hver enhetsgruppe. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Innledende synkronisering av samsvar av enhetsdata mellom Finance and Operations og Dataverse

### <a name="initial-synchronization-of-units"></a>Innledende synkronisering av enheter

Når dobbel skriving er aktivert, synkroniseres enheter fra Finance and Operations-apper til andre Dynamics 365-apper. Enhetsgruppene som synkroniseres fra Finance and Operations-apper i Dataverse, har et flaggsett som angir at de er "eksternt vedlikeholdt".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvare enheter og enhetsklasser/gruppedata fra Finance and Operations-apper og andre Dynamics 365-apper

For det første er det viktig å være klar over at integreringsnøkkelen for enheten er msdyn_symbol. Denne verdien må derfor være unik i Dataverse eller andre Dynamics 365-apper. Fordi det i andre Dynamics 365-apper er paret "enhetsgruppe-ID" og "navn" som definerer den unike enhetstypen, må du vurdere ulike scenarier for å samsvare enhetsdata mellom Finance and Operations-apper og Dataverse.

For enheter som samsvarer/overlapper i Finance and Operations-apper og andre Dynamics 365-apper:

+ **Enheten tilhører en enhetsgruppe i andre Dynamics 365-apper som tilsvarer den tilknyttede enhetsklassen i Finance and Operations-apper**. I dette tilfellet må kolonnen msdyn_symbol i andre Dynamics 365-apper fylles ut med enhetssymbolet fra Finance and Operations-apper. Derfor, når en enhetsgruppe skal samsvares, settes enhetsgruppen til "eksternt vedlikeholdt" i andre Dynamics 365-apper.
+ **Enheten tilhører en enhetsgruppe i andre Dynamics 365-apper som ikke samsvarer med den tilknyttede enhetsklassen i Finance and Operations-apper (ingen eksisterende enhetsklasse i Finance and Operations-apper for enhetsklassen i andre Dynamics 365-apper).** I dette tilfellet må msdyn_symbol fylles ut med en tilfeldig streng. Merk at denne verdien må derfor være unik i andre Dynamics 365-apper.

For enheter og enhetsklasser i Finance and Operations-apper som ikke finnes i andre Dynamics 365-apper:

Som en del av dobbel skriving opprettes og synkroniseres enhetsgruppene fra Finance and Operations-apper og tilsvarende enheter i andre Dynamics 365-apper og Dataverse, og enhetsgruppen angis som "eksternt vedlikeholdt". Det kreves ingen ekstra oppstart.

For enheter i andre Dynamics 365-apper som ikke finnes i Finance and Operations-apper:

Kolonnen msdyn_symbol må fylles ut for alle enheter. Enhetene kan alltid opprettes i Finance and Operations-apper i den tilsvarende enhetsklassen (hvis det finnes). Hvis enhetsklassen ikke finnes, må den først opprettes (vær oppmerksom på at du ikke kan opprette en enhetsklasse i Finance and Operations-apper bortsett ved utvidelse hvis du utvider opplistingen) som samsvarer med andre Dynamics 365-apper. Du kan deretter opprette enheten. Merk at enhetssymbolet i Finance and Operations-apper må være msdyn_symbol som er definert tidligere i andre Dynamics 365-apper for enheten.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Produktpolicyer: dimensjoner, sporing og lagringsgrupper

Produktpolicyene er sett med policyer som brukes til å definere produkter og tilhørende egenskaper i beholdning. Produktdimensjonsgruppen, produktsporingsdimensjonsgruppen og lagringsdimensjonsgruppen kan finnes som produktpolicyer. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Produkthierarkier

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Integreringsnøkkel for produkter 

Fo å identifisere produkter unikt mellom Dynamics 365 for Finance and Operations og produkter i Dataverse brukes integrasjonsnøkler. For produkter er **(productnumber)** den unike nøkkelen som identifiserer et produkt i Dataverse. Den består av sammenkoblingen av: **(firma, msdyn_productnumber)**. **Firmaet** angir den juridiske enheten i Finance and Operations, og **msdyn_productnumber** angir produktnummeret for det bestemte produktet i Finance and Operations. 

For brukere av andre Dynamics 365-apper er produktet identifisert i brukergrensesnittet med **msdyn_productnumber** (vær oppmerksom på at etiketten for kolonnen er **Produktnummer**). I produktskjemaet vises både selskapet og msydn_productnumber. Men (productnumber)-kolonnen, den unike nøkkelen for et produkt, vises ikke. 

Hvis du bygger apper på Dataverse, bør du være oppmerksom på å bruke **productNumber** (den unike produkt-IDen) som integrerings nøkkel. Ikke bruk **msdyn_productnumber**, fordi det ikke er unikt. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Første synkronisering av produkter og overføring av data fra Dataverse til Finance and Operations

### <a name="initial-synchronization-of-products"></a>Innledende synkronisering av produkter 

Når dobbel skriving er aktivert, synkroniseres produkter fra Finance and Operations-apper til Dataverse og kundeengasjementsapper. Produkter som er opprettet i Dataverse og andre Dynamics 365-apper før dobbel skriving ble lansert, ikke blir oppdatert eller samsvart med produktdata fra Finance and Operations-apper.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Samsvare produktdata fra Finance and Operations og andre Dynamics 365-apper

Hvis de samme produktene beholdes (overlappende/samsvarende) i Finance and Operations og i Dataverse og andre Dynamics 365-apper, vil aktivering av dobbel skriving vil synkroniseringen av produkter fra Finance and Operations finne sted, og like rader vil vises i Dataverse for det samme produktet.
For å unngå den forrige situasjonen, hvis andre Dynamics 365-apper har produkter som overlapper/samsvarer med Finance and Operations, må administratoren som aktiverer dobbel skriving, starte opp kolonnene **Selskap** (eksempel: «USMF») og **msdyn_productnumber** (eksempel: «1234: Black:S») før synkronisering av produkter finner sted. Med andre ord må disse to kolonnene i produktet i Dataverse fylles ut med det respektive selskapet i Finance and Operations som produktet må samsvares med, og med produktnummeret. 

Når synkroniseringen er aktivert og finner sted, blir produktene fra Finance and Operations synkronisert med de samsvarende produktene i Dataverse og andre Dynamics 365-apper. Dette gjelder både for forskjellige produkter og produktvarianter. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Overføring av produktdata fra Dynamics 365-apper til Finance and Operations

Hvis andre Dynamics 365-apper har produkter som ikke finnes i Finance and Operations, kan administratoren først bruke **EcoResReleasedProductCreationV2Entity** til å importere disse produktene i Finance and Operations. Samsvar deretter produktdataene fra Finance and Operations og andre Dynamics 365-apper som beskrevet ovenfor. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
