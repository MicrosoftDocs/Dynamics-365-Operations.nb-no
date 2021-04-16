---
title: Opprette dekningsalternativer
description: Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803687"
---
# <a name="create-coverage-options"></a>Opprette dekningsalternativer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dekningsalternativer i Microsoft Dynamics 365 Human Resources er nivåer av dekning for en deltakers valg i en fordelsplan eller et program. Dekningsalternativer kan for eksempel inkludere **Bare ansatte** for en medisinsk plan, eller **2x lønn** for en forsikringsplan for livstid. Når det er definert, kan du bruke alternativer for fordelsdekning på nytt. Du kan knytte et alternativ til én eller flere planer.

Når du har definert dekningsalternativer, knytter du dekningsalternativene til en fordelsplantype. Plantypen knyttes deretter til en fordelsplan eller et program. Dekningsalternativer som er knyttet til en plantype, er tilgjengelige for alle planer som opprettes med denne plantypen. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Dekningsalternativer**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Dekningsalternativ** | Et unikt navn på dekningsalternativet. |
   | **Beskrivelse** | En beskrivelse av dekningsalternativet. |
   | **Dekningskode** | Dekningskoder som tilordner minimums- og maksimumsbeløp for hver enkelt berettigede, dekkede persontype. En dekningskode angir hvem som er dekket av eller hvor mye dekning som er tillatt for en plantype. Du kan uttrykke dekningsbeløpet som et valutabeløp eller en prosent. For eksempel:</br></br>- **Emp+1** – for å være kvalifisert må den ansatte ha én avhengig valgt (hvis flere er valgt, er de ikke lenger kvalifisert).</br></br>- **Emp+familie** – for å være kvalifisert må den ansatte ha minst to avhengige valgt. |
   | **Maksimalt antall** | Det maksimale antall avhengige. |
   | **Status** | Statusen for dekningsalternativet. Hvis statusen for dekningsalternativet er satt til Inaktiv, kan ikke dekningsalternativet velges på plantyper. |
   | **Prosent** | Prosentbeløpet. Dette feltet er bare aktivt hvis % x lønn ble valgt i Dekningskode-feltet. |
   | **Divisor** | Divisoren som skal brukes i beregningen når du velger dekningskoden % x lønn. |
   | **Minste prosentandel** | Minimumsprosenten når du velger kode for prosentdekning. |
   | **Størst prosentandel** | Maksimumsprosenten når du velger kode for prosentdekning. |

4. Under **Alternativer for rettighet for personlig kontakt** knytter du det aktuelle rettighetsalternativet for personlige kontakter til hvert dekningsalternativ.

5. Under **Selvbetjening** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillat bidragsbeløp fra ansatt** | Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler. Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på fordeler selvbetjent. |
   | **Tillat dekningsbeløp fra ansatt** | Angir om ansatte skal kunne endre dekningsbeløpet på fordeler selvbetjent når de velger fordeler. Hvis du merker av i denne avmerkingsboksen, beregner systemet fordelsplanparametere basert på dekningsbeløpet den ansatte legger inn på i Ansattselvbetjening. |

6. Velg **Lagre**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]