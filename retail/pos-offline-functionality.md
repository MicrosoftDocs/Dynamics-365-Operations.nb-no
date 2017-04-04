---
title: Frakoblet funksjonalitet for salgssted
description: Denne artikkelen inneholder informasjon om frakoblet modus for moderne salgssted for detaljhandel, der salgsstedsenheter automatisk bytter fra kanaldatabasen til den frakoblede databasen hvis detaljhandelsserveren er utilgjengelig. Denne artikkelen inneholder generell oppsettinformasjon for frakoblet modus og forklarer datasynkroniseringen mellom den frakoblede databasen og kanaldatabasen.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>Frakoblet funksjonalitet for salgssted

Denne artikkelen inneholder informasjon om frakoblet modus for moderne salgssted for detaljhandel, der salgsstedsenheter automatisk bytter fra kanaldatabasen til den frakoblede databasen hvis detaljhandelsserveren er utilgjengelig. Denne artikkelen inneholder generell oppsettinformasjon for frakoblet modus og forklarer datasynkroniseringen mellom den frakoblede databasen og kanaldatabasen.

<a name="overview"></a>Oversikt
--------

I moderne Retail POS, et punkt av salg (POS) enheten går inn i frakoblet modus når retail-serveren ikke er tilgjengelig. Derfor, hvis tilkoblingen til retail-serveren brytes, moderne Priskontroll bytter automatisk til den frakoblede databasen. Hvis en dataforespørsel under en salgstransaksjon ikke lykkes innen tidsavbruddsintervallet som er konfigurert i den frakoblede profilen, bytter Retail Modern POS automatisk til den frakoblede databasen og fortsetter salgstransaksjonen. Mens salgsstedsenheten er i frakoblet modus, prøver Retail Modern POS å koble til detaljhandelsserveren etter intervallet for nytt tilkoblingsforsøk som er konfigurert i den frakoblede profilen. Dette tilkoblingsforsøket skjer bare i begynnelsen av en transaksjon.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>Fastsette tilkoblingsmodusen for Retail Modern POS

Statushodet i Retail Modern POS angir den gjeldende tilkoblingsstatusen, og **Tilkoblingsstatus**-vinduet viser statusen for det siste forsøket på å synkronisere med den frakoblede databasen. [![Connection status](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Opprette en knapp for å bytte manuelt mellom tilkoblet og frakoblet modus

Du kan legge til en knapp i Retail Modern POS for å bytte manuelt mellom tilkoblet og frakoblet modus. Opprette en knapp for salgsstedsoperasjon **917 – Databasetilkoblingsstatus**. Navnet på denne knappen er **Koble fra** når Retail Modern POS er koblet til detaljhandelsserveren, og **Koble til** når den er koblet fra. Du kan bruke denne knappen til å vise tilkoblingen, og til å koble fra eller til detaljhandelsserveren. [![Koble fra-knappen i moderne Priskontroll](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Konfigurasjon
Hvis du vil aktivere frakoblet støtte for en POS-enhet (register), kan du angi den **støtter frakoblet** å **Ja** på den **registrere** siden. En ny kanal database enhet er opprettet og lagt til butikkens kanalen data-gruppen. Kjør deretter alle de nødvendige distribusjonstidsplanene for å generere datapakkene for den frakoblede databasen. Deretter Installer den frakoblede versjonen av moderne Varelisten. Installasjonen oppretter den frakoblede databasen. Installere Microsoft SQL Server 2014 Express i tillegg, hvis det er nødvendig. Frakoblet datasynkronisering starter etter første pålogging i Retail Modern POS.

## <a name="data-synchronization"></a>Datasynkronisering
Detaljhandel Planlegger brukes til å sende hoveddata til den frakoblede databasen. Når en leveringsplan kjøres, sendes dataendringer som standard til både kanaldatabasen og den frakoblede databasen. Retail Modern POS omfatter Async-synkroniseringsbiblioteket, som laster ned alle tilgjengelige datapakker og setter dem inn i den frakoblede databasen. Hvis transaksjoner opprettes i frakoblet modus, laster Retail Modern POS dem opp til detaljhandelsserveren, slik at de kan settes inn i kanaldatabasen. Frakoblet datasynkronisering kan bare skje hvis Retail Modern POS kjører. [![Offline synchronization](./media/offline-sync-1024x521.png)](./media/offline-sync.png)


