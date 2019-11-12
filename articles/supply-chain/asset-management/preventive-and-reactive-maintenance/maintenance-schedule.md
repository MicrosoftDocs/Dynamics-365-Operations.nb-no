---
title: Vedlikeholdsplan
description: Dette emnet beskriver vedlikeholdsplan i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fab21d6f3a1b7386d304ece6ebf3b93cdc0c504d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570013"
---
# <a name="maintenance-schedule"></a>Vedlikeholdsplan

[!include [banner](../../includes/banner.md)]

 

Vedlikeholdsplanen inneholder en liste over alle forventede forebyggende vedlikeholdsplaner, vedlikeholdsforespørsler og vedlikeholdsrunder som skal utføres. Noen planleggingslinjer kan ha blitt konvertert til arbeidsordrer.

De fire visningene for vedlikeholdsplaner er litt forskjellige, avhengig av hvilke vedlikeholdsplanlinjer du vil se.

| Menyelement                  | Beskrivelse av innhold                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hele vedlikeholdsplan       | Alle vedlikeholdsplanlinjene vises.     |
| Min aktivumplan        | Alle vedlikeholdsplanlinjer som inneholder aktiva som finnes på arbeidssteder du er tilknyttet som arbeider (oppsett i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md)), vises i denne listen. |
| Åpne linjer for vedlikeholdsplan | Vedlikeholdsplanlinjer med statusen Opprettet – betyr at de ennå ikke er konvertert til en arbeidsordre eller forkastet – vises i denne listen.                                            |
| Åpne vedlikeholdsplansamlinger | Vedlikeholdsplanlinjer relatert til en arbeidsordrepulje vises i denne listen.                                                                                                                  |

>[!NOTE]
>Hvis en vedlikeholdsplanlinje er inkludert i flere arbeidsordrepuljer (se [Arbeidsordrepuljer](../work-orders/work-order-pools.md)), vises én post for hver pulje i **Åpne vedlikeholdsplanpuljer**. Dette gjøres for å optimalisere filtreringsalternativene i arbeidsordrepuljer.

Slik åpner du en vedlikeholdsplan:

1. Klikk på **Aktivastyring** > **Felles** > **Vedlikeholdsplan** > **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer**.

2. Hvis du vil oppdatere vedlikeholdsplanen, klikker du på **Vedlikeholdsplan** eller **Vedlikeholdsrunder**. 

3. Du kan redigere en vedlikeholdsplanlinje ved å merke den og klikke på **Rediger**. Du kan for eksempel enkelt oppdatere servicenivået eller arbeideren som er ansvarlig for jobben. Du kan bare redigere vedlikeholdsplanlinjer som ennå ikke er koblet til en arbeidsordre.

4. Du kan slette en vedlikeholdsplanlinje ved å velge den på listesiden og klikke på **Slett**.

5. Du kan forkaste en vedlikeholdsplanlinje ved å velge den på listesiden og klikke på **Forkast**. Denne funksjonen er nyttig hvis for eksempel et aktivum har en vedlikeholdsplan for 2 000 km og en vedlikeholdsplan for 10 000 km. Da vil du kanskje forkaste linjen som er opprettet fra 2 000 km-vedlikeholdsplanen når den sammenfaller med 10 000 km, 20 000 km, 30 000 km og så videre. Hvis du forkaster en vedlikeholdsplanlinje knyttet til en vedlikeholdsplan, vil denne linjen aldri vises igjen når denne vedlikeholdsplanen planlegges.

6. Du kan velge en rekke vedlikeholdsplanlinjer i **Alle vedlikeholdsplaner** og klikke på **Arbeidsordrepulje** hvis du vil at alle valgte linjer skal tas med i samme arbeidsordrepulje.

7. Du kan velge en rekke vedlikeholdsplanlinjer i **Alle vedlikeholdsplaner** eller **Åpne vedlikeholdsplanlinjer** eller **Åpne vedlikeholdsplanpuljer** og klikke på **Juster plan** hvis du vil foreta de samme justeringene på flere linjer. Du kan endre forventet start- og sluttdato, servicenivå og ansvarlig vedlikeholdspersongruppe eller ansvarlig vedlikeholdsperson knyttet til de valgte vedlikeholdsplanlinjene.

- Når en vedlikeholdsplanlinje er knyttet til en arbeidsordre, vises ID-en for arbeidsordren i **Arbeidsordre**-feltet.  
- I **Alle aktiva**-detaljvisningen > **Vedlikeholdsplaner for aktivum**-hurtigfanen kan du velge vedlikeholdsplaner for aktivaet. Hvis du senere sletter en vedlikeholdsplanlinje knyttet til et aktivum i **Alle aktiva**, sletter du også automatisk alle vedlikeholdsplanlinjer med statusen "Opprettet" som er opprettet basert på denne vedlikeholdsplanen. Se også [Opprette et aktivum](../objects/create-an-object.md).

Illustrasjonen nedenfor viser listesiden **Alle vedlikeholdsplaner**.

![Figur 1](media/16-preventive-maintenance.png)

