---
title: Du får en feilmelding når du kjører den innebygde hovedplanleggingsmotoren
description: Nrå du kjører den avskrevne innebygde hovedplanleggingsmotoren, mottar du en feilmelding.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7c0c674818a21d3ad422661fc427b0b9c4aad52b8d44d08791d2d703be528fe3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751727"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Du får en feilmelding når du kjører den innebygde hovedplanleggingsmotoren

Feilkode: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Symptomer

Nrå du kjører hovedplanlegging ved å bruke den avskrevne innebygde hovedplanleggingsmotoren, mottar du følgende feilmelding:

> Du får denne feilmeldingen fordi den innebygde hovedplanleggingsmotoren ble brukt til scenarioer som støttes av planleggingsoptimalisering. Du bør overføre til planleggingsoptimalisering nå, fordi den gjeldende innebygde hovedplanleggingen vil bli avskrevet. Legg merke til at denne hovedplanleggingskjøringen ble fullført. I tilfelle overføringen har sterke avhengigheter for ventende funksjoner, kan du be om et unntak for fortsatt bruk av den innebygde hovedplanleggingsmotoren. Fyll ut følgende spørreskjema for å komme i gang, og hvis det er relevant, forespør et unntak fra overføring til planleggingsoptimalisering. [Spørreskjemaet om migrering og unntak i Planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Årsak

Hvis du kjører planlegging og ikke bruker funksjoner for produksjonskontroll, bør du vurdere å migrere til Planleggingsoptimalisering. Den innebygde hovedplanleggingsmotoren blir avskrevet. Hvis du vil fortsette å bruke det uten å motta feilmeldingen, må du derfor søke om et unntak fra Microsoft.

## <a name="resolution"></a>Løsning

Hvis du vil ha mer informasjon om hvordan du migrerer til Planleggingsoptimalisering, eller hvordan du søker etter et unntak, slik at du kan fortsette å bruke den avkrevne, innebygde planleggingsmotoren i stedet, kan du se [Overføring til planleggingsoptimalisering for hovedplanlegging](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
