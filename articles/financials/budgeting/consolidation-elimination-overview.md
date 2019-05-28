---
title: Konsoliderings- og elimineringsoversikt
description: Denne artikkelen inneholder generell informasjon om konsoliderings- og elimineringsprosessen. Den inneholder svar på noen vanlige spørsmål.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c972b1a0b9be61875c17a05ce3ec8fce1ac5a4e0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572911"
---
# <a name="consolidation-and-elimination-overview"></a>Konsoliderings- og elimineringsoversikt

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder generell informasjon om konsoliderings- og elimineringsprosessen. Den inneholder svar på noen vanlige spørsmål.

Når du konsoliderer data, kombineres de økonomiske resultatene fra flere datterselskaper til resultater for ett konsolidert firma. Datterselskaper kan bruke forskjellige versjoner eller systemer, de eies kanskje ikke fullstendig og de bruker kanskje forskjellige valutaer. Det finnes flere alternativer for å konsolidere data:

-   **Konsolider på nettet** – Dette alternativet konsoliderer daglige saldoer etter valgte kontoer og dimensjoner, og lagrer dem i et konsolidert firma.
-   **Finansrapportering** – Dette alternativet konsoliderer transaksjoner og saldoer, og kan genereres når som helst. Du kan opprette flere hierarkinivåer, og du kan vise flere rapporteringsvalutaer.
-   **Konsolider med import** – Dette alternativet importerer saldoer til et konsolideringsfirma.
-   **Eksport av firmasaldoer** – Dette alternativet gir deg en eksportfil av firmasaldoer. Filen kan deretter importeres til andre forekomster eller systemer. Finansrapportering kan også brukes til å eksportere saldoene til en Microsoft Excel-fil.

Elimineringer kan rapporteres på flere måter:

-   Elimineringsregler kan defineres i systemet og deretter behandles i løpet av konsolideringsprosessen eller via et elimineringsforslag. Reglene kan posteres til alle firma som har valgt **Brukes til finanseliminering** under oppsettet av den juridiske enheten.
-   Et eget firma kan opprettes og brukes til å manuelt fastslå og postere elimineringstransaksjoner. Dette firmaet kan brukes i konsolideringsprosessen eller finansrapportering.
-   Kontoene og finansdimensjonene som brukes til å fastslå konsernintern aktivitet, kan filtreres på en raddefinisjon eller kolonnedefinisjon i Finansrapportering, og fullstendige funksjoner for neddrilling kan brukes. Beregnede kolonner og rader kan deretter brukes til å fjerne kontoer og finansdimensjoner fra en konsoliderte totalen.

Det finnes mange konsolideringsscenarier, og hver metode kan håndtere scenariene på forskjellige måter.

## <a name="frequently-asked-questions"></a>Vanlige spørsmål
1.  Jeg foretrekker å postere elimineringer i en database. Hvilke alternativer har jeg?

Du har flere alternativer. Du kan bruke alternativet **Konsolider på nettet** og ta med elimineringer i løpet av prosessen eller som et forslag. Transaksjonene posteres i det konsoliderte firmaet. Du kan eventuelt har et eget firma som du manuelt oppretter elimineringer i, og deretter kan du bruke dette firmaet i Finansrapportering eller i konsolideringsprosessen.

2.  Vi trenger våre konsoliderte resultater i flere rapporteringsvalutaer.

Alternativet **Finansrapportering** har ubegrenset antall rapporteringsvalutaer. Dataene oversettes under rapportgenerering, basert på valutakurstypen og valutaomregningsmetoden som angis for hovedkontoen. Alternativet **Konsolider på nettet** har imidlertid bare én rapporteringsvalutaen, det kreves et konsolidert firma for hver enkelt rapporteringsvaluta, hvis du bruker dette alternativet. Alternativet **Finansrapportering** er den anbefalte metoden.

3.  Jeg vil se detaljer på transaksjonsnivå for hvert firma.

Alternativet **Finansrapportering** er løsning fordi detaljer på transaksjonsnivå kan vises for så mange firmaer som er inkludert i rapporteringstredefinisjonen.

4.  Vi bruker budsjettplanlegging eller budsjettkontroll, og de må konsolideres.
Alternativet **Finansrapportering** er løsningen for å konsolidere budsjettplanlegging eller budsjettkontrolldata.

5.  Våre datterselskaper er spredt over hele verden, og vi har flere kontoplaner. Hva er den beste metoden for konsolidering av dataene våre?

Du har flere alternativer når du må håndtere flere kontoplaner. Du kan bruke alternativet **Konsolider på nettet** og deretter velge å bruke konsolideringskontoen som er definert for hovedkontoen, eller en konsolideringskontogruppe. Du kan også bruke alternativet **Finansrapportering**, inkludere flere koblinger til finansdimensjonene i raddefinisjonen og tilordne kontoene.

6.  Vi krever flere konsolideringsnivåer. Vi konsoliderer altså først vår europeiske datterselskaper til britiske pund (GBP). Deretter bruker vi disse dataene og oversetter det konsoliderte beløpet til amerikanske dollar. Hvordan kan vi gjøre dette?

Når det kreves flere konsolideringsnivåer og det brukes forskjellige valutaer på hvert nivå, må du bruke alternativet **Konsolider på nettet**. Det må opprettes flere konsolideringsfirmaer som har forskjellig regnskaps- og rapporteringsvalutaer. Konsolideringen må deretter kjøres flere ganger. Alternativet **Finansrapportering** oversetter alltid fra hvert kildefirmas regnskapsvaluta til den valgte valutaen.

7.  Vi har datterselskaper i et annet system. Hvordan kan vi konsolidere dem?

Bruk alternativet **Konsolider med import** for å bringe saldoene inn i et konsolideringsfirma.

8.  Noen av våre datterselskaper eies ikke fullstendig. Hva er den beste metoden for konsolidering av dem?

Du har flere alternativer for delvis eide datterselskaper. Du kan bruke alternativet **Finansrapportering** til å definere en rapporteringstredefinisjon og eierskapet. Du kan også bruke beregnede rader og kolonner som representerer det delvis eide beløpet. Du kan også vise minoritetsinteresser som en egen rad i en rapport. Du kan også bruke alternativet **Konsolider på nettet**. Kategorien **Juridiske enheter** har en **Eierskap**-kolonne der du kan definere prosentdelen som eies av hovedfirmaet.

9.  Organisasjonen vår må vise konsolideringer etter forretningsenhet eller ønsker å bruke organisasjonshierarkier.

Alternativet **Finansrapportering** er løsningen. Organisasjonshierarkier som har juridiske enheter eller finansdimensjoner i seg kan rapporteres i Finansrapportering. Du kan også opprette dine egne hierarkier med flere nivåer ved å bruke en rapporteringstredefinisjon som har en kombinasjon av juridiske enheter og dimensjonsverdier.

10. Vi har flere enn én forekomster av systemet.

Du kan konsolidere dataene ved å bruke alternativet **Eksport av firmasaldoer** til å eksportere fra én forekomst og deretter bruke alternativet **Konsolider med import** på den andre forekomsten.


Hvis du vil ha mer informasjon, se [Revaluering av valuta i et konsolideringsfirma](../general-ledger/currency-revaluation-consolidation-company.md).


