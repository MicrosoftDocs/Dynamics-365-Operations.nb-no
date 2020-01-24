---
title: Integrert avgift
description: Dette emnet beskriver integreringen av avgiftsdata mellom Finance and Operations og Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853865"
---
# <a name="integrated-tax"></a>Integrert avgift

[!include [banner](../includes/banner.md)]

Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt. Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.

## <a name="templates"></a>Maler

Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.

Finance and Operations   | Andre Dynamics 365-apper
-------------------------|---------------------------------
Mva-koder                  | msdyn\_taxcodes.md
Mva-grupper               | msdyn\_taxgroups.md
Mva-varegrupper          | msdyn\_taxitemgroups.md
Avgiftsfritak           | msdyn\_taxexemptcodes.md
Skattemyndigheter          | msdyn\_taxauthorities.md
Kildeskattkoder      | msdyn\_withholdingtaxcodes.md
Kildeskattgrupper   | msdyn\_withholdingtaxgroups.md
Finanskontogruppe for avgift | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

