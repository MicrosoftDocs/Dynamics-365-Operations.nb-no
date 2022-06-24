---
title: Inventory Visibility-støtte for WHS-varer
description: Denne artikkelen beskriver Lagersynlighet for varer som er aktivert for avanserte lagerprosesser (WHS-varer).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: ec2254d6cf203216acea88fdfb54ad491abdeb49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895677"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Inventory Visibility-støtte for WHS-varer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver Lagersynlighet for varer som er aktivert for avanserte lagerprosesser (WHS-varer). Funksjonen som legger til denne funksjonen i Lagersynlighet kalles *Avansert WHS*.

## <a name="whs-items"></a>WHS-varer

En WHS-vare er en vare som er aktivert for avanserte lagerprosesser (WHS) og behandles på et lager som også er WHS-aktivert.

Hvis du vil ha mer informasjon om WHS og modulen **Lagerstyring** i Microsoft Dynamics 365 Supply Chain Management, kan du se [Oversikt over lagerstyring](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Området for funksjonen

Avansert WHS-funksjonen for lagersynlighet fokuserer på beregning av lagerbeholdning som er basert på beholdningsspørringer. Funksjonen er ikke beregnet på å la deg bruke lagersynlighet til å administrere lagerbehandlingsaktiviteter generelt. Lagersynlighet viser ikke lagerspesifikke begreper for brukerne. Her er noen eksempler på disse konseptene:

- Reservasjonshierarki
- Om en vare eller et lager er WHS-aktivert
- Gruppe-ID for enhetssekvens
- Lagerspesifikke prosesser, for eksempel forsendelser, belastninger, bølger og arbeid

Lagersynlighet utleder denne informasjonen, basert på dataene som sendes fra Supply Chain Management. De WHS-spesifikke dataene (med andre ord data fra `WHSInventReserve`-tabellen) er ikke synlige for brukerne.

Når du bruker funksjonen Avansert WHS for lagersynlighet, er alle spørringsresultatene identiske med resultatene fra spørringer som sendes direkte i Supply Chain Management. De vil imidlertid ikke være identiske med resultatene fra spørringer som gjøres ved hjelp av Warehouse Management-mobilappen, fordi mobilappen bruker litt forskjellig beregningslogikk.

## <a name="when-to-use-the-feature"></a>Når funksjonen skal brukes

Vi anbefaler at du bruker funksjonen Avansert WHS for lagersynlighet i scenarioer der alle følgende betingelser er oppfylt:

- Du synkroniserer Supply Chain Management-data med lagersynlighet.
- Du bruker WHS i Supply Chain Management.
- Brukere foretar reservasjoner for WHS-varer på andre nivåer enn lagernivå (for eksempel fordi du bruker lagerarbeid).

I andre scenarioer vil beholdningsspørringsresultatene være like, uansett om funksjonen Avansert WHS for lagersynlighet er aktivert. I tillegg vil ytelsen være bedre hvis du ikke aktiverer funksjonen i disse scenarioene, fordi det er færre beregninger og færre indirekte kostnader.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Aktiver funksjonen Avansert WHS for lagersynlighet

For å aktivere funksjonen Avansert WHS for lagersynlighet følger du denne fremgangsmåten.

1. Logg deg på Supply Chain Management som en administrator.
1. Åpne arbeidsområdet [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og aktiver følgende funksjoner i denne ordren:

    1. *Integrering av lagersynlighet*
    1. *Aktiver lagervarer i lagersynlighet*

1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**.
1. På **Aktiver WHS-varer**-fanen angir du **Aktiver WHS-varer**-alternativet til *Ja*.
1. Logg på Power Apps.
1. Åpne **Konfigurasjon**-siden og aktiver funksjonen **AdvancedWHS** på fanen *Funksjonsbehandling*.
1. I Supply Chain Management går du til **Lagerstyring \> Regelmessige oppgaver \> Integrering av lagersynlighet**.
1. Velg **Deaktiver** i handlingsruten for å deaktivere lagersynlighet midlertidig.
1. Velg **Aktiver** i handlingsruten for å aktivere lagersynlighet på nytt. Tillegget lastes inn på nytt, og den nye funksjonen er nå aktivert. WHS-relaterte data blir synkronisert med lagersynligheten.

## <a name="query-on-hand-quantities-of-whs-items"></a>Spørring på lagerbeholdning av WHS-varer

Hvis du vil spørre etter WHS-varer, bruker du samme [API (Application Programming Interface) og meldingssyntaks](inventory-visibility-api.md) som du bruker for ikke-WHS-varer. Du trenger ikke å angi om en vare er en WHS-vare eller en vare som ikke er WHS. Lagersynlighet skiller automatisk mellom varer, basert på dataene som er lagret.

Resultatene fra spørringer for WHS-varer er egentlig de samme som resultatene for ikke-WHS-varer. Den eneste forskjellen er at følgende fysiske mål fra `fno`-datakilden beregnes basert på WHS-logikken i Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle andre fysiske mål beregnes på samme måte som de er når funksjonen Avansert WHS for lagersynlighet er deaktivert.

Hvis du vil ha detaljert informasjon om hvordan lagerbeholdninger for WHS-varer fungerer, kan du se det tekniske dokumentet [Reservasjoner i lagerstyring](https://www.microsoft.com/download/details.aspx?id=43284).

Dataenhetene som blir eksportert til Dataverse, kan ennå ikke oppdatere antallet for WHS-varer. Antallene som vises i dataenhetene, er riktige både for varer som ikke er WHS-varer og for antall som ikke berøres av WHS-logikken (det vil si mål unntatt `AvailPhysical`, `AvailOrdered`, `ReservPhysical` og `ReservOrdered` i `fno`-datakilden).

Det er ikke tillatt å endre WHS-vareantall som er lagret i Supply Chain Management-datakilden. På samme måte som andre funksjoner i lagersynlighet fremtvinges denne begrensningen for å forhindre konflikter.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Ikke-forpliktende reservasjoner for WHS-varer i lagersynlighet

Generelt støttes [ikke-forpliktende reservasjoner](inventory-visibility-reservations.md) på WHS-varer. Du kan inkludere WHS-relaterte fysiske mål i beregninger for ikke-forpliktende reservasjoner. 

I en kjent begrensning støttes ikke den *tilgjengelige for reservasjonsberegning* for WHS-varer. Hvis det er reservasjon over de nåværende dimensjonene der det forekommer en ikke-forpliktende reservasjon, er derfor *tilgjengelig for reservasjonsberegning* feil. Ikke-forpliktende reservasjoner påvirkes ikke når alternativet **ifCheckAvailForReserv** er deaktivert i [API-en for ikke-forpliktende reservasjon](inventory-visibility-api.md#create-one-reservation-event).

Denne begrensningen gjelder også funksjoner og tilpasninger som er basert på ikke-forpliktende reservasjoner (som tildeling).

## <a name="calculate-available-to-promise-quantities"></a>Beregn antall for tilgjengelig for ordre

Løsningen støtter fullt ut [tilgjengelig for ordre (ATP)](inventory-visibility-available-to-promise.md) for WHS-varer. Du kan definere ATP-beregninger uten å gjøre noe med WHS-spesifikke detaljer.
