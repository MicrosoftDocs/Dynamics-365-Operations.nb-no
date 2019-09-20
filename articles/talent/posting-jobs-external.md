---
title: Postere jobber på eksterne karriereområder fra Attract
description: Dette emnet forklarer hvordan du bruker Dynamics 365 for Talent - Attract til å postere jobber til eksterne områder for rekruttering
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
ms.openlocfilehash: 936ff85a4dabb715cb83b875a5c58c9fb7a0ac26
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739823"
---
# <a name="post-jobs-to-broadbean"></a>Postere jobber til Broadbean

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent : Attract hjelper deg å få talentet du trenger, ved å la deg postere jobber direkte fra Attract til Broadbean. Når du [har opprettet en jobb](./creating-jobs-attract.md), må du bare klikke på en knapp for å vise jobben for alle potensielle jobbkandidater på Broadbean.

Postering av jobber til Broadbean krever en passende Broadbean-lisens. Broadbean tilbyr ulike produkter og planer. For mer informasjon om Broadbean-lisensiering og -priser, [kontakt Broadbean](https://www.broadbean.com/contact-us/).

Hvis du er en administrator som trenger mer informasjon om hvordan du konfigurerer Broadbean-integrasjon med Attract, kan du se [Angi innstillinger for eksterne jobbtavler](./attract-admin-job-board-settings.md).

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

[Opprette jobber](./creating-jobs-attract.md)

[Angi innstillinger for eksterne jobbtavler](./attract-admin-job-board-settings.md)
