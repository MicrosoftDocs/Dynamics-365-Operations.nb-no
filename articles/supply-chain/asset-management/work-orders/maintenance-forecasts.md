---
title: Vedlikeholdsprognoser
description: Dette emnet beskriver vedlikeholdsprognoser i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875822"
---
# <a name="maintenance-forecasts"></a>Vedlikeholdsprognoser

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Når du oppretter en arbeidsordre, oppretter du arbeidsordrejobber med tilknyttede aktiva og vedlikeholdsjobbtyper. Når du velger en vedlikeholdsjobbtype som inneholder vedlikeholdsprognoser, kopieres prognosene automatisk til arbeidsordren.

Du kan kanskje legge til eller slette prognoselinjer i en arbeidsordre. Oppsettet for en arbeidsordrelivssyklustilstand, den tilknyttede prosjekttypen og stadiereglene knyttet til prosjekttypen bestemmer om du kan legge til eller redigere prognoselinjer. 

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren i listen, og klikk på **Prognose**. I **Vedlikeholdsprognose for arbeidsordre** vises prognoselinjer fra vedlikeholdsjobbtypen som er valgt i arbeidsordrejobben.


## <a name="add-hours-forecast-to-a-work-order"></a>Legge til prognose for timer i en arbeidsordre

1. Velg arbeidsordrejobben som du vil legge til en prognose for.

2. På hurtigfanen **Timer** klikker du på **Legg til** for å opprette en ny linje.

3. Velg en kategori i **Kategori**-feltet.

4. Sett inn antall prognosetimer i **Timer**-feltet.

5. I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.


## <a name="add-items-forecast-to-a-work-order"></a>Legge til prognose for varer i en arbeidsordre

Det finnes tre måter å legge til varer på i en vedlikeholdsprognose for arbeidsordre: Du kan opprette linjer for varer (reservedeler) som ikke er inkludert i reservedellisten eller stykklisten for aktiva, du kan velge reservedeler fra listen over godkjente reservedeler, og du kan velge varer fra stykklisten for aktiva.

1. Velg arbeidsordrejobben som du vil legge til en prognose for.

2. Velg hurtigfanen **Varer**.

3. Klikk på **Legg til** for å opprette en ny linje for en reservedel som ikke er i reservedellisten eller stykklisten for aktiva.

4. Velg varen i **Varenummer**-feltet.

5. Sett inn antall i **Salgsantall**-feltet, og velg en antallsenhet i **Enhet**-feltet.

6. Sett inn kostpris og valuta i de relevante feltene, og velg en **Linjeegenskap**.

7. Hvis du vil endre listen over dimensjoner som vises på varelinjene, kan du klikke på **Lager** > **Visningsdimensjoner**, velge dimensjonene og velge Ja på veksleknappen **Lagre oppsett**.

8. Hvis du vil legge til en godkjent reservedel i vedlikeholdsprognosen, klikker du på **Legg til reservedeler**, velger reservedelen, redigerer relatert informasjon om nødvendig, og klikker på **OK**.

9. Hvis du vil legge til stykklistevarer for aktiva i prognosen, klikker du på **Legg til stykklistevarer**, velger varen, redigerer relatert informasjon hvis nødvendig, og klikker på **OK**.

10. Klikk på **Vare der brukt** hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, vedlikeholdsjobbtypestandarder, reservedeler og arbeidsordrer. 



## <a name="add-expense-forecast-to-a-work-order"></a>Legge til utgiftsprognose i en arbeidsordre

1. Dette emnet forklarer hvordan du legger til en utgiftsprognose i en arbeidsordre. Til venstre i skjemaet velger du arbeidsordrejobben du vil legge til en prognose i.

2. Velg hurtigfanen **Utgift**.

3. Klikk på **Legg til** for å opprette en ny linje.

4. Velg en kategori i **Kategori**-feltet.

5. Sett inn antallet i **Antall**-feltet.

6. Sett inn kostpris, salgsvaluta og salgspris i de relevante feltene.

7. I **Linjeegenskap**-feltet velger du tilleggstypen som skal brukes på linjen.

>[!NOTE]
>I hurtigfanen **Totaler for vedlikeholdsprognose** får du en oversikt over antall linjer som er opprettet i hver kategori, for den valgte arbeidsordrejobben og for arbeidsordren. Du kan også se en sum for prognosearbeidstimer for arbeidsordrejobben og for arbeidsordren.

![Figur 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatisk oppdatering av arbeidsordreprognoser

I Aktivastyring kan du automatisk oppdatere eventuelle endringer i arbeidsordreprognoser for timekostnader, varekost og utgifter som er oppdatert i andre moduler i Dynamics 365 for Finance and Operations. Dette gjøres for å sikre at de siste kostprisene alltid brukes i arbeidsordreprognosene. Det er også mulig å utføre lignende oppdateringer for [vedlikeholdsjobbtypeprognoser](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Klikk på **Aktivastyring** > **Periodisk** > **Prognose** > **Oppdater arbeidsordreprognose**.

2. I rullegardinlisten **Oppdater arbeidsordreprognose** kan du legge til valg for bestemte arbeidsordrer eller arbeidsordrejobber om nødvendig. Klikk på **Filter** for å gjøre disse valgene.

3. På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, om nødvendig.

4. Klikk på **OK** for å starte prognoseoppdateringen.


![Figur 2](media/07-work-orders.png)

