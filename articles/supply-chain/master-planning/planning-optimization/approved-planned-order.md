---
title: Godkjenn planlagte ordrer
description: Dette emnet beskriver godkjenning av planlagte ordrer som støttes i planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434381"
---
# <a name="approve-planned-orders"></a>Godkjenn planlagte ordrer

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder informasjon om hvordan du oppdaterer statusen for planlagte ordrer i planleggingsoptimalisering.

Merk deg at godkjenning av planlagte ordrer er et valgfritt trinn for å opprette en autorisert ordre fra en planlagt ordre. Det anbefales at du godkjenner endrede planlagte ordrer, ellers blir redigeringene ignorert og overskrevet av neste planleggingskjøring.

![Planlagt ordreflyt](media/approved-planned-orders-1.png)

**Status**-feltet hjelper med å spore fremdriften ved hjelp av følgende verdier:

- **Ubehandlet:** Når hovedplanlegging genererer planlagte ordrer, har de planlagte ordrene statusen *Ubehandlet*. Planlagte ordrer med denne statusen blir slettet under neste planleggingskjøring.
- **Fullført:** Hvis du bestemmer deg for ikke å autorisere en planlagt ordre, kan du endre statusen til *Fullført* for å angi at du har fullført evalueringen av denne planlagte ordren. Legg merke til at statusen for *Ubehandlet* og *Fullført* behandles på samme måte av systemet.
- **Godkjent:** Hvis du vil beholde endringer eller planlegge å bekrefte en planlagt ordre, endrer du statusen til *Godkjent*. Planlagte ordrer med *Godkjent*-status anses som faste, og det forventes forsyning via hovedplanlegging. Demed blir de ikke endret eller slettet under senere panleggingskjøringer. For å oppnå dette kopierer planleggingslogikken de *godkjente* planlagte bestillingene fra den gamle planversjonen til den nye planversjonen under hovedplanlegging. Legg merke til at planlaget ordrer med statusen *Godkjente* bare regnes som forsyning i den bestemte hovedplanen.

Du kan administrere planlagte ordrer fra arbeidsområdet **Hovedplanlegging**, listen **Planlagt ordre** eller listene **Planlagte produksjonsordrer**, **Planlagte bestillinger** og **Planlagt overføring**.
