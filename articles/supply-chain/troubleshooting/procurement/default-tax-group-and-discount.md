---
title: Standard mva-gruppe og kontantrabatt blir ikke fylt ut fra fakturakontoen
description: En standard mva-gruppe og en standard kontantrabatt blir ikke fylt ut fra fakturakontoen
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477193"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Standard mva-gruppe og kontantrabatt blir ikke fylt ut fra fakturakontoen

## <a name="symptoms"></a>Symptomer

Hvis du bruker en fakturakonto som er forskjellig fra kundekontoen, blir det ikke fylt ut en standard mva-gruppe og en standard kontantrabatt fra fakturakontoen når en bestilling opprettes.

## <a name="resolution"></a>Løsning

Denne virkemåten er standard. Standardverdiene for mva-gruppen, kontantrabattene og annen prisinformasjon er basert på kundekontoen, ikke fakturakontoen.
