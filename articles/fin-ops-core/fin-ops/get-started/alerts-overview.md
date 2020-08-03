---
title: Oversikt over varsler
description: Dette emnet gir generell informasjon om varsler. Du kan bruke varsler til å holde deg informert om hendelser som du vil spore i løpet av arbeidsdagen.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 755181e956a3d93d87e9e5d57622283ff7bf4944
ms.sourcegitcommit: f62c2151be477acfaeace73878471abb9b1b832d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2020
ms.locfileid: "3602535"
---
# <a name="alerts-overview"></a>Oversikt over varsler

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Varsler
Varsler utgjør et meldingssystem for kritiske hendelser i systemet. Du kan bruke varsler til å holde deg informert om hendelser som du vil spore i løpet av arbeidsdagen. Du kan enkelt opprette ditt eget sett med varsler slik at du blir varslet om leveringer som er forfalt, ordrer som er slettet, priser som endres eller hendelser du må reagere på.

Det finnes flere vanlige scenarier hvor varslingsfunksjonen i Finance and Operations kan brukes. Her er noen eksempler.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Scenario 1: Opprett en varslingsregel for nye salgsordrer

1. Åpne siden **Alle salgsordrer**.
2. Velg **Opprett et egendefinert varsel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.
3. Velg **Post er opprettet** i feltet **Hendelse** i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Scenario 2: Opprett en varslingsregel for utsettelse av en leveringsdato

1. Åpne siden **Alle kjøpsordrer**.
2. Velg en bestillings-ID for å få tilgang til bestillingsdetaljer.
3. Utvid hurtigfanen **Bestillingshode**.
4. Velg **Opprett et egendefinert varsel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.
5. Velg **Leveringsdato** i feltet **Felt** i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**.
6. Velg **er utsatt** i feltet **Hendelse**.
    
Når du lukker dialogboksen **Opprett varslingsregel**, vises regelen på siden **Administrer varselregler**. Du kan bruke siden **Administrer varselregler** til å oppdatere dine eksisterende varselregler. Du kan for eksempel endre hendelsestriggerne, oppdatere varslinger om systemhendelser, og oppdatere utløpsdatoer. Bruk knappen **Varsle meg** i fanen **Alternativer** i handlingsruten for å åpne siden **Administrer varselregler**.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Hva skjer når en varslingsregel opprettes?

Når du oppretter varselregler, kan du knytte en forhåndsdefinert hendelse til et bestemt felt. Datoen som er angitt i feltet, kommer, eller innholdet i feltet endres. Du kan også knytte en hendelse til postene på en bestemt side. En post opprettes for eksempel eller slettes.

Når den valgte hendelsen skjer for feltet eller for en post på siden, sendes det et varsel til deg. Du oppretter for eksempel en regel der du knytter feltet **Leveringsdato** til en bestemt bestillingslinje med hendelsen **tid siden forfall**. Du setter tidsrammen til fem dager. I dette tilfellet sendes det et varsel fem dager etter leveringsdatoen for bestillingslinjen.

Du kan også forbedre varselreglene ved å angi betingelser. Du kan for eksempel bli varslet om nye bestillinger som opprettes for bestemte leverandørkontoer.

## <a name="preparing-for-an-alert"></a>Klargjør for et varsel

Før du oppretter en varslingsregel, må du vurdere når eller i hvilke situasjoner du vil motta varsler. Når du vet hvilke hendelser du vil varsles om, kan du finne siden der dataene som forårsaker den hendelsen, vises. Hendelsen kan være en dato som kommer, eller en bestemt endring som forekommer. Du må derfor finne siden der datoen er angitt, eller hvor feltet som endres eller den nye posten som opprettes, vises. Etter at du har denne informasjonen, kan du opprette varslingsregelen.

## <a name="components-of-an-alert-rule"></a>Komponentene i en varslingsregel

En varslingsregel har fem komponenter:

- **Hendelse** – Hendelsen som utløser en varslingsregel kan være en dato som kommer, eller en bestemt endring som forekommer. Du definerer hendelser i hurtigfanen **Send e-postvarsel når jobbstatus endres** i dialogboksen **Opprett varslingsregel**.
- **Betingelse** – I hurtigfanen **Varsle meg for** i dialogboksen **Opprett varslingsregel** kan du velge omfanget for betingelsen for å kontrollere når du varsles om hendelser. Du kan bruke regelen bare for gjeldende post eller for alle synlige poster på siden. Hvis regelen gjelder på tvers av juridiske enheter, kan du sette alternativet **Organisasjonsomfattende** til **Ja**.
- **Utløp av regel** – I hurtigfanen **Varsle meg inntil** i dialogboksen **Opprett varslingsregel** kan du angi hvor lenge varslingsregelen skal være aktiv.
- **Innhold** – I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi emneteksten og meldingsteksten som varslingsmeldingene skal bruke.
- **Bruker** – I hurtigfanen **Hvem skal varsles** i dialogboksen **Opprett varslingsregel** kan du angi hvilken bruker som skal motta varslene. Bruker-IDen er valgt som standard.

    > [!NOTE]
    > Dette alternativet er begrenset til administratorer for organisasjonen.

## <a name="videos"></a>Videoer

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Slik bruker du varsler til å overvåke filtrerte data

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

Videoen [Slik bruker du varsler til å overvåke filtrerte data](https://youtu.be/ZYKMcv6kl9s) (vises over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

### <a name="alert-rule-options"></a>Alternativer for varslingsregel

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

Videoen [Alternativer for varslingsregler](https://youtu.be/cpzimwOjicM) (vises over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.


