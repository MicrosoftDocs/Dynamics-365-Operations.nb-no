---
title: Dimensjonsbasert produktkonfigurasjon
description: "Dimensjonsbasert produktkonfigurasjon representerer en enkel løsning for oppretting av mange produktvarianter fra én enkelt produktstandard og dens stykkliste."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d13fc55342030d96d38f264f6bff9586832b4ab5
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="dimension-based-product-configuration"></a>Dimensjonsbasert produktkonfigurasjon

[!include[banner](../includes/banner.md)]


Dimensjonsbasert produktkonfigurasjon representerer en enkel løsning for oppretting av mange produktvarianter fra én enkelt produktstandard og dens stykkliste.

Dimensjonsbasert produktkonfigurasjon er én av tre innebygde teknologiene for produktkonfigurasjon. De to andre teknologiene er forhåndsdefinerte varianter og restriksjonsbasert konfigurasjon. Alle tre teknologiene bruker en produktstandard som utgangspunkt og lar brukeren opprette mange produktvarianter for én produktstandard.

## <a name="key-concepts"></a>Nøkkelbegreper
Dimensjonsbasert produktkonfigurasjon er basert på følgende nøkkelbegreper:

-   Produktstandarder
-   Konfigurasjonsproduktdimensjon
-   Konfigurasjonsgrupper
-   Stykkliste
-   Konfigurasjonsrute
-   Konfigurasjonsregler

### <a name="product-masters"></a>Produktstandarder

En produktstandard utgangspunktet for produktkonfigurasjonsprosesser. For den dimensjonsbaserte produktkonfigurasjonen må du ha en produktstandard med denne bestemte konfigurasjonsteknologien og en produktdimensjonsgruppe som omfatter konfigurasjonsproduktdimensjonen.

### <a name="configuration-product-dimension"></a>Konfigurasjonsproduktdimensjon

Konfigurasjonsproduktdimensjonen brukes til å identifisere produktvariantene for en produktstandard med den dimensjonsbaserte konfigurasjonsteknologien. Konfigurasjonsdimensjonsverdien angis av brukeren og skal bidra til å identifisere de individuelle produktvariantene.

### <a name="configuration-groups"></a>Konfigurasjonsgrupper

Konfigurasjonsgrupper defineres i et sentralt repositorium og kan brukes i forbindelse med alle produktkonfigurasjonsmodeller. Konfigurasjonsgrupper er knyttet til de enkeltstående stykklistelinjene og holder sammen en gruppe med linjer som er gjensidig utelukkende. Dette betyr at bare én linje i en gruppe kan velges for én produktvariant.

### <a name="bill-of-materials-bom"></a>Stykkliste

Stykklisten representerer byggeblokker for en dimensjonsbasert produktkonfigurasjon. Den må inneholde alle de ulike produktene som kan brukes i en hvilken som helst produktvariant. Hver linje i stykklisten kan referere til en konfigurasjonsgruppe. Hvis en linje ikke refererer til en konfigurasjonsgruppe, tas den med i alle produktvarianter.

### <a name="configuration-route"></a>Konfigurasjonsrute

Konfigurasjonsruten bestemmer rekkefølgen på konfigurasjonsgruppene, slik de vises for brukeren under produktkonfigurasjonsprosessen.

### <a name="configuration-rules"></a>Konfigurasjonsregler

Konfigurasjonsreglene representerer en mekanisme for å sikre at et produkt som er inkludert i én konfigurasjonsgruppe i en stykkliste, fremtvinger en inkludering eller en utelukkelse av et produkt i en annen konfigurasjonsgruppe i samme stykklisten.

## <a name="product-modeling-process"></a>Produktmodelleringsprosess
Den naturlige sekvensen i utviklingen av en produktmodell for et dimensjonsbasert produkt starter med definisjonen av de relevante konfigurasjonsgruppene. Det er viktig å sikre at alle produkter som skal brukes i stykklisten, er frigitt til firmaet som produktmodellen er utviklet for. Med disse byggeblokkene på plass kan brukeren opprette stykklisten og tilordne konfigurasjonsgrupper til alle relevante stykklistelinjer. Når stykklisten er fullført, kan en konfigurasjonsrute defineres for å ordne konfigurasjonsgruppene i riktig rekkefølge. \[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimensjonsbasert produktmodelleringsprosess](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimensjonsbasert produktmodelleringsprosess\[/caption\] Hvis det finnes bestemte produkter fra ulike konfigurasjonsgrupper som må eller ikke kan brukes sammen, kan du opprette konfigurasjonsregler som håndhever disse produktrelasjonene. Etter at stykklisten er knyttet sammen med en dimensjonsbasert produktstandard via en stykklisteversjon og begge er godkjent og aktivert, kan du opprette produktkonfigurasjoner og skrive inn et navn for hver konfigurasjon. Du kan definere konfigurasjonene før eventuelle transaksjoner er generert, eller du kan gjøre det når det er behov for en bestemt konfigurasjon.

### <a name="suggested-use"></a>Foreslått bruk

Teknologien for dimensjonsbasert konfigurasjon passer best for produkter med begrenset varians og kombinasjonen av de standard produktdimensjonene størrelse, farge, stil, og konfigurasjon er ikke egnet til å identifisere en bestemt produktvariant. Et eksempel kan være sykkel med rammehøyde, hjulstørrelse, bremstyper og ulike gir.




