---
title: Endre formater for elektronisk rapportering ved å bruke Excel-maler på nytt
description: Denne artikkelen beskriver hvordan du endrer formatet for elektronisk rapportering (ER) som brukes til å generere forretningsdokumenter ved å bruke en endret Excel-mal på nytt.
author: kfend
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 02423a75d96bef0452b8555f8c7a9f0aca0b6771
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283536"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Endre formater for elektronisk rapportering ved å bruke Excel-maler

[!include [banner](../includes/banner.md)]

Verktøyet for elektronisk rapportering (ER) brukes til å generere forretningsdokumenter i et elektronisk format. For å generere et forretningsdokument må du opprette et ER-format og deretter bruke ER-utforming til å definere oppsettet for forretningsdokumentet og angi hvilke data som skal inkluderes i det. Du kan deretter kjøre ER-formatet for å generere forretningsdokumentet.

ER-verktøyet kan brukes til å generere forretningsdokumenter som Microsoft Excel-filer. Du kan bruke et Excel-dokument som en mal for disse dokumentene. Hvis du vil definere oppsettet for dokumentet i ER-utformingen, kan du importere innholdet i Excel-dokumentet du vil bruke som mal i det definerte ER-formatet. Hvis du vil ha mer informasjon og prøve dette scenariet, spiller du av oppgaveveiledningen **ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format** (en del av forretningsprosessen 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)) . I trinnet i oppgaveveiledningen der du importerte en Excel-mal, kan du bruke den innledende malen for Excel-fil for Betalingsrapport, [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Hvis du redigerer Excel-dokumentet som brukes som en mal for et forretningsdokument, kan du bruke ny ER-funksjonalitet til å bruke den oppdaterte malen på nytt i ER-formatet. ER-formatet blir da oppdatert, slik at det samsvarer med den oppdaterte malen. Hvis du vil ha mer informasjon om denne funksjonen, kan du spille av oppgaveveiledningen **ER Endre et format for elektronisk rapportering ved å bruke en Excel-mal på nytt** (del av forretningsprosessene for 7.5.5.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10683)). I trinnet i oppgaveveiledningen der du importerte en oppdatert mal, kan du bruke den endrede malen for Excel-filen for Betalingsrapport, [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Tilleggsressurser

[Oppdatere en mal](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
