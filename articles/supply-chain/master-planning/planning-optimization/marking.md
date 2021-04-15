---
title: Lagermerking med planleggingsoptimalisering
description: Dette emnet inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809500"
---
# <a name="inventory-marking-with-planning-optimization"></a>Lagermerking med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder informasjon om alternativene som er tilgjengelige for merking av lager i autoriserte ordrer når du bruker planleggingsoptimalisering.

*Merking* brukes til å koble til forsyning og behov. Det ligner på *utligning*, som indikerer hvordan hovedplanleggingen forventes å dekke behov. Fra et planleggingssynspunkt er hovedforskjellen at merking er mer permanent enn utligning.

Merking ble innført for å støtte spesielle etterkalkuleringsscenarioer for først inn, først ut (FIFO) og sist inn, først ut (LIFO). Den brukes imidlertid også for noen ikke-etterkalkuleringsscenarioer. Merking mellom forsyning og behov er valgfritt og nesten permanent. Merking kan fjernes manuelt av en bruker, eller den kan fjernes ved å kjøre en nedbryting av salgsordrelinjen der alternativet **Fjern merking** er valgt.

Utligning kontrolleres av hovedplanleggingen under dekning for å koble behov med den påkrevde forsyningen. Utligning kan oppdateres for hver planleggingskjøring for å optimalisere forsyningen som kreves for å dekke behovet. Når hovedplanleggingen oppdaterer utligningsinformasjon, respekterer den eksisterende merking.

Utligning starter ved å inkludere relevante merking, lagerreservasjoner og ordrereservasjoner i følgende rekkefølge:

1. Merking mellom behov og forsyning
1. Lagerreservasjoner
1. Ordrereservasjoner

Når du autoriserer en planlagt bestilling, inneholder dialogboksen **Autorisering** et **Oppdater merking**-felt som du kan bruke til å angi merkingsalternativer for ordrene som opprettes under autorisering. Velg én av følgende verdier:

- **Nei** – Det brukes ingen lagermerking.
- **Standard** – Lagermerking oppdateres i forhold til utligningen. En kravordre (behov) merkes mot en innfrielsesordre (forsyning). Hvis det gjenstår varer på innfrielsesordren, blir den ikke merket, og referanseinformasjonen er tom. Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bare bli tilordnet salgsordren.
- **Utvidet** – Både kravordren (behov) og innfrielsesordren (forsyning) merkes, uansett om det gjenstår kvanta på innfrielsesordren. Hvis for eksempel en salgsordre for 100 ea utlignes mot en bestilling for 150 ea, vil referanseinformasjon bli tilordnet både salgsordren og bestillingen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]