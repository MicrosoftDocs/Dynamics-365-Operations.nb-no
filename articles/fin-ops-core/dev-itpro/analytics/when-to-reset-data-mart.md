---
title: Når skal et data mart tilbakestilles
description: Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988998"
---
# <a name="when-to-reset-a-data-mart"></a>Når skal et data mart tilbakestilles

Det kan være tidkrevende å tilbakestille et data mart. Denne handlingen er kanskje ikke løsningen som trengs, avhengig av forholdene. Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Når må jeg tilbakestille et data mart?
Vurder følgende spørsmål før du tilbakestiller et data mart. Hvis du svarer ja på ett eller flere spørsmål, kan det bety at organisasjonen kan dra nytte av å tilbakestille data mart.

- Ble applikasjonsdatabasen gjenopprettet?
- Hvis du har åpnet en støttehendelse og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Når passer det ikke å tilbakestille et data mart?
Det finnes visse omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart. Disse omfatter følgende. 

- Du har ytelsesproblemer som er knyttet til en datasynkronisering. 
- Hvis du har et gjentakende tilbakestillingsmønster av en av følgende årsaker: 
  - **Manglende data** 
  - **Fastlåst integreringstilstand** 
  - **Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart. Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.
 
## <a name="what-is-a-data-mart-reset"></a>Hva er en tilbakestilling av data mart?
- En tilbakestilling starter bare når eksisterende oppgaver er fullført. Dette sikrer at gamle data ikke settes inn. På dette tidspunktet kan du for eksempel få meldingen «Tilbakestillingen av data mart kan ikke behandles på grunn av en aktiv oppgave. Prøv på nytt senere.»
- Tilbakestillingen deaktiverer integreringsoppgavene og sletter alle data mart-data. Integreringen aktiveres på nytt.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Hvis jeg tilbakestiller data mart, vil jeg miste rapporter som jeg allerede har utformet? 
Nei, rapportene lagres i SQL-tabeller som ikke påvirkes av en tilbakestilling av data mart. Hvis du er opptatt av å miste rapporter du har utformet, kan du sikkerhetskopiere utformingene du ikke vil miste. Hvis du vil sikkerhetskopiere dem, åpner du Rapportutforming og går til **Firma > Firmaer > Byggesteiner > Eksporter**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Er det nødvendig for alle brukere å avslutte systemet for å tilbakestille data mart?
Nei, brukere kan fortsette å arbeide i systemet under tilbakestillingen av data mart. De vil imidlertid ikke få tilgang til rapporter som ble opprettet med finansrapportering før tilbakestillingen er fullført. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
