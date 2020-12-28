---
title: Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon
description: Opprett en arbeidsflyt for forespørsel om kjøp og salg av permisjon for å kjøpe og selge permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419949"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon

Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle kjøps- og salgsforespørsler konsekvent. Med en arbeidsflyt for **Kjøp og selg permisjon** kan du:

- Definere oppgaver
- Bestemme hvem som må fullføre oppgavene
- Angi hvem som kan godkjenne eller avvise forespørsler

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Personalarbeidsflyter**.

3. Velg **Ny**, og velg deretter **Forespørsel om kjøp og salg av permisjon**. 

4. Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.

5. Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene. Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler

Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for forespørsler om kjøp og salg av permisjon:

- **Beløp**
- **Kjøps- og salgspolicy for permisjon**
- **Bedrift**
- **Opprettet av**
- **Opprettingsdato og -klokkeslett**
- **Sluttdato**
- **Permisjonstype**
- **Endret av**
- **Endringsdato og -klokkeslett**
- **Forespørsels-ID**
- **Startdato**
- **Status** 
- **Innsendingsdato**
- **Sendt av**
- **Sendt av personalavdeling**
- **Sendt av leder**
- **Sendt på vegne**
- **Worker**

## <a name="workflow-examples"></a>Arbeidsflyteksempler

Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:

- Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler for kjøp og salg automatisk som disse rollene sender inn på vegne av ansatte. Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.

## <a name="see-also"></a>Se også

[Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)<br>
[Administrere policyer for kjøp og salg av permisjon](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

