---
title: Frigi stykkliste- og formellinjer til lageret
description: Dette emnet beskriver prosessen for frigivelse av råvarer for stykklistelinjer og formellinjer til lageret.
author: johanhoffmann
manager: tfehr
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm, ProdParmReleaseToWarehouse, WHSReleaseToWarehouseProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: bf2beef30ba1cf6877325e686b76de5dc8d3ba55
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017236"
---
# <a name="release-bom-and-formula-lines-to-the-warehouse"></a>Frigi stykkliste- og formellinjer til lageret

[!include [banner](../includes/banner.md)]

Dette emnet beskriver prosessen for frigivelse av råvarer for stykklistelinjer og formellinjer til lageret. Når du frigir en stykkliste- eller formellinje til lageret, kontrollerer systemet først om materialet allerede er tilgjengelig for produksjonsinnleveringsstedet i produksjonslokalet der materialene brukes i produksjonsprosessen.

- Hvis materialene er tilgjengelige på produksjonsinnleveringsstedet, plukkes de fra dette stedet umiddelbart etter at signalet er gitt for frigivelse av materialer til lageret.
- Hvis materialet ikke er tilgjengelig på produksjonsinnleveringsstedet, angir materialfrigivelsen at materialet må flyttes fra lokasjonene på lageret til produksjonsinnleveringsstedet. Materialet flyttes via lagerarbeid for råvareplukking. Derfor må lagerprosesser for råvareplukking konfigureres. Hvis du vil ha mer informasjon, kan du se [Oversikt over etterfylling](../warehousing/replenishment.md) og [Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver](../warehousing/control-warehouse-location-directives.md).

## <a name="methods-for-releasing-bom-and-formula-lines"></a>Metoder for å frigi stykkliste- og formellinjer

Du kan konfigurere frigivelsen av stykkliste- og formellinjer slik at den skjer som en del av frigivelsen av en produksjonsordre eller partiordre. Frigivelsen kan også styres av en satsvis jobb eller utføres som en manuell samhandling.

Metoden som brukes for å frigi stykkliste- og formellinjer styres av **Frigivelse av produksjonslinje** -parameteren. Du finner denne parameteren i **Produksjonskontroll** \> **Oppsett** \> **Produksjonsparametere**.

- **Frigi stykkliste- og formellinjer som en del av produksjons- eller partordrefrigivelse** – I denne metoden frigis stykkliste- og formellinjer for en produksjons- eller partiordre som en del av prosessen med å frigi ordren. Vanligvis under frigivelsen av en produksjons- eller partiordre, frigis produksjonsjobber frigis til produksjonsarbeiderne og produksjonspapirer skrives ut. Under denne prosessen endres også ordrens status til **Frigitt**.
- **Frigi stykkliste- og formellinjer via en partijobb eller som en manuell samhandling** – I denne metoden kan stykkliste- og formellinjer bare frigis gjennom **Automatisk frigivelse av stykklister og formellinjer** -partijobben eller som en manuell samhandling. Hvis du vil frigi manuelt stykkliste- og formellinjer, velger du **Frigi til lager** på produksjonsordrelistesiden eller produksjonsordredetaljsiden i handlingsruten.

