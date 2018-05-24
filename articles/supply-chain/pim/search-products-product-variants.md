---
title: "Søk etter produkter og produktvarianter under ordreregistrering"
description: "Bruk feltet **Varenummer** til å søke etter produkter og produktvarianter når du oppretter en salgsordrelinje eller en bestillingslinje manuelt. Dermed kan du raskt finne produktvarianter når du bare har konfigurasjonsstrengen eller én av produktdimensjonene tilgjengelige."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d6a45d89ba20994c06a77c646fa5099fa34b3b2e
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Søk etter produkter og produktvarianter under ordreregistrering

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

Bruk feltet **Varenummer** til å søke etter produkter og produktvarianter når du oppretter en salgsordrelinje eller en bestillingslinje manuelt.  Dermed kan du raskt finne produktvarianter når du bare har konfigurasjonsstrengen eller én av produktdimensjonene tilgjengelige.

Noen ganger er det å ha for mye av noe ikke den beste situasjonen å være i, og dette er spesielt viktig hvis du selger en rekke produkter som er like, og du samtidig prøver å huske varenumre eller navn i produktsøk for å finne det riktige produktet til en salgsordre. Du kan bruke feltet **Varenummer** på en salgsordrelinje eller en bestillingslinje som et søkefelt. Du kan angi en del av et produktnavn, tall eller dimensjon og få et oppslag som viser alle elementene som samsvarer med søkeordet.

## <a name="how-search-works"></a>Slik fungerer søket
Når du søker etter produkter og produktvarianter, er det viktig å forstå hvordan søkefunksjonen finner produktene som samsvarer med teksten du angir. De viktigste søkereglene for å levere søkeresultater er:

-   Søkeresultatene vil returnere en samsvarende post, uavhengig av feltet som søketeksten er angitt i.
-   Søketeksten må finnes i den tilsvarende posten i sin hele lengde.
-   Samsvar oppstår selv om det finnes tekst midt i en tekststreng i den tilsvarende posten. Den trenger ikke vises i begynnelsen av en tekststreng.
-   Søketeksten behandles som en tekststreng, selv om den inneholder mellomrom.

### <a name="examples"></a>Eksempler

Følgende eksempler bruker produkter og produktvarianter som illustrerer hvordan søk skal håndteres i ulike scenarier. **Forutsetning:** Under **Salg og markedsføring &gt; Oppsett &gt; Søk &gt; Søkeparametere &gt; Søketype** velger du alternativet **Fullstendig samsvar**.

| Produkttype     | Produktnavn    | Visningsproduktnummer | Varenummer | Konfigurasjon |
|------------------|-----------------|------------------------|-------------|---------------|
| Spesifikt produkt | SpeakerMidRange | D0001                  | D0001       | I/T            |
| Produktvariant  | Aktiv høyttaler  | D0010:::Svart:         | D0010       | 000005        |
| Produktvariant  | Aktiv høyttaler  | D0010:::Hvit:         | D0010       | Hvit         |

Hvis du skriver inn "snakke" i feltet **Varenummer**, vil du få alle produkter ovenfor som et resultat i oppslaget. Hvis du skriver inn "svart i feltet **Varenummer**, får du det andre produktet som et resultat fordi det ikke har "svart" i visningen av produktnummer. Disse to eksemplene viser at søket ikke er bare er i begynnelsen av feltet. Samsvar skjer selv om søketekst finnes midt i en tekststreng den tilsvarende posten.  

Hvis du skriver inn "05", får du bare den andre produktvarianten som resultat fordi den har "05" i konfigurasjonen. Dette viser at det søkes på tvers av alle de aktiverte feltene på siden **Søkekriterier**.  

Hvis du skriver inn "snakke 05", vil du ikke får noen treff. Dette skyldes at det søkes etter den fullstendige teksten som er angitt. Søket prøver ikke å finne "snakke", avgrenser deretter resultatene til de som inneholder "05".  

