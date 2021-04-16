---
title: Vedlikeholdsprognoser
description: Dette emnet beskriver vedlikeholdsprognoser i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dd652af3100f8de59e06490443baeebca58a4dd3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838544"
---
# <a name="maintenance-forecasts"></a>Vedlikeholdsprognoser

[!include [banner](../../includes/banner.md)]



Når du oppretter en arbeidsordre, oppretter du arbeidsordrejobber med tilknyttede aktiva og vedlikeholdsjobbtyper. Når du velger en vedlikeholdsjobbtype som inneholder vedlikeholdsprognoser, kopieres prognosene automatisk til arbeidsordren.

Det kan hende at du kan legge til prognoselinjer i en arbeidsordre eller slette dem fra en arbeidsordre. Oppsettet for arbeidsordrelivssyklustilstanden, den tilknyttede prosjekttypen og stadiereglene som er knyttet til prosjekttypen, bestemmer om du kan legge til eller redigere prognoselinjer. Hvis du vil ha mer informasjon om livssyklustilstander for arbeidsordrer og relaterte prosjektstadier, kan du se [Prognoser, arbeidsordrer og prosjekter](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren i listen, og deretter, i handlingsruten > fanen **Arbeidsordre** > gruppen **Prosjekt** og deretter **Prognose**. Siden **Vedlikeholdsprognose for arbeidsordre** viser prognoselinjer fra vedlikeholdsjobbtypen som velges i arbeidsordrejobben.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Legge til prognose for timer i en arbeidsordre

1. På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.

2. På hurtigfanen **Timer** velger du **Legg til** for å opprette en ny linje.

3. Velg en kategori i feltet **Kategori**.

4. Sett inn antall prognosetimer i **Timer**-feltet.

5. I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.


## <a name="add-an-items-forecast-to-a-work-order"></a>Legge til prognoser for varer i en arbeidsordre

Det er tre måter å legge til varer i en vedlikeholdsprognose for arbeidsordre. Du kan opprette linjer for varer (reservedeler) som ikke er inkludert i reservedellisten eller stykklisten for aktiva, du kan velge reservedeler fra listen over godkjente reservedeler, eller du kan velge varer fra stykklisten for aktiva.

- På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.

- I hurtigfanen **Varer** legger du til varer i vedlikeholdsprognosen ved å bruke den riktige metoden.

For å opprette en linje for en reservedel som ikke er i reservedellisten eller stykklisten for aktiva, følger du disse trinnene:

1. Velg **Legg til**.
2. Velg varen i **Varenummer**-feltet.
3. Angi antallet i **Salgsantall**-feltet.
4. I **Enhet**-feltet velger du måleenheten for antallet.
5. I feltene **Kostpris** og **Valuta** angir du riktige verdier.
6. I feltet **Linjeegenskap** velger du en linjeegenskap.
7. Hvis du vil endre listen over dimensjoner som vises på varelinjene, velger du **Lager** > **Visningsdimensjoner**, velger dimensjonene, og deretter setter du **Lagre oppsett** til **Ja**.

Hvis du vil legge til en reservedel fra en godkjent reservedelsliste, følger du denne fremgangsmåten:

1. Velg **Legg til reservedeler**.
2. Velg reservedelen, og rediger den tilknyttede informasjonen slik du ønsker.
3. Velg **OK**.

Følg denne fremgangsmåten for å legge til en vare fra stykklisten for aktiva:

1. Velg **Legg til stykklistevarer**.
2. Velg varen, og rediger den tilknyttede informasjonen slik du ønsker.
3. Velg **OK**.

Hvis du vil ha en oversikt som viser hvor varen på den valgte linjen brukes i forhold til aktiva, vedlikeholdjobbtypestandarder, reservedeler og arbeidsordrer i Aktivastyring, velger du **Vare der brukt**. Hvis du vil ha mer informasjon om denne oversikten, kan du se [Brukssted for vare](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Legge til en utgiftsprognose i en arbeidsordre

1. På siden **Prognose for vedlikehold av arbeidsordre** velger du arbeidsordrejobben du vil legge til en prognose i.

2. På hurtigfanen **Utgift** velger du **Legg til** for å opprette en linje.

3. Velg en kategori i feltet **Kategori**.

4. Angi antallet i **Antall**-feltet.

5. I feltene **Kostpris**, **Salgsvaluta** og **Salgspris** angir du de gjeldende verdiene.

6. I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.

>[!NOTE]
>Hurtigfanen **Totaler for vedlikeholdsprognose** viser en oversikt over antall linjer som er opprettet, for den valgte arbeidsordrejobben og for arbeidsordren, på hver hurtigfane. Den viser også totale prognosearbeidstimer for arbeidsordrejobben og arbeidsordren.

Illustrasjonen nedenfor viser et eksempel på siden **Prognose for vedlikehold av arbeidsordre**.

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatisk oppdatering av arbeidsordreprognoser

Hvis timekostnader, varekost og utgifter oppdateres i andre moduler i Microsoft Dynamics 365 for Finance and Operations, kan arbeidsordreprognoser i Aktivastyring oppdateres automatisk for å reflektere disse endringene. Denne funksjonaliteten garanterer at de siste kostprisene alltid brukes i arbeidsordreprognosene. Du kan også gjøre lignende oppdateringer for [vedlikeholdsjobbtypeprognoser](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Velg **Aktivastyring** > **Periodisk** > **Prognose** > **Oppdater arbeidsordreprognose**.

2. I dialogboksen **Oppdater arbeidsordreprognose** på hurtigfanen **Poster som skal inkluderes** kan du legge til valg for bestemte arbeidsordrer eller arbeidsordrejobber, etter behov. Klikk på **Filter** for å gjøre de relevante valgene.

3. På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, slik du ønsker.

4. Velg **OK** for å starte prognoseoppdateringen.


Illustrasjonen nedenfor viser et eksempel på dialogboksen **Oppdater arbeidsordreprognose**.

![Figur 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]