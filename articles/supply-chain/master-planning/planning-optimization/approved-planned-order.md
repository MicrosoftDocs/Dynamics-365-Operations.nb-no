---
title: Vise, behandle og godkjenne planlagte bestillinger
description: Dette emnet inneholder informasjon om hvordan du viser, behandler og godkjenner planlagte ordrer i planleggingsoptimalisering.
author: ChristianRytt
ms.date: 04/07/2021
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
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935663"
---
# <a name="view-manage-and-approve-planned-orders"></a>Vise, behandle og godkjenne planlagte bestillinger

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder informasjon om hvordan du viser, behandler og godkjenner planlagte ordrer i planleggingsoptimalisering.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Vise og behandle planlagte bestillinger

Du kan vise og administrere planlagte bestillinger på en hvilken som helst listeside med planlagte bestillinger. Gå til et av følgende steder, avhengig av hvilken type planlagte bestillinger du vil arbeide med:

- Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging
- Hovedplanlegging \> Hovedplanlegging \> Planlagte bestillinger
- Produksjonskontroll \> Produksjonsordrer \> Planlagte produksjonsordrer
- Innkjøp og leverandører \> Bestillinger \> Planlagte bestillinger
- Lagerstyring \> Innkommende ordrer \> Planlagte overføringer
- Lagerstyring \> Utgående ordrer \> Planlagte overføringer

## <a name="view-and-edit-the-status-of-planned-orders"></a>Vis og rediger statusen for planlagte ordrer

Du kan bruke **Status**-feltet for hver planlagte bestilling til å spore fremdriften eller endre hvordan en planlagt bestilling skal behandles. Følgende verdier for **Status** er tilgjengelige:

- **Ubehandlet** – Når hovedplanlegging genererer planlagte ordrer, gis de denne statusen. Planlagte ordrer med denne statusen blir slettet under neste planleggingskjøring.
- **Fullført** – Denne statusen angir at den planlagte bestillingen er fullført. Hvis du velger ikke å bekrefte en planlagt bestilling, kan du endre statusen manuelt til *Fullført*. Legg merke til at systemet behandler statusene *Ubehandlet* og *Fullført* på samme måte.
- **Godkjent** – Denne statusen angir at den planlagte bestillingen er godkjent for autorisering. Hvis du vil autorisere en planlagt ordre, kan du endre statusen til *Godkjent*. Hvis du vil beholde endringene som er gjort i en planlagt bestilling, eller hvis du planlegger å autorisere en planlagt bestilling, endrer du statusen til *Godkjent*. Planlagte bestillinger med status *Godkjent* betraktes som fast og forventet forsyning i hovedplanleggingen. Derfor blir de ikke endret eller slettet i løpet av senere hovedplanleggingskjøringer. For å oppnå denne atferden kopierer planleggingslogikken planlagte ordrer med statusen *Godkjent* fra den gamle planversjonen til den nye planversjonen under hovedplanlegging. Legg merke til at planlaget ordrer med statusen *Godkjent* bare regnes som forsyning i den bestemte hovedplanen.

Hvis du vil endre statusen for én enkelt planlagt bestilling, [åpner du en listeside for planlagte bestillinger](#view-planned-orders), åpner ordren og følger deretter ett av disse trinnene:

- I hurtigkategorien **Generelt** endrer du verdien for **Status**-feltet.
- I handlingsruten i fanen **Planlagt ordre** **Behandle**-gruppen velger du **Endre status**.
- Hvis du vil merke orden som godkjent, velger du **Godkjenn** i handlingsruten.

Hvis du vil endre statusen for flere planlagte bestillinger samtidig, [åpner du en listeside for planlagte ordrer](#view-planned-orders), merker av for hver ordre du vil endre, og deretter følger ett av disse trinnene:

- I handlingsruten i fanen **Planlagt ordre** **Behandle**-gruppen velger du **Endre status**.
- Hvis du vil merke ordrene som godkjent, velger du **Godkjenn** i handlingsruten.

## <a name="approve-planned-orders"></a>Godkjenn planlagte ordrer

Godkjenning av planlagte ordrer er et valgfritt trinn i prosessen med å opprette en autorisert ordre fra en planlagt ordre.

Illustrasjonen nedenfor viser hvordan du kan bruke **Status**-verdien som er tilordnet hver planlagte ordre, til å implementere en godkjenningsarbeidsflyt. Når du skal implementere en godkjenningsprosess, justerer du **Status**-verdien manuelt for hver planlagte ordre som beskrevet i den forrige delen.

![Planlagt ordreflyt](media/approved-planned-orders-1.png)

> [!TIP]
> Det anbefales at du godkjenner alle endrede planlagte bestillinger. Ellers blir endringene ignorert og overskrevet av neste planleggingskjøring.

## <a name="additional-resources"></a>Tilleggsressurser

- [Autoriser planlagte ordrer](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
