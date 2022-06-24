---
title: Behandle satsendringer
description: Denne artikkelen beskriver hvordan du behandler endringer i fordelssatser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09714c70cb00b1a1b5dbd4613bbd70ff11d35cb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882960"
---
# <a name="process-rate-changes"></a>Behandle satsendringer


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen forklarer hvordan du behandler endringer i fordelssatser i Microsoft Dynamics 365 Human Resources når en ny eller eksisterende fordelsplan har en endring i innstillingene for rettighetsregel. Hvis en ny rettighets regel opprettes og tilordnes til planen, vil dette be systemet om å kjøre arbeiderrettigheter på nytt for å kontrollere om arbeidere nå kan være berettiget til planen, basert på nye rettighetsalternativer. 

1. I arbeidsområdet **Fordelsbehandling**, under **Behandling**, velger du **Behandling av oppdatering av satsendring**.

2. I dialogboksen **Kjør prosess for oppdatering av fordelssats** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Registreringsperiode** | Registreringsperioden som det skal behandles satsendringer for. |

3. Hvis du vil kjøre prosessen i bakgrunnen, velger du **Kjør i bakgrunnen** og utfører følgende oppgaver:

   1. Angi informasjon for prosessen.

   2. Hvis du vil definere en gjentakende jobb, velger du **Gjentakelse**, angir gjentakelsesinformasjonen og velger **OK**.

   3. Når du skal definere et jobbvarsel, velger du **Varsler**, velger varslene du vil motta, og velger deretter **OK**.

   4. Velg **OK**. Prosessen vil kjøre med parameterne du angir.

4. Velg **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
