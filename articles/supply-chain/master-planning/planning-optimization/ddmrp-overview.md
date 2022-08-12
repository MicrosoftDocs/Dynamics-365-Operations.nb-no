---
title: Oversikt over DDMRP (etterspørselsdrevet planlegging av materialkrav)
description: Denne artikkelen gir informasjon om DDMRP (etterspørselsdrevet planlegging av materialkrav), en planleggingsmetode som er basert på utkobling av tilbud og etterspørsel.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186751"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Oversikt over DDMRP (etterspørselsdrevet planlegging av materialkrav)

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Firmaer har i mange år brukt planlegging av materialkrav (MRP) som et system for beregning av materialene og komponentene som kreves for å produsere et produkt. Forsyningskjedene er imidlertid nå endret. Deler har lengre leveringstider fordi de i økende grad blir hentet fra utlandet. Derfor er det mange firmaer som har rapportert om tomme lagre eller overfylte lagre, fordi de ikke vet hvor mye beholdning de skal ha på lager. Det er også større markedssvingninger (noen ganger unøyaktig prognose), og kunder etterspør produkter på kort leveringstid. Derfor er det forsyningskjedemangler over hele verden. I tillegg medfører MRP-verktøy ofte at planleggere har tusenvis av handlinger å utføre. Derfor er det vanskelig å vite hva du skal fokusere på. Ofte er løsningen på mange av disse spørsmålene å bytte til DDMRP (etterspørselsdrevet planlegging av materialkrav).

DDMRP er en planleggingsmetode som er basert på utkobling av tilbud og etterspørsel. Denne utkoblingen oppnås ved å definere varer som har utkoblingspunkter. For disse varene vedlikeholdes buffere for å sikre at riktig mengde beholdning beholdes. Utkoblingen av tilbud og etterspørsel forhindrer "piskesnerteffekten", fordi avviket ikke passerer gjennom kjeden. (*Piskesnerteffekten* refererer til hvor små variasjoner i etterspørselen på detaljhandelsnivået som kan forårsake gradvis større variasjoner i etterspørselen på grossist-, distributør-, produsent- og råvareleverandørnivået.) Hver buffer er ment for å dekke gjennomsnittlig bruk av en del, og kan også justeres for å dekke etterspørselstopper.

DDMRP har vist seg å være en verdifull planleggingsmetode for variable miljøer der kundetoleransetider er kortere enn kumulative leveringstider.

## <a name="the-five-components-of-ddmrp"></a>De fem komponentene i DDMRP

DDMRP har fem sekvensielle komponenter (trinn). De første tre komponentene definerer essensielt sett den innledende og utviklende konfigurasjonen av en etterspørselsdrevet modell for planlegging av materialkrav. De to siste komponentene definerer daglige operasjoner for metoden.

1. **[Strategisk lagerplassering](ddmrp-inventory-positioning.md)** – Identifiser utkoblingspunkter i forsyningskjedenettverket. Utkoblingspunkter er bestemte punkter i forsyningskjeden der du plasserer en beholdningsbuffer som du vil overvåke og etterfylle.
2. **[Bufferprofiler og -nivåer](ddmrp-buffer-profile-and-levels.md)** – For hvert utkoblingspunkt identifiserer du bufferstørrelsene (minimumsantall, maksimumsantall og gjenbestillingspunkt) og gjenbestillingsantallet.
3. **[Dynamiske bufferjusteringer](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Juster buffernivåer, basert på ulike driftsparametere eller planlagte fremtidige hendelser.
4. **[Etterspørselsdrevet planlegging](ddmrp-planning.md)** – Generer forsyningsordrer etter behov. Disse forsyningsordrene omfatter produksjonsordrer, bestillinger og lageroverføringsordrer.
5. **[Svært samarbeidsbasert og synlig kjøring](ddmrp-visual-and-collaborative-execution.md)** – Kjør forsyningsordrene ved hjelp av visualisering.

DDMRP brukes vanligvis av produsenter som har en stykkliste med flere nivåer. Det kan imidlertid også brukes på distribusjons- og detaljhandelsnettverk.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP i Dynamics 365 Supply Chain Management

DDMRP er inkludert med Microsoft Dynamics 365 Supply Chain Management og krever ingen ekstra lisensgebyrer. I Supply Chain Management er DDMRP-funksjonaliteten lagt til i den eksisterende **Hovedplanlegging**-modulen. Det krever imidlertid at du bruker tillegget for planleggingsoptimalisering. 

DDMRP er integrert med de eksisterende planleggingsoppsettene i Supply Chain Management og brukes sammen med disse oppsettene for å komme frem til riktig planleggingskonfigurasjon for bedriften din. Det styres av en ny dekningskode som er helt forskjellig fra periode, min/maks, krav og så videre. Det er ikke en ny modul, og den erstatter ikke eksisterende planleggingsfunksjonalitet. Den gir deg imidlertid mer funksjonalitet å bruke.
