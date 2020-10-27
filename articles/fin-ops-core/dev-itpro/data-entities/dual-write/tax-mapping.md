---
title: Integrert avgift
description: Dette emnet beskriver integreringen av avgiftsdata mellom Finance and Operations og Common Data Service .
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979335"
---
# <a name="integrated-tax"></a>Integrert avgift

[!include [banner](../../includes/banner.md)]



Avgiftsoppsettsdata definerer oppsettet for både indirekte avgifter (mva, merverdiavgift, salgsskatt) og kildeskatt. Den beskriver avgiftsberegningsregelen, mva-satsen, avgiftsregnskapet, utligningen og andre begreper.

## <a name="templates"></a>Maler

Avgiftsdata inkluderer en samling enhetstilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.

Finance and Operations-apper | Modelldrevne apper i Dynamics 365 | beskrivelse |
-------------------------|---------------------------------|----|
Merverdiavgiftsgruppe for vare | msdyn_taxitemgroups |
Skattemyndigheter | msdyn_taxauthorities |
Enhet for mva-fritakskoder for CDS | msdyn_taxexemptcodes |
Mva-grupper | msdyn_taxgroups |
Finansposteringsgrupper for mva V2 | msdyn_taxpostinggroups |
Kildeskattkoder | msdyn_withholdingtaxcodes |
Kildeskattgrupper | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

