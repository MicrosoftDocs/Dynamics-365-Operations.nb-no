---
title: Produktnummerterminologi
description: "Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet, [Produktstandardnummer – Konfigurasjon – Størrelse – Farge – Stil], med et bestemt format som inkluderer hovedproduktnummer, aktive produktdimensjoner og skilletegn for tekst du velger. Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren. Disse terminologiene kan inneholde attributtene du velger."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Produktnummerterminologi

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du kan definere en produktnummerterminologi for å erstatte det faste formatet, [Produktstandardnummer – Konfigurasjon – Størrelse – Farge – Stil], med et bestemt format som inkluderer hovedproduktnummer, aktive produktdimensjoner og skilletegn for tekst du velger. Du kan også bygge en terminologi for å identifisere konfigurasjonene som er opprettet av den restriksjonsbaserte produktkonfiguratoren. Disse terminologiene kan inneholde attributtene du velger.

Med den nye terminologien for produktvariantnummer kan du ta med segmenter i produktvariant-IDene. Disse segmentene kan inkludere produktstandardnummer, produktdimensjoner, nummerserier, tekstkonstanter og attributter. Med denne funksjonen kan du raskt finne en bestemt produktvariant når du oppretter en salgsordre eller bestilling.

## <a name="nomenclature-of-predefined-product-variants"></a>Terminologi for forhåndsdefinerte produktvarianter
Produktvarianter genereres for produktstandarder i henhold til én av tre konfigurasjonsteknologier:

-   Forhåndsdefinerte varianter
-   Restriksjonsbasert
-   Dimensjonsbasert

Hver produktvariant har et nummer, og med terminologien for produktvariant-ID kan du velge segmentene som skal inkluderes i hvert produktnummervariant. Du kan velge de følgende segmentene på siden **Produktterminologi**.

-   Produktstandardnummer
-   Nummerserieverdi
-   Tekstkonstant
-   Produktdimensjoner
    -   Konfigurasjon
    -   Farge
    -   Størrelse
    -   Stil

Når terminologien for en produktvariant-ID er definert, kan det være tilknyttet en produktdimensjonsgruppe. Derfor vil alle produktstandarder som refererer til denne dimensjonsgruppen, blir tilordnet produktvariantnumre i henhold til terminologien. Det er også mulig å tilordne terminologien for en produktvariantidentifikasjon direkte til en produktstandard. I så fall tilordnes produktvariantene som er knyttet til denne malen, til produktvariantnumre i henhold til terminologien.

### <a name="example"></a>Eksempel

En T-skjorte (TS1234) er produsert i 3 ulike størrelser (S, M, L), 4 forskjellige farger (rød, grønn, blå, gul) og 2 stiler (Polo, V). Dette gir totalt 24 mulige produktvarianter. Terminologien for en produktvariantidentifikasjon opprettes med følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant: '-'
3.  Farge
4.  Tekstkonstant: '-'
5.  Størrelse
6.  Tekstkonstant: '-'
7.  Stil

Produktvariantnummeret for Rød, Small, Polo er: TS1234-Rød-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Terminologi for restriksjonsbaserte konfigurasjoner
For restriksjonsbaserte konfigurasjoner bygges en dedikert terminologi for konfigurasjonsproduktdimensjonen. Du kan velge de følgende segmentene på siden **Produktterminologi**.

-   Nummerserieverdi
-   Tekstkonstant
-   Attributtverdi 

Hver komponent i en produktkonfigurasjonsmodell kan ha sin egen konfigurasjonsterminologi. Bare attributtene som er knyttet til komponenten, kan brukes. Attributter fra delkomponenter eller brukerkrav er ikke tilgjengelige.

### <a name="example"></a>Eksempel

En produktkonfigurasjonsmodell har en rotkomponenter med to attributter.

-   Materialer (plast, tre, stål)
-   Lengde (10... 100)

En konfigurasjonsterminologi defineres ved hjelp av følgende segmenter:

1.  Attributtverdi: Materiale
2.  Tekstkonstant: 'AAA'
3.  Attributtverdi: Lengde

Konfigurasjons-ID for tremateriale med en lengde på 78 får følgende konfigurasjons-ID: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Terminologi for dimensjonsbasert konfigurasjoner
For dimensjonsbaserte konfigurasjoner bygges en dedikert terminologi for konfigurasjonsproduktdimensjonen. Du kan velge de følgende segmentene på siden **Produktterminologi**.

-   Nummerserieverdi
-   Tekstkonstant
-   Konfigurasjonsgruppeelement

En konfigurasjonsterminologi kan defineres for en stykkliste.

### <a name="example"></a>Eksempel

En stykkliste har 4 stykklistelinjer som er delt inn i 2 konfigurasjonsgrupper.

-   Stykklistelinje: M0007, Standardkabinett
    -   Konfigurasjonsgruppe: Kabinett
