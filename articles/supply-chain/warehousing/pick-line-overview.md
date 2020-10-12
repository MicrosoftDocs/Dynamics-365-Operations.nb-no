---
title: Definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt
description: Dette emnet beskriver hvordan du definerer når en liste over alle arbeidslinjer skal vises til lagermedarbeidere som behandler lagerarbeid på en mobilenhet. Denne funksjonen kan være nyttig for lagerarbeidere som ofte må ha en oversikt over plukklinjene i en arbeidsordre, slik at de kan optimalisere plukkingsrekkefølgen.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837318"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du konfigurerer alternativer som er knyttet til plukklinjeoversikten for menyvarer for mobilenheter som brukes til å behandle plukking av arbeid. Plukklinjeoversikten lar lagerarbeidere vise og velge fra en liste over alle arbeidslinjene som er knyttet til den gjeldende oppgaven. Denne funksjonen kan hjelpe arbeiderne med å optimalisere plukksekvensen. Funksjonen inneholder alternativer som erstatter standard **Hopp over**-knapp, som la arbeidere bla gjennom linjene én om gangen, i en fast rekkefølge. (Alternativet for å bruke denne knappen er imidlertid fremdeles tilgjengelig.)

Administratorer kan konfigurere hvert menyelement for seg for å styre hvordan, når og hvor lagerappen presenterer plukklinjeoversikten.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Aktivere funksjonen Oversikt over arbeidsplukklinje

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** _Lagerstyring_
- **Funksjonsnavn:** _Oversikt over arbeidsplukklinje_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Konfigurere menyelementer for å vise en liste over alle arbeidslinjer

Følg disse trinnene for å definere et menyelement for en mobilenhet for å angi en plukklinjeoversikt.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg eller opprett et menyelement som er knyttet til plukking av arbeid, og angi følgende verdier:

    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*
    - **Styrt av:** *Brukerstyrt* eller *Systemstyrt*

    Hvis du vil ha mer informasjon om hvordan du oppretter menyelementer og bruker de ulike innstillingene som er tilgjengelige på siden **Menyelementer på mobilenheten**, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).

1. På hurtigfanen **Generelt** konfigurerer du funksjonen ved å sette feltet **Vis arbeidslinjeliste** til én av følgende verdier:

    - **Vis bare ved forespørsel** – Arbeidere kan velge å vise plukklinjelisten ved å velge **Hopp til**-knappen i lagerappen.
    - **Vis ved starten av hver plukking** – Arbeidere ser listen hver gang de starter eller fullfører en plukklinje. De kan også vise listen på nytt ved å velge **Hopp til**-knappen i lagerappen.
    - **Vis bare ved starten av første plukking** – Arbeidere ser listen hver gang de starter nytt plukkarbeid, men ikke etter hver linje. De kan også vise listen på nytt ved å velge **Hopp til**-knappen i lagerappen.
    - **Vis aldri** – Standardknappen **Hopp over** vises i lagerappen, og visning av arbeidslinjelisten er deaktivert. Med **Hopp over**-knappen kan en arbeider bla gjennom linjene én om gangen, i en fast rekkefølge. De kan også gå gjennom listen så mange ganger som de treger, til alle linjene er behandlet.

1. Velg **Lagre** i handlingsruten.

    Hvis du setter feltet **Vis arbeidslinjeliste** til en hvilken som helst verdi unntatt *Vis aldri*, blir knappen **Feltliste** aldri tilgjengelig.

1. Velg **Feltliste** i handlingsruten.
1. På siden **Feltliste** konfigurerer du informasjonen som lagerappen viser for hver linje i listen.

    - Feltet for **primærkontroll** er alltid satt til *LineNum*. Derfor begynner hver rad i listen med et linjenummer.
    - Bruk de gjenstående feltene **Visningsfelt** for å legge til opptil sju ekstra visningsfelt, i henhold til hva du trenger. I hvert **Visningsfelt**-felt velger du navnet på et arbeidslinjefelt. Deretter vil hver linje vise en verdi for dette feltet. Verdiene vil bli vist i den rekkefølgen du velger her. Du kan la noen av **Visningsfelt**-feltene stå tomme hvis du ikke har behov for alle de sju verdiene.

1. I handlingsruten velger du **Lagre**, og deretter lukker du siden **Feltliste**.
