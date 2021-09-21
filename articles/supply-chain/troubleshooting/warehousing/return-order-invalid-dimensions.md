---
title: Kan ikke opprette belastningslinje på grunn av ugyldige lagerdimensjoner
description: Når du prøver å frigi en retursalgsordre til lageret, kan det hende du får en feilmelding om ugyldige lagerdimensjoner. Fjern disse fra ordrelinjen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477216"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Kan ikke opprette belastningslinje for retursalgsordre på grunn av ugyldige lagerdimensjoner

## <a name="symptoms"></a>Symptomer

Du kan få følgende feilmelding når du prøver å frigi en retursalgsordre til lageret:

> Du kan ikke opprette en lastlinje for denne ordrelinjen fordi den inneholder lagerdimensjoner som er ugyldige. Du kan ikke referere til lagerdimensjoner som finnes under lokasjonsdimensjonen i reservasjonshierarkiet. Fjern de ugyldige dimensjonene fra ordrelinjen.

## <a name="resolution"></a>Løsning

Dessverre støtter ikke produktet lastbehandling for en salgsreturprosess. Derfor kan du ikke frigi retursalgsordren til lageret.

På salgsordretransaksjoner kan du ikke referere til lagerdimensjoner som finnes under **Lokasjon**-dimensjonen i reservasjonshierarkiet. Løsningen er å fjerne de ugyldige dimensjonene fra ordrelinjen.
