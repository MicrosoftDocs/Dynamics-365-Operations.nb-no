---
title: Hovedplanlegging er å planlegge mer enn den tilgjengelige kapasiteten
description: Hovedplanleggingen ser ikke ut til å respektere kapasitetsbegrensninger og planlegger mer enn tilgjengelig kapasitet
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477214"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Hovedplanlegging er å planlegge mer enn den tilgjengelige kapasiteten

## <a name="symptoms"></a>Symptomer

Hovedplanleggingen ser ikke ut til å respektere kapasitetsbegrensninger og planlegger mer enn tilgjengelig kapasitet.

Når du bruker grovplanlegging der det er begrenset kapasitet, og der ruten angir en blanding av krav for både en ressursgruppe og individuelle ressurser, er det en liten sjanse for overbestilling på grunn av måten algoritmen validerer på kapasitetskonflikter på. Denne overbestillingen kan forekomme når du bruker hjelpeprogrammer til å kjøre hovedplanlegging. Det er mest sannsynlig at det oppstår hvis det finnes mange jobber som har en relativt kort kjøretid.

## <a name="resolution"></a>Løsning

Hvis det er viktig at ingen overbestilling forekommer for grovplanlegging, kan du gjøre planleggingsdelen av enkelttrådbasert hovedplanlegging ved å aktivere alternativet **Nøyaktig, begrenset kapasitet for grovplanlegging** på siden **Parametere for hovedplanlegging**. Dette alternativet er ikke tilgjengelig som standard. Du må legge den til siden manuelt ved hjelp av tilpasningsfunksjonene. Når du bruker dette alternativet, vil planleggingen kjøre saktere på grunn av mangelen på parallell behandling.
