---
title: Postere jobber til Broadbean fra Attract
description: Dette emnet forklarer hvordan du bruker Dynamics 365 Talent – Attract til å postere jobber til Broadbean
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 41fa057606887069a9ea0f1f2178eeaff59f33ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462158"
---
# <a name="post-jobs-to-broadbean-from-attract"></a>Postere jobber til Broadbean fra Attract

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract hjelper deg å få talentet du trenger, ved å la deg postere jobber direkte fra Attract til Broadbean. Når du [har opprettet en jobb](./creating-jobs-attract.md), må du bare klikke på en knapp for å vise jobben for alle potensielle jobbkandidater på Broadbean.

Postering av jobber til Broadbean krever en passende Broadbean-lisens. Broadbean tilbyr ulike produkter og planer. For mer informasjon om Broadbean-lisensiering og -priser, [kontakt Broadbean](https://www.broadbean.com/contact-us/).

Hvis du er administrator og trenger mer informasjon om hvordan du konfigurerer Broadbean-integrasjon med Attract, kan du se [Aktivere Broadbean-integrering i Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md).

## <a name="post-jobs-to-broadbean"></a>Postere jobber til Broadbean

Når Broadbean er aktivert, kan rekrutteringspersoner og administratorer postere en jobb til den. Du må ha en URL-adresse for jobben.

1. I Attract åpner du jobben du vil postere til Broadbean.
2. I **Posteringer**-delen velger du **Legg ut nå**-knappen som tilsvarer Broadbean.
3. Følg instruksjonene i Broadbean-vinduet.

Attract sender følgende informasjon til Broadbean:

- Forespørsels-ID
- Jobbtittel
- Beskrivelse av jobb
- Jobbsted
- Søk-URL
- Informasjon om verver

Når Broadbean har fullført posteringen, viser **Posteringer**-delen av jobben i Attract statusen for Broadbean som **Postert**.

> [!NOTE]
> - Broadbean krever **Bransje**-feltet. For øyeblikket er dette feltet satt til **IT** som standard. Du kan imidlertid endre verdien til riktig bransje i vinduet for Broadbean-stillingsposteringen.
> - Det tar litt tid for Broadbean å fullføre postering av jobben til alle jobbtavlene du har valgt. Derfor kan være en liten forsinkelse før Attract gir en statusoppdatering for jobben.

### <a name="view-a-broadbean-job-posting"></a>Vise en Broadbean-jobbpostering

Når du posterer en jobb til Broadbean, kan du vise den fra Attract.

1. I Attract åpner du jobben du vil vise på Broadbean.
2. I kategorien **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Vis**.

Broadbean-jobbposteringen vises i et nytt vindu.

### <a name="update-a-broadbean-job-posting"></a>Oppdatere en Broadbean-jobbpostering

Du kan oppdatere en Broadbean-jobbpostering på to forskjellige måter.

1. I Attract åpner du jobben du vil oppdatere.
2. I **Posteringer**-delen velger du **Oppdater oppføring**-knappen som tilsvarer Broadbean.
3. Rediger posteringen i Broadbean-vinduet.

    – eller –

1. I Attract åpner du jobben du vil vise på Broadbean.
2. I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Vis**.
3. Rediger jobbdetaljene i Broadbean-vinduet, og poster deretter jobben på nytt. Jobbdetaljene i Attract endres ikke.

### <a name="remove-a-broadbean-job-posting"></a>Fjerne en Broadbean-jobbpostering

Du kan fjerne en jobbpostering fra Broadbean etter behov.

1. I Attract åpner du jobben du vil fjerne.
2. I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Fjern utlysing**.

Når Broadbean fjerner jobben, har Broadbean-elementet i Attract en **Legg ut nå**-knapp. Denne knappen angir at jobben er fjernet og kan posteres på nytt.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Feilsøke jobbpostering til Broadbean

Hvis du har problemer med å postere en jobb til Broadbean, kan du prøve følgende fremgangsmåte:

1. Kontroller at Broadbean-legitimasjonen du har angitt, er gyldig og korrekt.
2. Hvis legitimasjonen er gyldig og korrekt, kan du kontakte [Broadbean-støtten](https://www.broadbean.com/resources/support/).
3. Hvis problemet vedvarer, kontakter du [Microsoft Kundestøtte](./talent-support.md).

## <a name="see-also"></a>Se også

[Opprette, godkjenne og postere jobber i Attract](./creating-jobs-attract.md)

[Aktivere Broadbean-integrering i Microsoft Dynamics 365 Talent - Attract](./attract-admin-job-board-settings.md)
