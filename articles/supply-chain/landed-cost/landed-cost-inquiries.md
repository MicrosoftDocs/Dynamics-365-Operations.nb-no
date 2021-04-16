---
title: Forespørsler om netto innkjøpspris
description: Dette emnet beskriver hvordan du finner og bruker de ulike forespørselstypene som er tilgjengelige for modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 22a2e76780adb43b053b6cf7fd08411a4a60aeac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823367"
---
# <a name="landed-cost-inquiries"></a>Forespørsler om netto innkjøpspris

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Forespørsler om sjøreiselinje

Forespørselen **Sjøreiselinjer** viser alle sjøreiselinjer når de gjelder for lager. Denne forespørselen kan brukes som et filter for å hjelpe deg med å finne en vare, en bestilling eller annen nyttig opplysing. Den kan også brukes til å identifisere den forventede leveringsdatoen for en vare som kan være på én eller flere forventede sjøreiser. På denne måten kan det hjelpe deg med å administrere forventet lagermottak.

Hvis du vil åpne denne forespørselen, går du til **Netto innkjøpspris \> Forespørsler \> Sjøreiselinjer**.

### <a name="overview-tab"></a>Fanen Oversikt

Fanen **Oversikt** på forespørselssiden **Sjøreiselinjer** omfatter et rutenett som viser grunnleggende informasjon om hver relevante sjøreiselinje. I tabellen nedenfor beskrives de forskjellige kolonnene i rutenettet.

| Stående stolpe | beskrivelse |
|---|---|
| **Varenummer** | Varen for sjøreiselinjen. |
| **Referanse** | Ordretypen (bestilling eller overføringsordre). |
| **Antall** | Bestillingsnummeret eller nummeret for overføringsordre. |
| **Folio** | Folioen som er knyttet til sjøreiselinjen. |
| **Fraktcontainer** | Forsendelsescontaineren som er knyttet til sjøreiselinjen. |
| **Sjøreise** | Sjøreisen som er knyttet til sjøreiselinjen. |
| **Antall** | Antallet av varen på for sjøreiselinjen. |
| (Andre dimensjoner) | Du kan vise kolonner for tilleggsdimensjoner etter behov. Disse dimensjonene inkluderer partinummer, lagerstatus og lager. Velg **Lager \> Visningsdimensjoner** i handlingsruten for å åpne en dialogboks der du kan velge hvilke dimensjoner som skal tas med. |

### <a name="general-tab"></a>Fanen Generelt

Velg fanen **Generelt** for å vise mer informasjon om linjen som for øyeblikket er valgt i fanen **Oversikt**.

### <a name="dimensions-tab"></a>Fanen Dimensjon

Velg fanen **Dimensjoner** for å vise verdier for alle tilgjengelige dimensjoner for linjen som for øyeblikket er valgt i fanen **Oversikt**, uavhengig av dimensjonene du har valgt for å vise den fanen.

## <a name="cost-estimate-inquiries"></a>Forespørsler for kostnadsestimat

