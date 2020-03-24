---
title: Definere en kanal for nettbutikk
description: Denne artikkelen inneholder informasjon om nettbutikker og hvordan du definerer dem i Dynamics 365 Commerce.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096900"
---
# <a name="set-up-an-online-store-channel"></a>Definere en kanal for nettbutikk

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder informasjon om nettbutikker og hvordan du definerer dem i Dynamics 365 Commerce.

Commerce støtter flere kanaler for detaljhandel. Disse kanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker). Med en nettbutikk får en forhandler en tilstedeværelse på nettet, slik at kundene får mulighet til å kjøpe produkter i nettbutikken i tillegg til den vanlige butikken. Hvis kunder kjøper produkter fra nettbutikken, kan disse produktene sendes til dem, eller de kan hente produktene i en lokal butikk. 

Du oppretter en elektronisk butikk i Commerce-klienten. Denne nettbutikken blir deretter publisert til en nettbutikk for tredjeparter som er integrert i Commerce. Tredjeparts nettbutikken fungerer som butikkfasaden (UI) for nettbutikken, og gir deg et valg av kundebehandlingssystem (CMS) og funksjoner for brukergrensesnitt. Det finnes flere integreringer av denne typen. 

Egenskapene som du definerer for nettbutikken, styrer virkemåten til nettbutikken. La oss si at du definerer navigasjonskategorihierarkiet og tilordner det til nettbutikken. Når du publiserer nettbutikken på tredjeparts nettbutikken, vises navigasjonskategorihierarkiet i nettversjonen av butikken. Kunder bruker deretter navigasjonskategorihierarkiet til å søke i nettbutikken og søke etter produkter. 

Hvis du vil opprette en nettbutikk, må du konfigurere komponentene som gjør det mulig å behandle transaksjonene for butikken. Du må for eksempel legge til sortimenter, bruke attributter og definere betalingsmåter og leveringsmetoder. Du kan også definere priser, kampanjer, rabatter, forretningsavtaler og leveringsbetingelser som er spesifikke for nettbutikken. 

Når du har publisert nettbutikken på den tredjeparts nettbutikken, kan du opprette produktkataloger for nettbutikken. Produktene i katalogen blir produktoversikter i nettbutikken. Når en handlende kjøper produkter fra nettbutikken, blir den tilgjengelige beholdningen oppdatert og synkronisert i klienten. I tillegg genereres salgsordrer for kjøpene som sendes til klienten for å bli oppfylt og behandlet.

## <a name="set-up-an-online-store"></a>Definere en nettbutikk

Du må fullføre følgende oppgaver hvis du vil definere en nettbutikk.

1. Opprett nettbutikken.
2. Legg til nettbutikken i aktuelle organisasjonshierarkier.
3. Legg til sortimenter som inneholder produktene som er tilgjengelige i nettbutikken.
4. Tilordne eller opprett prisgrupper for nettbutikken.
5. Definer leveringsmåter som er tilgjengelige for nettbutikken.
6. Tilordne betalingsmåtene som er godtatt av nettbutikken.
7. Hvis du lar kunder bestille produkter på Internett og deretter hente dem i en lokal butikk, kan du tilordne butikklokatorgrupper til nettbutikken.
8. Tilordne attributter for kanaler, produkter og salgsordrer til nettbutikken. Kanalattributter gjelder for hele nettbutikken, produktattributter gjelder for produktene som tilbys i nettbutikken, og salgsordreattributter gjelder for salgsordrene som genereres fra nettbutikken.
9. Tilordne attributter for å angi egenskaper som bestemmer hvordan attributtene fungerer i nettbutikken. Du kan for eksempel angi attributter som skal være obligatoriske eller søkbare.
10. Publiser nettbutikken for å generere butikkstrukturen på ditt valg av tredjeparts nettbutikk.

    > [!IMPORTANT]
    > Før du publiserer nettbutikken, må du definere en leveringslokasjon for den.

## <a name="commerce-channel-navigation-hierarchies"></a>Navigasjonshierarkier for handelskanal

Før du oppretter en nettbutikk, må du definere navigasjonshierarkiet for handelskanalen du vil bruke for den. Navigasjonshierarkiet for handelskanalen representerer kategorihierarkiet som vises i nettbutikken etter at lageret er publisert. Når du publiserer produktkataloger i nettbutikken, tilordnes produktene i katalogen til kategoriene i navigasjonshierarkiet for kanalen. Hierarkiet brukes deretter av kunder til å navigere i nettbutikken.

## <a name="organization-hierarchies"></a>Organisasjonshierarkier

Organisasjonshierarkier brukes til å strukturere handelskanaler og til å representere relasjonene mellom organisasjonene som utgjør virksomheten. Når du definerer nettbutikker, kan du legge dem til i et organisasjonshierarki. Butikken lagrer og deler dataene som brukes for sortimenter, etterfylling og rapportering. 

Når du oppretter et organisasjonshierarki, må du tilordne et formål til det. Formålet angir hvordan hierarkiet brukes i forretningsstrukturen. Du kan opprette ett organisasjonshierarki for butikkprosessene og bruke dette hierarkiet til sortimenter, etterfylling og rapportering. 

Alternativt kan du opprette et eget organisasjonshierarki for hvert formål. Du kan også opprette flere hierarkier som har samme formål, og tilordne en egen kanal til hvert av dem. Hvis du har tenkt å publisere produktkataloger i nettbutikken, bør du minst legge til nettbutikken i et organisasjonshierarki for sortimenter. Produktene i en katalog velges fra sortimentene som er tilordnet til nettbutikken. Når katalogen publiseres, sammenligner publiseringsprosessen ikrafttredelsesdatoene for sortimentet som er tilordnet til nettbutikken, med produktene som er inkludert i katalogen, for å finne ut hvilke produkter som skal gjøres tilgjengelige i nettbutikken.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp URL-adresser for omadressering samtidig](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
