---
title: Nedetid ved vedlikehold for arbeidsordrer
description: Denne artikkelen beskriver hvordan du oppretter registreringer av nedetid ved vedlikehold for aktivumet som er valgt i en arbeidsordre.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a310152685f733093cc7e50404c23b6f24c40cc
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016659"
---
# <a name="maintenance-downtime-for-work-orders"></a>Nedetid ved vedlikehold for arbeidsordrer

[!include [banner](../../includes/banner.md)]


Du kan opprette registreringer av nedetid ved vedlikehold for aktivumet som er valgt i en arbeidsordre. Denne funksjonen er nyttig hvis du vil registrere vedlikeholdsnedetid på én eller flere maskiner i produksjonsområdet. Først oppretter du årsakskodene for vedlikeholdsnedetid du vil bruke, for eksempel **Stopp** og **Planlagt stopp**. Dette trinnet utføres på siden **Årsakskoder for nedetid ved vedlikehold**. Du kan deretter opprette registreringer for nedetid ved vedlikehold på siden **Nedetid ved vedlikehold** og legge til de aktuelle årsakskodene for nedetiden.

## <a name="create-maintenance-downtime-reason-codes"></a>Opprette årsakskoder for nedetid ved vedlikehold

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Årsakskoder for nedetid ved vedlikehold**.

2. Velg **Ny**.

3. I feltet **Årsakskode for nedetid ved vedlikehold** angir du en ID for årsakskoden nedetid ved vedlikehold.

4. Angi et navn i **Navn**-feltet.

5. Merk av for **KPI inkluder** hvis årsakskoden skal tas med i beregninger av sentrale nøkkelytelsesindikatorer (KPIer) for aktivumet. Generelt bør ikke planlagte produksjonsstopp tas med i KPI-beregninger fordi de ikke påvirker forventet ytelse.

6. Velg **Lagre**.

Illustrasjonen nedenfor viser et eksempel på siden **Årsakskoder for nedetid ved vedlikehold**.

![Figur 1.](media/15-work-orders.png)

Når du har opprettet årsakskodene for vedlikeholdsnedetid som du vil bruke, kan du opprette registreringer for nedetid ved vedlikehold for arbeidsordrer og aktiva.


## <a name="create-maintenance-downtime-registrations"></a>Opprette registreringer for nedetid ved vedlikehold

1. Klikk på **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren, og deretter går du til fanen **Arbeidsordre** i gruppen **Aktivum** og velger **Nedetid ved vedlikehold**.

3. Velg **Ny**.

4. Angi dato- og klokkeslettsintervall for registreringen av vedlikeholdsnedetid i **Fra**- og **Til**-feltene.

>[!NOTE]
>Når du går ut av **Til**-feltet, settes varigheten i timer automatisk inn i **Varighet**-feltet.

5. Velg en årsakskode i feltet **Årsakskode for nedetid ved vedlikehold**.

6. Gjenta trinn 3 til og med 5 hvis du vil legge til flere registreringer.

7. Velg **Lagre**.

Illustrasjonen nedenfor viser et eksempel på en registreringer for nedetid ved vedlikehold.

![Figur 2.](media/16-work-orders.png)

Kalenderen som brukes til å beregne en registrering av nedetid ved vedlikehold er avhengig av hva du velger i oppsettet for aktiva og parametere. Hvis en ressurs er valgt for et aktiva i feltet **Ressurs** i hurtigfanen **Anleggsmiddel** på siden **Alle aktiva**, brukes kalenderoppsettet for den tilknyttede ressursgruppen, som vist i følgende illustrasjon.

![Figur 3.](media/17-work-orders.png)

Hvis det ikke er valgt en ressurs for aktivumet, brukes standardkalenderen som er valgt på siden **Aktivabehandlingsparametere**, som vist i følgende illustrasjon.

![Figur 4.](media/18-work-orders.png)

Klikk på **Aktivabehandling** > **Forespørsler** > **Nedetid ved vedlikehold** hvis du vil se en oversikt over alle registreringer av vedlikeholdsnedetid.

>[!NOTE]
>Alle kalendere som brukes i modulen **Aktivastyring**, defineres i **Organisasjonsstyring** > **Oppsett** > **Kalendere** > **Kalendere**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]