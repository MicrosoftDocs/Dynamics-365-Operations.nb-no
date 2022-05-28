---
title: Oppsett av reise med flere etapper
description: Dette emnet beskriver hvordan du definerer reiser med flere etapper for modulen Netto innkjøpspris.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c65a3d3971593ccf832a6af3c8c27d56a68b46c8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689726"
---
# <a name="multi-leg-journey-setup"></a>Oppsett av reise med flere etapper

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du definerer reiser med flere etapper for modulen **Netto innkjøpspris**.

## <a name="legs"></a>Strekninger

Etapper brukes til å identifisere atskilte deler av en reise. Hver etappe bygges ved å velge til- og fra-utskipningshavner og transportmåten som brukes for den etappen. Leveringstiden kan knyttes til hver etappe. Leveringstider kan bidra til å spore en forsendelse, og kan også brukes til å beregne den forventede leveringsdatoen for varene for en sjøreise. Når en etappe av en reise er fullført, kan statusen for sjøreisen, forsendelsescontaineren og tilknyttede bestillingslinjer dessuten oppdateres via sporingskontrolloppsettet. Etapper kan brukes av én reisemal, eller de kan brukes på nytt av flere reisemaler. Containerlastning, toll og lokal transport er generelt sett definert som etapper, og en ikke-spesifikk forsendelseshavn brukes for dem.

Hvis du vil arbeide med etapper, går du til **Netto innkjøpspris \> Oppsett for reise med flere etapper \> Etapper**. Der kan du vise, åpne, opprette og slette poster for etapper. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Strekning | Angi et unikt identifikasjonsnavn/-nummer for reiseetappen. |
| beskrivelse | Angi en beskrivelse av reiseetappen. Vanligvis identifiserer denne beskrivelsen til- og fra-havnene, eller trinnet i reisen. |
| Fra-havn | Angi opprinnelsesstedet for varene på etappen. |
| Til-havn | Angi destinasjonsstedet for varene på etappen. |
| Leveringsmetode | Angi transportmåte for etappen. |

## <a name="journey-templates"></a>Reisemaler

En reisemal definerer en reise med flere etapper mellom to havner som varer i løpet av en sjøreise. Etappene i reisen blir kombinert for å beregne hvor lang tid det vil ta for varer å reise fra leverandørens opprinnelsessted til den endelige lagerdestinasjonen. Når etappene er plassert i reisemalen i en bestemt rekkefølge, vil leveringstidene identifisere datoen for hver etappe og status for sjøreisen, containeren og innkjøpslinjene for sjøreisen. Du bruker [sporingskontrollsenteret](delivery-information-setup.md) til å definere leveringstidene som er knyttet til hver etappe som utgjør reisemalen. Reisemalen brukes også når de automatiske kostnadene til en sjøreise defineres. Når en reise defineres, kan kostnaden som er knyttet til transporten av varene, defineres på siden for automatiske kostnader.

Hvis du vil arbeide med reisemaler, går du til **Netto innkjøpspris \> Oppsett for reise med flere etapper \> Reisemaler**. Der kan du vise, åpne, opprette og slette reisemaler.

Angi følgende felt i hodet for hver reisemal.

| Felt | beskrivelse |
|---|---|
| Reisemal | Angi et unikt identifikasjonsnavn/-nummer for reisemalen. Reisemalen beskriver som regel opprinnelses- og destinasjonsstedet for reisen. |
| beskrivelse | Angi en beskrivelse av reisemalen. Beskrivelsen indikerer som regel til- og fra-havnene og reisetypen. |

I delen **Linjer** legger du til en linje for hver etappe av reisen, og plasserer linjene i rekkefølge. Bruk pilene **Opp** og **Ned** på verktøylinjen til å endre rekkefølgen på linjene. Følgende tabell beskriver feltene som er tilgjengelige for hver linje.

| Felt | beskrivelse |
|---|---|
| Strekning | Velg en etappe som skal legges til reisen. |
| beskrivelse | Beskrivelsen av etappen. |
| Fra-havn | Havnen som er opprinnelsesstedet for varene på etappen. Denne havnen er til-havnen som brukes til å fastslå de automatiske kostnadene for en sjøreise. |
| Til-havn | Den endelige destinasjonshavnen for varene på etappen. |
| Leveringsmiddel | Leveringsmåten som brukes for etappen. |
| Reise fra havn | Hvis havnen som er angitt for etappen, brukes til å fastslå de automatiske kostnadene, merker du av i denne avmerkingsboksen for å identifisere den som "reise fra"-havnen. Denne havnen vil bli vist i sjøreisehodet. |
| Reise til havn | Hvis havnen som er angitt for etappen, brukes til å fastslå de automatiske kostnadene, merker du av i denne avmerkingsboksen for å identifisere den som "reise til"-havnen. Denne havnen vil bli vist i sjøreisehodet. |
| Forsendelsesfirma | Velg forsendelsesfirmaet som brukes for etappen. |

## <a name="activities"></a>Aktiviteter

Innstillingene på siden **Aktiviteter** fastsetter hvilke typer aktiviteter som kan forekomme i destinasjonshavnen til en etappe. Brukere som arbeider på siden **Alle forsendelsescontainere**, kan velge blant disse verdiene når de estimerer varigheten til hver aktivitet og registrerer den faktiske varigheten til sammenligningsformål.

Hvis du vil definere aktiviteter, går du til **Netto innkjøpspris \> Oppsett av reise med flere etapper \> Aktiviteter**. Der kan du legge til, fjerne og redigere aktiviteter ved hjelp av knappene i handlingsruten.

Følgende tabell beskriver feltene som er tilgjengelige for hver aktivitet i rutenettet.

| Felt | beskrivelse |
|---|---|
| Aktivitet | Navnet på aktiviteten. |
| beskrivelse | En beskrivelse av akiviteten. |
| Forsendelsesfirma | Leverandørkontoen for forsendelsesfirmaet som er knyttet til aktiviteten. |
