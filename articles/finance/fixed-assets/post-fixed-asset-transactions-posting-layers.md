---
title: Postere anleggsmiddeltransaksjoner til posteringslag
description: Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.
author: moaamer
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a80e4d1a081b5bd8c58238b0f154f8fbdc660ccb
ms.sourcegitcommit: f80819c67c0a7475315fc68ce1cb568831e2c0e7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2020
ms.locfileid: "4493678"
---
# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Postere anleggsmiddeltransaksjoner til posteringslag

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over posteringslag for anleggsmiddeltransaksjoner.

Anleggsmidler avskrives ofte på forskjellige måte for forskjellige formål. Avskrivning for skatte- og avgiftsformål beregnes ved hjelp av gjeldende skatteregler for å oppnå høyest mulig avskrivning for skatter og avgifter, mens avskrivning for rapporteringsformål beregnes i henhold til regnskapslover og standarder. De forskjellige typene avskrivning beregnes og registreres separat i posteringslagene.

Hvert tablå som er knyttet til et anleggsmiddel, er definert for et bestemt posteringslag som inneholder det totale avskrivningsmålet. Det finnes ti posteringslag: gjeldende, operasjoner, mva og sju egendefinert lag. Du kan også deaktivere postering i Finans for tablået ved å sette Poster i økonomimodul til Nei. Feltet Posteringslag settes deretter automatisk til Ingen. Tablåer som ikke posteres i Finans brukes vanligvis for mva-rapporteringsformål. Dette gir deg mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået fordi de ikke er lagret i Finans.

Anleggsmiddeljournaler defineres ved hjelp av  Journalnavn-siden under Økonomimodul > Journaloppsett > Journalnavn. Hver journal du kan postere avskrivninger i, defineres av journalnavnet for bare ett posteringslag. Posteringslaget i journalen kan ikke endres. Denne begrensningen bidrar til å sikre at transaksjoner for hvert posteringslag holdes separat. Minst ett journalnavn må opprettes for hvert posteringslag. Hvis du bruker tablåer som ikke posteres til økonomimodulen, må du også opprette en journal der posteringslaget er satt til Ingen.

Du kan angi finanskontoer for anleggsmiddeltransaksjoner på siden Posteringsprofiler for anleggsmidler. For hver posteringsprofil må du velge den relevante transaksjonstypen og tablået, og deretter angi finanskontoene. Definer posteringsprofilposten for hvert tablå som skal posteres til økonomimodulen.

Anleggsmidlet kan angis i dokumenter som bare støtter **Gjeldende** posteringslag, for eksempel **Bestilling**, **Ventende leverandørfakturaer**, **Salgsordre** eller **Fritekstfaktura**. Når du velger en anleggsmiddel-ID i ett av disse dokumentene, blir aktivatablået filtrert til tablået med **Gjeldende** posteringslag, og fylles ut automatisk under postering når systemet validerer at anleggsmiddelposteringslaget er **Gjeldende**. Hvis denne valideringen ikke kan fullføres, stoppes posteringsprosessen. 

> [!NOTE] 
> Ved å bruke avledede tablåer, kan du postere transaksjoner til forskjellige posteringslag samtidig. Transaksjonene for det primære tablået opprettes i en journal eller et kildedokument der posteringslaget samsvarer med posteringslaget for tablået. Under posteringen posteres de avledede tablåtransaksjonene til de respektive posteringslagene. 


Hvis du vil ha mer informasjon, kan du se [Avledede tablåer](derived-books.md) og [Postere med avledede tablåer](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]