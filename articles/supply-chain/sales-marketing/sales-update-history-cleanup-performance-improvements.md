---
title: Planlegg opprydding i salgshistorikkdata
description: Denne artikkelen beskriver hvordan du kan forbedre systemytelsen ved å planlegge en periodisk oppryddingsoppgave for salgsoppdateringsloggen som skal kjøres etter regelmessige intervaller.
author: myvakalo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e9a4dd5372afa8a0452449d1cb9121107e6e1610
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335511"
---
# <a name="schedule-sales-history-data-cleanup"></a>Planlegg opprydding i salgshistorikkdata

[!include [banner](../includes/banner.md)]

Som en del av standardoperasjonen genererer og lagrer Microsoft Dynamics 365 Supply Chain Management salgshistorikkdata fortløpende. Over tid kan en stor mengde utdaterte salgshistorikkdata akkumuleres i systemet. Disse akkumulerte dataene kan forårsake ytelses- og funksjonsproblemer når dokumenter som er knyttet til salgsordrer, posteres. (Disse dokumentene omfatter salgsordrebekreftelser, salgsfølgesedler, salgsplukklister og fakturaer). Derfor bør du konfigurere og planlegge den periodiske oppgaven for *opprydding av salgsoppdateringshistorikk* for kjøring etter regelmessige intervaller. Denne oppgaven fjerner alle oppdateringsdata i salgshistorikken som ikke lenger er nødvendige.

