---
title: "Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose"
description: "Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose. Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose

Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose. Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen.

Du kan utelate outliers for å forbedre nøyaktigheten av prognosen. Denne oppgaven er valgfri. Her er en oversikt over prosessen:

1.  Klikk **Master planning**&gt;**oppsett**&gt;**etterspørselen prognoser**&gt;**fjerning av Outlier** å åpne den **fjerning av Outlier** -siden der du kan bruke en spørring til å velge transaksjonene som skal ekskluderes.
2.  Velg firmaet som spørringen gjelder for, og skriv inn et navn og en beskrivelse. **Spørringsdato**-feltet settes automatisk til den gjeldende datoen.
3.  Merk av for **Aktiv** for å utelate transaksjoner som blir funnet av spørringen, fra historiske data. Denne innstillingen trer i kraft når du oppretter en basislinjeprognose.
4.  På **Spørring etter fjerning av utestående**-siden kan du legge til, fjerne og velge kriteriene som definerer hvilke transaksjoner som skal utelates når basislinjeprognosen beregnes. Velg for eksempel en bestemt vare eller ordretransaksjon som skal ekskluderes.
5.  Klikk **Vis transaksjoner**. **Utestående transaksjoner**-siden viser transaksjonene som oppfyller kriteriene som du definerte i spørringen, og som utelates fra historiske data når behovsprognosen beregnes.

**Merk:** Du kan også opprette en spørring som er basert på en eksisterende spørring. Velg spørringen du vil kopiere, og klikk deretter **Duplikat**. **Spørringsdato**-feltet identifiserer versjonen. Du kan bruke spørringen som den er, eller du kan klikke **Rediger spørring** for å endre vilkårene. Du kan også endre navnet og beskrivelsen av den nye spørringen.

<a name="see-also"></a>Se også
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


