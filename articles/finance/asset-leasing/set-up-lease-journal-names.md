---
title: Definere leiejournalnavn
description: Dette emnet forklarer hvordan du definerer navn på leierjournaler. Leiejournalnavn angir journalene som oppføringer som kommer fra aktivaleie, posteres til.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990923"
---
# <a name="set-up-lease-journal-names"></a>Definere leiejournalnavn

[!include [banner](../includes/banner.md)]

Leiejournalnavn angir journalene som aktivaleietransaksjoner posteres til. Bare journalnavn som er tilordnet til **Aktivaleie**-journaltyper, vises i feltene **Opprinnelig føring** og **Månedlig journalnavn** på siden **Parametere for aktivaleie**. Bare journaltypen **registrering av leverandørfaktura** kan tilordnes til feltet for **fakturajournalnavn**.

Følg denne fremgangsmåten for å konfigurere navn på leiejournaler:

1. Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.
2. Gå til kategorien **Generelt** i feltet **navn på journal for opprinnelig føring**, og velg en journal. Alle journaloppføringer for opprinnelig føring posteres til dette journalnavnet.
3. I feltet for **fakturajournalnavn** velger du en journal. Hvis alternativet **Betal til leverandør** er satt til **Ja** for leietablået, vil leie- og utgiftsbetalingsfakturaer posteres til dette journalnavnet.
4. I feltet for **leiejournalnavn** velger du en journal. Alle poster for avskrivning, rente og kortsiktige omklassifiseringer vil bli postert til dette journalnavnet. Hvis alternativet **Betal til leverandør** er satt til **Nei** for leietablået, vil leiebetalings- og utgiftsbetalingsoppføringer også posteres til dette journalnavnet.
