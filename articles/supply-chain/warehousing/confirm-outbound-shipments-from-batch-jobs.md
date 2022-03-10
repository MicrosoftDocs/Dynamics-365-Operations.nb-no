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
ms.openlocfilehash: f68dcfc0c1454ee5b095e186c52faa6c83bf8dc6
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103921"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Bekreft utgående forsendelser fra satsvise jobber

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer en satsvis jobb som automatisk bekrefter utgående overføringsordreforsendelser for laster som er klare til levering. Den satsvise jobben som beskrives her, gjelder bare for overføringsordreforsendelser, ikke salgsordrer.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Bekreft utgående forsendelser fra satsvise jobber

Du må aktivere funksjonen *Bekreft utgående forsendelser fra satsvise jobber* for systemet for å kunne bruke funksjonaliteten som beskrives i dette emnet. Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Bekreft utgående forsendelser fra satsvise jobber* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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