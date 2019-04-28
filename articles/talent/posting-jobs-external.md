---
title: Postere jobber på eksterne karriereområder fra Attract
description: Dette emnet forklarer hvordan du bruker Dynamics 365 for Talent - Attract til å postere jobber til eksterne områder for rekruttering
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/15/2019
ms.locfileid: "993674"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Postere jobber på eksterne karriereområder fra Attract

[!include [banner](../includes/banner.md)]

Du vil gjerne vise ledige stillingene for så mange kvalifiserte kandidater som mulig. Rekrutteringsområder, for eksempel Broadbean, hjelper deg med å oppnå dette målet. Microsoft Dynamics 365 Talent: Med Attract kan du postere jobber til Broadbean, og Microsoft gir deg kontinuerlig nye tilbud på dette området.

## <a name="post-jobs-to-broadbean"></a>Legge inn jobber på Broadbean

Før du kan postere jobber til Broadbean må du konfigurere Broadbean-integreringen.

> [!NOTE]
> - Hvis du vil postere jobber til eksterne områder, må du ha [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Denne funksjonen er for øyeblikket i forhåndsvisningen. Hvis du vil prøve dette, må du [aktiverer funksjonen i innstillingene for administrasjon av Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Konfigurere Broadbean-integrering

1. Logge på Attract som en administrator.
2. Velg **Innstillinger**-knappen (tannhjulssymbolet) i øvre høyre hjørne på siden, og velg deretter **Administrasjonssenter**.
3. I kategorien **Innstillinger for jobbtavle** i delen **Aktiver Broadbean-integrering** aktiverer du integreringen.
4. Kontakt Broadbean, og skriv inn informasjonen din i **Brukernavn, Klient-ID, Krypteringstoken**.

> [!WARNING]
> Broadbean-legitimasjonen din er sensitiv og konfidensiell. Derfor må du lagre og dele den på en ansvarlig måte. Alle som har en Administrator-rolle i Attract, kan vise denne legitimasjonen.

> [!NOTE]
> Microsoft og Attract er ikke er involvert i å opprette og vedlikeholde disse verdiene. Det er ditt ansvar å holde dem oppdatert i Attract og arbeide sammen med Broadbean for å løse problemer som involverer legitimasjonen.

### <a name="post-a-job-to-broadbean"></a>Legge inn en jobb på Broadbean

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
2. I delen **Posteringer** velger du ellipseknappen (**...**) som tilsvarer Broadbean, og velg deretter **Vis**.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Feilsøke Broadbean-integreringen

Hvis du har problemer med å postere en jobb til Broadbean, kan du prøve følgende fremgangsmåte:

1. Kontroller at Broadbean-legitimasjonen du har angitt, er gyldig og korrekt.
2. Hvis legitimasjonen er gyldig og korrekt, kan du kontakte [Broadbean-støtten](https://www.broadbean.com/resources/support/).
3. Hvis problemet vedvarer, kontakter du [Microsoft Kundestøtte](./talent-support.md).
