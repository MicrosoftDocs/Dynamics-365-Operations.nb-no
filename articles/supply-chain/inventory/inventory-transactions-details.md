---
title: Lagertransaksjonsdetaljer
description: Dette emnet gir en oversikt over Transaksjonsdetaljer-siden som viser detaljer om en valgt lagertransaksjon.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735917"
---
# <a name="inventory-transaction-details"></a>Lagertransaksjonsdetaljer

Bruk **Transaksjonsdetaljer**-siden til å vise detaljer for alle valgte lagertransaksjoner.

## <a name="open-the-transaction-details-page"></a>Åpne Transaksjonsdetaljer-siden

Følg denne fremgangsmåten for å åpne **Transaksjonsdetaljer**-siden.

1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Transaksjoner**.
1. Velg transaksjonen du vil inspisere.
1. Velg **Transaksjonsdetaljer** i handlingsruten.

## <a name="fasttabs-overview"></a>Oversikt over hurtigfaner

**Transaksjonsdetaljer**-siden er delt inn i flere hurtigfaner. Tabellen nedenfor beskriver formålet med hver hurtigfane.

| Hurtigfane | Beskrivelse |
|---|---|
| Generelt | Denne hurtigfanen viser grunnleggende informasjon om den valgte lagertransaksjonen. I tillegg til feltene som vises på **Lagertransaksjoner**-siden, inneholder den tilleggsfeltene som beskrives senere i dette emnet. |
| Oppdateringer | Denne hurtigfanen viser informasjon som er knyttet til de fysiske og økonomiske aspektene og utligningsaspektet ved den valgte lagertransaksjonen. Noen felter kan være tomme, avhengig av gjeldende status for transaksjonen. Disse feltene angis imidlertid automatisk når transaksjoner posteres. I tillegg til feltene som vises på **Lagertransaksjoner**-siden, inneholder denne hurtigfanen tilleggsfeltene som beskrives senere i dette emnet. |
| Finansposteringer | Denne hurtigfanen viser posteringstypen og finanskontoen som brukes til den fysiske oppdateringen, økonomiske oppdateringen, fysiske omsetningen, fysiske tilleggene, finansinntekten og gebyrene som er knyttet til den valgte lagertransaksjonen. |
| Referanser | Denne hurtigfanen viser tilleggsinformasjon om kildetransaksjonen som opprettet den valgte lagertransaksjonen. Denne informasjonen kan for eksempel omfatte detaljer fra bestillingen eller salgsordren. |
| Beslektet informasjon | Denne hurtigfanen viser tilleggsinformasjon om den valgte lagertransaksjonen. Det kan hende at disse feltene ikke angis hvis det er enkelte funksjoner du ikke bruker, for eksempel innkjøpskategorier eller prosjekter. |
| Finansdimensjoner – fysisk | Denne hurtigfanen viser finansdimensjonsverdiene som ble brukt da den fysiske oppdateringen ble postert. Hvis den fysiske oppdateringen ikke er postert, er feltene tomme. |
| Finansdimensjoner – økonomisk | Denne hurtigfanen viser finansdimensjonsverdiene som ble brukt da den økonomiske oppdateringen ble postert. Hvis den økonomiske oppdateringen ikke er postert, er feltene tomme. |
| Lagerdimensjoner | Denne hurtigfanen viser lagerdimensjonsverdiene som er tilordnet til den valgte lagertransaksjonen. Disse verdiene omfatter område, lager, størrelse, farge, konfigurasjon, sted, partinummer, serienummer, lagerstatus, nummerskilt og eier. |

## <a name="fields-on-the-general-fasttab"></a>Felter i hurtigfanen Generelt

Tabellen nedenfor beskriver feltene i hurtigfanen **Generelt** som ikke også vises på **Lagertransaksjoner**-siden.

