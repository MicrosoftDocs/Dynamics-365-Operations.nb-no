---
title: Behandle endringer i levetidshendelse
description: Denne artikkelen beskriver hvordan du behandler endringer i livshendelser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38b36f2165c9794091321c193f10dd37cc92b866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858192"
---
# <a name="process-life-event-changes"></a>Behandle endringer i levetidshendelse


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Behandle endringer i levetidshendelser i Microsoft Dynamics 365 Human Resources for to endringer i levetidshendelse:

- Bursdagsendringer
- Overstyr utløpsendringer for rettighetsregel 

1. I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av endring av levetidshendelse**.

2. I dialogboksen **Kjør prosess for endring av levetidshendelse** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | Registreringsperiode | Registreringsperioden som det skal behandles endringer i levetidshendelse for. |
   | Juridisk enhet | Den juridiske enheten som det skal behandles endringer i levetidshendelse for. |

3. Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for prosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Prosessen vil kjøre med parameterne du angir.

4. Velg **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
