---
title: Oversikt over hovedplaner
description: Du kan bruke forskjellige hovedplaner for å ha støtte for firmaets daglige arbeidsoperasjoner, simulere forskjellige strategier du vil overvåke og implementere en firmapolicy, for eksempel angående intern ytelse eller kundetilfredsstillelse.
author: roxanadiaconu
manager: tfehr
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70a5b8f0c7e4857aa2904003b458bf6d02b72064
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982239"
---
# <a name="master-plans-overview"></a>Oversikt over hovedplaner

[!include [banner](../includes/banner.md)]

Du kan bruke forskjellige hovedplaner for å ha støtte for firmaets daglige arbeidsoperasjoner, simulere forskjellige strategier du vil overvåke og implementere en firmapolicy, for eksempel angående intern ytelse eller kundetilfredsstillelse. 

Du kan konfigurere hovedplaner på siden **Hovedplaner** .

Det finnes to typer planer:
-   **Statisk plan** – Beregningen for hovedplanlegging bruker gjeldende data til å generere en nettobehovsplan. Denne planen forblir uendret til neste gang du utfører hovedplanlegging eller endrer planen manuelt. Dette er en driftsplan som forskjellige firmaansatte, for eksempel innkjøper eller produksjonsplanleggere, kan bruke til å basere avgjørelsene sine på og utføre de daglige aktivitetene.
-   **Dynamisk plan** – Denne planen starter med de samme nettobehovene som ble generert ved hjelp av hovedplanlegging. Du kan imidlertid oppdatere den dynamiske planen hver gang hoveddataene endres. Dette kan for eksempel være når du oppretter en ny salgsordre. Dette gjør at du kan overvåke det endrede ordrenettverket og varetilgjengeligheten uten å forstyrre den statiske planen som andre bruker til arbeidsrutinene.

Et firma kan velge å arbeide med bare en dynamisk plan, eller den kan bruke både statiske og dynamiske planer. I tillegg kan du konfigurere en hvilken som helst hovedplan for å gjenspeile en bestemt strategi eller håndtere et problem. Eksempler er som følger:
-   Angi høyere lagernivåer for å sikre mot manko.
-   Angi lengre sikkerhetsmarginer for å beskytte mot upålitelige leverandører.

Du kan også konfigurere den første dynamiske planen til å oppdateres med den nye behovsplanen hver gang du utfører hovedplanlegging. Du kan angi disse innstillingene på siden **Hovedplanleggingsparametere** .



<a name="additional-resources"></a>Tilleggsressurser
--------

[Dekningsinnstillinger](coverage-settings.md)

[Skille taktisk og operativ planlegging for hovedplanlegging](https://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[Hovedplanlegging: Bruke en statisk og dynamisk hovedplan eller bruke én plan?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)



