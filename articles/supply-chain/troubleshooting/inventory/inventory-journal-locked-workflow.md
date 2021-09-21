---
title: Lagerjournalen er låst, og den satsvise jobben for arbeidsflyten fungerer ikke
description: En av lagerjournalene er låst av en eller annen operasjon og blir ikke frigitt
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477173"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Lagerjournalen er låst, og den satsvise jobben for arbeidsflyten fungerer ikke

## <a name="symptoms"></a>Symptomer

En av lagerjournalene er låst av en eller annen operasjon og blir ikke frigitt. Hvis det for eksempel oppstår en ukjent feil under postering (som er en systemlåst operasjon), kan det hende at journalen forblir låst av systemet. I dette tilfellet vil behandlingsprogrammet for arbeidselement for arbeidsflyt generere en feil mens det foretar låsvalidering.

## <a name="resolution"></a>Løsning

Logg deg på SQL Server-forekomsten for Supply Chain Management, og kontroller om **InventJournalTable.SystemBlocked** er satt til *1*. Hvis den er det, må du kontrollere at journalen ikke er låst, og deretter tilbakestille **InventJournalTable.SystemBlocked** til *0*.
