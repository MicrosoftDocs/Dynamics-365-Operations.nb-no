---
title: Konfigurer parametere for Fordelsbehandling per firma
description: Konfigurer parametere for Fordelsadministrasjon per firma i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057628"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Konfigurer parametere for Fordelsbehandling per firma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

For hver organisasjon som tilbyr fordeler, må du konfigurere innstillinger for bekreftelse-e-poster for fordeler.

## <a name="configure-confirmation-email-settings"></a>Konfigurere e-postinnstillinger for bekreftelse

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Human Resources**.

2. I kategorien **Fordelsbehandling** angir du verdier for følgende felt: 

   | Felt | beskrivelse |
   | --- | --- |
   | **Send e-postbekreftelse** | Når denne funksjonen er aktivert, sendes det en bekreftelses-e-post til ansatte når de sjekker ut fra fordelsregistreringen i Ansattselvbetjening. |
   | **Mal for e-postbekreftelse** | Velg e-postmalen for organisasjonen som skal brukes ved sending av registreringsbekreftelsen. Hvis du ikke velger en mal, blir følgende generelle e-post sendt:<br><br>%EmployeeFirstName%,<br><br>Gratulerer! Du har fullført fordelsregistreringen.<br><br>Takk,<br><Company/Org name>-fordeler. |
   | **Standard e-postadresse for avsender** | E-postadressen som skal brukes når du sender e-postmeldingen med bekreftelsen. |

3. Velg **Lagre**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]