Hver gang du genererer et kostnadsestimat, blir estimatet lagt til på forespørselssiden **Kostnadsestimater**. Hvis du vil ha fullstendige detaljer om hvordan du genererer, viser og arbeider med kostnadsestimater (inkludert estimater på forespørselssiden), kan du se [Estimere og behandle netto innkjøpspris](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Varesporing

Bruk siden **Varesporing** til å vise åpne bestillingslinjer og deres gjeldende status. Linjer trenger ikke å være knyttet til en sjøreise for å vises her. Hvis en vare er knyttet til en sjøreise, viser imidlertid varesporingspostlinjen sjøreise-ID-en.

Hvis du vil åpne denne siden, går du til **Netto innkjøpspris \> Forespørsler \> Sporing \> Varesporing**.

Ettersom systemet sannsynligvis inneholder et svært høyt antall bestillingslinjer, viser siden **Varesporing** i utgangspunktet ingen poster. Start med å bruke filterfeltene øverst på siden for å definere settet med bestillingslinjer du vil se etter. Velg deretter **Oppdater** i handlingsruten for å generere listen. Du kan bruke en stjerne (\*) som jokertegn i et av filterfeltene. Hvis du for eksempel vil finne alle bestillingslinjer for varer som inneholder ordet "DVD" i navnet, setter du feltet **Type** til **Produktnavn**, og angir *\*DVD\** i feltet **Feltverdi**.

> [!NOTE]
> Restordrer omfatter for øyeblikket bare salgsordrer. Salgstilbud vises ikke eller anses som restordrer.

I tabellen nedenfor beskrives kolonnene i rutenettet på siden **Varesporing**.

| Stående stolpe | beskrivelse |
|---|---|
| **Til-havn** | Det endelige målet. |
| **Bekreftet** | Den bekreftede datoen for bestillingslinjen. |
| **Leveringsdato** | Leveringsdatoen for bestillingslinjen. |
| **Sjøreise** | Hvis linjen er knyttet til en sjøreise, vises sjøreise-ID-en. |
| **Forsendelsescontainer** | Hvis linjen er knyttet til en forsendelsescontainer, vises container-ID-en. |
| **Forsendelseshavn** | Gjeldende havn, basert på den første etappen i sporingsskjemaet der det ikke er angitt noen faktisk dato for forsendelsescontaineren som er knyttet til bestillingslinjen. |
| **Aktivitet** | Gjeldende aktivitet, basert på den første etappen i sporingsskjemaet der det ikke er angitt noen faktisk dato for forsendelsescontaineren som er knyttet til bestillingslinjen. |
| **Estimert sluttdato** | Datoen da sjøreisen er forventet å mottas ved destinasjonslageret. |
| **Navn** | Navnet på leverandøren. |
| **Sjøreisestatus** | Forsendelsesstatusen som er knyttet til bestillingslinjen. |
| **Varenummer** | Varenummeret for gjeldende bestillingslinje. |
| **Ekstern** | Leverandørens varenavn. |
| **Produktnavn** | Navnet på varen for bestillingslinjen. |
| **Antall** | Antallet på bestillingslinjen for bestillingslinjen. |
| **Enhet** | Måleenheten for bestillingslinjen. |
| **Referanse** | Ordretypen (bestilling eller overføringsordre) |
| **Referansenummer** | Bestillingsnummeret eller nummeret for overføringsordre. |
| **Restordre** | Et symbol angir at det finnes restordrer for varen. |
| (Andre dimensjoner) | Du kan vise kolonner for tilleggsdimensjoner etter behov. Disse dimensjonene inkluderer partinummer, lagerstatus og lager. Velg **Visningsdimensjoner** i handlingsruten for å åpne en dialogboks der du kan velge hvilke dimensjoner som skal tas med. |

### <a name="related-information-about-backorders"></a>Beslektet informasjon om restordrer

Hvis du vil vise mer informasjon om restordrer, velger du fanen **Beslektet informasjon** til høyre på siden, og deretter velger du **Restordrer**. Hvis du vil vise mer informasjon om en bestemt restordre, merker du raden for den, og velger deretter koblingen **Mer**.

## <a name="individual-shipping-container-tracking"></a>Individuell fraktcontainersporing

Forespørselen **Sporing av individuell forsendelsescontainer** har et filter som gjør det mulig å finne en forsendelsescontainer og deretter identifisere alle sjøreiselinjene i containeren.

Hvis du vil åpne denne forespørselen, går du til **Netto innkjøpspris \> Forespørsler \> Sporing \> Sporing av individuell forsendelsescontainer**.

## <a name="multiple-shipping-container-tracking"></a>Sporing av flere fraktcontainere

Forespørselen **Sporing av flere forsendelsescontainere** har et filter som gjør det mulig å finne en samling forsendelsescontainere og deretter identifisere alle sjøreiselinjene i de containerne.

Hvis du vil åpne denne forespørselen, går du til **Netto innkjøpspris \> Forespørsler \> Sporing \> Sporing av flere forsendelsescontainere**.
