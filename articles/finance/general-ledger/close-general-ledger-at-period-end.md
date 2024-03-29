---
title: Lukk økonomimodulen ved periodeslutt
description: Denne artikkelen beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42a5df1cd1a73462c93012b26f9b9b5c1631f2ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878048"
---
# <a name="close-the-general-ledger-at-period-end"></a>Lukk økonomimodulen ved periodeslutt

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver oppgavene som vanligvis utføres når du utfører en periodeavslutning for økonomimodulen. 

I Økonomimodul kan du fullføre avslutningsprosedyrer for en periode eller et år. Avslutningsprosesser gjør systemet klart for en ny periode. Hvis du vil gjøre klart for et nytt år, må du kjøre årsavslutningsprosessen. Hver organisasjon har forskjellige prosesser og trinn som utføres på slutten av en periode. Her er noen av de valgfrie trinnene for periodeslutt:

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

Arbeidsområdet **Regnskapsperiodeavslutning** kan brukes til å ordne og spore oppgavene som kreves for forskjellige prosesser for periodeslutt. 


Hvis du vil ha mer informasjon, kan du se følgende emner:
- [Arbeidsområde for regnskapsperiodeavslutning](financial-period-close-workspace.md) 
- [Årsavslutning](Year-end-close.md)  
- [Lukke masseregnskapsperiode](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
