---
title: Finansdimensjoner
description: Denne artikkelen forklarer de forskjellige typene finansdimensjoner og hvordan de er definert.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ee2d132f0b23ceec2a79ee6b0ee33862d6a0518
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions"></a>Finansdimensjoner

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer de forskjellige typene finansdimensjoner og hvordan de er definert.

Bruk Finansdimensjoner-siden til å opprette finansdimensjoner som du kan bruke som kontosegmenter for kontoplaner. Det finnes to typer finansdimensjoner, egendefinerte dimensjoner og enhetsstøttede dimensjoner. Egendefinerte dimensjoner deles på tvers av juridiske enheter, og verdiene angis og vedlikeholdes av brukeren. Enhetsstøttede dimensjoner er dimensjoner med verdier som er definert andre steder i systemet, for eksempel kunder eller butikker. Noen enhetsstøttede dimensjoner deles på tvers av juridiske enheter, og noen enhetsstøttede dimensjoner er firmaspesifikke. 

Når du har opprettet finansdimensjonene, bruker du Finansdimensjonsverdier-siden til å tilordne flere egenskaper til hver finansdimensjon. 

Selv om du kan bruke finansdimensjoner til å representere juridiske enheter uten å opprette de juridiske enhetene i Microsoft Dynamics 365 for Operations, er ikke finansdimensjoner utviklet for å håndtere de drifts- og forretningsmessige behovene til juridiske enheter. Funksjonen internenhetsregnskap i Microsoft Dynamics 365 for Operations er utviklet for bare å håndtere regnskapsoppføringene som opprettes av hver transaksjon. 

Før du setter opp finansdimensjoner som juridiske enheter, vurderer du forretningsprosessene i følgende områder for å se om dette oppsettet fungerer for din organisasjon:

-   Beholdning
-   Kjøp og salg mellom finansdimensjoner og juridiske enheter
-   Mva-beregning og rapportering
-   Driftsrapportering

Her er noen eksempler på begrensninger:

-   Du kan bare bruke mva-funksjonaliteten med juridiske enheter, ikke med finansdimensjoner.
-   Noen rapporter omfatter ikke finansdimensjoner, så du kan ikke alltid rapportere etter finansdimensjon med mindre disse rapportene endres.

**Egendefinerte dimensjoner** 

For å opprette en brukerdefinert finansdimensjon velger du &lt; Egendefinerte dimensjoner &gt; i feltet Bruk verdier fra. Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier. Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek. Du kan også angi nummertegn (\#) og og-tegn (&) om plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes. Bruk et nummertegn (\#) som plassholder for et tall og et og-tegn (&) som plassholder for en bokstav. 

**Eksempel** 

Hvis du vil begrense dimensjonsverdien til bokstavene CC og tre tall, kan du angi CC-\#\#\# som formatmaske. Dette feltet er bare tilgjengelig når du velger &lt; Egendefinert dimensjon &gt; i feltet Bruk verdier fra. 

**Enhetsstøttede dimensjoner** 

Hvis du vil opprette en enhetsstøttet finansdimensjon, velger du en systemdefinert enhet som basis for finansdimensjonen, i feltet Bruk verdier fra. Finansdimensjonsverdier opprettes fra dette utvalget. Hvis du for eksempel vil opprette dimensjonsverdier for prosjekter, velger du Prosjekter. En dimensjonsverdi opprettes for hvert prosjektnavn. Siden med dimensjonsverdier viser verdiene for enheten, og hvis de er firmaspesifikke, firmaet for verdien. 

**Aktivering av dimensjoner** 

Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes noe sted før den er aktivert. Du kan for eksempel ikke legge til en finansdimensjon i en kontostruktur før finansdimensjonen er aktivert. Hvis du klikker Aktiver, oppdateres alle dimensjoner med statusendringer. 

**Oversettelser** 

På siden Tekstoversettelse kan du angi tekst som skal vises på ulike språk for den valgte finansdimensjonen. På siden Oversetting av hovedkonto kan du angi tekst som skal vises på ulike språk for hovedkontoen. 

**Overstyringer for juridisk enhet** 

Ikke alle dimensjoner er gyldige for alle juridiske enheter, og noen er kanskje bare relevante i en bestemt tidsperiode. I denne situasjonen kan delen Overstyringer for juridisk enhet brukes til å identifisere hvilke firmaer dimensjonen skal suspenderes for, hvem som er eier, og tidsperioden dimensjonen er aktiv.






