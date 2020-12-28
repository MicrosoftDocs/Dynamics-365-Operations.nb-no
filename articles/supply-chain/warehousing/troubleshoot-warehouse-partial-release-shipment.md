---
title: Feilsøke delvise frigivelser og delvise leveringer
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645954"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Feilsøke delvise frigivelser og delvise leveringer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med delvise frigivelser og delvise leveringer i Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Frigivelsesstatusen til en salgsordre forblir Delvis frigitt, selv etter at salgsordren er fakturert.

### <a name="issue-description"></a>Problembeskrivelse

En salgsordre er en leveringsordre, men én eller flere varer i den har en annen leveringsmåte. Når ordren er fakturert, har den fremdeles frigivelsesstatusen *Delvis frigitt*.

En salgsordre har for eksempel to varer: en for levering og en for plukking. Både leveringen og plukkingen er utført. Derfor er begge linjene fakturert. Frigivelsesstatusen vises imidlertid fremdeles som *Delvis frigitt*, som er villedende.

### <a name="issue-resolution"></a>Problemløsning

Frigivelsesstatusen gjelder bare for ordrelinjer der varene er aktivert for lagerstyring. Derfor forblir frigivelsesstatusen *Delvis frigitt* i dette scenarioet. Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. En utvidelse kan legges til som en del av følgeseddelen og faktureringsprosessen for å oppdatere frigivelsesstatusen.
