---
title: Regnskapskildeutforsker
description: "Denne artikkelen inneholder informasjon om regnskapskildeutforsker, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: d21f214ef8a29c19f0af1d4a2bdfc3264987f0b8
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---

# <a name="accounting-source-explorer"></a>Regnskapskildeutforsker

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om regnskapskildeutforsker, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen.

Regnskapskildeutforsker er en ny side som viser kildeinformasjon. Du kan bruke Regnskapskildeutforsker enten som et frittstående verktøy eller til å analysere detaljene bak regnskapsoppføringer i økonomimodulen. Du kan for eksempel bruke Regnskapskildeutforsker til å få den mest detaljerte kildeinformasjonen for en saldo i Råbalanse eller for en bilagstransaksjon. Du kan deretter bruke funksjonen Eksporter til Microsoft Excel for å dele opp informasjonen ytterligere i Microsoft Excel (for eksempel i en pivottabell eller pivottabellrapport).

Regnskapskildeutforsker viser alltid det samme totalbeløpet per finanskonto som Økonomimodul viser (for eksempel i Råbalanse). På samme måte som i Råbalanse kan du vise segmenter i separate kolonner. Bare velg det riktige finansdimensjonssettet. 

Du kan bruke parametere til å definere et datointervall for analysen. Denne funksjonen ligner også funksjonaliteten i Råbalanse.

Regnskapskildeutforsker viser tilleggsinformasjon basert på regnskapsdistribusjoner og, hvis det er aktuelt, prosjektregnskapsdistribusjoner for alle dokumenter som bruker kildedokumentrammeverket. Denne informasjonen omfatter pengebeløpstype, prosjekt, aktivitet, kategori og linjeegenskap. Her er noen eksempler på analysen du kan foreta:

-   Avvik mellom bestillinger og leverandørfakturaer, fordi hvert enkelt avvik representeres av en pengebeløpstype, for eksempel gebyravvik
-   Fakturerbare kontra ikke-fakturerbare timer og utgifter per prosjekt, forretningsenhet og hovedkonto

Når det gjelder kildedokumenter som bruker konseptet referanse-ID-er for kildedokument, viser Regnskapskildeutforsker ytterligere detaljer, for eksempel kunde, leverandør, arbeider, produkt, antall, enhetstekst og beskrivelser. Her er noen eksempler på analysen du kan foreta:

-   Hotellutgifter per forretningsenhet og hotellmerke for en regnskapsperiode, basert på reiseregninger
-   Rabatter per leverandør, produkt, avdeling

Når det gjelder disse dokumentene, kan du også navigere til det faktiske kildedokumentet fra Regnskapskildeutforsker.




