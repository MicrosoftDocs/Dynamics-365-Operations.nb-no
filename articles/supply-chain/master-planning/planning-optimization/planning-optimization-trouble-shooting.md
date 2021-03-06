---
title: Feilsøke planleggingsoptimalisering
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med planleggingsoptimalisering.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2100235fadabe6af87849aab7d9ec55d85ea66fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812889"
---
# <a name="troubleshoot-planning-optimization"></a>Feilsøke planleggingsoptimalisering 

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med planleggingsoptimalisering.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Installasjon av tillegget for planleggingsoptimaliseringen fullføres ikke

Planleggingsoptimalisering krever at et LCS-miljø (Lifecycle Services) er aktivert med høy tilgjengelighet, lag 2 eller høyere (ikke et OneBox-miljø), med Dynamics 365 Supply Chain Management versjon 10.0.7 eller nyere. Hvis du prøver å installere tillegget i et OneBox-miljø, vil ikke installasjonen fullføres.

**Løsning**: Avbryt installasjonen og bruk et miljø med høy tilgjengelighet, lag 2 eller høyere (ikke et Onebox-miljø).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Planlegging av satsvise jobber mislykkes når planleggingsoptimalisering aktiveres

Når du aktiverer planleggingsoptimalisering, deaktiveres den innebygde hovedplanleggingsmotoren automatisk. Satsvise jobber for hovedplanlegging som ble opprettet for den innebygde planleggingsmotoren i Supply Chain Management, vil mislykkes hvis de blir utløst mens planleggingsoptimalisering er aktivert. Du kan få en feilmelding, for eksempel *Denne operasjonen utløste hovedplanlegging som ikke støttes når planleggingsoptimalisering er aktivert*.

**Løsning**: Avbryt alle satsvise jobber for hovedplanlegging som ble opprettet for den innebygde planleggingsmotoren for Supply Chain Management.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Resultatene av planleggingsoptimalisering er forskjellige fra tidligere resultater

Planleggingsoptimalisering er forskjellig fra den innebygde hovedplanleggingsutformingen i noen områder. Dette kan også skyldes ventende funksjoner.

**Løsning**: Kjør analyse for tilpassing av planleggingsoptimalisering, og analyser deretter resultatene ved henvisning til den relaterte dokumentasjonen for å forstå virkningen. Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Kan ikke aktivere planleggingsoptimalisering

**Tilkoblingsstatusen** må være **Tilkoblet** før du kan sette **Bruk planleggingsoptimalisering** til **Ja**. Hvis du vil ha mer informasjon, se [Kom i gang med planleggingsoptimalisering](get-started.md).

**Løsning**: Kontroller at tillegget for planleggingsoptimalisering ble installert.

## <a name="error-message-is-shown-during-ctp"></a>Det vises en feilmelding under CTP

Hvis du prøver å kjøre leveringskapasitet (CTP) fra en salgsordre når planleggingsoptimalisering er aktivert, får du følgende feil melding: *Denne operasjonen utløste hovedplanlegging som ikke støttes når planleggingsoptimaliseringen er aktivert*.

Dette er knyttet til en ventende funksjon som er planlagt som en del av støtten for produksjonsordrer.

**Løsning:** Unngå CTP-beregninger når planleggingsoptimalisering er aktivert til CTP-støtte er tilgjengelig.

## <a name="additional-resources"></a>Tilleggsressurser

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Analyse for tilpassing av planleggingsoptimalisering](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]