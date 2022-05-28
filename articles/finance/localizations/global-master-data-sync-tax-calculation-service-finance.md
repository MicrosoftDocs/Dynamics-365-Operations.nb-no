---
title: Synkroniser avgiftsoppsettet fra avgiftsberegningstjenesten til Dynamics 365 Finance
description: Dette emnet beskriver hvordan du synkroniserer hoveddata for avgiftsoppsett fra avgiftsberegningstjenesten til Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a9c11a6f5946d56b9e58a02c37f18adec155661
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687793"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Synkroniser avgiftsoppsettet fra avgiftsberegningstjenesten til Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du synkroniserer hoveddata for avgiftsoppsett fra avgiftsberegningstjenesten til Microsoft Dynamics 365 Finance.

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
