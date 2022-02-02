---
title: Synkroniser mva-oppsettet fra avgiftsberegningstjenesten til Dynamics 365 Finance
description: Dette emnet beskriver hvordan du synkroniserer hoveddata for mva-oppsett fra avgiftsberegningstjenesten til Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d5d994934014a146f825431cb53dfbef8fe20bc8
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965143"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Synkroniser mva-oppsettet fra avgiftsberegningstjenesten til Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du synkroniserer hoveddata for mva-oppsett fra avgiftsberegningstjenesten til Microsoft Dynamics 365 Finance.

Når du har fullført de nødvendige trinnene i [Kom i gang med avgiftsberegning](global-get-started-with-tax-calculation-service.md), synkroniseres følgende avgiftsoppsettsdata automatisk fra avgiftsberegningstjenesten til Finance.

## <a name="sales-tax-code"></a>Mva-kode

| Avgiftsberegningstjeneste           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Avgiftskode                          | Mva-kode                      |
| Beskrivelse                       | Navn                                |
| Brukerinndata                        | Utligningsperiode                   |
| Brukerinndata                        | Finansposteringsgruppe                |
| Brukerinndata                        | Merverdiavgiftsvaluta                  |
| En negativ avgiftssats er konfigurert | Tillat negativ mva-prosent |

## <a name="tax-value"></a>Avgiftsverdi

| Avgiftsberegningstjeneste | Finance                   |
| ----------------------- | ------------------------- |
| Fra transaksjonsdato   | Fra dato                 |
| Til transaksjonsdato     | Til dags dato                   |
| Minimumsbeløp          | Minimumsgrense             |
| Maksimumsbeløp          | Maksimumsgrense             |
| Sats                | Verdi                     |
| Ikke-fradragsberettiget sats     | Ikke-fradragsberettiget prosent |

## <a name="tax-limits"></a>Avgiftsgrenser

| Avgiftsberegningstjeneste | Finance           |
| ----------------------- | ----------------- |
| Fra transaksjonsdato   | Fra dato         |
| Til transaksjonsdato     | Til dags dato           |
| Minimum avgiftsbeløp      | Minste merverdiavgift |
| Maksimum avgiftsbeløp      | Høyeste merverdiavgift |

## <a name="sales-tax-group"></a>Merverdiavgiftsgruppe

| Avgiftsberegningstjeneste                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Avgiftsgruppe                                       | Merverdiavgiftsgruppe                            |
| Avgiftskoder under denne avgiftsgruppen                  | Mva-koder under denne mva-gruppen |
| Avgiftskoden er merket som **Er fritak**         | Avgiftsfri                                     |
| Avgiftskoden er merket som **Er fritak**         | Fritakskode                                |
| Avgiftskoden er merket som **Er Snudd avregning** | Snudd avregning                             |
| Avgiftskoden er merket som **Er Bruk avgift**        | Use tax                                    |

## <a name="item-sales-tax-group"></a>Varens mva-gruppe

| Avgiftsberegningstjeneste             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Vareavgiftsgruppe                      | Varens mva-gruppe                            |
| Avgiftskoder under denne vareavgiftsgruppen | Mva-koder under denne mva-varegruppen |

Når synkroniseringen er fullført, kan du fortsette å vedlikeholde de gjenværende parameterne i Finance for posterings- og rapporteringsformål.

> [!NOTE]
> Synkronisering av avgiftsoppsettet fra Finance til avgiftsberegningstjenesten støttes ikke. For et eksisterende Finance-miljø må du først opprette avgiftsoppsettet i avgiftsberegningstjenesten. Deretter synkroniserer du oppsettsdataene tilbake til Finance-miljøet.
