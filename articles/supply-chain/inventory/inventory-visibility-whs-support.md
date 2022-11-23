---
title: Inventory Visibility-støtte for WMS-varer
description: Denne artikkelen beskriver Lagersynlighet for varer som er aktivert for Warehouse Management-prosesser (WMS-varer).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762761"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Inventory Visibility-støtte for WMS-varer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver Lagersynlighet for varer som er aktivert for Warehouse Management-prosesser (WMS). Funksjonen som legger til denne funksjonen i Lagersynlighet kalles *Avansert WMS*.

## <a name="wms-items"></a>WMS-varer

En WMS-vare er en vare som er aktivert for WMS og behandles på et lager som også er WMS-aktivert.

Hvis du vil ha mer informasjon om WMS og modulen **Lagerstyring** i Microsoft Dynamics 365 Supply Chain Management, kan du se [Oversikt over lagerstyring](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Området for funksjonen

Avansert WMS-funksjonen for lagersynlighet fokuserer på beregning av lagerbeholdning som er basert på beholdningsspørringer. Funksjonen er ikke beregnet på å la deg bruke lagersynlighet til å administrere lagerbehandlingsaktiviteter generelt. Lagersynlighet viser ikke lagerspesifikke begreper for brukerne. Her er noen eksempler på disse konseptene:

- Reservasjonshierarki
- Om en vare eller et lager er WMS-aktivert
- Gruppe-ID for enhetssekvens
- Lagerspesifikke prosesser, for eksempel forsendelser, belastninger, bølger og arbeid

Lagersynlighet utleder denne informasjonen, basert på dataene som sendes fra Supply Chain Management. De WMS-spesifikke dataene (med andre ord data fra `WHSInventReserve`-tabellen) er ikke synlige for brukerne.

Når du bruker funksjonen Avansert WMS for lagersynlighet, er alle spørringsresultatene identiske med resultatene fra spørringer som sendes direkte i Supply Chain Management. De vil imidlertid ikke være identiske med resultatene fra spørringer som gjøres ved hjelp av Warehouse Management-mobilappen, fordi mobilappen bruker litt forskjellig beregningslogikk.

## <a name="when-to-use-the-feature"></a>Når funksjonen skal brukes

Vi anbefaler at du bruker funksjonen WMS for lagersynlighet i scenarioer der alle følgende betingelser er oppfylt:

- Du synkroniserer Supply Chain Management-data med lagersynlighet.
- Du bruker WMS i Supply Chain Management.
- Brukere foretar reservasjoner for WMS-varer på nivåer under lagernivå (for eksempel på nummerskiltnivå, fordi du behandler lagerarbeid).

I andre scenarioer vil beholdningsspørringsresultatene være like, uansett om funksjonen Avansert WMS for lagersynlighet er aktivert. I tillegg vil ytelsen være bedre hvis du ikke aktiverer funksjonen i disse scenarioene, fordi det er færre beregninger og færre indirekte kostnader.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Aktiver funksjonen WMS for lagersynlighet

For å aktivere funksjonen WMS for lagersynlighet følger du denne fremgangsmåten.

1. Logg deg på Supply Chain Management som en administrator.
1. Åpne arbeidsområdet [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og aktiver følgende funksjoner i denne ordren:

    1. *Integrering av lagersynlighet*
    1. *Aktiver lagervarer i lagersynlighet*

1. Gå til **Lagerstyring \> Oppsett \> Parametere for integrering av lagersynlighet**.
1. På **Aktiver WMS-varer**-fanen angir du **Aktiver WMS-varer**-alternativet til *Ja*.
1. Logg deg på Power Apps-miljøet, og åpne **Lagersynlighet**.
1. Åpne **Konfigurasjon**-siden og aktiver funksjonen **AdvancedWHS** på fanen *Funksjonsbehandling*.
1. I Supply Chain Management går du til **Lagerstyring \> Regelmessige oppgaver \> Integrering av lagersynlighet**.
1. Velg **Deaktiver** i handlingsruten for å deaktivere lagersynlighet midlertidig.
1. Velg **Aktiver** i handlingsruten for å aktivere lagersynlighet på nytt. Tillegget lastes inn på nytt, og den nye funksjonen er nå aktivert. WMS-relaterte data blir synkronisert med lagersynligheten.

## <a name="query-on-hand-quantities-of-wms-items"></a>Spørring på lagerbeholdning av WMS-varer

Hvis du vil spørre etter WMS-varer, bruker du samme [API (Application Programming Interface) og meldingssyntaks](inventory-visibility-api.md) som du bruker for ikke-WMS-varer. Du trenger ikke å angi om en vare er en WMS-vare eller en vare som ikke er WMS. Lagersynlighet skiller automatisk mellom varer, basert på dataene som er lagret.

Resultatene fra spørringer for WMS-varer er egentlig de samme som resultatene for ikke-WMS-varer. Den eneste forskjellen er at følgende fysiske mål fra `fno`-datakilden beregnes basert på WMS-logikken i Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Alle andre fysiske mål beregnes på samme måte som de er når funksjonen WMS for lagersynlighet er deaktivert.

Hvis du vil ha detaljert informasjon om hvordan lagerbeholdninger for WMS-varer fungerer, kan du se det tekniske dokumentet [Reservasjoner i lagerstyring](https://www.microsoft.com/download/details.aspx?id=43284).

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Lagerlistevisning og dataenhet for WMS-varer

På siden **Forhåndslast lagersynlighetssammendraget** finner du en visning for enheten *Forhåndslast lagerindeksspørring*. I motsetning til enheten *Lagersammendrag* inneholder enheten *Forhåndslast lagerindeksspørring* en lagerbeholdningsliste for produkter sammen med valgte dimensjoner. Lagersynlighet synkroniserer de forhåndslastede sammendragsdataene hvert 15. minutt.

Hvis du bruker lagersynlighet med WMS-varer og vil vise lagerbeholdningslisten for WMS-varer, anbefaler vi at du aktiverer funksjonen *Forhåndslast sammendrag av lagersynlighet* (se også se også [Forhåndslast en strømlinjeformet spørring på lager](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Tilsvarende dataenhet i Dataverse-butikker lagrer forhåndslastingsresultat, som oppdateres hvert 15. minutt. Navnet på dataenheten er `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> Dataverse-enheten er skrivebeskyttet. Du kan vise og eksportere dataene i lagersynlighetsenhetene, men **ikke endre dem**.

Det er ikke tillatt å endre WMS-vareantall som er lagret i Supply Chain Management-datakilden (`fno`). Denne virkemåten samsvarer med virkemåten til andre funksjoner i Lagersynlighet. Denne begrensningen fremtvinges for å forhindre konflikter.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS-varekompatibilitet for andre funksjoner i Lagersynlighet

[Ikke-forpliktende reservasjoner](inventory-visibility-reservations.md) og [lagertilordning](inventory-visibility-allocation.md) av WMS-varer støttes. Du kan inkludere WMS-relaterte fysiske mål i beregninger for ikke-forpliktende reservasjoner og tildelinger.

## <a name="calculate-available-to-promise-quantities"></a>Beregn antall for tilgjengelig for ordre

Løsningen støtter fullt ut [tilgjengelig for ordre (ATP)](inventory-visibility-available-to-promise.md) for WMS-varer. Du kan definere ATP-beregninger uten å gjøre noe med WMS-spesifikke detaljer.
