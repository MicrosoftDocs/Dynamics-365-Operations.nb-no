---
title: Opprette en arbeidsflyt for permisjonsforespørsel
description: Opprett en arbeidsflyt for permisjon og fravær for å behandle permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c985a0cb242fb6696b55a2514bd788ff4269f8ca
ms.sourcegitcommit: def66a9dc7feadd33411248af2545ee4a9e27c4f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2020
ms.locfileid: "3385554"
---
# <a name="create-a-leave-request-workflow"></a>Opprette en arbeidsflyt for permisjonsforespørsel

Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle permisjons- og fraværsforespørsler konsekvent. Med en arbeidsflyt for **permisjon og fravær** kan du:

- Definere oppgaver
- Bestemme hvem som må fullføre oppgavene
- Angi hvem som kan godkjenne eller avvise forespørsler

## <a name="create-a-leave-and-absence-request-workflow"></a>Opprette en arbeidsflyt for permisjons- og fraværsforespørsler

1. På siden **Permisjon og fravær** velger du **Koblinger**-fanen.

2. Under **Oppsett** velger du **Personalarbeidsflyter**.

3. Velg **Ny**, og velg deretter **Permisjons- og fraværsforespørsel**. 

4. Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.

5. Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene. Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

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

- Bruk **Årsakskode** i et betingelsesuttrykk for å rute permisjonsforespørsler for sykefravær med årsakskoden for **Operasjon** til personalavdelingen for godkjenning, mens alle andre årsakskoder rutes til prosjektlederen. Hvis du vil ha mer informasjon om betingelsessetninger, se [Konfigurere betingede beslutninger i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler automatisk som disse rollene sender inn på vegne av ansatte. Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.

## <a name="see-also"></a>Se også

- [Oversikt over permisjon og fravær](hr-leave-and-absence-overview.md)
