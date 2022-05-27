---
title: Spore innkommende sjøreiser og reiser med forsendelsescontainer
description: Dette emnet beskriver hvordan du kan bruke den innkommende sporingssiden til å spore fremdriften av sjøreiser og forsendelsescontainere under reiser.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 07f93cfe563c90d06dd73d46bad678a11a51c5eb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693451"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Spore innkommende sjøreiser og reiser med forsendelsescontainer

[!include [banner](../../includes/banner.md)]

Fra siden **Innkommende sporing** kan du spore fremdriften av sjøreiser og forsendelsescontainere under reiser. Hver sjøreise deles inn etter *aktiviteter*, som hver har sin egen rad på siden. Du kan bruke siden til å vise og angi estimerte datoer og faktiske datoer etter aktivitet.

Disse aktivitetene viser automatisk den estimerte leveringsdatoen ved det endelige målet, avhengig av oppsettet i [Sporingskontrollsenteret](delivery-information-setup.md#tracking-control-center). Avhengig av oppsettet oppdaterer også siste dato vanligvis leveringsdatoen eller den bekreftede datoen på bestillingslinjer. For overføringsordrelinjer kan du konfigurere systemet til å oppdatere mottaksdatoen.

Hvis du vil åpne siden **Innkommende sporing**, går du til **Netto innkjøpspris \> Sporing \> Innkommende sporing**.

## <a name="filter-the-activities-list"></a>Filtrere aktivitetslisten

Du kan bruke feltene **Sjøreise** og **Forsendelsescontainer** på siden **Innkommende sporing** til å filtrere siden slik at den bare viser aktiviteter som er knyttet til den valgte sjøreise- og forsendelsescontaineren.

## <a name="update-tracking-information"></a>Oppdatere sporingsinformasjon

Hvis du vil oppdatere planen for en sjøreise eller reise, angir du startdatoen for den første aktiviteten. Den estimerte sluttdatoen for siste aktivitet oppdateres deretter. Oppsettet for hver etarppe og reisemal i [sporingskontrollsenteret](delivery-information-setup.md#tracking-control-center) fastsetter de estimerte leveringstidene. De estimerte sluttdatoene bruker leveringstiden fra startdatoen til aktiviteten. Når den faktiske sluttdatoen registreres, oppdateres startdatoen for den neste aktiviteten til den samme datoen som den forrige aktivitetens faktiske sluttdato. Den faktiske leveringstiden oppdateres slik at sammenligning og analyse kan utføres. Tilleggsmerknader kan angis i feltet **Merknad**.

Rekkefølgen på aktivitetene i rutenettet bestemmes av rekkefølgen på etappene i den relevante reisemalen. Hvis etapperekkefølgen i den tilknyttede reisen endres, endres også sporingskontrollen.

Du kan oppdatere datoene for alle containere ved å velge **Oppdater startdato** eller **Oppdater faktisk sluttdato** i handlingsruten. Du kan også angi datoene per container på forsendelsen. Denne fremgangsmåten gir større fleksibilitet, fordi containere kan deles i et miljø med flere reiser.

## <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruten

Du kan bruke knappene i handlingsruten på siden **Innkommende sporing** til å arbeide med innkommende sjøreiser og reiser. Følgende tabell beskriver knappene som er tilgjengelige.

| Knapp | beskrivelse |
|---|---|
| Rediger | Rediger en sjøreise eller reise med forsendelsescontainer. |
| Nye | Opprett en ny sjøreise eller reise med forsendelsescontainer. |
| Delete | Slett en valgte sjøreise eller reise med forsendelsescontainer. |
| Oppdater startdato | Oppdater startdatoen for en aktivitet for alle containere i en sjøreise. Når startdatoen for en bestemt aktivitet eller etappe av en reise blir oppdatert, oppdateres de etterfølgende forventede startdatoene basert på den angitte leveringstiden. |
| Oppdater avsetningssluttdato | Oppdater sluttdatoen for en aktivitet for alle containere i reise. Når sluttdatoen for en bestemt aktivitet blir oppdatert, oppdateres de etterfølgende aktivitetene basert på den angitte leveringstiden. |
| Legg til aktiviteter | Legge til en aktivitet i en sjøreise manuelt. Du kan for eksempel legge til en desinfeksjonsaktivitet. Tillegget kan føre til at bekreftet leveringsdato for varene i transportmidlet eller selve sjøreisen endres. Når en aktivitet legges til i reisen, legges estimert antall dager inn før startdatoen for en reiseetappe er oppdatert. |

## <a name="information-and-settings-on-the-overview-tab"></a>Informasjon og innstillinger i fanen Oversikt

Fanen **Oversikt** viser en liste over alle aktiviteter som tilhører sjøreisen og/eller forsendelsescontaineren som er valgt øverst på siden. Følgende tabell beskriver feltene som er tilgjengelige for hver aktivitet.

| Felt | beskrivelse |
|---|---|
| Strekning | Etappe-ID-en for aktiviteten, slik den er definert av reisemalen. |
| Leveringsmiddel | Den forventede leveringsmåten for aktiviteten. |
| Aktivitet | Dette feltet identifiserer vanligvis jobben eller oppgaven som er knyttet til aktiviteten. Vanlige eksempler er *Seiling* og *Klarering*. |
| beskrivelse | En lengre beskrivelse av aktiviteten. |
| Startdato | Dette feltet viser opprinnelig den estimerte startdatoen for aktiviteten. Når den forrige aktivitetens faktiske sluttdato er angitt, vises imidlertid den faktiske startdatoen. Dette feltet brukes til å bestemme den estimerte sluttdatoen, basert på leveringstiden. |
| Estimert sluttdato | Verdien i dette feltet beregnes basert på startdato og leveringstid. Du vil ikke vanligvis redigere verdien direkte. |
| Faktisk sluttdato | En bruker bør oppdatere dette feltet så snart som mulig etter at aktiviteten er skjedd. Den faktiske leveringstiden oppdateres deretter. |
| Estimerte dager | Den estimerte tiden (i dager) som kreves for å fullføre aktiviteten. |
| Faktiske dager | Den faktiske tiden (i dager) som kreves for å fullføre aktiviteten. |
| Merk | Bruk dette feltet til å legge til merknader og detaljer om aktiviteten. |

## <a name="information-and-settings-on-the-general-tab"></a>Informasjon og innstillinger i fanen Generelt

Fanen **Generelt** viser informasjon om etappen som er valgt i fanen **Oversikt**. Selv om den gjentar noe av informasjonen som vises i fanen **Oversikt**, inneholder den også tilleggsinformasjon om den valgte etappen.
