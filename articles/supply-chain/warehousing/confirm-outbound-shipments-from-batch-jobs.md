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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4af84383fe1d214849d5d05463bd0cbfad7d0536
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778479"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Bekreft utgående forsendelser fra satsvise jobber

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering. Den satsvise jobben som beskrives her, gjelder bare for overføringsordreforsendelser, ikke salgsordrer.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Aktivere funksjonen Bekreft utgående forsendelser fra satsvise jobber

Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Administratorer kan bruke siden [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere eller deaktivere den hvis det er nødvendig. Her vises funksjonen som:

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