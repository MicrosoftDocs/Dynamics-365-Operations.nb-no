---
title: Terminologi for produktvariantnumre og navn
description: "Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil]. Den nye terminologien har et bestemt format som inkluderer produktstandardnummer, aktive produktdimensjoner og skilletegn for tekst du velger. Du kan også opprette en terminologi for produktnavn. Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren. Disse terminologiene kan inneholde attributtene du velger."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0c3c1a3e64b016aa72e933f4d6cba854549ff13a
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Terminologi for produktvariantnumre og navn

Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet [Produktstandardnummer - Konfigurasjon - Størrelse - Farge - Stil]. Den nye terminologien har et bestemt format som inkluderer produktstandardnummer, aktive produktdimensjoner og skilletegn for tekst du velger. Du kan også opprette en terminologi for produktnavn. Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren. Disse terminologiene kan inneholde attributtene du velger.

Med de nye terminologiene for produktvariantnumre og navn på produktvariant kan du ta med segmenter i identifikatorene for produktvarianter. Disse segmentene kan inkludere produktstandardnummer og navn, produktdimensjon-IDer og navn, nummerserier, tekstkonstanter og attributter. Med denne funksjonen kan du raskt finne en bestemt produktvariant når du oppretter en salgsordre eller bestilling. Du oppretter terminologier for både produktvariantnumre og produktvariantnavn fra siden **Produktterminologi**. Du åpner denne siden ved å klikke **Behandling av produktinformasjon** &gt; **Oppsett**.

## <a name="nomenclature-of-predefined-product-variants"></a>Terminologi for forhåndsdefinerte produktvarianter
Produktvarianter genereres for produktstandarder i henhold til én av tre konfigurasjonsteknologier:

-   Forhåndsdefinerte varianter
-   Restriksjonsbasert
-   Dimensjonsbasert

Hver produktvariant har et nummer og navn, og med terminologien for produktvariant-ID kan du velge segmentene som skal inkluderes i hvert produktnummervariant og navn. Du kan velge de følgende segmentene på siden **Produktterminologi**:

-   Produktstandardnummer
-   Navn på produktstandard
-   Nummerserieverdi
-   Tekstkonstant
-   Produktdimensjoner
    -   Konfigurasjons-ID eller navn
    -   Farge-ID eller navn
    -   Størrelses-ID eller navn
    -   Stil-ID eller navn

Når terminologien for et produktvariant-ID-nummer er definert, kan det være tilknyttet en produktdimensjonsgruppe. Alle produktstandarder som refererer til denne dimensjonsgruppen, blir deretter tilordnet produktvariantnumre i henhold til terminologien. Terminologier for produktvariantnavn kan imidlertid ikke knyttes til produktdimensjonsgrupper. Du kan også tilordne en terminologi for produktvariantidentifikasjon direkte til en produktstandard. I så fall tilordnes produktvariantene som hører til produktstandarden, til produktvariantnumre og navn i henhold til terminologiene.

### <a name="example"></a>Eksempel

En T-skjorte (TS1234) er produsert i tre størrelser (S, M, L), fire farger (rød, grønn, blå, gul) og to stiler (Polo, V). 24 produktvarianter er derfor mulig (= 3 × 4 x 2). Du kan opprette en terminologi for produktvariantnummer med følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant: "-"
3.  Farge
4.  Tekstkonstant: "-"
5.  Størrelse
6.  Tekstkonstant: "-"
7.  Stil

I dette tilfellet er produktvariantnummeret for en rød, liten polo-T-skjorte: TS1234-Rød-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Terminologi for restriksjonsbaserte konfigurasjoner
For restriksjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen. Du kan velge de følgende segmentene på siden **Produktterminologi**:

-   Nummerserieverdi
-   Tekstkonstant
-   Attributtverdi

Hver komponent i en produktkonfigurasjonsmodell kan ha sin egen konfigurasjonsterminologi. Bare attributtene som hører til komponenten, kan brukes. Attributter fra delkomponenter eller brukerkrav kan ikke brukes.

### <a name="example"></a>Eksempel

En produktkonfigurasjonsmodell har en rotkomponenter med to attributter:

-   Materialer (plast, tre, stål)
-   Lengde (10... 100)

Du kan opprette en konfigurasjonsterminologi med følgende segmenter:

1.  Attributtverdi: Materiale
2.  Tekstkonstant: "AAA"
3.  Attributtverdi: Lengde

I dette tilfellet blir konfigurasjons-ID-en for tremateriale som har en lengde på 78, WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Terminologi for dimensjonsbasert konfigurasjoner
For dimensjonsbaserte konfigurasjoner kan du opprette en dedikert terminologi for konfigurasjonsproduktdimensjonen. Du kan velge de følgende segmentene på siden **Produktterminologi**:

-   Nummerserieverdi
-   Tekstkonstant
-   Konfigurasjonsgruppeelement

Du kan definere en konfigurasjonsterminologi for en stykkliste.

### <a name="example"></a>Eksempel

En stykkliste har fire stykklistelinjer som er delt inn i to konfigurasjonsgrupper:

