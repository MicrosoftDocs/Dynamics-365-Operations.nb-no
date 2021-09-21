---
title: Ferdigmeldingsoppdatering mislykkes med en manglende antallsfeil
description: Hvis du prøver å avslutte en produksjonsordre mens du rapporterer antall feil, men ikke tiden eller materialantallet, fullføres ikke ferdigmeldingsoppdateringen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477171"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Ferdigmeldingsoppdatering mislykkes med en manglende antallsfeil

## <a name="symptoms"></a>Symptomer

Du prøver å rapportere en produksjonsordre som fullført mens du rapporterer antall feil, men ikke mens du rapporterer tiden eller materialantallet. Ferdigmeldingsoppdateringen mislykkes når du prøver å avslutte produksjonsordren, og du får følgende feilmelding:

> Manglende ferdigmeldt antall.

## <a name="resolution"></a>Løsning

Hvis du rapporterer antallet feil i en produksjonsordre, må du også rapportere det korrekte antallet.
