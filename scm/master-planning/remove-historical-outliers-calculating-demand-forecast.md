---
title: "Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose"
description: "Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose. Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 72735c9e3fb4291076f0b577f45384dec319b2a7
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Fjerne utestående fra historiske transaksjonsdata ved beregning av en behovsprognose

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du utelater utestående fra de historiske dataene som brukes til å beregne en behovsprognose. Ved å ekskludere utestående kan du forbedre nøyaktighet av prognosen.

Du kan utelate utestående for å forbedre nøyaktighet av prognosen. Denne oppgaven er valgfri. Her er en oversikt over prosessen:

1.  Klikk **Hovedplanlegging** &gt; **Oppsett** &gt; **Behovsprognose** &gt; **Fjerning av utestående** for å åpne **Fjerning av utestående**-siden der du kan bruke en spørring for å velge transaksjonen som skal ekskluderes.
2.  Velg firmaet som spørringen gjelder for, og skriv inn et navn og en beskrivelse. **Spørringsdato**-feltet settes automatisk til den gjeldende datoen.
3.  Merk av for **Aktiv** for å utelate transaksjoner som blir funnet av spørringen, fra historiske data. Denne innstillingen trer i kraft når du oppretter en basislinjeprognose.
4.  På **Spørring etter fjerning av utestående**-siden kan du legge til, fjerne og velge kriteriene som definerer hvilke transaksjoner som skal utelates når basislinjeprognosen beregnes. Velg for eksempel en bestemt vare eller ordretransaksjon som skal ekskluderes.
5.  Klikk **Vis transaksjoner**. **Utestående transaksjoner**-siden viser transaksjonene som oppfyller kriteriene som du definerte i spørringen, og som utelates fra historiske data når behovsprognosen beregnes.

**Merk:** Du kan også opprette en spørring som er basert på en eksisterende spørring. Velg spørringen du vil kopiere, og klikk deretter **Duplikat**. **Spørringsdato**-feltet identifiserer versjonen. Du kan bruke spørringen som den er, eller du kan klikke **Rediger spørring** for å endre vilkårene. Du kan også endre navnet og beskrivelsen av den nye spørringen.

<a name="see-also"></a>Se også
--------

[Innføring i behovsprognoser](introduction-demand-forecasting.md)

[Overvåke prognosenøyaktighet](monitor-forecast-accuracy.md)




