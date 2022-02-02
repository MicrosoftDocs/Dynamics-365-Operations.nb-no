---
title: Oversikt over hovedplaner
description: Du kan bruke forskjellige hovedplaner for å ha støtte for firmaets daglige arbeidsoperasjoner, simulere forskjellige strategier du vil overvåke og implementere en firmapolicy, for eksempel angående intern ytelse eller kundetilfredsstillelse.
author: ChristianRytt
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03467778025287f3692e171bea37b1bfb2ca1646
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982360"
---
# <a name="master-plans-overview"></a>Oversikt over hovedplaner

[!include [banner](../includes/banner.md)]

Du kan bruke forskjellige hovedplaner for å ha støtte for firmaets daglige arbeidsoperasjoner, simulere forskjellige strategier du vil overvåke og implementere en firmapolicy, for eksempel angående intern ytelse eller kundetilfredsstillelse.

Du kan konfigurere hovedplaner på siden **Hovedplaner**.

Det finnes to typer planer:

- **Statisk plan** – Beregningen for hovedplanlegging bruker gjeldende data til å generere en nettobehovsplan. Denne planen forblir uendret til neste gang du utfører hovedplanlegging eller endrer planen manuelt. Dette er en driftsplan som forskjellige firmaansatte, for eksempel innkjøper eller produksjonsplanleggere, kan bruke til å basere avgjørelsene sine på og utføre de daglige aktivitetene.
- **Dynamisk plan** – Denne planen starter med de samme nettobehovene som ble generert ved hjelp av hovedplanlegging. Du kan imidlertid oppdatere den dynamiske planen hver gang hoveddataene endres. Dette kan for eksempel være når du oppretter en ny salgsordre. Dette gjør at du kan overvåke det endrede ordrenettverket og varetilgjengeligheten uten å forstyrre den statiske planen som andre bruker til arbeidsrutinene.

Et firma kan velge å arbeide med bare en dynamisk plan, eller den kan bruke både statiske og dynamiske planer. I tillegg kan du konfigurere en hvilken som helst hovedplan for å gjenspeile en bestemt strategi eller håndtere et problem. Eksempler er som følger:

- Angi høyere lagernivåer for å sikre mot manko.
- Angi lengre sikkerhetsmarginer for å beskytte mot upålitelige leverandører.

Du kan også konfigurere den første dynamiske planen til å oppdateres med den nye behovsplanen hver gang du utfører hovedplanlegging. Du kan angi disse innstillingene på siden **Hovedplanleggingsparametere**.

## <a name="additional-resources"></a>Tilleggsressurser

- [Dekningsinnstillinger](coverage-settings.md)
- [Skille taktisk og operativ planlegging for hovedplanlegging](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Hovedplanlegging: Bruke en statisk og dynamisk hovedplan eller bruke én plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
