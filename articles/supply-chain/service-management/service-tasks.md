---
title: Serviceoppgaver
description: Bruk serviceoppgaver til å beskrive oppgaven som skal fullføres under en serviceordre. Både teknikere og kunder kan se denne informasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549846"
---
# <a name="service-tasks"></a>Serviceoppgaver  

[!include [banner](../includes/banner.md)]

Bruk serviceoppgaver til å beskrive oppgaven som skal fullføres under en serviceordre.
Både teknikere og kunder kan se denne informasjonen.

Du oppretter serviceoppgaver på **Serviceoppgaver**-siden, og du knytter serviceoppgaver til en bestemt serviceavtale eller serviceordre ved å opprette serviceoppgaverelasjoner. Hver gang du oppretter en serviceoppgaverelasjon, kan du opprette følgende:

-  Interne merknader for oppgaven, for eksempel detaljerte tekniske forespørsler for oppgaven som teknikeren bør kjenne til.

-  Eksterne merknader som kunden kan se. Disse kan gi en mindre teknisk forklaring av oppgaven som utføres, i henhold til avtalen mellom kunden og servicefirmaet.

Når du har definert en serviceoppgaverelasjon mellom en serviceoppgave og en serviceordre eller serviceavtale, kan du angi denne serviceoppgaven når du oppretter serviceordrelinjer eller serviceavtalelinjer for den gjeldende serviceordren eller serviceavtalen.

Når du genererer serviceordrer fra en serviceavtale, kan du bruke serviceoppgavene som er tilordnet hver serviceavtalelinje, til å gruppere serviceordrelinjer i serviceordrer.

## <a name="create-a-service-task"></a>Opprette en serviceoppgave

1. Klikk **Servicestyring** \> **Oppsett** \> **Serviceoppgaver**.
2. Opprett en ny linje.
3. Angi service-ID og -beskrivelse.

## <a name="example"></a>Eksempel

En tekniker må fullføre to jobber på en girkasse (serviceobjekt GB-1234) hos en kunde. Det opprettes en serviceavtale for kunden, og flere transaksjoner knyttes til jobbene. Serviceavtalen og serviceavtalelinjene for de to jobbene er som følger:

### <a name="service-agreement"></a>Serviceavtale

| Project | Serviceavtale | beskrivelse                                  | Gruppere   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Inspeksjon og rutineerstatning – GB-1234 | Bonus |

### <a name="service-agreement-lines"></a>Serviceavtalelinjer

| beskrivelse             | transaksjonstype | Serviceobjekt | Serviceoppgave |
|-------------------------|------------------|----------------|--------------|
| Inspeksjon og rengjøring | Time             | GB-1234        | I/C - GB1234 |
| Reise                  | Expense          | GB-1234        | I/C - GB1234 |
| Materialer               | Element             | GB-1234        | I/C - GB1234 |
| Rutineerstatning     | Time             | GB-1234        | RR - GB1234  |
| GR-1                    | Element             | GB-1234        | RR - GB1234  |
| GR-5                    | Element             | GB-1234        | RR - GB1234  |

Serviceavtalelinjene for de to jobbene har to serviceoppgaver tilknyttet. Serviceoppgavene bestemmer hvilke transaksjoner som tilhører hver jobb. I det første tilfellet identifiserer serviceoppgaven I/C - GB1234 alle serviceavtalelinjene i forbindelse med inspeksjonen og rengjøringen av objekt GB-1234. I det andre tilfellet, identifiserer serviceoppgave RR - GB1234 alle serviceavtalelinjene i forbindelse med å fullføre en rutineerstatningsjobb.

Serviceoppgaverelasjonene som kobler serviceoppgavene til den bestemte avtalen, er som følger:

### <a name="service-tasks"></a>Serviceoppgaver

| Serviceoppgave | Beskrivelse                             | Intern merknad                                                                                                                 | Ekstern merknad                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Inspeksjon av girkasse GB-1234           | Visuell og mekanisk inspeksjon og rengjøring av girkasse GB-1234.                                                              | Rutineinspeksjon av girkasse |
| RR - GB1234  | Rutineerstatning av deler i GB-1234 | Rutineserviceerstatning av GR-1- og GR-5-komponenter (for girkasser som er produsert før 2002, erstatt også GR-2-komponenten) | Rutineerstatning av deler  |

## <a name="group-service-orders"></a>Gruppeserviceordrer

Når du oppretter serviceordrer automatisk, kan du bruke serviceoppgaver som et grupperingskriterium. Hvis du vil gruppere serviceordrer etter serviceoppgaver, kan du på serviceavtalen definere at serviceordrer som er basert på serviceavtalen, skal grupperes etter serviceoppgave-ID-en som de første grupperingskriteriene.

**Gruppere etter serviceoppgave**

1. Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.
2. I kategorien **Oppsett** velger du **Etter serviceoppgave** i **Kombiner serviceordrer**-feltet.


