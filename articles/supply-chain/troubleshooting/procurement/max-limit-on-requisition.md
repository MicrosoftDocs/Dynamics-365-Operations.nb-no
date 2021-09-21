---
title: Maksimumsgrensen for innkjøpsavtale som ikke er effektiv på en innkjøpsrekvisisjon
description: Maksimumsgrensen for innkjøpsavtale som ikke er effektiv på en innkjøpsrekvisisjon
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477178"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>Maksimumsgrensen for innkjøpsavtale som ikke er effektiv på en innkjøpsrekvisisjon

## <a name="symptoms"></a>Symptomer

Når en innkjøpsrekvisisjon er koblet til en kjøpsavtale, gjelder ikke maksimumsgrensen fra kjøpsavtalen i innkjøpsrekvisisjonen. Standard prisinformasjon angis på riktig måte, men mer enn maksimumsgrensen fra kjøpsavtalen kan bestilles i innkjøpsrekvisisjonen.

## <a name="resolution"></a>Løsning

Denne virkemåten er forventet. Fordi rekvisisjoner ikke alltid er godkjent, skal det ikke reserveres et antall eller et beløp på kjøpsavtalen. Derfor oppfyller du ikke maksimumsgrensen fra kjøpsavtalen.
