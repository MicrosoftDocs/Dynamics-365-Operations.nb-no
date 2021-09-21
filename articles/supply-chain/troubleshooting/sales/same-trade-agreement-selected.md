---
title: Samme handelsavtale valgt ved oppretting av salgsordrelinjer
description: Hvis det finnes mer enn én handelsavtale definert for en gitt dato, velges alltid avtalen som har den laveste prisen ved oppretting av salgsordrelinjer.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477205"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Hvis det finnes to forretningsavtaler for overlappende datoer, velges alltid den samme

## <a name="symptoms"></a>Symptomer

Hvis to forretningsavtaler er definert for samme periode eller ved overlappende perioder, ser det ut til at samme forretningsavtale blir valgt hver gang du oppretter salgsordrelinjer som inneholder disse varene.

## <a name="resolution"></a>Løsning

Hvis det finnes mer enn én forretningsavtale for en gitt dato, velges alltid forretningsavtalen som har den laveste prisen. Hvis du vil ha mer informasjon, laster du ned følgende tekniske informasjon: [Forretningsavtaler i Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
