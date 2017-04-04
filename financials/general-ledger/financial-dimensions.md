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
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Finansdimensjoner

Denne artikkelen forklarer de forskjellige typene finansdimensjoner og hvordan de er definert.

Bruk Finansdimensjoner-siden til å opprette finansdimensjoner som du kan bruke som kontosegmenter for kontoplaner. Det finnes to typer finansdimensjoner, egendefinerte dimensjoner og enhetsstøttede dimensjoner. Egendefinerte dimensjoner deles på tvers av juridiske enheter, og verdiene angis og vedlikeholdes av brukeren. Enhetsstøttede dimensjoner er dimensjoner med verdier som er definert andre steder i systemet, for eksempel kunder eller butikker. Noen enhetsstøttede dimensjoner deles på tvers av juridiske enheter, og noen enhetsstøttede dimensjoner er firmaspesifikke. 

Når du har opprettet finansdimensjonene, bruker du Finansdimensjonsverdier-siden til å tilordne flere egenskaper til hver finansdimensjon. 

Selv om du kan bruke økonomiske dimensjoner til å representere juridiske enheter uten juridiske enheter i Microsoft Dynamics 365 for operasjoner, finansdimensjoner ikke er utviklet for å håndtere den operative eller bedriften trenger med juridiske enheter. Enhetsinternt regnskap funksjonaliteten i Microsoft Dynamics 365 for operasjoner er utviklet for å håndtere bare regnskap oppføringene som er opprettet ved hver transaksjon. 

Før du setter opp finansdimensjoner som juridiske enheter, vurderer du forretningsprosessene i følgende områder for å se om dette oppsettet fungerer for din organisasjon:

-   Beholdning
-   Kjøp og salg mellom finansdimensjoner og juridiske enheter
-   Mva-beregning og rapportering
-   Driftsrapportering

Her er noen eksempler på begrensninger:

-   Du kan bare bruke mva-funksjonaliteten med juridiske enheter, ikke med finansdimensjoner.
-   Noen rapporter omfatter ikke finansdimensjoner, så du kan ikke alltid rapportere etter finansdimensjon med mindre disse rapportene endres.

**Custom dimensions** 

Hvis du vil opprette en brukerdefinert finansdimensjon, i feltet Bruk verdier fra-feltet, velger du &lt;egendefinert dimension&gt;. Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier. Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek. Du kan også angi nummertegnene (\#) og &-tegn (&) som plassholdere for bokstaver og tall som endres hver gang det opprettes en dimensjonsverdi. Bruk et nummertegn (\#) som en plassholder for et tall og en ampersand (&) som en plassholder for en bokstav. 

**Eksempel** 

Hvis du vil begrense dimensjonsverdien brev kopi og tre tall, angir du CC -\#\#\# som Formatmaske. Dette feltet er bare tilgjengelig når du velger &lt;egendefinert dimension &gt;i Bruk verdier fra-feltet. 

**Enheten støttet dimensjoner** 

Hvis du vil opprette finansdimensjon en enhet som er tatt i Bruk verdier fra-feltet, velger du en systemdefinert enhet å basere finansdimensjonen på. Finansdimensjonsverdier opprettes fra dette utvalget. Hvis du for eksempel vil opprette dimensjonsverdier for prosjekter, velger du Prosjekter. En dimensjonsverdi opprettes for hvert prosjektnavn. Siden med dimensjonsverdier viser verdiene for enheten, og hvis de er firmaspesifikke, firmaet for verdien. 

**Aktivering av dimensjoner** 

Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner. Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes noe sted før den er aktivert. Du kan for eksempel ikke legge til en finansdimensjon i en kontostruktur før finansdimensjonen er aktivert. Hvis du klikker Aktiver, oppdateres alle dimensjoner med statusendringer. 

**Translations** 

Siden tekst oversettelse kan du skrive inn teksten som skal vises på ulike språk for den valgte finansdimensjonen. På siden Oversetting av hovedkonto kan du angi tekst som skal vises på ulike språk for hovedkontoen. 

**Legal entity overrides** 

Ikke alle dimensjonene som er gyldig for alle juridiske enheter og noen kan bare være relevant for en bestemt tidsperiode. I denne situasjonen kan delen Overstyringer for juridisk enhet brukes til å identifisere hvilke firmaer dimensjonen skal suspenderes for, hvem som er eier, og tidsperioden dimensjonen er aktiv.




