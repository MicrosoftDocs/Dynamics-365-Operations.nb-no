---
title: Globale mobilenhetsparametere
description: Dette emnet beskriver hvordan du definerer mobilenhetsinnstillinger på siden Lagerstyringsparametere.
author: HuberIvan
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-huberivan
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 03c10232d55c99c73e625170797f89f6c77e812b
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505591"
---
# <a name="global-mobile-device-parameters"></a>Globale mobilenhetsparametere

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer globale lagerstyringsparametere som påvirker hvordan systemet fungerer sammen med mobilenheter.

Hvis du vil ha mer informasjon om hvordan du definerer lagerarbeidere, kan du se [Administrere lagerarbeider](manage-warehouse-workers.md). For mer informasjon om nummerskiltbehandling på mobile enheter, se [Nummerskiltmottak via mobilappen Warehouse Management](warehousing-mobile-device-app-license-plate-receiving.md). Hvis du vil ha mer informasjon om syklusopptellingsprosessene, kan du se [Syklusopptelling](cycle-counting.md) og [Eksempelscenarier for syklustelling](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Åpne siden Lagerstyringsparametere

For å åpne siden **Lagerstyringsparametere** går du til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**. Deretter kan du definere feltene som er knyttet til mobilenhetsarbeid, som beskrevet i neste del av dette emnet.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Hurtigkategori for mobilenhet i kategorien Generelt

Du finner de globale innstillingene for mobilenhet i hurtigkategorien **Mobilenhet** i kategorien **Generelt** på siden **Lagerstyringsparametere**. Følgende felt er tilgjengelige.

| Felt | beskrivelse |
|---|---|
| Merknadstype på mobilenheten | Velg informasjonstypen som vises til arbeidere under plukking av salgsordre. |
| Grense for skannet antall | Angi maksimalt vareantall som en arbeider kan skanne i løpet av hver økt ved hjelp av et menyelement for mobilenhet som har verdien **Justering inn** for *Arbeidsopprettelsesprosess*. Dette feltet påvirker ikke skanninger som utføres ved hjelp av andre typer menyelement. |
| Bruk øktlogging for mobilenheten | Sett dette alternativet til *Ja* for å beholde en logg over arbeiderpålogging. Hvis du vil vise loggen, kan du gå til **Arbeidsbrukerøkter \> Forespørsler og rapporter \> Logger for mobilenheter \> Arbeidsbrukerøkter**. |
| Antall lagrede feil | Angi det maksimale antallet feilposter som systemet skal lagre. Hvis du vil vise feilloggen, kan du gå til **Arbeidsbrukerøkter \> Forespørsler og rapporter \> Logger for mobilenheter \> Arbeidsbrukerøkter**. |
| Standardjournal for lageroverføring | Velg journalen som skal brukes når arbeidere bruker en mobilenhet til å flytte produkter fra et lager til et annet. |
| Tillat registrering av bestillingslinje i ekstern vurdering | Sett dette alternativet til *Ja* hvis arbeidere skal kunne bruke en mobilenhet til å registrere ordrelinjer for bestillinger som har **Godkjenningsstatus**-verdien *Til ekstern vurdering*. Sett dette alternativet til *Nei* for å hindre at arbeidere registrerer linjer for bestillinger som er under ekstern gjennomgang. |
| Aktiver RSAT-støtte | Feltet aktiverer oppgavevalidereren for mobilappen Warehouse Management, som logger og validerer hvert trinn som appen utfører. Fordi denne prosessen kan senke systemytelsen betydelig, bør du bare aktivere validatoren under testing. Du bør aldri aktivere den i et produksjonsmiljø. |
