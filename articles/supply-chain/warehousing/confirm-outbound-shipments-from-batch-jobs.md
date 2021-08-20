---
title: Bekreft utgående forsendelser fra satsvise jobber
description: Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 82945ac3426bb5e063006495a20463d204fb3c8c9dd90bb51a1f023edeaff728
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762752"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Bekreft utgående forsendelser fra satsvise jobber

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering. Den satsvise jobben som beskrives her, gjelder bare for overføringsordreforsendelser, ikke salgsordrer.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Aktivere funksjonen Bekreft utgående forsendelser fra satsvise jobber

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. Funksjonen er oppført som:

- **Modul** - *Lagerstyring*
- **Funksjonsnavn** - *Bekreft utgående forsendelser fra satsvise jobber*

## <a name="process-outbound-shipments"></a>Behandle utgående forsendelser

Slik setter du opp en planlagt satsvis jobb for å kjøre den utgående forsendelsesbekreftelsen for laster som er klare til levering:

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle utgående forsendelser**.
1. Dialogboksen **Bekreft forsendelse** åpnes. Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .
1. Dialogboksen for redigeringsprogram for spørring åpnes. På **Område**-fanen legger du til en tabell med følgende verdier:
    - **Tabell** - *Laster*
    - **Utledet tabell** - *Laster*
    - **Felt** - *Laststatus*
    - **Vilkår** - *Lastet*
1. Velg **OK** for å gå tilbake til dialogboksen **Bekreft forsendelse**.
1. På hurtigfanen **Kjør i bakgrunnen** setter du **Satsvis behandling** til **Ja**.
1. På hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.
1. Dialogboksen **Definer regelmessighet** åpnes. Angi kjøretidsplanen etter behov for firmaet.
1. Velg **OK** for å gå tilbake til dialogboksen **Bekreft forsendelse**.
1. Velg **OK** i dialogboksen **Bekreft forsendelse** for å legge til den satsvise jobben i den satsvise køen.

Hvis du vil ha mer informasjon, kan du se [Oversikt over satsvis behandling](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]