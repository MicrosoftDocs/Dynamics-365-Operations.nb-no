---
title: Fraktcontainere
description: Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen Netto innkjøpspris.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 96710cf2b5a2e39f9492aadb0ba6f3241f0666f4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690561"
---
# <a name="shipping-container-setup"></a>Oppsett av forsendelsescontainere

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du definerer forsendelsescontainere for modulen **Netto innkjøpspris**.

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a>Definere typer forsendelsescontainere

Typer forsendelsescontainere definerer typene forsendelsescontainere som er tilgjengelige for bruk under forsendelse og sjøreiser.

Hvis du vil arbeide med typer forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Typer forsendelsescontainere**. Der kan du vise, legge til og fjerne poster for containertypene dine. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Fraktcontainertype | Angi et unikt identifikasjonsnavn/-nummer for type forsendelsescontainer. |
| beskrivelse | Angi en beskrivelse av typen forsendelsescontainer. |
| Volum | Angi det maksimale volumet som er tillatt for forsendelsescontainere av denne typen. |
| Tykkelse | Angi den maksimale vekten som er tillatt for forsendelsescontainere av denne typen. |
| Returnerbar | Angi om forsendelsescontainere av denne typen kan returneres til leverandøren etter at de er brukt under en sjøreise. Hvis du velger *Ja*, kan det hende at tilleggskostnader påløper for retur av forsendelsescontainere av denne typen til opprinnelseshavnen. |

## <a name="set-up-shipping-containers"></a>Definere forsendelsescontainere

Du bruker poster for forsendelsescontainer til å identifisere hver container du bruker under sjøreiser. Når du oppretter en sjøreise, kan du velge en bestemt container for sjøreisen i listen over alle postene for forsendelsescontainer du har definert her. Denne funksjonen er spesielt nyttig hvis firmaet eier sine egne forsendelsescontainere.

Du behøver ikke å angi forsendelsescontainernumre for forsendelsescontainere som bare skal brukes én gang. I stedet kan du legge til forsendelsescontainernummeret når du oppretter en sjøreise.

Poster for forsendelsescontainer brukes bare i Netto innkjøpspris. De er ikke tilgjengelige i standardmodulen **Transportstyring** (TMS).

Hvis du vil arbeide med forsendelsescontainere, går du til **Netto innkjøpspris \> Containeroppsett \> Forsendelsescontainere**. Der kan du vise, legge til og fjerne poster for forsendelsescontainerne. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Fraktcontainer | Angi et unikt identifikasjonsnavn/-nummer for forsendelsescontainer. |
| Fraktcontainertype | Velg typen forsendelsescontainer. Hvis du vil ha mer informasjon, kan du se delen [Konfigurere typer forsendelsescontainer](#shipping-container-types) tidligere i dette emnet. |

> [!NOTE]
> - Oppsettet av forsendelsescontainere er valgfritt. Vanligvis bruker du det bare hvis firmaet eier sine egne forsendelsescontainere eller ofte bruker de samme forsendelsescontainerne på nytt.
> - Ingen kontrollsifre beregnes for forsendelsescontainernumre.

## <a name="set-up-unit-types"></a><a name="unit-types"></a>Definere enhetstyper

Enhetstyper fastsetter ytterligere grupperinger og identifikasjonsmetoder for forsendelsescontainere. Enhetstypen brukes vanligvis til å identifisere containertypen varer er pakket i, for eksempel paller eller tromler. Du kan velge en enhetstype når du definerer en container på siden **Alle forsendelsescontainere**.

Enhetstyper brukes bare i Netto innkjøpspris. De er ikke tilgjengelige i TMS.

Hvis du vil arbeide med enhetstyper, går du til **Netto innkjøpspris \> Containeroppsett \> Enhetstyper**. Der kan du vise, legge til og fjerne poster for enhetstypene dine. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Enhetstype | Angi et unikt identifikasjonsnavn/-nummer for enhetstypen. |
| beskrivelse | Skriv inn en beskrivelse av enhetstypen. |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a>Definere kjøletyper

Kjøletyper oppretter tilleggsgrupperinger og identifikasjonsmetoder for forsendelsescontainere (vanligvis kjølecontainere). Du kan velge en kjøletype når du definerer en container på siden **Alle forsendelsescontainere**.

Hvis du vil arbeide med kjøletyper, går du til **Netto innkjøpspris \> Containeroppsett \> Kjøletyper**. Der kan du vise, legge til og fjerne poster for kjøletypene dine. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Kjøletype | Angi et unikt identifikasjonsnavn/-nummer for kjøletypen. |
| beskrivelse | Angi en beskrivelse av kjøletypen. |
