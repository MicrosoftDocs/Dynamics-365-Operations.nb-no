---
title: 'Øyeblikksbilder av aldersfordeling for kunde '
description: Dette emnet gir informasjon om øyeblikksbilde av aldersfordeling for kunde. Et øyeblikksbilde av aldersfordeling beregner aldersfordelte saldoer for en kundegruppe på ett tidspunkt.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a768b2508988c77d669bac2ac443d69a995a5617971693caed8e0563a146f853
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769113"
---
# <a name="customer-aging-snapshots"></a>Øyeblikksbilder av aldersfordeling for kunde 

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om øyeblikksbilde av aldersfordeling for kunde. Et øyeblikksbilde av aldersfordeling beregner aldersfordelte saldoer for en kundegruppe på ett tidspunkt. Du kan opprette øyeblikksbilde av aldersfordeling enten for alle kunder eller for kundene i en kundepulje.

Informasjon fra øyeblikksbilde av aldersfordeling vises på listesiden **Aldersfordelte saldoer** og på siden **Innkrevinger**. Du må opprette et øyeblikksbilde av aldersfordeling før du kan bruke listesiden **Aldersfordelte saldoer**. Listesiden viser bare kunder som det er opprettet et øyeblikksbilde av aldersfordeling for.

Arbeidsområdet **Kundekreditt og innkrevinger** viser også aldersfordeling for kunder. Hvis du vil ha mer informasjon, kan du se [Power BI-innholdet Behandling av kreditt og innkrevinger](credit-collections-power-bi.md).

> [!NOTE]
> For å redusere tiden som kreves for å opprette et øyeblikksbilde av aldersfordeling, kan du slå på funksjonen for **Ytelsesforbedring for aldersfordeling for kunde** i arbeidsområdet for **Funksjonsbehandling**. Bruk imidlertid ikke kundepuljene når denne funksjonen er aktivert. Hvis en kundepulje er valgt, vil ikke funksjonen fungere, men du kan likevel opprette et øyeblikksbilde av aldersfordeling.

Når du oppretter et øyeblikksbilder av aldersfordeling for kunde , bruker du følgende felt til å angi informasjon om det:

- **Definisjon av aldersfordelingsperiode** - Velg definisjonen av aldersfordelingsperiode for øyeblikksbilde av aldersfordeling. Du kan ha ett øyeblikksbilde av aldersfordeling for hver definisjon av aldersfordelingsperiode. Øyeblikksbildet av aldersfordeling og definisjon av aldersfordelingsperiode må opprettes separat.
- **Pulje-ID** – Dette feltet er valgfritt. Du kan bruke en pulje til å definere settet med kunder som skal behandles i øyeblikksbildet av aldersfordeling. Du kan velge en kundepulje i dette feltet, et øyeblikksbilde av aldersfordeling opprettes bare for kundekontoer som er en del av kundepuljen. Den valgte kundepuljen må være av typen **Øyeblikksbilde av aldersfordeling**. Hvis dette feltet er tomt, opprettes det et øyeblikksbilde av aldersfordeling for alle kundekontoer.

    > [!NOTE]
    > Hvis funksjonen **Ytelsesforbedring for aldersfordeling for kunde** er aktivert, må du ikke velge en kundepulje.

- **Kriterier** – Øyeblikksbilde av aldersfordeling baseres på datoen du velger:

    - **Transaksjonsdato** – Hver transaksjon aldersfordeles på transaksjonsdatoen.
    - **Forfallsdato** – Hver transaksjon aldersfordeles basert på forfallsdatoen.
    - **Dokumentdato** – Hver transaksjon aldersfordeles basert på dokumentdatoen.

- **Aldersfordeling per** – Velg datoen som skal brukes i feltet **Gjeldende dato** for øyeblikksbildet av aldersfordeling. Aldersfordelingsperioder beregnes deretter basert på denne datoen. 

    - **Dagens dato** – Bruk systemdatoen. Velg dette alternativet hvis behandling er konfigurert til å kjøre på en gjentakende bunke. Hver gang den satsvise jobben kjøres, brukes da systemdatoen for kjøringen.
    - **Valgt dato** – Bruk en dato du angir. Hvis du velger dette alternativet, må du angi en aldersfordelingsdato.

    Gjeldende aldersfordelingsperiode er for eksempel 30 dager. Hvis du velger **Dagens dato** i dette feltet, starter gjeldende aldersfordelingsperiode på dagens dato og inkluderer deretter de forrige 29 dagene. Hvis du velger **Valgt dato** og angir en dato, starter gjeldende aldersfordelingsperiode på den angitte datoen og inkluderer deretter de forrige 29 dagene.

- **Oppdater purrestatus** – Sett dette alternativet til **Ja** for å oppdatere samlingsstatusen til transaksjoner på **Samlinger**-siden fra **Løfte om betaling** til **Brutt løfte om betaling** hvis aldersfordelingsdatoen er utover datoen i feltet **Dato for løfte om betaling**. Sett dette alternativet til **Nei** hvis du ikke vil at samlingsstatusen skal være uendret på **Samlinger**-siden.
- **Ta med kunder med null saldo-kontoer** – Sett dette alternativet til **Ja** for å inkludere alle kunder, uavhengig av saldoen. Hvis du inkluderer alle kunder, anbefaler vi at du slår på funksjonen for **Ytelsesforbedring for aldersfordeling for kunde** og at du ikke bruker kundepuljene. Sett dette alternativet til **Nei** hvis du bare vil inkludere kunder som har en saldo. Denne innstillingen gir raskere ytelse, fordi kunder som ikke har saldo, hoppes over.
- **Firmaområde** – I kategorien **FIrmaområde** velger du de juridiske enhetene (firmaene) som skal tas med i øyeblikksbilde av aldersfordeling. Bare juridiske enheter som er konfigurert for sentralisert betaling, er tilgjengelige for valg. Transaksjoner fra de valgte juridiske enhetene inkluderes deretter i aldersfordelingsperiodene for kunder som har samme part-ID i alle de juridiske enhetene. Valutabeløp konverteres til valutaen for den juridiske enheten som du er logget på når du oppretter øyeblikksbildet av aldersfordeling.

Vi anbefaler at du planlegger at denne prosessen skal kjøre satsvis.

> [!NOTE]
> Du kan få hjelp til å forbedre den satsvise ytelsen når det opprettes øyeblikksbilder av aldersfordelinger, angir du et tall i feltet **Maksimalt antall satsvise oppgaver** i hurtigkategorien **Innkrevingsstandarder** i kategorien **Samlinger** på siden **Kundeparametere**. I feltet **Aldersfordel kundesaldoer** anbefaler vi at du starter med standardverdien på **100** og justerer deretter verdien for å optimalisere behandlingen for situasjonen din.

