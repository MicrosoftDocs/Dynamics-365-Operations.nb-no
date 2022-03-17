---
title: Automatisk bruk av forskuddsbetalinger på leverandørfakturaer
description: Dette emnet beskriver muligheten for automatisk bruk av forskuddsbetalinger på leverandørfakturaer.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8583962c41a7ac5e27463f325ddc2ccd367331cc
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358225"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatisk bruk på leverandørfakturaer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver muligheten for automatisk bruk av forskuddsbetalinger på leverandørfakturaer. Det kan opprettes en forskuddsbetaling for en bestilling som del av en innkjøpsavtale. Når en leverandørfaktura er mottatt, kan forskuddsbetalingen brukes til å utligne leverandørgjeld fra leverandørfakturaen. Ved hjelp av den nye funksjonen kan systemet automatisk bruke bestillingsnumre på en leverandørfaktura til å slå opp tilsvarende forskuddsbetalinger når leverandørfakturaen importeres.

Hvis det blir funnet forskuddsbetalinger som kan brukes, legges linjer til de eksisterende fakturalinjene for å bruke forskuddsbetalingene. Det blir aldri tatt hensyn til forskuddsbetalingslinjene under fakturasamsvarsprosessen.

Følgende punkt beskriver hvordan forskuddsbetalinger brukes når ulike innkjøpsprosesser følges:

- **Én leverandørfaktura per bestilling** – Forskuddsbetalingen på bestillingen blir brukt på leverandørfakturaen.
- **Én leverandørfaktura for flere bestillinger** – Forskuddsbetalingene på alle bestillingene blir brukt på leverandørfakturaen.
- **Flere leverandørfaktura per bestilling** – Forskuddsbetalingen på bestillingen blir brukt på den første importerte leverandørfakturaen. Hvis forskuddsbetalingsbeløpet overskrider fakturabeløpet, mislykkes forskuddsbetalingsprogrammet, og du må bruke forskuddsbetalingen manuelt.
- **Flere leverandørfaktura for flere bestillinger** – Forskuddsbetalingene på bestillingene blir brukt på den første relevante leverandørfakturaen. Hvis forskuddsbetalingsbeløpet overskrider fakturabeløpet, mislykkes forskuddsbetalingsprogrammet, og du må bruke forskuddsbetalingene manuelt. Hvis det gjenstår forskuddsbetalinger etter forskuddsbetalinger brukes på den første fakturaen, kan de brukes på fakturaene som følger.

Hvis et forsøk på å bruke en forskuddsbetaling mislykkes, er det innstillingen for alternativet **Blokker oppfølgingsautomatiseringsprosess ved feil med forskuddsbetalingsplassering** som avgjør de neste trinnene:

- **Ja** – Feilmeldingen "Automatisk program for forskuddsbetaling: Mislykket" legges til i historikken for automatisk betaling, og fakturaen forblir i listen over ventende leverandørfakturaer. Fakturaen vil forbli sperret til du bruker forskuddsbetalingen manuelt.

Hvis du vil bruke forskuddsbetalinger manuelt, kan du gå til den ventende leverandørfakturaen. På **Fakturadetaljer**-siden angir du alternativet **Inkluder i automatisert behandling** for den blokkerte fakturaen til **Nei**. Du kan nå bruke forskuddsbetalingen manuelt. Når forskuddsbetalingen er brukt, setter du alternativet **Ta med i automatisert behandling** tilbake til **Ja**, slik at fakturaen kan behandles automatisk.

Du kan også hoppe over automatisk bruk av forskuddsbetalingen ved å sette alternativet **Inkluder i automatisert behandling** til **Nei** og deretter sette det tilbake til **Ja**. Du får følgende melding: "Det finnes allerede en forskuddsbetaling for bestillingen. Vil du ignorere den for den valgte leverandørfakturaen? Velg **Ja**. Meldingen "Plassering av forskuddsbetaling ble omgått manuelt" legges til i historikken for automatisk betaling, og leverandørfakturaen blokkeres ikke når den automatiserte prosessen kjøres på nytt.

- **Nei** – Oppfølging av automatisk behandling vil fortsette. Du kan fremdeles bruke forskuddsbetalingen under utligning.