| Felt | Beskrivelse |
|---|---|
| Part | Navnet på den relevante parten for den valgte lagertransaksjonen. En bestillingstransaksjon viser for eksempel navnet på leverandøren på bestillingen, og en salgsordretransaksjon viser navnet på kunden. Dette feltet er ikke tilgjengelig for alle typer lagertransaksjoner. |
| Lagerreferanse | Typen for en annen lagertransaksjon hvis denne andre lagertransaksjonen er knyttet til den valgte lagertransaksjonen. Hvis en bestilling for eksempel er merket mot en salgsordre, angis *Salgsordre* i feltet **Lagerreferanse** for bestillingstransaksjonen. Merking skjer automatisk for direkteleveringsordrer og konserninterne ordrer. Når du bruker merking med andre etterkalkuleringsmetoder enn *standardkost* og *glidende gjennomsnitt*, oppretter systemet utligninger og justeringer for nøyaktig de transaksjonene som er merket. Dermed kan du oppnå «faktisk» etterkalkulering som overstyrer logikken for først inn, først ut (FIFO); sist inn, først ut (LIFO) eller avveid gjennomsnitt. |
| Lagernummer | Den spesifikke transaksjonen som er knyttet til den valgte lagertransaksjonen. Hvis en bestilling for eksempel er merket mot en salgsordre, angis salgsordrenummeret i feltet **Lagernummer** for bestillingstransaksjonen. |
| Prosjekt-ID | Hvis den valgte lagertransaksjonen er knyttet til et prosjekt, angis prosjektnummeret i dette feltet. |
| Parti-ID | Den unike parti-ID-en som systemet har tilordnet til den valgte lagertransaksjonen. |
| Referanseparti | Parti-ID-en for en annen lagertransaksjon hvis denne andre lagertransaksjonen er knyttet til den valgte lagertransaksjonen. Hvis en bestilling for eksempel er merket mot en salgsordre, er **Parti-ID**-verdien for salgsordrelinjens lagertransaksjon i feltet **Referanseparti** for bestillingstransaksjonen. |
| Dimensjonsnummer | En unik ID som representerer kombinasjonen av alle lagerdimensjonsverdiene som er tilordnet til den valgte lagertransaksjonen. |
| Verdi åpen | En verdi som angir om den valgte lagertransaksjonen er utlignet av lagerlukkingsprosessen. Hvis *Ja* er angitt for dette feltet, er ikke transaksjonen utlignet. |
| Forventet dato | Når det gjelder tilgangstransaksjoner, er dette datoen da lagertilgangen forventes å forekomme. Dette feltet kan for eksempel vise den forventede tilgangsdatoen på en lagerblokkeringsordre eller leveringsdatoen på en bestillingslinje. |
| Lagerdato | Dette feltet angis når det ble utført en registreringstransaksjon på mottaksordren før en fysisk tilgang ble postert. |
| Ikke-finansoverføring | En verdi som angir om den valgte lagertransaksjonen er en ikke-finansoverføring. En ikke-finansoverføring skjer når en endring i lagerdimensjoner ikke spores økonomisk på siden **Varemodellgruppe**. |
| Overføringsparti-ID | Hvis den valgte lagertransaksjonen er en ikke-finansoverføring, angis **Parti-ID**-verdien til den andre lagertransaksjonen som den valgte transaksjonen utlignes mot, i dette feltet. |

## <a name="fields-on-the-updates-fasttab"></a>Felter i hurtigfanen Oppdateringer

Tabellen nedenfor beskriver feltene i hurtigfanen **Oppdateringer** som ikke også vises på **Lagertransaksjoner**-siden.

| Felt | Beskrivelse |
|---|---|
| Fysisk bilag | Bilagsnummeret fra økonomimodulen der den fysiske posteringen for den valgte lagertransaksjonen ble generert. |
| Rute | Ruten som er knyttet til den valgte lagertransaksjonen. Dette feltet angis bare for plukklistetransaksjoner for produksjon der stykklisten eller formellinjen er knyttet til en bestemt vare. |
| Følgeseddel | Følgeseddelnummeret som ble angitt for en mottaksseddeltransaksjon for bestilling. |
| Fysisk kostbeløp | Beløpet som ble postert i økonomimodulen for den fysiske oppdateringen. For et standardkostnadsprodukt representerer dette beløpet standardkostnaden. For andre etterkalkuleringsmetoder representerer det avveid gjennomsnitt for produktet ved postering. |
| Fysisk omsetning | Beløpet for utsatt inntekt som ble postert i økonomimodulen for den fysiske oppdateringen. |
| Last-ID | Hvis gjeldende transaksjon er knyttet til en last i Transportstyring, viser dette feltet det unike nummeret på lasten som omfattet varen. |
| Fysisk postert | En verdi som angir om den valgte lagertransaksjonen er fysisk postert. Hvis gjeldende transaksjon er postert i økonomimodulen, finnes det også et fysisk bilag. |
| Økonomisk postert | En verdi som angir om den valgte lagertransaksjonen er økonomisk postert. Hvis gjeldende transaksjon er postert i økonomimodulen, finnes det også et økonomisk bilag. |
| Postert fysisk tillegg | En verdi som angir om de fysiske tilleggene som er knyttet til den valgte lagertransaksjonen, er postert. |
| Postert gebyr | En verdi som angir om gebyrene som er knyttet til den valgte lagertransaksjonen, er postert. |
| Økonomisk bilag | Bilagsnummeret i økonomimodulen der den økonomiske posteringen ble generert. |
| Faktura | Fakturanummeret som ble generert, for eksempel for en bestilling eller salgsordre. |
| Justering | Beløpet som ble justert for den valgte lagertransaksjonen, fra prosessen for lagerlukking og -justering. |
| Resultat, postert beløp | Beløpet for den valgte lagertransaksjonen som ble postert i resultatregnskapet. |
| Ikke-postert faktura | Fakturanummeret til en tilknyttet bestilling som vises på siden **Ventende leverandørfaktura**. |
| Økonomisk lukket | Datoen da transaksjonen ble fullstendig utlignet. |
| Dekket antall for faktisk vekt | Faktisk vekt-antallet som dekkes av utligningen. |
| Utlignet antall | Antallet som er utlignet for den valgte lagertransaksjonen. |
| Beløp som er utlignet | Verdien som er utlignet for den valgte lagertransaksjonen. |
