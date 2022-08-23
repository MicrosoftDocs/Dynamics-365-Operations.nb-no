---
title: Lagermerking med planleggingsoptimalisering
description: Denne artikkelen inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 55c83cdbc144f194fe80e8281a35ec7ff43d551e
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219945"
---
# <a name="inventory-marking-with-planning-optimization"></a>Lagermerking med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.

*Merking* brukes til å koble til forsyning og behov. Det ligner på *utligning*, som indikerer hvordan hovedplanleggingen forventes å dekke behov. Fra et planleggingssynspunkt er hovedforskjellen at merking er mer permanent enn utligning.

Merking ble innført for å støtte spesielle etterkalkuleringsscenarioer for først inn, først ut (FIFO) og sist inn, først ut (LIFO). Den brukes imidlertid også for noen ikke-etterkalkuleringsscenarioer. Merking mellom forsyning og behov er valgfritt og nesten permanent. Merking kan fjernes manuelt av en bruker, eller den kan fjernes ved å kjøre en nedbryting av salgsordrelinjen der alternativet **Fjern merking** er valgt.

Utligning kontrolleres av hovedplanleggingen under dekning for å koble behov med den påkrevde forsyningen. Utligning kan oppdateres for hver planleggingskjøring for å optimalisere forsyningen som kreves for å dekke behovet. Når hovedplanleggingen oppdaterer utligningsinformasjon, respekterer den eksisterende merking.

Utligning starter ved å inkludere relevante merking, lagerreservasjoner og ordrereservasjoner i følgende rekkefølge:

1. Merking mellom behov og forsyning
1. Lagerreservasjoner
1. Ordrereservasjoner

Når du autoriserer en planlagt bestilling, inneholder dialogboksen **Autorisering** et **Oppdater merking**-felt som du kan bruke til å angi merkingsalternativer for ordrene som opprettes under autorisering. Velg én av følgende verdier:

- *Nei* – Det brukes ingen lagermerking.
- *Standard* – Lagermerking oppdateres i forhold til utligningen. En kravordre (behov) merkes mot en innfrielsesordre (forsyning). Hvis det gjenstår varer på innfrielsesordren, blir den ikke merket, og referanseinformasjonen er tom. Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bare bli tilordnet salgsordren.
- *Utvidet* – Både kravordren (behov) og innfrielsesordren (forsyning) merkes, uansett om det gjenstår kvanta på innfrielsesordren. Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bli tilordnet både salgsordren og bestillingen.
- *Standard på enkeltnivå* – Merking på enkeltnivå brukes. Merking på enkeltnivå merker bare hovedvaren, ikke stykklistekomponentene. Derfor kan du holde komponenttildeling for produksjonsordrer fleksible etter autorisering. Med merking på enkeltnivå kan systemet optimalisere for endringer i etterspørselen i siste øyeblikk. I *standard* merking på enkeltnivå merkes behovsordrer mot oppfyllelsesordrene, men oppfyllelsesordrer er ikke merket hvis de har restantall.
- *Utvidet på enkeltnivå* – Merking på enkeltnivå brukes. I *utvidet* merking på enkeltnivå merkes behovsordrer mot oppfyllelsesordrene, og oppfyllelsesordrer er alltid merket uansett restantall.

Hvis du vil angi standard merkingsalternativ for systemet, kan du gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**. I fanen **Standardoppdatering** angir du deretter feltet **Oppdateringsmerking** til det foretrukne alternativet.

> [!NOTE]
> Alternativene *Standard på enkeltnivå* og *Utvidet på enkeltnivå* er bare tilgjengelige hvis funksjonen *Automatisering av produksjon etter ordre* er aktivert på systemet. Hvis du vil ha mer informasjon om denne funksjonen og hvordan du aktiverer den, kan du se [Automatisering av produksjon etter ordre](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
