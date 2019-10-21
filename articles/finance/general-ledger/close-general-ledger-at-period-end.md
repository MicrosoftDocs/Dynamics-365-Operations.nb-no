---
title: Lukke økonomimodulen ved periodeslutt
description: Dette emnet beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eca533ed1621ec3507d8510f75842c0f0165275
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186745"
---
# <a name="close-the-general-ledger-at-period-end"></a>Lukke økonomimodulen ved periodeslutt

[!include [banner](../includes/banner.md)]

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

Arbeidsområdet Regnskapsperiodeavslutning kan brukes til å ordne og spore oppgavene som kreves for forskjellige prosesser for periodeslutt. 


Hvis du vil ha mer informasjon, kan du se følgende emner:
- [Arbeidsområde for regnskapsperiodeavslutning](financial-period-close-workspace.md) 
- [Årsavslutning](Year-end-close.md)  
- [Lukke masseregnskapsperiode](tasks/mass-financial-period-close.md)




