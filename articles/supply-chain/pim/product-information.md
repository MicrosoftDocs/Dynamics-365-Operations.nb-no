---
title: Oversikt over produktinformasjon
description: Dette emnet inneholder informasjon om produktinformasjonsadministrasjon. Behandling av produktinformasjon fungerer sammen med en delt produktdefinisjon, -kategorisering og -identifikatorer på tvers av alle juridiske enheter, og bestemte konfigurasjoner av et produkt, slik at den passer til forretningsprosessene.
author: t-benebo
manager: tfehr
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace, EcoResProductVariantPerCompanyImagePart, EcoResProductRelationType,EcoResProductAvailabilityPart,  EcoResProductReleasedSelect, EcoResProductLookup, EcoResProductVariantsPendingReleaseFormPart, EcoResProductSearchLookup, EcoResProductNumberRename, EcoResDimensionBasedConfigWorkspace, EcoResProductVariantImagePart, EcoResProductImagePart, EcoResProductVariantsPerCompanyPart, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleaseSessions, EcoResProductVariantMaintainWorkspaceConfiguration, EcoResProductProcessManufacturingWorkspaceConfiguration, EcoResProductMasterVariantsPart, EcoResProductDiscreteManufacturingWorkspaceConfiguration, EcoResProductVariantAvailabilityPart, EcoResProductInformationFactBox, EcoResProductLookupTest, EcoResProductImageTest, EcoResProductReleasedRecentlyCreatedFormPart, EcoResPhysicalProductDimensions, PdsMRCRegulatedListItem, EcoResProductAvailabilityPart, PdsMRCRestrictionList, InventItemIdLookupAllocationId, EcoResProductAvailability, EcoResProductEntityAttributeTableFieldAssociation, EcoResProductImagePart, EcoResProductRelation, EcoResProductReleaseAddProduct, EcoResProductPerCompanyListPage, EcoResProductParameters, PdsMRCRestrictedItemByCountryState, EngChgCasePreview, InventTablePreview, PdsMRCItemDetails, EngChgCaseAssociate, PdsMRCCustomerHistory, PdsMRCVendorHistory, PdsMRCRestrictedCountryStateByItem, InventItemIdGroupLookup, InventLocationLookup, PdsMRCValidityIntervalbyCountry, PdsMRCValidityIntervalbyCountry, PdsMRCEventTracker, PdsMRCReportingCountry, PdsMRCDocument, PdsMRCReportingList, PdsMRCItemCAS, GraphicsTestForm, EngChgPicklist
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e797e8d9e2c7b30d3f94a03bd0cb8024afe5835
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247868"
---
# <a name="product-information-overview"></a>Oversikt over produktinformasjon

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder informasjon om produktinformasjonsadministrasjon. Behandling av produktinformasjon fungerer sammen med en delt produktdefinisjon, -kategorisering og -identifikatorer på tvers av alle juridiske enheter, og bestemte konfigurasjoner av et produkt, slik at den passer til forretningsprosessene. 

Produktinformasjon er ryggraden i forsyningskjeden og handelsprogrammer på tvers av alle bransjer. Den refererer til prosesser og teknologier som fokuserer på sentral administrasjon av informasjon om produkter (for eksempel på tvers av forsyningskjeder). Det er svært viktig at delte produktdefinisjoner, dokumentasjon, attributter og identifikatorer brukes. I de forskjellige modulene i en bedriftsløsning kreves produktspesifikk informasjon og konfigurasjon for å behandle forretningsprosesser som er knyttet til bestemte produkter, produktfamilier eller produktkategorier.

## <a name="product-definition"></a>Produktdefinisjon

Et produkt er først og fremst definert av produktnummer, navn og beskrivelse. Andre data er imidlertid også nødvendig for å beskrive et produkt eller en tjeneste:

- Produkttype: vare eller service
- Produktets undertype: forskjellige produkter og produktstandarder
- Definisjon av produktvariantmodellen:

     - Produktdimensjoner og dimensjonsgrupper
     - Produktterminologi
     - Produktkonfigurasjonsmodeller

- Tilknytning av produktet til én eller flere kategorier
- Definisjon av attributtene for produkt og kategori
- Produktbilder
- Vedlegg
- Måleenheter og tilknyttede konverteringer
- Oversettelser for alle navn og beskrivelser

## <a name="distribution-export-and-import-of-product-data"></a>Distribusjon, eksport og import av produktdata

Produktdefinisjonen kan opprettes i Supply Chain Management. Den kan også importere fra administrasjon av produktlivssyklus (PLM), administrasjon av produktdata (PDM) eller behandling av produktinformasjon (PIM). Når det brukes mer enn én forekomst av Supply Chain Management, brukes én forekomst vanligvis som samme mal for produktdataene for alle andre forekomster. Denne metoden støttes av en rekke dataenheter som muliggjør eksport og import av produktdefinisjonsdata fra én forekomst til en annen.

For å støtte distribusjonen av produktdata for mange forekomster lar Supply Chain Management deg bruke Microsoft Dataverse. Produktdefinisjonene kan eksporteres fra en forekomst av Supply Chain Management til Microsoft Dataverse. Produktdefinisjonene kan deretter brukes til å klargjøre andre forretningsprogrammer, for eksempel Dynamics 365 Sales, med produktdata.

Legg merke til at produktopplysninger endres hver dag i dynamiske og fleksible organisasjoner. Vedlikehold av nøyaktige og faktiske produktdata er derfor en viktig forretningsprosess i seg selv.

