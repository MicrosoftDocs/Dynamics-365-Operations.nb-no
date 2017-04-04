---
title: Oppgrader avskrivning bok-oversikt
description: "I tidligere versjoner var det to vurdering konsepter for anleggsmidler - verdimodeller og avskrivningstablåer. I 1611-versjonen av Microsoft Dynamics 365 for Operations er verdimodellfunksjonaliteten og funksjonaliteten for avskrivningstablå slått sammen til ett enkelt konsept som kalles et tablå. Dette emnet inneholder noen ting å ta hensyn til for oppgraderingen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Oppgrader avskrivning bok-oversikt

I tidligere versjoner var det to vurdering konsepter for anleggsmidler - verdimodeller og avskrivningstablåer. I 1611-versjonen av Microsoft Dynamics 365 for Operations er verdimodellfunksjonaliteten og funksjonaliteten for avskrivningstablå slått sammen til ett enkelt konsept som kalles et tablå. Dette emnet inneholder noen ting å ta hensyn til for oppgraderingen. 

Oppgraderingsprosessen flytter eksisterende oppsett og alle eksisterende transaksjoner til den nye tablåstrukturen. Verdimodeller forblir slik de er for øyeblikket, som et tablå som posterer til økonomimodulen. Avskrivningstablåer flyttes til et tablå bok med alternativet **Poster til økonomimodul** satt til **Ingen**. Journalnavn for avskrivningstablå vil bli flyttet til et journalnavn for økonomimodulen med posteringslaget som er satt til **ingen**. Avskrivningstablåtransaksjoner vil bli flyttet til anleggsmiddeltransaksjoner. 

Før du kjører dataoppgraderingen, må du forstå de to alternativene som er tilgjengelige for oppgradering av journallinjer for avskrivningstablå til transaksjonsbilag, og nummerserien som brukes for bilagsserien. 

Alternativ 1: **Systemdefinert nummerserie** – Dette er standardalternativet for å optimalisere ytelsen til dataoppgraderingen. Oppgraderingen kan ikke bruke rammeverket for nummerserie, men vil i stedet tildele bilag med en settbasert tilnærmingsmåte. Ny nummerserien skal opprettes etter oppgraderingen, med den **neste angitt** basert på riktig måte på de oppgraderte transaksjonene. Som standard blir nummerseriene som brukes i FADBUpgr\#\#\#\#\#\#\#\#\# format. Det finnes noen parametere for å justere formatet når du bruker denne fremgangsmåten:

-   **Nummerseriekode** -koden som identifiserer nummerserien. Denne nummerseriekode kan ikke eksistere siden opprettes etter oppgraderingen.
    -   Konstantnavn: **NumberSequenceDefaultCode**
    -   Standardverdi: "FADBUpgr"
-   **Prefiks** – Konstantsstrengverdien som skal brukes som et prefiks for bilagsnumrene.
    -   Konstantnavn: **NumberSequenceDefaultParameterPrefix**
    -   Standardverdi: "FADBUpgr"
-   **Alfanumerisk lengde** – Lengden på det alfanumeriske segmentet i nummerserien.
    -   Konstant navn: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Standardverdi: 9
-   **Startnummer** – Det første tallet som skal brukes i nummerserien.
    -   Konstant navn: ** NumberSequenceDefaultParameterStartNumber **
    -   Standardverdi: 1

Alternativ 2: **eksisterende brukerdefinert nummerserie** -dette alternativet lar deg definere nummerserien som skal brukes for oppgraderingen. Vurder å bruke dette alternativet hvis du har behov for avansert nummerseriekonfigurasjon. Hvis du vil bruke en nummerserie, må du endre klassen upgrade ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans med følgende informasjon:

-   **Nummerseriekode** – Koden til nummerserien.
    -   Konstant navn: ** NumberSequenceExistingCode **
    -   Standardverdi: Ingen standard. Dette må oppdateres til nummerseriekoden.
-   **Felles nummerserie** – En boolsk verdi for å identifisere omfanget for nummerserien. Bruk "true" for nummerserier som deles på tvers av alle firmaer, og "false" for et firmaomfang. Når du bruker "false", må nummerserien med det angitte navnet finnes i hvert firma som inneholder avskrivningstablåtransaksjoner. Det finnes delte nummerserier i hver partisjon som inneholder avskrivningstablåtransaksjoner.
    -   Konstant navn: ** NumberSequenceExistingIsShared **
    -   Standardverdi: true

Parameterne er plassert i begynnelsen av ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans-klassen. 

*Angi en foretrekke tilnærming av bilag tildeling*<ph id="t1">
</ph>*/ / SANN hvis du vil bruke en eksisterende nummerseriekode*<ph id="t2">
</ph>*/ / USANN, hvis du har tenkt å bruke systemet nummersekvensen (standard)* const boolsk NumberSequenceUseExistingCode = false;  

*Hvis bruker sekvens tilnærming systemdefinerte tall, angir du parameterne for nummerserien. *<ph id="t3">
</ph>*/ / Vil bli opprettet en ny nummerserie med disse parameterne.* Str Const NumberSequenceDefaultCode = FADBUpgr; str Const NumberSequenceDefaultParameterPrefix = FADBUpgr; int Const NumberSequenceDefaultParameterAlpanumericLength = 9; int Const NumberSequenceDefaultParameterStartNumber = 1;   

*Hvis bruker eksisterende tall sekvens-metoden, angir du eksisterende nummerseriekode. *<ph id="t4">
</ph>*/ / Bilagstilordning går rad for rad for eksisterende nummerserier.* Str Const NumberSequenceExistingCode = ''; */ / Angi omfanget av eksisterende nummerseriekoden*<ph id="t5">
</ph>*/ / SANN hvis den angitte nummerserien er delt*<ph id="t6">
</ph>*/ / USANN hvis den angitte nummerserien er per firma*<ph id="t7">
</ph>*/ / standard systemdefinerte nummerserien som skal brukes hvis en nummerseriekode med det angitte omfanget ikke finnes.* const boolean NumberSequenceExistingIsShared = true; 

Bygg på nytt prosjektet som inneholder klassen når konstantene har blitt endret. 

Når du bruker systemgenerert nummer rekkefølge tilnærmingen (alternativ 1), vil oppgraderingen bruke set-basert behandling til å tildele bilagsnumre som er angitt i parameterne oppgraderingsskriptet. Det vil også opprette en ny nummerserie med angitte parametere etter tildelingen. 

Når du bruker fremgangsmåten for brukerdefinert nummerserie (alternativ 2), sjekker dataoppgraderingen om nummerserien med det angitte omfanget finnes i databasen for hver partisjon og firma med avskrivningstablåtransaksjoner. Hvis den finnes, bruker oppgraderingen rad for rad-behandling til å tildele bilagsnumre som angitt av nummerserien ved hjelp av nummerserierammeverket. Hvis nummerserien ikke eksisterer med det angitte omfanget, oppgraderingen vil bruke standard systemdefinerte tall sekvens tilnærmingen til å tildele bilagsnumre til og oppretter en ny nummerserie med parametere angitt som standard etter tildelingen.

For begge fremgangsmåtene vil skriptet for dataoppgradering også bruke nummerserien for **Bilagsserie**-feltet på de nye journalnavnene for økonomimodulen som er opprettet for de tidligere journalnavnene for avskrivningstablå.


