---
title: Definere standardbeskrivelser for automatisk postering
description: Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen. Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f5fc73f636a5cac25c259ce2cbae5c5407dca9b7
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117367"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Definere standardbeskrivelser for automatisk postering

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen. Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.

> [!NOTE]
> For enkelte transaksjonstyper i noen land eller områder kan du også inkludere tekst fra felter i Microsoft Dynamics AX-databasen som er relatert til disse transaksjonstypene. Hvis du vil ha en liste over transaksjonstypene og landene og regionene, se [Valgfritt: Legge til annen tekst i standardbeskrivelser](#optional-add-other-text-to-default-descriptions) senere i dette emnet.

## <a name="set-up-default-descriptions"></a>Definere standardbeskrivelser

1. Gå til **Organisasjonsstyring** \> **Oppsett** \> **Standardbeskrivelser**.
2. Velg **Ny** i handlingsruten.
3. Velg transaksjonstypen du vil opprette en standardbeskrivelse for i feltet **Beskrivelse**.
4. I **Språk**-feltet velger du språket denne beskrivelsen gjelder for.
5. I **Tekst**-feltet angir du standardbeskrivelsen. Du kan skrive inn tekst i feltet, eller du kan bruke én eller flere av de følgende fritekstvariablene:

    - **%1** – Legg til transaksjonsdatoen.
    - **%2** – Legg til en identifikator som tilsvarer dokumenttypen som posteres til økonomimodulen. Fo transaksjonstyper som er relatert til fakturaer for eksempel, legger variabelen **%2** til fakturanummeret.
    - **%3** – Legg til en identifikator som er relatert til dokumenttypen som posteres til økonomimodulen. For transaksjonstyper som er relatert til fakturaer for eksempel, legger variabelen **%3** til kundens kontonummer.

## <a name="optional-add-other-text-to-default-descriptions"></a>Valgfritt: Legge til annen tekst i standardbeskrivelser

For enkelte transaksjonstyper i noen land eller områder, kan tekst inkluderes i standardbeskrivelsene som kommer fra felt i dataene som er relatert til disse transaksjonstypene. Følgende liste viser transaksjonstyper og land/områder som dette alternativet er tilgjengelig for.

**Transaksjonstyper**

Du kan legge til annen tekst i standardbeskrivelser for transaksjonstyper som er knyttet til følgende dokumenttyper:

- Kundefakturaer
- Kundekredittnotaer
- Kundekontantbetalinger
- Leverandørbetalinger
- Salgsordre
- Bestillinger
- Lagerjournaler
- Hovedplanlegging (MPS)
- Anleggsmidler

**Land og områder**

Dette alternativet er tilgjengelig for følgende land og regioner:

- Brasil
- Kina
- Tsjekkia
- Øst-Europa
- Ungarn
- India
- Japan
- Litauen
- Latvia
- Polen
- Russland

### <a name="add-text-to-default-descriptions"></a>Legge til tekst i standardbeskrivelser

Når du har fullført trinnene i [Definere standardbeskrivelser](#set-up-default-descriptions) tidligere i dette emnet, følger du denne fremgangsmåten for å legge til annen tekst i standardbeskrivelsene.

1. Velg **Legg til** på hurtigfanen **Parametere**.
2. Velg databasetabellen du vil legge til parameterdata i beskrivelsen fra, i **Referansetabell**-feltet.
3. Velg feltet du vil legge til parameterdata i beskrivelsen fra, i **Referansefelt**-feltet.
4. Gjenta trinn 1 til og med 3 hvis du vil legge til flere parametere.
