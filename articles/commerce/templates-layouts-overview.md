---
title: Oversikt over maler og oppsett
description: Dette emnet dekker maler og oppsett i Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d805c39b77d653eaa9935751ae89012c98b930d2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414759"
---
# <a name="templates-and-layouts-overview"></a>Oversikt over maler og oppsett


[!include [banner](includes/banner.md)]

Maler er et grunnleggende element i Microsoft Dynamics 365 Commerce-sidemodellen. Hvis målet er å oppnå størst mulig effektivitet og konsekvens for arbeidsflyter for områderedigering, er det viktig at du lærer deg hvordan du kan dra nytte av maler for webområdet ditt. Tidlige avgjørelser om malstruktur er viktig og kan påvirke kostnadene og fleksibiliteten for daglige, sesongbaserte og områdeomfattende merkeoppdateringer. Godt strukturerte maler har også andre fordeler. De hjelper for eksempel med å forbedre resultatene av søkemotoroptimalisering (SEO) på tvers av hele området og minimere antall feil.

En god måte å begynne å arbeide med maler på er å forstå de funksjonelle fordelene med maler og oppsett, forskjellen mellom dem og hierarkiet.

Følgende illustrasjon viser sidemodellhierarkiet bak en gjengitt webside.

![Diagram for sidemodell](../commerce/media/page-model-diagram.png)

| Enhet        | Basisfunksjon |
|---------------|----------------|
| Mal      | Maler definerer modulalternativene og grunnstruktur for et sett med oppsett og sideforekomster. |
| Utseende        | Oppsett definerer det endelige utvalget og ordningen av moduler for en side eller et sett med sider. |
| Sideforekomst | Sideforekomster definerer dataene og innholdet for bestemte sider. |

## <a name="templates"></a>Maler

Maler er øverst i Dynamics 365 Commerce-sidemodellhierarkiet og representerer et viktig tidlig trinn for områdekonfigurasjonen. Begrepsmessig bidrar maler til å kontrollere konsekvens på tvers av en serie med underordnede oppsett og sider ved å definere basisstrukturen og redigeringsalternativer for nedstrøms arbeidsflyter for oppsett- og sideoppretting. Maler kan bidra til å forenkle innholdsredigeringsprosessen gjennom forhåndsdefinerte, sentralt behandlede elementer (for eksempel topptekst og bunntekst) og styrte redigeringsflyter som bidrar til å garantere at modulkonfigurasjonsvalgene er merkevarebaserte.

### <a name="controlling-consistency"></a>Kontrollere konsekvens

Når du utformer en mal, er den største forretningsbeslutningen du må angi, hvor mye kontroll malen skal ha på sidenopprettingsprosessen. En mal som lar alt stå åpent for en nedstrømsforfatter, er den enkleste typen mal du kan opprette, men den kan ha langsiktig konsekvens når det gjelder vedlikehold av sider som opprettes fra den. En velskrevet mal gir veiledning og en strømlinjeformet redigeringsopplevelse, men den gir også tilstrekkelig fleksibilitet slik at redigerere kan fullføre oppgaven. Alle disse aspektene avhenger av kontrollnivået som malen fremtvinger.

Maler kan hjelpe innholdsforfattere til å være mer effektive og merkevarebaserte på følgende måter:

- Begrenser modulene som kan brukes på en side.
- Foreslå standard modul- og konfigurasjonsvalg.
- Eksplisitt foreta enkelte modul- og konfigurasjonsvalg som styres på malnivået. Denne prosessen kalles også å *låse* en innstilling.

Følgende eksempel viser hvordan en grunnleggende mal (mal X) kan konfigureres:

- Alle underordnede oppsett for mal X må ha en topptekstcontainer, en brødtekstcontainer og en bunntekstcontainer.
- I mal X er konfigurasjonen av topptekstcontaineren låst og kan bare endres i selve mal X. Alle underordnede oppsett og sider har alltid denne toppteksten.
- Brødtekstcontaineren krever minst én modul og opptil maksimalt ti moduler. Disse modulene defineres ved hjelp av nedstrøms oppsett og sider.
- For brødtekstcontaineren er modulene hero, funksjonen, karusell og banner tilgjengelige.
- En bunntekstcontainer er mal X, men den kan overstyres av nedstrøms oppsett og sider.

Malen i dette eksemplet definerer en enkel struktur og et sett med alternativer for nedstrøms innholdsforfattere. Legg merke til at noen deler av en side (i dette tilfellet toppteksten) er fullstendig definert og låst i malen, og at de ikke kan endres av nedstrømsforfattere. Andre deler (i dette tilfellet brødteksten) kan være definert av nedstrømsforfattere i bestemte retningslinjer (i dette tilfellet et minimumsantall og maksimumsantall moduler og spesifikke typer). Og andre deler (i dette tilfellet bunnteksten) er definert i malen, men kan overstyres av nedstrømsforfattere.

Et viktig utgangspunkt for område- og varemerkeadministratorer er å fastslå riktig balanse mellom begrensning og fleksibilitet for underordnede oppsett og sideforfattere. Når det brukes maler, er denne saldoen fullstendig konfigurerbar. Det påvirker om sideelementer er sentralt oppdatert (låst i malen) eller overlatt til individuelle underordnede nivåer som er lavere i sidehierarkiet.

For å begynne å bruke maler, [Arbeide med maler](work-with-templates.md).

## <a name="layouts"></a>Oppsett