-   Stykklistelinje: M0007, Standardkabinett
    -   Konfigurasjonsgruppe: Kabinett
-   Stykklistelinje: M0008, High end-kabinett
    -   Konfigurasjonsgruppe: Kabinett
-   Stykklistelinje: M0021, Frontgrill av tøy
    -   Konfigurasjonsgruppe: Frontgrill
-   Stykklistelinje: M0022, Frontgrill metall
    -   Konfigurasjonsgruppe: Frontgrill

Du kan opprette en konfigurasjonsterminologi med følgende segmenter:

1.  Konfigurasjonsgruppe: Kabinett
2.  Tekstkonstant: "&"
3.  Konfigurasjonsgruppe: Frontgrill

I dette tilfellet er konfigurasjons-IDen for et standardkabinett med frontgrill av tøy: M0007 og M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Terminologi for en kombinasjon av produktvarianter og konfigurasjoner
Når du bruker enten restriksjonsbasert eller dimensjonsbasert konfigurasjonsteknologi til å konfigurere produktvarianter for en produktstandard, kan produktvariantnumrene til produktvariantene inkludere terminologien fra konfigurasjonsdimensjonen. Hvis du vil konfigurere varianter, gjør du følgende:

1.  Definer en terminologi for et produktvariantnummer som inkluderer konfigurasjonsdimensjonen på siden **Produktterminologi**.
2.  Tilordne terminologien til en produktdimensjonsgruppe som har konfigurasjonsdimensjonen.
3.  Definer en konfigurasjonsterminologi for komponentene eller stykklistene som skal brukes til å konfigurere produktvariantene.

Du kan også opprette en terminologi for produktvariantnavn. Produktvariantnavnet kan konfigureres til å inkludere konfigurasjons-ID eller navn.

### <a name="example-for-constraint-based-configurations"></a>Eksempel for restriksjonsbaserte konfigurasjoner

I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant "\_"
3.  Konfigurasjon

Konfigurasjonsterminologien består av følgende segmenter:

1.  Attributtverdi: Materiale
2.  Tekstkonstant: "AAA"
3.  Attributtverdi: Lengde

Du angir følgende verdier for segmenter:

-   Produktstandardnummer = **M0099**
-   Materiale = **plast**
-   Lengde = **12**

I dette tilfellet er produktvariantnummeret M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Eksempel for dimensjonsbaserte konfigurasjoner

I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant "//"
3.  Konfigurasjon

Konfigurasjonsterminologien består av følgende segmenter:

1.  Konfigurasjonsgruppe: Kabinett
2.  Tekstkonstant: "&"
3.  Konfigurasjonsgruppe: Frontgrill

Du angir følgende verdier for segmenter:

-   Produktstandardnummer = **D0123**
-   Kabinett = **M0008**
-   Frontgrill = **M0022**

I dette tilfellet er produktvariantnummeret D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummereringskonflikter
I noen tilfeller kan det hende at en terminologi for produktvariantnummer du angir, ikke fører til ulike produktvariantnumre. Dette kan for eksempel skje hvis produktvariantnumrene ikke er unike hvis én aktiv produktdimensjon ikke er inkludert i terminologien for en produktstandard som bruker forhåndsdefinerte variantkonfigurasjonsteknologi. Måten du håndterer konflikter på, varierer avhengig av konfigurasjonsteknologien.

### <a name="predefined-variants"></a>Forhåndsdefinerte varianter

Det vil oppstå en feil hvis du manuelt oppretter eller automatisk prøver å generere produktvarianter der én eller flere fører til samme produktvariantnummer. Hvis du vil unngå denne situasjonen, bør du bruke alle aktive produktdimensjoner i produktdimensjonsgruppen. Du kan også inkludere en nummerserie for å garantere at produktvariantnumrene er unike.

### <a name="constraint-based-configurations"></a>Restriksjonsbaserte konfigurasjoner

Avhengig av terminologien kan systemet prøve å tilordne et ikke-unikt produktvariantnummer til en konfigurasjon. I så fall vil systemet bruke nummerserien for konfigurasjonsdimensjonen som produktvariantnummer i stedet, og du får en advarsel. Hvis du vil unngå denne situasjonen, bør du ta med nok attributter i terminologien for å garantere unike produktvariantnumre. Du bør også kontrollere at alternativet **Bruk på nytt** er merket av for komponenten.

### <a name="dimension-based-configurations"></a>Dimensjonsbaserte konfigurasjoner

Under ett trinn i konfigurasjonsprosessen foreslår systemet en konfigurasjonsverdi i henhold til terminologien. I dette trinnet kan du endre konfigurasjonsverdien manuelt. Når du lagrer konfigurasjonen, kontrolleres det om konfigurasjonsverdien er unik. Hvis verdien du angav, ikke er unik, får du en feilmelding. For å lagre konfigurasjonen må du angi en unik konfigurasjonsverdi.

<a name="see-also"></a>Se også
--------

[Opprette produktnummerterminologi for forhåndsdefinerte produktvarianter](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[Opprette produktnummerterminologi for konfigurerte produktvarianter](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


