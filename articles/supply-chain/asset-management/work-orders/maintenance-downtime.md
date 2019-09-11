---
title: Nedetid ved vedlikehold
description: Dette emnet beskriver nedetid ved vedlikehold i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918250"
---
# <a name="maintenance-downtime"></a>Nedetid ved vedlikehold


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Du kan opprette registreringer av nedetid ved vedlikehold for aktivaet som er valgt i en arbeidsordre. Dette er nyttig hvis du vil registrere vedlikeholdsnedetid på én eller flere maskiner i produksjonsområdet. Først oppretter du årsakskodene for vedlikeholdsnedetid du vil bruke, for eksempel stopp og planlagt stopp. Dette gjøres i **Årsakskoder for nedetid ved vedlikehold**. Deretter kan du opprette registreringer for nedetid ved vedlikehold, i **Nedetid ved vedlikehold**, og legge til de aktuelle årsakskodene.

## <a name="create-maintenance-downtime-reason-codes"></a>Opprette årsakskoder for nedetid ved vedlikehold

1. Klikk på **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Årsakskoder for nedetid ved vedlikehold**.

2. Klikk på **Ny**.

3. Sett inn en ID i feltet **Årsakskode for nedetid ved vedlikehold**.

4. Sett inn et navn på årsakskoden i **Navn**-feltet.

5. Merk av for **KPI inkluder** hvis årsakskoden skal tas med i aktiva-KPI-beregninger. Vanligvis bør ikke planlagte produksjonsstopp tas med i KPI-beregninger fordi de ikke påvirker forventet ytelse.

6. Klikk **Lagre**.

![Figur 1](media/15-work-orders.png)


Når du har opprettet årsakskodene for vedlikeholdsnedetid som du vil bruke, kan du opprette registreringer for nedetid ved vedlikehold for arbeidsordrer og aktiva.


## <a name="create-maintenance-downtime-registrations"></a>Opprette registreringer for nedetid ved vedlikehold

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren, og klikk på **Nedetid ved vedlikehold**.

3. Klikk på **Ny**.

4. Sett inn dato- og klokkeslettsintervall for registreringen av vedlikeholdsnedetid i **Fra**- og **Til**-feltene.

5. Når du går ut av **Til**-feltet, settes varigheten i timer automatisk inn i **Varighet**-feltet.

6. Velg en årsakskode i feltet **Årsakskode for nedetid ved vedlikehold**.

7. Gjenta trinn 3-6 hvis du vil legge til flere registreringer.

8. Klikk **Lagre**.


![Figur 2](media/16-work-orders.png)


Kalenderen som brukes til å beregne en registrering av nedetid for vedlikehold er avhengig av hva du velger i oppsettet for aktiva og parametere. Hvis en ressurs er valgt for et aktiva i **Alle aktiva** > **Anleggsmiddel**-hurtigfanen > **Ressurs**-feltet, brukes kalenderoppsettet for den tilknyttede ressursgruppen, som vist i følgende figur.

![Figur 3](media/17-work-orders.png)


Hvis det ikke er valgt en ressurs for aktivaet, brukes standardkalenderen som er valgt i **Aktivabehandlingsparametere**, som vist i følgende figur.

![Figur 4](media/18-work-orders.png)


Klikk på **Enterprise asset management** > **Forespørsler** > **Nedetid ved vedlikehold** hvis du vil se en oversikt over alle registreringer av vedlikeholdsnedetid.

>[!NOTE]
>Alle kalendere som brukes i modulen **Aktivastyring**, defineres i **Organisasjonsstyring** > **Oppsett** > **Kalendere** > **Kalendere**.

