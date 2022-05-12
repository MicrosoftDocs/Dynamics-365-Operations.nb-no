---
title: Definere leiejournalnavn
description: Dette emnet forklarer hvordan du definerer navn på leierjournaler. Leiejournalnavn angir journalene som oppføringer som kommer fra aktivaleie, posteres til.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a92461e742f1675e4cfda89e6c80c5b087ff5bfb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644904"
---
# <a name="set-up-lease-journal-names"></a>Definere leiejournalnavn

[!include [banner](../includes/banner.md)]


Leiejournalnavn angir journalene som aktivaleietransaksjoner posteres til. Bare journalnavn som er tilordnet til **Aktivaleie**-journaltyper, vises i feltene **Opprinnelig føring** og **Månedlig journalnavn** på siden **Parametere for aktivaleie**. Bare journaltypen **registrering av leverandørfaktura** kan tilordnes til feltet for **fakturajournalnavn**.

Systemet låser bestemte økonomiske felt fra å bli redigert for å forhindre avvik mellom transaksjonene og planene. Noen av feltene som er låst, inkluderer: **Konto**, **Beløp**, **Finansdimensjoner**, **Valuta** og **Transaksjonstype**. I tillegg kan du ikke legge til eller slette journaloppføringslinjer i noen journaloppføringer for anleggsmiddelleasing, fordi dette kan føre til avvik mellom planene og transaksjonene.


Følg denne fremgangsmåten for å konfigurere navn på leiejournaler.

1. Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.
2. Gå til kategorien **Generelt** i feltet **navn på journal for opprinnelig føring**, og velg en journal. Alle journaloppføringer for opprinnelig føring posteres til dette journalnavnet.
3. I feltet for **fakturajournalnavn** velger du en journal. Hvis alternativet **Betal til leverandør** er satt til **Ja** for leietablået, vil leie- og utgiftsbetalingsfakturaer posteres til dette journalnavnet.
4. I feltet for **leiejournalnavn** velger du en journal. Alle poster for avskrivning, rente og kortsiktige omklassifiseringer vil bli postert til dette journalnavnet. Hvis alternativet **Betal til leverandør** er satt til **Nei** for leietablået, vil leiebetalings- og utgiftsbetalingsoppføringer også posteres til dette journalnavnet.
5. I feltet for **Journalnavn for leieendring** velger du en journal. Transaksjoner for leiejustering, oppsigelse og verdiforringelse blir postert til dette journalnavnet. Journalnavnet du velger, bør ikke ha en arbeidsflyt eller godkjenning tilordnet. Hvis navnet på leieendringsjournalen ikke er definert, vil utleiejustering, oppsigelse og transaksjonen for verdiforringelse bli postert til journalnavnet som er valgt i feltet for **leiejournalnavn**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