For en rask demonstrasjon av hvordan du frigir stykkliste- og formellinjer til produksjon ved hjelp av en satsvis jobb, kan du se denne korte YouTube-videoen: [Frigi produksjonsplukking til lageret satsvis](https://www.youtube.com/watch?v=8urAJn50dQ8).

## <a name="releasing-the-bom-and-formula-lines-by-using-a-batch-job"></a>Frigi stykkliste- og formellinjer ved hjelp av en partijobb

**Automatisk frigivelse av stykklister og formellinjer** -partijobben går gjennom valgte stykkliste- og formellinjer som har et restantall som skal frigis. Jobben vurderer bare ordrer med statusen **Frigitt** , **Startet** eller **Ferdigmeldt**. Hvis en stykkliste- eller formellinje har et restantall som skal frigis, frigir jobben opptil antallet som kan dekkes av antallet som allerede er fysisk reservert, og antallet som er fysisk tilgjengelig.

### <a name="example-of-a-batch-job-release"></a>Eksempel på frigivelse av partijobb

| Scenario | Restantall som skal frigis | Fysisk reservert antall | Fysisk tilgjengelig antall | Antall frigitt av partijobben |
|----------|-------------------------------|------------------------------|-------------------------------|------------------------------------|
| 1        | 100                           | 20                           | 90                            | 100                                |
| 2        | 100                           | 20                           | 70                            | 90                                 |
| 3        | 100                           | 0                            | 90                            | 90                                 |
| 4        | 100                           | 0                            | 110                           | 100                                |
| 5        | 100                           | 20                           | 0                             | 20                                 |

### <a name="batch-job-setup"></a>Oppsett av partijobb

I spørringen for **Automatisk frigivelse av stykkliste- og formellinjer** -partijobben kan du definere et filterkriterium for å angi hvor mange dager fremover jobben skal se etter linjer som har ikke-frigitt antall. I spørringen for jobben, i **Råvaredato** -feltet, bruker du **(LessThanDate())** -funksjonen som et filterkriterium.

Illustrasjonen nedenfor viser en produksjonsordre som har to jobber, 10 og 20, som dekker monteringen og pakkingen for produksjonsordren. Hver jobb er konfigurert til å bruke et antall materialer. I denne illustrasjonen er frigivelseshorisonten som er angitt ved den grønne pilen under tidslinjen,lik antall dager som er angitt i **(LessThanDate())** -kriteriet. For eksempel, **(LessThanDate(2))** angir at jobben bare skal se etter ikke-frigitte antall innenfor en horisont på to dager.

![Eksempel på en produksjonsordre som har to partijobber](media/bach-job-setup.PNG)

## <a name="releasing-material-per-operation-number-or-in-proportion-to-the-amount-of-finished-goods"></a>Frigi materiale per operasjonsnummer eller i forhold til mengde ferdigvarer

Hvis du frigir materiale ved hjelp av **I frigivelse av produksjonsordre** -parameterinnstillingen, har du to alternativer for å kontrollere materialfrigivelsen når du foretar en manuell frigivelse:

- Frigi materiale per operasjonsnummer.
- Frigi materiale i forhold til mengde ferdigvarer.

### <a name="release-material-per-operation-number"></a>Frigi materiale per operasjonsnummer

Hvis du vil kontrollere operasjonene som materialet skal frigis til, bruker du **Frigi til lager** -siden.

- Velg **Produksjonskontroll** \> **Produksjonsordrer** \> **Alle produksjonsordrer** , velg en produksjonsordre, og velg deretter **Frigi til lager** i fanen **Lager**. Bruk deretter **Fra oper.nr.** - og **Til oper.nr.** -feltet for å angi intervallet med operasjonsnumre.

Illustrasjonen nedenfor viser en produksjonsordre som har to operasjoner, 10 og 20. I dette eksemplet, hvis du begrenser frigivelsen til operasjon 10, frigis bare materiale M9203.

![Eksempel på frigivelse av materiale per operasjonsnummer](media/two-operations.PNG)

For en rask demonstrasjon av hvordan du frigir materiale i forhold til mengde ferdigvarer, kan du se denne korte YouTube-videoen om [forbedringer i frigivelsesprosessen for produksjonsordrer](https://www.youtube.com/watch?v=Rm3ojAz6Zu0).

### <a name="release-material-in-proportion-to-the-amount-of-finished-goods"></a>Frigi materiale i forhold til mengde ferdigvarer

Du kan frigi råvarer for en delvis mengde ferdigvarer eller i en bestemt enhet.

- Hvis du vil fri råvarer for en delvis mengde ferdigvarer, velger du **Produksjonskontroll** \> **Produksjonsordrer** \> **Alle produksjonsordrer** , velger en produksjonsordre, og velger deretter **Frigi til lager** i fanen **Lager**. Angi deretter et antall i **Antall** -feltet.

    For eksempel, en produksjonsordre opprettes og planlegges for 1 000 stykker (stk.). Arbeidslederen planlegger produksjonen av 100 stk. for neste skift og ønsker å frigi materialer bare for dette skiftet. I dette tilfellet kan lederen bruke **Antall** -feltet for å frigi materialer for 100 stk. som er planlagt for det neste skiftet.

- Hvis du vil frigi råvarer i en bestemt enhet, velger du **Produksjonskontroll** \> **Produksjonsordrer** \> **Alle produksjonsordrer** , velger en produksjonsordre, og velger deretter **Frigi til lager** i fanen **Lager**. Bruk deretter **Enhet** -feltet for å velge enheten med ferdigvare for å frigi materiale i.

    Enhetene som er tilgjengelige, er definert i enhetssekvensgruppe-ID-en for den ferdige varen.

    En ferdigvare har for eksempel følgende enhetsomregning mellom pund (lbs.) og pall (PL): 1 PL = 100 lbs. Hvis du vil opprette en produksjonsordre for 10 000 lbs. med ferdigvare, kan du frigi råvarer for antallet paller som du planlegger å produsere. Velg **PL** som enhet, og velg deretter et tilsvarende tall i **Antall** -feltet.
