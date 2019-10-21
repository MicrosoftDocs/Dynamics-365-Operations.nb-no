---
title: Registrere forbruk
description: Dette emnet forklarer hvordan du registrerer forbruk i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024666"
---
# <a name="register-consumption"></a>Registrere forbruk

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Når en vedlikeholdsjobb er fullført i en arbeidsordre, er neste trinn å gjøre forbruksregistreringer og postere journalene. Du kan gjøre registreringer for følgende forbrukstyper: timer, varer og utgifter. De forskjellige forbrukstypene registreres og posteres på siden **Arbeidsordrejournaler**. Journaloppsettet i **Aktivastyring** brukes til å opprette og postere separate journaler for timer, varer og utgifter i modulen **Prosjektstyring og regnskap**.

Du kan kanskje legge til eller slette prognoselinjer i en arbeidsordre. Oppsettet for en arbeidsordrelivssyklustilstand, den tilknyttede prosjekttypen og stadiereglene knyttet til prosjekttypen bestemmer om du kan legge til eller redigere journallinjer. Les mer om livssyklustilstander for arbeidsordrer og relaterte prosjektstadier i [Integrering til prosjektstyring og regnskap](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Det er mulig å definere automatisk postering av journaler for en livssyklustilstand for arbeidsordrer. Se [Livssyklustilstand for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md) hvis du vil ha mer informasjon.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren, og klikk på **Journaler**.

3. Klikk på **Kopier fra prognose** for å overføre eventuelle prognoselinjer som kan være knyttet til arbeidsordren. Du kan velge hvilke forbrukstyper du vil overføre.

4. Hvis det er nødvendig, kan du legge til flere forbrukslinjer i den aktuelle hurtigfanen ved å klikke på **Legg til linje** og fylle ut data på linjen.

5. Klikk på **Valider journaler** for å validere journallinjene før postering.

6. Klikk på **Poster journaler** for å postere journallinjene.

7. Når du har postert forbruksjournalene, kan du oppdatere livssyklustilstanden for arbeidsordren, for eksempel Avsluttet, for å angi at arbeidsordren er fullført.

- I **Vis**-feltet som er plassert øverst på siden **Arbeidsordrejournaler**, velger du hvilke journallinjer du vil vise: alle, ikke postert eller postert. Posterte journaler har en hake i avmerkingsboksen **Postert**.  
- Når varelinjer opprettes i arbeidsordrejournalen, blir produktdimensjoner og sporingsdimensjoner som er knyttet til varen, automatisk overført til journallinjen.  

Skjermbildet nedenfor viser et eksempel på time- og vareregistreringer for en arbeidsordre i **Arbeidsordrejournaler**.

![Figur 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Dele timer i arbeidsordrer med flere arbeidsordrejobber

Hvis en arbeidsordre inneholder flere arbeidsordrejobber, kan du registrere arbeidstimer ved hjelp av funksjonaliteten **Del timer**, som betyr at én timeregistreringslinje kan distribueres likt på hver arbeidsordrejobb.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren, og klikk på **Journaler**.

3. Velg timeregistreringslinjen du vil dele, og klikk på **Del timer**.

4. I dialogboksen **Del timer for vedlikeholdsjobber for arbeidsordre** vises navnet på arbeideren som er logget på, automatisk, i **Arbeider**-feltet. Hvis det er nødvendig, kan du velge en annen arbeider.

5. Velg en kategori for timeregistreringen i **Kategori**-feltet.

6. Sett inn antall arbeidstimer som skal deles, i **Timer**-feltet.

![Figur 2](media/02-consumption.png)

7. Klikk **OK**.

*Eksempel:* I skjermbildet nedenfor vises journallinjer for en arbeidsordre som inneholder tre arbeidsordrejobber. Den første linjen som inneholder tre arbeidstimer, er delt, og én arbeidstime er registrert på hver arbeidsordrejobb. Når de tre timeregistreringslinjene er opprettet, bestemmer du hva du skal gjøre med den opprinnelige timeregistreringslinjen (den første linjen i eksemplet). Du kan beholde den slik den er, eller slette den. 

![Figur 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Finansdimensjoner på forbruksregistreringer

Når du utfører forbruksregistreringer, legges finansdimensjoner som er knyttet til de ulike registreringstypene, til i registreringene i en bestemt rekkefølge. 

*Time- og utgiftsregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til. Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til. Til slutt legges finansdimensjoner fra ressursen (arbeideren) til.

*Vareregistreringer:* Først blir finansdimensjoner fra journalhodet lagt til. Så legges finansdimensjoner fra det tilknyttede arbeidsordreprosjektet til. Deretter legges finansdimensjoner fra området til. Til slutt legges finansdimensjoner fra varen til.

>[!NOTE]
>For alle tre registreringstypene valideres finansdimensjonskombinasjonen, og ugyldige kombinasjoner er tomme. Dette er standardoppsett i Finance and Operations.
