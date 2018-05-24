---
title: Forsinkelser
description: "Denne artikkelen inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a>Forsinkelser

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.

Hovedplanlegging kan beregne den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider, materialtilgjengelighet, tilgjengelig kapasitet og forskjellige planleggingsparametere. 

Hvis hovedplanleggingen beregner en ordredato som kommer før gjeldende dato, kan ikke ordren fullføres i tide. Derfor er ordren forsinket. I så fall fremoverplanlegger hovedplanleggingen ordren fra gjeldende dato og inkluderer leveringstider. Disse leveringstidene starter med komponentvarer på lavere nivå. Ordren får deretter en forsinkelsesdato. En forsinket dato er en realistisk forfallsdato basert på gjeldende data. Hovedplanlegging beregner også antall dager forsinket. 

I noen tilfeller kan det hende du velger ikke å beregne forsinkelser, for eksempel når brukerne vet at de kan fremskynde leveringstider ved å velge alternative leveringsmåter. 

Du kan konfigurere hvordan forsinkelser beregnes for en dekningsgruppe. Du kan deretter knytte dekningsgruppen til en vare senere. 

På siden **Hovedplanleggingsparametere** kan du angi starttidspunktet for beregning av forsinkelser. Hvis en ordre er utført etter dette tidspunktet, legges det til én dag i forsinkelsen av ordren. 

**Obs!**  I tidligere versjoner ble beregnede forsinkelser kalt *terminmeldinger*, forsinkelsesdatoen ble kalt *termindatoen*, og en forsinket transaksjon ble kalt *en transaksjon som var satt til fremtiden*.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Dekningsinnstillinger](coverage-settings.md)




