---
title: Feilsøke arbeidsflyter for innkjøp og leverandører
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med arbeidsflyter for innkjøp og leverandører.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d5d688c5769a62580e48908117d0562b26eab10a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222831"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Feilsøke arbeidsflyter for innkjøp og leverandører

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med arbeidsflyter for innkjøp og leverandører.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Feil under ny sending av en bestilling til arbeidsflyten etter en endring: "Endringer i bestilling X er bare tillatt i kladdetilstand når endringsadministrasjon er aktivert"

Dette problemet oppstår bare hvis bestillingen var i en *Bekreftet* tilstand før du forespurte endringer. Hvis du ber om endringer mens bestillingen er i en *Godkjent* tilstand, kan arbeidsflyten behandles på riktig måte.

### <a name="error-description"></a>Feilbeskrivelse

Følgende feil oppstår i arbeidsflyten når en bestilling sendes på nytt etter en endring:

> Stoppet (feil): X++ Unntak: Endringer i bestilling PO0000569 er bare tillatt i tilstanden Utkast når endringsadministrasjon er aktivert på<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Problemløsning

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Problemet vil bli løst via [denne artikkelen i Microsoft Knowledge Base (KB)](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert.

Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.

Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**. Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Hvis en leveringsrest blir annullert på en bestilling der endringsstyring er aktivert, går bestillingen til en bekreftet status.

### <a name="issue-description"></a>Problembeskrivelse

For en bestilling som er underlagt endringsstyring, hvis den eneste endringen som blir forespurt, er annullering av en leveringsrest på én eller flere av linjene, vil bestillingen gå direkte til en *Bekreftet* tilstand når den er godkjent, og det vil ikke bli opprettet noen journal.

### <a name="issue-resolution"></a>Problemløsning

Annullering av en leveringsrest påvirker ikke innholdet i bekreftelsesjournalen. Denne funksjonaliteten bør brukes når linjen er delvis mottatt, og den gjenværende kvaliteten skal avbrytes i prosesstrinnet etter at bestillingen er bekreftet hos leverandøren.

Hvis dette skal reflekteres på bestillingsbekreftelsen, skal antallet justeres på bestillingslinjen slik at bekreftelsen blir nødvendig. Hvis det ikke er mottatt noe på linjen, kan du eventuelt fjerne antallet. I dette tilfellet kreves det en bekreftelse på nytt.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Annullerte bestillinger vises i kladdelisten i arbeidsområdet for bestillingsforberedelse.

### <a name="issue-description"></a>Problembeskrivelse

Når du har annullert bestillinger som var i *Bekreftet* tilstand, vises de annullerte bestillingene likevel i listen over utkastbestillinger i arbeidsområdet for **Bestillingsklargjøring**.

### <a name="issue-resolution"></a>Problemløsning

Dette problemet oppstår bare for bestillinger som er underlagt endringsadministrasjon. Dette skjer fordi avlysningen regnes som en endring som må godkjennes. Godkjenningen kan gjøres automatisk av systemet. Prosessen er derfor å sende den annullerte bestillingen til godkjenningsarbeidsflyten slik at den kan gå til *Godkjent* tilstand. På dette punktet vises ikke bestillingen lenger i listen over bestillingsforslag i arbeidsområdet **Bestillingsklargjøring**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]