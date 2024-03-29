---
title: Oversikt over dimensjonsbasert produktkonfigurasjon
description: Dimensjonsbasert produktkonfigurasjon representerer en enkel løsning for oppretting av mange produktvarianter fra én enkelt produktstandard og dens stykkliste.
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754117"
---
# <a name="dimension-based-product-configuration-overview"></a>Oversikt over dimensjonsbasert produktkonfigurasjon

[!include [banner](../includes/banner.md)]

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
Den naturlige sekvensen i utviklingen av en produktmodell for et dimensjonsbasert produkt starter med definisjonen av de relevante konfigurasjonsgruppene. Det er viktig å sikre at alle produkter som skal brukes i stykklisten, er frigitt til firmaet som produktmodellen er utviklet for. Med disse byggeblokkene på plass kan brukeren opprette stykklisten og tilordne konfigurasjonsgrupper til alle relevante stykklistelinjer. Når stykklisten er fullført, kan en konfigurasjonsrute defineres for å ordne konfigurasjonsgruppene i riktig rekkefølge. [![Dimensjonsbasert produktmodelleringsprosess.](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Hvis det er visse produkter fra forskjellige konfigurasjonsgrupper som enten må, eller ikke må brukes sammen, kan du opprette konfigurasjonsregler som vil håndheve disse produktrelasjonene. Etter at stykklisten er knyttet sammen med en dimensjonsbasert produktstandard via en stykklisteversjon og begge er godkjent og aktivert, kan du opprette produktkonfigurasjoner og skrive inn et navn for hver konfigurasjon. Du kan definere konfigurasjonene før eventuelle transaksjoner er generert, eller du kan gjøre det når det er behov for en bestemt konfigurasjon.

### <a name="suggested-use"></a>Foreslått bruk

Teknologien for dimensjonsbasert konfigurasjon passer best for produkter med begrenset varians og kombinasjonen av de standard produktdimensjonene størrelse, farge, stil, og konfigurasjon er ikke egnet til å identifisere en bestemt produktvariant. Et eksempel kan være sykkel med rammehøyde, hjulstørrelse, bremstyper og ulike gir.

### <a name="next-step"></a><a name="sequence"></a>Neste trinn

Følgende åtte oppgavelinjer er oppført i den rekkefølgen du skal fylle dem ut. 

1.  [Opprette en dimensjonsbasert produktstandard](tasks/create-dimension-based-product-master.md)
2.  [Frigi en dimensjonsbasert produktstandard](tasks/release-dimension-based-product-master.md)
3.  [Fullføre grunnleggende oppsett av en frigitt produktstandard](tasks/complete-basic-setup-released-product-master.md)
4.  [Definere konfigurasjonsgrupper](tasks/define-configuration-groups.md)
5.  [Opprette en stykkliste for en dimensjonsbasert produktstandard](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [Definere konfigurasjonsruter](tasks/define-configuration-route.md)
7.  [Opprette konfigurasjonsregler](tasks/create-configuration-rules.md)
8.  [Opprette dimensjonsbaserte konfigurasjoner](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]