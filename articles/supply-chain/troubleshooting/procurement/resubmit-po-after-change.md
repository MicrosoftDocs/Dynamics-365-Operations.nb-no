---
title: Feil under sending av en bestilling på nytt til en arbeidsflyt etter en endring
description: Feil under sending av en bestilling på nytt til en arbeidsflyt etter en endring
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477247"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Feil under sending av en bestilling på nytt til en arbeidsflyt etter en endring


## <a name="symptoms"></a>Symptomer

Følgende feil oppstår i arbeidsflyten når en bestilling sendes på nytt etter en endring:

> Stoppet (feil): X++ Unntak: Endringer i bestilling PO0000569 er bare tillatt i tilstanden Utkast når endringsadministrasjon er aktivert på<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

Dette problemet oppstår bare hvis bestillingen var i en *Bekreftet* tilstand før du forespurte endringer. Hvis du ber om endringer mens bestillingen er i en *Godkjent* tilstand, kan arbeidsflyten behandles på riktig måte.

## <a name="resolution"></a>Løsning

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problemet vil bli løst via [denne artikkelen i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