Oppsett er det neste nivået i sidemodellhierarkiet, under maler. En mal definerer alle modulene som er tillatt for en side, et oppsett er et eksplisitt utvalg og en ordning av moduler. Sider er det neste nivået i sidemodellhierarkiet, under oppsett. De definerer det lokaliserte innholdet for modulene som er valgt i oppsettet.

Eksemplet nedenfor bygger på maleksemplet fra den forrige delen og viser hvordan et grunnleggende oppsett kan konfigureres:

- Den overordnede malen for oppsettet krever at brødtekstcontaineren har mellom én og ti moduler. Disse modulene kan bare være hovedbanner, funksjon, karusell og banner. Derfor kan oppsettet definere følgende utvalg og ordning av moduler:

    - Den første modulen i brødtekstcontaineren er en bannermodul, og den etterfølges av en hovedbannermodul og to funksjonsmoduler.
    - Den første funksjonsmodulen er venstrejustert, og den andre funksjonsmodulen er høyrejustert.

- Selv om en standard bunntekst arves fra den overordnede malen, er den venstre bunnteksten låst opp av malforfatteren. Derfor kan oppsettet overstyre den ved å definere et annet bunntekstfragment.

Oppsettet i dette eksemplet definerer den endelige ordningen av moduler for underordnede sider. I likhet med en mal kan et oppsett definere standard eller låste modulegenskaper som alltid vil bli arvet av underordnede sider (for eksempel justeringen av funksjonsmodulene). Det faktiske innholdet eller dataene for hver modul i oppsettet defineres deretter lengre nedover i hierarkiet, på hver forekomst av underordnet side. En viktig forskjell her er at oppsett ikke inneholder direkte lokalisert innhold, mens underordnede sider gjør det. Hovedfunksjonen for oppsettet er å definere den endelige ordningen og standardkonfigurasjonen for moduler for de underordnede sidene.

Dette hierarkiet er kraftig av to årsaker. For det første blir oppsett som deler den samme overordnede malen, behandlet som kompatible for scenarier med oppsettsveksling. Derfor kan oppsettet for en hvilken som helst side endres til et annet oppsett fra samme malhierarki, uten å kreve at innholdet på sidenivå blir redigert på nytt. Du kan dra nytte av denne funksjonen for å utføre oppdateringer av sesongdesign, eksperimentere eller utføre en permanent omforming av området. For det andre gir oppsett en annen metode for å endre delte elementer sentralt for en gruppe med sider uten å kreve oppdatering av enkelt sider. Hvis en produktkategori for eksempel har 1 000 sider som har samme oppsett, kan modulene sorteres på nytt i oppsettet, og denne endringen vil umiddelbart gjenspeiles på alle 1 000 underordnede sider.

Ved å forstå dette hierarkiet kan du levere en smidig og effektiv områdestruktur som bidrar til å spare kostnader, er skalerbar og gir bedre resultater fordi området utvikler seg over tid.

### <a name="preset-and-custom-layouts"></a>Forhåndsinnstilte og egendefinerte oppsett

Oppsett på området kan enten være *forhåndsinnstilte* eller *egendefinerte*:

- **Forhåndsinnstilte oppsett** tillater en arbeidsflyt for sideoppretting der alle moduler allerede er valgt og ordnet, og bare dataregistrering er nødvendig. Denne fremgangsmåten kan spare tid når mange sider må forfattes med de samme oppsettskravene. Forhåndsinnstilte oppsett har en én-til-mange-relasjon til de underordnede sidene. Derfor kan et enkelt forhåndsinnstilt oppsett brukes til å styre modulordningen for hundrevis eller tusenvis av underordnede sider sentralt.
- **Egendefinerte oppsett** er hovedsakelig engangsoppsett som er innebygd på én side. De vises ikke som et alternativ når andre nye sider opprettes, eller i scenarier med oppsettsveksling. Fordelen med denne fremgangsmåten er at en forfatter kan eksperimentere ved å redigere en side som bruker et egendefinert oppsett. Hvis forfatteren ønsker å bruke utformingen på nytt for andre sider, kan det enkelt konverteres til et forhåndsdefinert oppsett. Det nye forhåndsdefinerte oppsettet vises deretter som et alternativ i arbeidsflyter for sideoppretting og i scenarier med oppsettsveksling for sider fra samme malhierarki. Forhåndsinnstilte oppsett kan derimot være forgreninger til egendefinerte oppsett. På denne måten kan en forfatter bryte en side bort fra det forhåndsinnstilte oppsettet og opprette et nytt egendefinert engangsoppsett. (Dette nye egendefinerte oppsettet er fremdeles bundet av begrensninger i den overordnede malen.)

Forhåndsinnstilt oppsett og egendefinerte oppsett redigeres i forskjellige deler av redigeringsverktøysettet. Siden egendefinerte oppsett ikke har noen avhengigheter til andre sider, redigeres de direkte i sideredigeringsprogrammet. I dette tilfellet er utformingen for det meste synlig for brukeren, og vises bare i egenskaper på sidenivå og gjennom handlingene for oppsettalternativer. Siden endringer i forhåndsinnstilte oppsett kan påvirke mange underordnede sider, må de redigeres i redigeringsprogrammet for oppsett, der publiseringshandlinger kan vurdere den fullstendige nedstrømsvirkningen på underordnede sider.

Følgende illustrasjoner viser scenarier for forhåndsinnstilte og egendefinerte oppsett.

![Forhåndsinnstilte og egendefinerte oppsettsscenarier](../commerce/media/template-figure1.png)

Hvis du vil begynne å bruke forhåndsinnstilte oppsett, se [Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Arbeide med maler](work-with-templates.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)

[Arbeide med publiseringsgrupper](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]