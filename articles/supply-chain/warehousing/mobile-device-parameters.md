---
title: Globale mobilenhetsparametere
description: Denne artikkelen beskriver hvordan du definerer mobilenhetsinnstillinger på siden Lagerstyringsparametere.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6e03414edd9243fcc4156195928455b30a7cee9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847766"
---
# <a name="global-mobile-device-parameters"></a>Globale mobilenhetsparametere

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer globale lagerstyringsparametere som påvirker hvordan systemet fungerer sammen med mobilenheter.

Hvis du vil ha mer informasjon om hvordan du definerer lagerarbeidere, kan du se [Administrere lagerarbeider](manage-warehouse-workers.md). For mer informasjon om nummerskiltbehandling på mobile enheter, se [Nummerskiltmottak via mobilappen Warehouse Management](warehousing-mobile-device-app-license-plate-receiving.md). Hvis du vil ha mer informasjon om syklusopptellingsprosessene, kan du se [Syklusopptelling](cycle-counting.md) og [Eksempelscenarier for syklustelling](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>Åpne siden Lagerstyringsparametere

For å åpne siden **Lagerstyringsparametere** går du til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**. Deretter kan du definere feltene som er knyttet til mobilenhetsarbeid, som beskrevet i neste del av denne artikkelen.

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
