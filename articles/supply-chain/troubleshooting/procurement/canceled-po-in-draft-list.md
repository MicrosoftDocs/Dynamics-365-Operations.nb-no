---
title: Annullerte bestillinger vises i kladdelisten i arbeidsområdet
description: Annullerte bestillinger vises i kladdelisten i arbeidsområdet for bestillingsforberedelse
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477222"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Annullerte bestillinger vises i kladdelisten i arbeidsområdet

## <a name="symptoms"></a>Symptomer

Når du har annullert bestillinger som var i *Bekreftet* tilstand, vises de annullerte bestillingene likevel i listen over utkastbestillinger i arbeidsområdet for **Bestillingsklargjøring**.

## <a name="resolution"></a>Løsning

Dette problemet oppstår bare for bestillinger som er underlagt endringsadministrasjon. Dette skjer fordi avlysningen regnes som en endring som må godkjennes. Godkjenningen kan gjøres automatisk av systemet. Prosessen er derfor å sende den annullerte bestillingen til godkjenningsarbeidsflyten slik at den kan gå til *Godkjent* tilstand. På dette punktet vises ikke bestillingen lenger i listen over bestillingsforslag i arbeidsområdet **Bestillingsklargjøring**.