-   Stykklistelinje: M0008, High end-kabinett
    -   Konfigurasjonsgruppe: Kabinett
-   Stykklistelinje: M0021, Frontgrill av tøy
    -   Konfigurasjonsgruppe: Frontgrill
-   Stykklistelinje: M0022, Frontgrill metall
    -   Konfigurasjonsgruppe: Frontgrill

En konfigurasjonsterminologi defineres ved hjelp av følgende segmenter:

1.  Konfigurasjonsgruppe: Kabinett
2.  Tekstkonstant: '&'
3.  Konfigurasjonsgruppe: Frontgrill

Konfigurasjons-IDen for et standardkabinett med frontgrill av tøy er: M0007 og M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Terminologi av en kombinasjon av produktvarianter og konfigurasjoner
Når du bruker enten restriksjonsbasert eller dimensjonsbasert konfigurasjonsteknologi til å konfigurere produktvarianter for en produktstandard, kan produktvariantene få produktvariantnumre som omfatter terminologien fra en konfigurasjonsdimensjon. Hvis du vil konfigurere varianter, gjør du følgende:

1.  Definer en terminologi for et produktvariantnummer som inkluderer konfigurasjonsdimensjonen på siden **Produktterminologi**.
2.  Tilordne denne terminologien til en produktdimensjonsgruppe med konfigurasjonsdimensjonen.
3.  Definer en konfigurasjonsterminologi for komponentene eller stykklistene som skal brukes til å konfigurere produktvariantene.

### <a name="example-for-constraint-based-configurations"></a>Eksempel for restriksjonsbaserte konfigurasjoner

I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant \_
3.  Konfigurasjon

Konfigurasjonsterminologien kan bestå av følgende segmenter:

1.  Attributtverdi: Materiale
2.  Tekstkonstant: 'AAA'
3.  Attributtverdi: Lengde

Du kan angi følgende verdier for segmenter:

-   Produktstandardnummer = M0099
-   Materiale = plast
-   Lengde = 12

Produktvariantnummer blir: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Eksempel for dimensjonsbaserte konfigurasjoner

I dette eksemplet kan du bruke en terminologi for et produktvariantnummer som består av følgende segmenter:

1.  Produktstandardnummer
2.  Tekstkonstant '//'
3.  Konfigurasjon

Konfigurasjonsterminologien kan bestå av følgende segmenter:

1.  Konfigurasjonsgruppe: Kabinett
2.  Tekstkonstant: '&'
3.  Konfigurasjonsgruppe: Frontgrill

Du kan angi følgende verdier for segmenter:

-   Produktstandardnummer = D0123
-   Kabinett = M0008
-   Frontgrill = M0022

Produktvariantnummeret blir: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Nummereringskonflikter
Det er mulig å konfigurere terminologi for produktvariantnummer som ikke fører til ulike produktvariantnumre. Dette kan for eksempel skje hvis én aktiv produktdimensjon ikke er inkludert i terminologien for en produktstandard som bruker forhåndsdefinerte variantkonfigurasjonsteknologi. Konflikter håndteres forskjellig for de ulike konfigurasjonsteknologiene.

### <a name="predefined-variants"></a>Forhåndsdefinerte varianter

Det vil oppstå en feil hvis du manuelt eller automatisk prøver å generere produktvarianter der én eller flere fører til samme produktvariantnummer. Hvis du vil unngå dette, bør du bruke alle aktive produktdimensjoner i produktdimensjonsgruppen, eller inkludere en nummerserie for å sikre at produktvariantnumrene er unike.

### <a name="constraint-based-configurations"></a>Restriksjonsbaserte konfigurasjoner

Avhengig av terminologien kan systemet prøve å tilordne et ikke-unikt produktvariantnummer til en konfigurasjon. I så fall vil systemet bruke nummerserien for konfigurasjonsdimensjonen som produktvariantnummer i stedet. Hvis dette skjer, får du en advarsel. Hvis du vil unngå dette, bør du ta med nok attributter i terminologien til å sikre unikhet, og forsikre deg om at alternativet **Bruk på nytt** er merket av for komponenten.

### <a name="dimension-based-configurations"></a>Dimensjonsbaserte konfigurasjoner

Konfigurasjonsprosessen inneholder et trinn der systemet foreslår en konfigurasjonsverdi i henhold til terminologien. I dette trinnet kan du endre konfigurasjonsverdien manuelt. Når du lagrer konfigurasjonen, kontrolleres det om konfigurasjonsverdien er unik. Hvis ikke får du en feilmelding. Du må angi en unik konfigurasjonsverdi for å lagre konfigurasjonen.



<a name="see-also"></a>Se også
--------

[Opprette produktnummerterminologi for forhåndsdefinerte produktvarianter (oppgaveveiledning)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Opprette produktnummerterminologi for konfigurerte produktvarianter (oppgaveveiledning)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