## <a name="product-masters-and-product-variants"></a>Produktstandarder og produktvarianter

I en fleksibel verden der varer raskt må tilpasset kundekrav, angir produktdefinisjoner et sett med produkter i stedet for spesifikke produkter. I Supply Chain Management er de generell produktene kjent som *produktstandarder*. Produktstandarder inneholder definisjonen og regler som angir hvordan spesifikke produkter beskrives og fungerer i forretningsprosesser. Basert på disse definisjonene kan spesifikke produkter genereres. Disse spesifikke produktene er kjent som *produktvarianter*.

En produktstandard er tilknyttet en produktdimensjonsgruppe og en konfigurasjonsteknologi for å angi forretningsreglene. Produktdimensjoner (farge, størrelse, stil og konfigurasjon) er et bestemt sett med attributter som kan brukes i hele programmet til å definere og spore bestemt virkemåten til de tilknyttede produktene. Disse dimensjonene hjelper også brukere å søke etter og identifisere produktene.

## <a name="configuration-technologies"></a>Konfigurasjonsteknologier

Du kan velge mellom tre konfigurasjonsteknologier:

- Forhåndsdefinerte varianter defineres av forhåndsdefinerte produktdimensjoner. Variantdefinisjonen inneholder definisjonen av en bestemt gyldig kombinasjon av dimensjoner, for eksempel farge, stil og størrelse. Hver kombinasjon produserer en spesifikk produktvariant.
- Dimensjonsbasert konfigurasjon brukes vanligvis i scenarier for produksjon, og kan du bruke konfigurasjonsdimensjonen i definisjonen av stykklisten. Når en bestemt konfigurasjon er valgt, bruker systemet delsettet med stykklistelinjer som er gyldige for denne konfigurasjonen, for planlegging og produksjon. Dette konseptet kalles også *global stykkliste*, fordi én delt stykkliste brukes for alle konfigurasjoner til et produkt.
- Restriksjonsbasert konfigurasjon bruker en produktkonfigurasjonsmodell til å beskrive alle mulige attributter og komponenter som kreves for å beskrive alle mulige varianter av et produkt i en enkelt modell. Begrensingene for kombinasjoner av attributter kan beskrives gjennom vanlige uttrykk eller tabellbaserte begrensninger. Konfigurasjonsmodeller og konfiguratorer blir viktigere i behandling av produktinformasjon og brukes på tvers av alle bransjer.

Når du planlegger implementeringen av Supply Chain Management, er det svært viktig at du velger den riktige konfigurasjonsteknologien for en forretningsprosess. Et produkt kan ikke konverteres fra én modell til en annen etter implementering.

## <a name="product-variant-model-definition-workspace"></a>Arbeidsområdet Definisjon av produktvariantmodell

Arbeidsområdet **Definisjon av produktvariantmodell** gir en oversikt over produktstandarder. Det viser også status for versjonen av maler og tilknyttede varianter for bestemte juridiske enheter.

## <a name="released-products"></a>Frigitte produkter

Produktene som er frigitt til et bestemt juridisk enhet, er kjent som *frigitte produkter*. Produkter kan frigis samlet til én eller flere juridiske enheter samtidig. Fordi ulike egenskaper og attributter for produktene kanskje må legges til per juridisk enhet, kan du bruke arbeidsområdet **Vedlikehold av frigitt produkt** til å overvåke og fullføre de nylig frigitte produktene i hver juridiske enhet, eller i de underordnede organisasjonene for en juridisk enhet.

### <a name="released-product-maintenance-workspace"></a>Arbeidsområdet Vedlikehold av frigitt produkt

Du kan konfigurere arbeidsområdet **Vedlikehold av frigitt produkt** i menyelementet **Konfigurer mitt arbeidsområde**. Velg et kategorihierarki og en kategori du vil filtrere arbeidsområdet etter. For å justere de relevante produktdataene i arbeidsområdet kan du også definere, i dager, horisontene for **Nylig frigitte produkter** og **Frigitte produkter som er stoppet**.

Arbeidsområdet består av et sammendrag av fliser og to lister. Listen **Åpne tilfeller** viser produktendringssaker som har produkter i det valgte produktkategorihierarkiet som ikke er fullført og lukket. Listen **Nylig utgitt** viser produkter som er frigitt i horisonten som er angitt i konfigurasjonen for arbeidsområdet. Validering kjøres for hvert element i listen, og valideringsstatusen vises. Denne statusen kan indikere at de nødvendige konfigurasjonene for den juridiske enheten ikke er fullført. Fra listen har du direkte tilgang til sidene **Detaljer om frigitt produkt**, **Vedlikehold av produktattributt**, **Vedlikehold av produktkategori**, **Standard ordreinnstillinger** og **Tekstoversettelser** for å fullføre den konfigurasjonen av produktet.

### <a name="manually-creating-a-new-released-product"></a>Manuell oppretting av et nytt frigitt produkt

Du kan manuelt opprette et frigitt produkt i en enkelt kjøring, avhengig av organisasjonens forretningsprosesser og eventuelle regler for hvorvidt denne funksjonen skal brukes. Denne funksjonen oppretter et nytt produkt, og frigjør det automatisk til den gjeldende juridiske enheten. For å opprette et nytt produkt klikker du **Frigitte produkter** i arbeidsområdet **Vedlikehold av frigitt produkt** eller på listesiden **Frigitt produkt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]