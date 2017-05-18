---
title: "Lukke økonomimodulen ved periodeslutt"
description: "Dette emnet beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 54bd0296d2569c38fccd0ff13a2316cb18466675
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>Lukke økonomimodulen ved periodeslutt

[!include[banner](../includes/banner.md)]


Dette emnet beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen. 

I Økonomimodul kan du fullføre avslutningsprosedyrer for en periode eller et år. Avslutningsprosesser gjør systemet klart for en ny periode. Hvis du vil klargjøre systemet for et nytt år, må du kjøre årsavslutningsprosessen. Hver organisasjon har forskjellige prosesser og trinn som utføres på slutten av en periode. Her er noen av de valgfrie trinnene for periodeslutt:

-   Fullfør alle oppgavene for alle andre moduler, for eksempel Kunder, Leverandører og Beholdning.
-   Kontroller at alle journaler er postert.
-   Kjør revaluering av utenlandsk valuta for å generere eventuelle urealiserte fortjeneste- eller tapsbeløp.
-   Utlign transaksjoner for hver finanskonto.
-   Behandle eventuelle nødvendige fordelinger.
-   Poster periodesluttjusteringer manuelt.
-   Journalfør transaksjoner, og se gjennom **Finansjournal**-rapporten.
-   Foreta en konsolidering ved å bruke et konsolideringsfirma eller Finansrapportering.
-   Generer regnskapsoppgjør ved periodeslutt ved å bruke Finansrapportering.
-   Sett finansperioder til **På vent**, slik at ingen ytterligere postering forekommer. Du kan også begrense en periode til en bestemt brukergruppe mens periodesluttaktiviteter forekommer, slik at du oppnår bedre kontroll. Det er ikke lurt å sette perioder til **Lukket permanent**, fordi du kan ikke åpne en periode som er lukket, på nytt.

Arbeidsområdet Regnskapsperiodeavslutning kan brukes til å ordne og spore oppgavene som kreves for forskjellige prosesser for periodeslutt. Refererer til emnene [Arbeidsområdet Regnskapsperiodeavslutning](financial-period-close-workspace.md) og [Årsavslutning](Year-end-close.md) hvis du vil ha mer informasjon. 