Hvis du bruker den periodiske oppgaven for *opprydding av salgsoppdateringshistorikk*, anbefaler vi at du aktiverer funksjonen *Forbedringer av ytelse for opprydding i salgshistorikk*, som gjør oppgaven mer effektiv. (Uansett kan du også kjøre oppgaven uten å aktivere denne funksjonen.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Aktiver funksjonene for opprydding i salgshistorikk

Hvis du vil konfigurere og bruke den periodiske oppgaven *Opprydding av salgsoppdateringshistorikk*, sammen med alle funksjonene som beskrives i denne artikkelen, må du aktivere funksjonene *Forbedringer av ytelse for opprydding i salgshistorikk* og *Rydd opp i salgsoppdateringshistorikk basert på alder* i Funksjonsstyring, som beskrevet i følgende underavsnitt.

### <a name="sales-history-cleanup-performance-improvements"></a>Forbedringer av ytelse for opprydding i salgshistorikk

Den periodiske satsvise jobben **Opprydding av salgsoppdateringshistorikk** kan ta lang tid hvis det kjøres sjelden i miljøer med høyt volum på salgsoppdateringer. I disse situasjonene kan funksjonen *Forbedringer av ytelse for opprydding i salgshistorikk* redusere varigheten til kjøringen og forbedre påliteligheten.

Funksjonen forbedrer den eksisterende oppryddingsjobben på følgende måter:

- Den deler oppryddingen i bunker (du kan endre bunkestørrelsen ved hjelp av tilpasninger).
- Den vil kjøre i maksimalt 2 timer (du kan endre varigheten ved hjelp av tilpasninger).
- Der det er mulig, vil den bruke databasefunksjoner for å minimere låsekonflikt og unngå å slå sammen transaksjonstabeller under opprydding.

Etter at funksjonen er aktivert, kjøres den satsvise jobben **Opprydding av salgoppdateringshistorikk** (**Salg og markedsføring \> Opprydding \> Periodeoppgaver \> Opprydding av salgsoppdateringshistorikk**) som den gjorde før, men med bedre ytelse og maksimum 2 timer. Det betyr at det kan hende at det må kjøres flere ganger for å rydde opp i alle dataene for en bestemt oppbevaringstidsramme.

Før du kan bruke denne funksjonen, må den være aktivert for systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Salg og markedsføring*
- **Funksjonsnavn:** *Forbedringer av ytelse for opprydding i salgshistorikk*

### <a name="clean-up-sales-update-history-based-on-age"></a>Rydd opp i salgsoppdateringshistorikk basert på alder

Med funksjonen *Rydd opp i salgsoppdateringshistorikk basert på alder* kan du angi maksimal alder for poster som skal beholdes når den periodiske oppgaven *Opprydding av salgsoppdateringshistorikk*. Eldre poster blir slettet. Denne funksjonen er nyttig når du angir at oppgaven skal kjøres periodisk, fordi alderen alltid beregnes i forhold til datoen når oppgaven kjøres. Hvis du ikke bruker denne funksjonen, kan du bare angi en bestemt dato for å beholde de eldste postene.

For å bruke denne funksjonen må den være aktivert for systemet. Funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Varslinger for bølgekjøring* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Definer og planlegg den periodiske oppgaven for opprydding i salgshistorikk

Gjør følgende for å definere og planlegge den periodiske oppgaven for *opprydding i salgshistorikk*.

1. Analyser forretningsbehovene for å finne ut hvor mange dager med historiske salgsordreposteringsdata du må beholde. Vi anbefaler vanligvis at du kjører oppryddingsoppgaven hver tredje måned og maksimalt hver sjette måned.
1. Gå til **Salg og markedsføring \> Periodiske oppgaver \> Oppgaver \> Opprydding av salgsoppdateringshistorikk**.
1. I dialogboksen **Rydd opp i salgsoppdateringshistorikk** angir du følgende felter på hurtigfanen **Parametere**:

    - **Rydd opp** – Velg en av følgende verdier for å angi hvilken type poster som skal ryddes opp:

        - **Utført** – Slett bare poster som er fullstendig behandlet. Siden du sannsynligvis ikke har mer bruk for disse postene, er dette alternativet det sikreste alternativet.
        - **Utført og med feil** – Slett både fullstendig behandlede poster og poster der det har oppstått en feil. Dette alternativet er det vanligste. Det kan hende at du vil kontrollere og til og med korrigere poster med feil i stedet for å rydde dem opp automatisk. Men mange firmaer velger å rydde opp i disse postene også etter omtrent en måned, fordi de sannsynligvis ikke lenger er relevante innen den tiden.
        - **Alle** – Slett utførte, ventende poster og poster med feil. Ventende poster er gyldige, men er ikke fullstendig behandlet ennå. I de fleste tilfeller ønsker du sannsynligvis ikke at de skal slettes automatisk. I noen situasjoner kan du imidlertid velge å slette dem automatisk etter at det har gått en viss tid.

    - **Behold poster basert på alder** – Angi om du vil rydde opp i poster basert på alderen den dagen oppgaven kjøres, eller slette poster som ble opprettet før en fast dato. Hvis du planlegger oppryddingen som en gjentakende oppgave, bør du sette dette alternativet til *Ja* fordi alderen alltid beregnes i forhold til datoen da oppgaven kjøres.

        - Sett dette alternativet til *Ja* for å aktivere feltet **Maksimumsalder**. Du bruker dette feltet til å angi maksimumsalderen for postene som skal beholdes hver gang oppgaven kjøres. Feltet **Opprettet til** ignoreres.
        - Sett dette alternativet til *Nei* for å aktivere feltet **Opprettet til**. Du bruker dette feltet til å angi den eldste opprettelsesdatoen for postene som skal beholdes når oppgaven kjøres. Feltet **Maksimumsalder** ignoreres.

    - **Opprettet til** – Denne innstillingen gjelder bare når alternativet **Behold poster basert på alder** er angitt til *Nei*. Angi den eldste opprettelsesdatoen for postene som skal beholdes når oppgaven kjøres. Poster som ble opprettet før denne datoen, vil bli slettet.
    - **Maksimumsalder** – Denne innstillingen gjelder bare når alternativet **Behold poster basert på alder** er angitt til *Ja*. Angi maksimumsalderen (i dager) for postene som skal beholdes hver gang oppgaven kjøres. Eldre poster blir slettet.

1. Angi hvordan, når og hvor ofte oppgaven skal kjøres, på hurtigfanen **Kjør i bakgrunnen**. Bruk disse innstillingene til å implementere tidsplanen som du fastsatte i trinn 1. Feltene fungerer på samme måte som de fungerer for andre typer [satsvise jobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og lukke dialogboksen.
