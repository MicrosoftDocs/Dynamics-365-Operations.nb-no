---
title: Definere standardbeskrivelser for automatisk postering
description: Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen. Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 772c754e9980e693daf7542de273cbe278ca7038
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722443"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Definere standardbeskrivelser for automatisk postering

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du definerer standardtekst som brukes til å beskrive regnskapsoppføringer som posteres automatisk til økonomimodulen. Du kan definere standard beskrivelsestekst ved å bruke frihåndstekst eller velge faste variabler.

> [!NOTE]
> For enkelte transaksjonstyper i noen land eller områder kan du også inkludere tekst fra felter som er relatert til disse transaksjonstypene. Hvis du vil ha en liste over transaksjonstypene og landene og regionene, se [Valgfritt: Legge til annen tekst i standardbeskrivelser](#optional-add-other-text-to-default-descriptions) senere i dette emnet.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
