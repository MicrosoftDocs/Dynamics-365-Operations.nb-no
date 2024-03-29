---
title: Opprette en arbeidsflyt for permisjonsforespørsel
description: Opprett en arbeidsflyt for permisjon og fravær for å behandle permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855093"
---
# <a name="create-a-leave-request-workflow"></a>Opprette en arbeidsflyt for permisjonsforespørsel

> [!Important]
> Funksjonaliteten som er nevnt i denne artikkelen, er for øyeblikket tilgjengelig for kunder i frittstående Dynamics 365 Human Resources. Noe av eller all funksjonaliteten vil være tilgjengelig som en del av en fremtidig versjon av Finance-infrastrukturen etter Finance versjon 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle permisjons- og fraværsforespørsler konsekvent. Med en arbeidsflyt for **permisjon og fravær** kan du:

- Definere oppgaver
- Bestemme hvem som må fullføre oppgavene
- Angi hvem som kan godkjenne eller avvise forespørsler

## <a name="create-a-leave-and-absence-request-workflow"></a>Opprette en arbeidsflyt for permisjons- og fraværsforespørsler

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Personalarbeidsflyter**.

3. Velg **Ny**, og velg deretter **Permisjons- og fraværsforespørsel**. 

4. Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.

5. Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene. Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler

Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for permisjons- og fraværsforespørsler:

- **Beløp**
- **Kommentar**
- **Bedrift**
- **Opprettet av**
- **Opprettingsdato og -klokkeslett**
- **Sluttdato**
- **Permisjonstype**
- **Endret av**
- **Endringsdato og -klokkeslett**
- **Årsakskode**
- **Forespørsels-ID**
- **Startdato**
- **Status** 
- **Innsendingsdato**
- **Sendt av**
- **Sendt av personalavdeling**
- **Sendt av leder**
- **Sendt på vegne**
- **Worker**
- **Arbeidertype**

Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:

- Bruk **Årsakskode** i et betingelsesuttrykk for å rute permisjonsforespørsler for sykefravær med årsakskoden for **Operasjon** til personalavdelingen for godkjenning, mens alle andre årsakskoder rutes til prosjektlederen. Hvis du vil ha mer informasjon om betingelsessetninger, se [Konfigurere betingede beslutninger i en arbeidsflyt](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler automatisk som disse rollene sender inn på vegne av ansatte. Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
