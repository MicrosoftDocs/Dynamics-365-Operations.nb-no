---
title: Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt
description: Dette emnet beskriver hvordan du endrer formatet for elektronisk rapportering (ER) som brukes til å generere forretningsdokumenter ved å bruke en endret Excel-mal på nytt.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d828412e0d804acf6e6141778512e899bc78a7d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092850"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Endre formater for elektronisk rapportering ved å bruke Excel-maler

[!include [banner](../includes/banner.md)]

Verktøyet for elektronisk rapportering (ER) brukes til å generere forretningsdokumenter i et elektronisk format. For å generere et forretningsdokument må du opprette et ER-format og deretter bruke ER-utforming til å definere oppsettet for forretningsdokumentet og angi hvilke data som skal inkluderes i det. Du kan deretter kjøre ER-formatet for å generere forretningsdokumentet.

ER-verktøyet kan brukes til å generere forretningsdokumenter som Microsoft Excel-filer. Du kan bruke et Excel-dokument som en mal for disse dokumentene. Hvis du vil definere oppsettet for dokumentet i ER-utformingen, kan du importere innholdet i Excel-dokumentet du vil bruke som mal i det definerte ER-formatet. Hvis du vil ha mer informasjon og prøve dette scenariet, spiller du av oppgaveveiledningen **ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format** (en del av forretningsprosessen 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)) .

Hvis du redigerer Excel-dokumentet som brukes som en mal for et forretningsdokument, kan du bruke ny ER-funksjonalitet til å bruke den oppdaterte malen på nytt i ER-formatet. ER-formatet blir da oppdatert, slik at det samsvarer med den oppdaterte malen. Hvis du vil ha mer informasjon om denne funksjonen, kan du spille av oppgaveveiledningen **ER Endre et format for elektronisk rapportering ved å bruke en Excel-mal på nytt** (del av forretningsprosessene for 7.5.5.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10683)). I trinnet i oppgaveveiledningen der du importerte en oppdatert mal, kan du bruke den endrede malen for Excel-filen for Betalingsrapport, SampleVendPaymWsReport2, som mal.
