---
title: Opprett dekningsalternativer
description: Dette emnet beskriver dekningsalternativene i Microsoft Dynamics 365 Human Resources for en deltakers valg i en fordelsplan eller et program.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01eb0c56578cf6f6b070c4a05768ec5361993555
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065874"
---
# <a name="create-coverage-options"></a>Opprett dekningsalternativer


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dekningsalternativer bestemmer hvem som bør dekkes, eller hvor mye dekning som er tilgjengelig i en forsikringsplan. For en medisinsk plan kan du for eksempel ha et **Bare ansatt**-alternativ, et **Ansatt + 1**-alternativ, og et **Familie**-alternativ. For livsforsikring kan du tilby dekning for **1 x lønn** eller **2 x lønn**.

Når alternativer for fordelsdekning er definert, kan du bruke dem på nytt. Du kan knytte et alternativ til én eller flere planer.

> [!IMPORTANT]
> Når du har definert dekningsalternativer, knytter du dem til en fordelsplantype. Plantypen knyttes deretter til en fordelsplan eller et program. Dekningsalternativer som er knyttet til en plantype, er tilgjengelige for alle planer som opprettes med denne typen.

## <a name="create-coverage-options"></a>Opprette dekningsalternativer
1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Dekningsalternativ** | Et unikt navn på dekningsalternativet. |
   | **Beskrivelse** | En beskrivelse av dekningsalternativet. |
   | **Dekningskode** | Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype. En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype. Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent. For eksempel:<ul><li>**Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</li><li>**Emp+family** – for å være kvalifisert må den ansatte ha minst to avhengige valgt.</li></ul> |
   | **Maksimalt antall** | Det maksimale antall avhengige. |
   | **Status** | Statusen for dekningsalternativet. Hvis statusen for dekningsalternativet er satt til **Inaktiv**, kan ikke dekningsalternativet velges på plantyper. |
   | **Prosent** | Prosentbeløpet. Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet. |
   | **Divisor** | Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn. |
   | **Minste prosentandel** | Minimumsprosenten når du velger kode for prosentdekning. |
   | **Størst prosentandel** | Maksimumsprosenten når du velger kode for prosentdekning. |

4. Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.

5. Under **Selvbetjening** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillat bidragsbeløp fra ansatt** | Angir om ansatte skal kunne endre dekningsbeløpet i fordeler selvbetjent når de velger fordeler. Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn i fordeler selvbetjent. |
   | **Tillat dekningsbeløp fra ansatt** | Angir om ansatte skal kunne endre dekningsbeløpet i fordeler selvbetjent når de velger fordeler. Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening. |

6. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
