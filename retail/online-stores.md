---
title: Oversikt over nettbutikk
description: Denne artikkelen inneholder informasjon om nettbutikker for detaljhandel og hvordan du definerer dem i Microsoft Dynamics 365 for Operations.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: c41343c73d01235deee30fed4ff899cb8a6f50a5
ms.contentlocale: nb-no
ms.lasthandoff: 04/26/2017


---

# <a name="online-store-overview"></a>Oversikt over nettbutikk

[!include[banner](includes/banner.md)]


Denne artikkelen inneholder informasjon om nettbutikker for detaljhandel og hvordan du definerer dem i Microsoft Dynamics 365 for Operations.

Detaljhandel og handel i Dynamics 365 for Operations støtter flere kanaler for detaljhandel. Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker). Med en nettbutikk får en forhandler en tilstedeværelse på nettet, slik at kundene får mulighet til å kjøpe produkter i nettbutikken i tillegg til den vanlige butikken. Hvis kunder kjøper produkter fra nettbutikken, kan disse produktene sendes til dem, eller de kan hente produktene i den lokale detaljhandelsbutikken. Du oppretter en nettbutikk i Dynamics 365 for Operations-klienten. Denne nettbutikken blir deretter publisert til en nettbutikk for tredjeparter som er integrert i Dynamics 365 for Operations. Tredjeparts nettbutikken fungerer som butikkfasaden (UI) for nettbutikken, og gir deg et valg av kundebehandlingssystem (CMS) og funksjoner for brukergrensesnitt. Det finnes flere integreringer av denne typen for Dynamics 365 for Operations. Egenskapene som du definerer for nettbutikken, styrer virkemåten til nettbutikken. La oss si at du definerer navigasjonskategorihierarkiet i Dynamics 365 for Operations og tilordner det til butikken. Når du publiserer nettbutikken på tredjeparts nettbutikken, vises navigasjonskategorihierarkiet i nettversjonen av butikken. Kunder bruker deretter navigasjonskategorihierarkiet til å søke i nettbutikken og søke etter produkter. Hvis du vil opprette en nettbutikk, må du konfigurere komponentene som gjør det mulig å behandle transaksjonene for butikken. Du må for eksempel legge til sortimenter, bruke attributter og definere betalingsmåter og leveringsmetoder. Du kan også definere priser, kampanjer, rabatter, forretningsavtaler og leveringsbetingelser som er spesifikke for nettbutikken. Når du har publisert nettbutikken på tredjeparts nettbutikken, kan du opprette detaljhandelsproduktkataloger for nettbutikken. Produktene i katalogen blir produktoversikter i nettbutikken. Når en handlende kjøper produkter fra nettbutikken, blir den tilgjengelige beholdningen oppdatert og synkronisert i klienten. I tillegg genereres salgsordrer for kjøpene som sendes til klienten for å bli oppfylt og behandlet.

## <a name="set-up-an-online-store"></a>Definere en nettbutikk
Du må fullføre følgende oppgaver hvis du vil definere en nettbutikk.

1.  Opprett nettbutikken.
2.  Legg til nettbutikken i aktuelle organisasjonshierarkier.
3.  Legg til sortimenter som inneholder produktene som er tilgjengelige i nettbutikken.
4.  Tilordne eller opprett prisgrupper for nettbutikken.
5.  Definer leveringsmåter som er tilgjengelige for nettbutikken.
6.  Tilordne betalingsmåtene som er godtatt av nettbutikken.
7.  Hvis du lar kunder bestille produkter på Internett og deretter hente dem i en lokal butikk, kan du tilordne butikklokatorgrupper til nettbutikken.
8.  Tilordne attributter for kanaler, produkter og salgsordrer til nettbutikken. Kanalattributter gjelder for hele nettbutikken, produktattributter gjelder for produktene som tilbys i nettbutikken, og salgsordreattributter gjelder for salgsordrene som genereres fra nettbutikken.
9.  Tilordne attributter for å angi egenskaper som bestemmer hvordan attributtene fungerer i nettbutikken. Du kan for eksempel angi attributter som skal være obligatoriske eller søkbare.
10. Publiser nettbutikken for å generere butikkstrukturen på ditt valg av tredjeparts nettbutikk. **Viktig!** Før du publiserer nettbutikken, må du definere en leveringslokasjon for den.

## <a name="retail-channel-navigation-hierarchies"></a>Navigasjonshierarkier for detaljhandelskanal
Før du oppretter en nettbutikk, må du definere navigasjonshierarkiet for detaljhandelskanal du vil bruke for den. Navigasjonshierarkiet for detaljhandelskanal representerer kategorihierarkiet som vises i nettbutikken etter at lageret er publisert. Når du publiserer detaljhandelsproduktkataloger i nettbutikken, tilordnes produktene i katalogen til kategoriene i navigasjonshierarkiet for detaljhandelskanalen. Hierarkiet brukes deretter av kunder til å navigere i nettbutikken.

## <a name="organization-hierarchies"></a>Organisasjonshierarkier
Organisasjonshierarkier brukes til å strukturere detaljhandelskanaler. Organisasjonshierarkier representerer relasjonene mellom organisasjonene som utgjør virksomheten. Når du definerer nettbutikker, kan du legge dem til i et organisasjonshierarki. Butikken lagrer og deler dataene som brukes for sortimenter, etterfylling og rapportering. Når du oppretter et organisasjonshierarki, må du tilordne et formål til det. Formålet angir hvordan hierarkiet brukes i forretningsstrukturen. Du kan opprette ett organisasjonshierarki for butikkprosessene og bruke dette hierarkiet til sortimenter, etterfylling og rapportering. Alternativt kan du opprette et eget organisasjonshierarki for hvert formål. Du kan også opprette flere hierarkier som har samme formål, og tilordne en egen kanal til hvert av dem. Hvis du har tenkt å publisere detaljhandelsproduktkataloger i nettbutikken, bør du minst legge til nettbutikken i et organisasjonshierarki for sortimenter. Produktene i en katalog velges fra sortimentene som er tilordnet til nettbutikken. Når katalogen publiseres, sammenligner publiseringsprosessen ikrafttredelsesdatoene for sortimentet som er tilordnet til nettbutikken, med produktene som er inkludert i katalogen, for å finne ut hvilke produkter som skal gjøres tilgjengelige i nettbutikken.




