---
title: Postere anleggsmiddeltransaksjoner til posteringslag
description: Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 4b112eee303604149c7609972a60c2014d4be423
ms.lasthandoff: 03/31/2017


---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Postere anleggsmiddeltransaksjoner til posteringslag

Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.

Anleggsmidler avskrives ofte på forskjellige måte for forskjellige formål. Avskrivning for skatte- og avgiftsformål beregnes ved hjelp av gjeldende skatteregler for å oppnå høyest mulig avskrivning for skatter og avgifter, mens avskrivning for rapporteringsformål beregnes i henhold til regnskapslover og standarder. De forskjellige typene avskrivning beregnes og registreres separat i posteringslagene.

Hvert tablå som er knyttet til et anleggsmiddel, er definert for et bestemt posteringslag som inneholder det totale avskrivningsmålet. Det finnes ti posteringslag: gjeldende, operasjoner, mva og sju egendefinert lag. Du kan også deaktivere postering i Finans for tablået ved å sette Poster i økonomimodul til Nei. Feltet Posteringslag settes deretter automatisk til Ingen. Bøker som ikke bokfører i Finans brukes vanligvis for mva-rapporteringsformål. Denne metoden gir mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået, fordi de ikke har blitt lagret i Finans.

Anleggsmiddeljournaler defineres ved hjelp av  Journalnavn-siden under Økonomimodul > Journaloppsett > Journalnavn. Hver journal du kan postere avskrivninger i, defineres av journalnavnet for bare ett posteringslag. Posteringslaget i journalen kan ikke endres. Denne begrensningen bidrar til å sikre at transaksjoner for hvert posteringslag holdes separat. Minst ett journalnavn må opprettes for hvert posteringslag. Hvis du bruker bøker som ikke postere til finans, må du også opprette en journal der posteringslaget er satt til ingen.

Du kan angi finanskontoer for anleggsmiddeltransaksjoner på siden Posteringsprofiler for anleggsmidler. For hver posteringsprofil må du velge den relevante transaksjonstypen og tablået, og deretter angi finanskontoene. Definer posteringsprofilposten for hvert tablå som skal posteres til økonomimodulen.

> [!NOTE] 
> Ved hjelp av avledede bøker, kan du postere transaksjoner til forskjellige posteringslag samtidig. Du oppretter transaksjonene for det primære tablået i en journal der posteringslaget samsvarer med posteringslaget for tablået. Under posteringen posteres de avledede tablåtransaksjonene til de respektive posteringslagene.

For mer informasjon, se [avledet bøker](derived-books.md) og [postering med avledede bøker](post-derived-value-models.md).


