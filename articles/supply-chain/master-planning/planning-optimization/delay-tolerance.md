---
title: Forsinkelsestoleranse (negative dager)
description: Dette emnet gir informasjon om forsinkelsestoleranseberegningen og hvordan den påvirker oppretting av planlagte bestillinger i planleggingsoptimaliseringen.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c0bc3d429a1bf13285b385130d419f628330bb3728c6f071cf118edac2a59d87
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778706"
---
# <a name="delay-tolerance-negative-days"></a>Forsinkelsestoleranse (negative dager)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Med funksjonaliteten for forsinkelsestoleranse kan planleggingsoptimalisering vurdere verdien for **Negative dager** som er angitt for dekningsgrupper. Den brukes til å forlenge toleranseperioden for forsinkelsestoleranse som brukes under hovedplanlegging. På denne måten kan du unngå å opprette nye forsyningsordrer hvis eksisterende forsyning vil være i stand til å dekke behovet etter en kort forsinkelse. Formålet med funksjonen er å fastslå om det er fornuftig å opprette en ny forsyningsordre for et gitt behov.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funksjonen i systemet

Hvis du vil gjøre denne funksjonaliteten for forsinkelsestoleranse tilgjengelig i systemet, kan du gå til [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Negative dager for Planleggingsoptimalisering*.

## <a name="delay-tolerance-in-planning-optimization"></a>Forsinkelsestoleranse i planleggingsoptimalisering

Forsinkelsestoleranse representerer antall dager utover leveringstiden som du er villig til å vente før du bestiller ny etterfylling når eksisterende forsyning allerede er planlagt. Forsinkelsestoleranse defineres ved å bruke kalenderdager, ikke virkedager.

Når systemet beregner forsinkelsestoleransen under hovedplanleggingen, vurderer det innstillingen for **Negative dager**. Du kan angi verdien **Negative dager** på **Varedekning**-siden eller **Dekningsgrupper**-siden.

Systemet kobler beregningen av forsinkelsestoleranse til den *tidligste etterfyllingsdatoen*, som er lik dagens dato pluss leveringstiden. Forsinkelsestoleransen beregnes ved å bruke følgende formel, der *maks()* finner den største av to verdier:

*maks(Tidligste etterfyllingsdato, Forfallsdato for etterspørsel)* – *Forfallsdato for etterspørsel* + *Negative dager*

Denne formelen sikrer at hovedplanlegging ikke oppretter nye forsyningsordrer når det finnes nok forsyning i løpet av leveringstiden for produktet.

> [!NOTE]
> Beregningen av forsinkelsestoleranse i Planleggingsoptimalisering bruker alltid beregning av dynamiske negative dager fra innebygd hovedplanlegging. Innstillingen **Bruk dynamiske negative dager** på siden **Hovedplanleggingsparametere** har ingen innvirkning på denne virkemåten.

Hvis den eksisterende forsyningen innebærer en forsinkelse i etterspørselen som er mindre enn eller lik den beregnede forsinkelsestoleransen, utligner Planleggingsoptimalisering eksisterende forsyning med behovet. I noen tilfeller er det bedre å forsinke behovet enn å ende opp med for stor forsyning.

Følgende underdeler er eksempler som viser hvordan forsinkelsestoleranse påvirker oppretting av planlagte ordrer i Planleggingsoptimalisering.

### <a name="example-1"></a>Eksempel 1

Et produkt har følgende konfigurasjon:

- **Leveringstid:** *10*
- **Negative dager:** *2*

Følgende tilbud og etterspørsel finnes for produktet:

- **Behov for i dag:** En salgsordre for et antall på 10
- **Forsyning om 12 dager:** En bestilling av et antall på 10

Eksisterende forsyning kan dekke behovet innen 12 dager, og denne perioden er lik forsinkelsestoleransen. Når hovedplanleggingen kjøres, blir det derfor ikke opprettet noen planlagte bestillinger.

### <a name="example-2"></a>Eksempel 2

Et produkt har følgende konfigurasjon:

- **Leveringstid:** *10*
- **Negative dager:** *0*

Følgende tilbud og etterspørsel finnes for produktet:

- **Behov for i dag:** En salgsordre for et antall på 10
- **Forsyning om 12 dager:** En bestilling av et antall på 10

Eksisterende forsyning kan dekke behovet bare etter 12 dager. Forsinkelsestoleransen er imidlertid 10 dager. Når hovedplanleggingen kjøres, vil det derfor opprettes en planlagt bestilling på et antall på 10.

### <a name="example-3"></a>Eksempel 3

Et produkt har følgende konfigurasjon:

- **Leveringstid:** *10*
- **Negative dager:** *2*

Følgende tilbud og etterspørsel finnes for produktet:

- **Behov om 11 dager:** En salgsordre for et antall på 10
- **Forsyning om 14 dager:** En bestilling av et antall på 10

Eksisterende forsyning kan dekke behovet bare etter tre dager. Forsinkelsestoleransen er imidlertid to dager. (I dette tilfellet inkluderer forsinkelsestoleransen bare de to negative dagene. Behovsdatoen er ikke inkludert, fordi den er etter produktets leveringstid.) Når hovedplanleggingen kjøres, vil det derfor opprettes en planlagt bestilling på et antall på 10.
