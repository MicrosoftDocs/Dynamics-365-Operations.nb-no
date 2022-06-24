---
title: Får ikke tilgang til avgiftstjeneste
description: Denne artikkelen forklarer hvordan du feilsøker en tilgangsfeil i avgiftsberegningstjenesten.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 65d819b97be3d1238bc0ecfc201b4e24edac8616
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861229"
---
# <a name="failed-to-access-tax-service"></a>Får ikke tilgang til avgiftstjeneste

[!include [banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du retter feilen «Får ikke tilgang til avgiftstjeneste» i avgiftsberegningstjenesten.

## <a name="symptoms"></a>Symptomer

I Microsoft Dynamics 365 Finance går du til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftstjeneste**. I **Generelt**-fanen aktiverer du alternativet **Aktiver avgiftsberegning**. Hvis du deretter prøver å velge en verdi i feltet **Navn på funksjonsoppsett**, oppstår det en feil. Feilmeldingen er «Får ikke tilgang til avgiftstjeneste.»

## <a name="cause"></a>Årsak

Denne feilen oppstår fordi Finance ikke får tilgang til avgiftsberegningstjenesten.

## <a name="resolution"></a>Oppløsning 

1. Logg på Microsoft Dynamics Lifecycle Services (LCS).
2. Finn elementet **Avgiftsberegning** i **Miljøtillegg**-fanen på **Miljø**-siden, og gå gjennom statusen for det. Statusen skal være **Installerer** eller **Installert**. Hvis tilleggsprogrammet for avgiftsberegningstjenesten ikke er installert, får du feilmeldingen.

## <a name="mitigation"></a>Reduksjon

1. Velg **Installer et nytt tilleggsprogram** i delen **Power Platform-integrering** på **Finans**-siden i LCS.
2. Rull ned til bunnen av siden, og velg tilleggsprogrammet **Avgiftsberegning** for å installere det.
3. Gå tilbake til Finance-miljøet, og prøv å få tilgang til avgiftsberegningstjenesten.

> [!NOTE]
> Før du installerer avgiftsberegningstjenesten, går du gjennom [forutsetningene for avgiftsberegningstjenesten](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Hvis du ikke kan installere tilleggsprogrammet fordi delen **Power Platform-integrering** ikke er tilgjengelig, kan du se [Oversikt over tilleggsprogram](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Hvis du fortsatt får feilen etter at du har installert tilleggsprogrammet, kontakter du systemansvarlig.
