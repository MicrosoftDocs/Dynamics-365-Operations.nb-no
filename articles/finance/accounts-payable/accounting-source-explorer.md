---
title: Regnskapskildeutforsker
description: Denne artikkelen inneholder informasjon om siden Regnskapskildeutforsker, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806440"
---
# <a name="accounting-source-explorer"></a>Regnskapskildeutforsker

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om siden **Regnskapskildeutforsker**, som du kan bruke for detaljert analyse av kildeinformasjonen bak regnskapsoppføringer i økonomimodulen.

Siden **Regnskapskildeutforsker** viser kildeinformasjon. Du kan bruke den enten som et frittstående verktøy eller til å analysere detaljene bak regnskapsoppføringer i økonomimodulen. Du kan for eksempel bruke siden til å få den mest detaljerte kildeinformasjonen for en saldo i råbalansen eller for en bilagstransaksjon. Du kan deretter bruke funksjonen **Eksporter til Microsoft Excel** for å dele opp informasjonen ytterligere i Microsoft Excel (for eksempel i en pivottabell eller pivottabellrapport).

Siden **Regnskapskildeutforsker** viser alltid det samme totalbeløpet per finanskonto som Økonomimodul viser (for eksempel i råbalanse). På samme måte som i en råbalanse kan du vise segmenter i separate kolonner. Bare velg det riktige finansdimensjonssettet. 

Du kan bruke parametere til å definere et datointervall for analysen. Denne funksjonen ligner også funksjonaliteten i en råbalanse.

Regnskapskildeutforsker viser tilleggsinformasjon basert på siden **Regnskapskildeutforsker** og, hvis det er aktuelt, prosjektregnskapsdistribusjoner for alle dokumenter som bruker kildedokumentrammeverket. Denne informasjonen omfatter verdiene **Pengebeløpstype**, **Prosjekt**, **Aktivitet**, **Kategori** og **Linjeegenskap**. Her er noen eksempler på analysen du kan foreta:

- Avvik mellom bestillinger og leverandørfakturaer, fordi hvert enkelt avvik representeres av en pengebeløpstype, for eksempel gebyravvik
- Fakturerbare kontra ikke-fakturerbare timer og utgifter per prosjekt, forretningsenhet og hovedkonto

Når det gjelder kildedokumenter som bruker konseptet referanse-ID-er for kildedokument, viser **Regnskapskildeutforsker** ytterligere detaljer, for eksempel verdiene **Kunde**, **Leverandør**, **Arbeider**, **Produkt**, **Antall**, **Enhetstekst** og **Beskrivelse**. Her er noen eksempler på analysen du kan foreta:

- Hotellutgifter per forretningsenhet og hotellmerke for en regnskapsperiode, basert på reiseregninger
- Rabatter per leverandør, produkt, avdeling

Når det gjelder disse dokumentene, kan du også navigere til det faktiske kildedokumentet fra siden **Regnskapskildeutforsker**.

> [!NOTE]
> Fra og med versjon 10.0.31 er en ny funksjon for **avansert filtrering for regnskapskildeutforsker** tilgjengelig i Funksjonsbehandling. Denne funksjonen erstatter **Oppdater**-knappen for å gi en mer robust, avansert spørringserfaring som ligner på det som er tilgjengelig på siden **Bilagstransaksjoner**. Med det avanserte filteret kan du filtrere på lignende felt i forhold til det du finner på siden for **spørring for bilagstransaksjoner**, for eksempel **Finanskonto**, **Forretningsenhet**, **Kostnadssenter** og **Avdeling**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