Du kan begrense antallet søkeresultater ved å bruke feltet **Antall resultater** på siden **Salg og markedsføring &gt; Oppsett &gt; Søk &gt; Søkeparametere**. Hvis du setter dette feltet til 0, returneres alle søkeresultatene. Hvis du setter det til 10, returneres det for eksempel maksimalt 10 søkeresultater.

## <a name="configure-the-product-search"></a>Konfigurere produktsøket
Før du kan bruke søkefunksjonen for produktet og produktvarianten, følger du denne fremgangsmåten for å konfigurere produktsøket. [![3 trinn for å konfigurere produktsøk\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Trinn 1: Ta med ID-er og dimensjoner for alle relevante produkter og produktvarianter i søkekriteriene

Eksempler på ID-er og dimensjoner for produkter og produktvarianter som du kan søke etter, er **Produktnavn, Varenummer**, **Visningsproduktnummer, Konfigurasjon, Farge, Størrelse, Stil, Søkenavn osv**.  

Gå til siden **Salg og markedsføring &gt; Oppsett &gt; Søk &gt; Søkekriterier**. På siden **Søkekriterier** kan du definere kriterier for kunde, kundeemne og produktsøk. Sørg for at du filtrerer siden ved å bruke produktsøkekriterier. Du kan gjøre dette ved å bytte til **Produkt** på menyen på siden.  

Hvis du vil legge til visningsproduktnummer i søkekriteriene, klikker du på **Ny** på menyen på siden. Dermed legges det til en ny post i rutenettet **Søkekriterier**. Åpne kolonneoppslaget **Feltnavn** og velg **Visningsproduktnummer**. Hvis du vil legge til produktets konfigurasjon i søkekriteriene, kan du opprette en ny post i rutenettet **Søkekriterier** og velge **configId** i kolonnen **Feltnavn**. På samme måte kan du opprette en post med **InventColorId** i **Feltnavn** for fargedimensjonen, **InventSizeId** for størrelsesdimensjonen og **InventStyleId** for stildimensjonen.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Trinn 2: Fylle ut databasetabellen som skal brukes for produktsøk

På siden **Søkekriterier** klikker du knappen **Oppdater søkedata**. I dialogboksen **Oppdater søkedata** kontrollerer du at **Kilde** er satt til **Produkt** og klikker deretter **OK**. Systemet vil slå sammen alle søkekriterier som er angitt i trinn 1, i én tabell. Hvis du har mange produkter og produktvarianter, kan denne operasjonen ta ganske lang tid, og du mottar kanskje en advarsel. Det anbefales at du planlegger utfylling av søketabellen på den satsvise serveren på et tidspunkt da serveren ikke er for opptatt.  

Inntil tabellen fylles ut, vil ikke produktsøk gi riktige resultater. Hvis du ikke får noen søkeresultater, må du sørge for at denne tabellen fylles ut.  

Tabellen trenger bare fylles ut når søkekriteriene blir endret. Nylig utgitte produkter og varianter legges automatisk til i tabellen. Slettede produkter og varianter fjernes automatisk fra tabellen.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Trinn 3: Aktivere oppslag for produktsøk på salgs- og bestillingslinjer

Du kan aktivere denne funksjonaliteten ved å gå til **Salg og markedsføring &gt; Oppsett &gt; Søk &gt; Søkeparametere** og sette **Aktiver oppslag for søk** til **Ja** i kategorien **Generelt**.  

For salgsordreregistrering er standard atferd å åpne siden **Produktsøk** når du begynner å skrive i feltet **Varenummer**, og deretter trykker du **Tab**-tasten. Siden **Produktsøk** endrer konteksten under oppretting av ordrelinjer, og kan anses som unødvendig påtrengende. Hvis du foretrekker å få søkeresultatene i et oppslag og ikke miste kontekst under ordrelinjeregistrering, kan du i stedet bruke søkeoppslaget. Hvis du søker etter et produkt eller en produktvariant, men ikke velger noe i oppslaget og trykker **Tab**-tasten, vises siden **Produktsøk**.




