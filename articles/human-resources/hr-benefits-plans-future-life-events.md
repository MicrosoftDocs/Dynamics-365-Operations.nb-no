---
title: Konfigurere fremtidige levetidshendelser
description: Denne artikkelen beskriver hvordan du planlegger fremtidige livshendelser i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227993"
---
# <a name="configure-future-life-events"></a>Konfigurere fremtidige levetidshendelser

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Du kan planlegge fremtidige levetidshendelser i Dynamics 365 Human Resources.

1. I arbeidsområdte **Fordelsbehandling**, under **Oppsett**, velger du **Fremtidige levetidshendelser**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | Levetidshendelsesdato | Systemet behandler alle hendelser i løpet av registreringsperioden som inntreffer frem til denne datoen. |
   | Levetidshendelse logget | Datoen og klokkeslettet da levetidshendelsen ble logget. |
   | Loggtype | Viser om handlingen er én av følgende:</br></br>- **Oppdatering** – en endring i en eksisterende post som sporer levetidshendelser</br></br>- **Sett inn** – oppretting av en ny levetidshendelsespost |
   | ID for levetidshendelsestype | Den unike ID-en for levetidshendelsestypen. |
   | Levetidshendelsestype | En katalysator for å oppdatere en ansatts fordelsregistrering. Hvis du vil ha mer informasjon, kan du se delen om utløsere for levetidshendelser. |
   | Status | Om levetidshendelsen er behandlet eller ikke. |
   | Linje | Linjenummeret til den fremtidige levetidshendelsen. |

4. Velg **Lagre**. 

Du kan slette fremtidige levetidshendelser. Hvis en behandlet fremtidig livshendelse slettes, slettes også den fremtidige posten. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
