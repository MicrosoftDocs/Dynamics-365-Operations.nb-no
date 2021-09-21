---
title: Du kan bare utføre en bestillingshandling for fullt distribuerte linjenumre
description: Du kan bare utføre en handling på en bestilling etter at linjenumrene er fullt distribuert
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1ef2a938a2a17bc2dbf38d09918eabdbccca8a28
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477238"
---
# <a name="you-can-only-complete-a-purchase-order-action-for-fully-distributed-line-numbers"></a>Du kan bare utføre en bestillingshandling for fullt distribuerte linjenumre

## <a name="symptom"></a>Symptom

Du kan bare utføre en handling på en bestilling etter at linjenumrene er fullt distribuert.

## <a name="cause"></a>Årsak

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

## <a name="resolution"></a>Løsning

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
