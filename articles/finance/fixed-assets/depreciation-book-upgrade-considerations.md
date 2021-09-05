---
title: Oversikt over oppgradering for avskrivningstablå
description: I tidligere versjoner var det to vurderingskonsepter for anleggsmidler, verdimodeller og avskrivningstablåer.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1d14154cd2e9bd18a886ba490891a02afeb0b05
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344720"
---
# <a name="depreciation-book-upgrade-overview"></a>Oversikt over oppgradering av avskrivningstablå

[!include [banner](../includes/banner.md)]

I tidligere versjoner var det to vurderingskonsepter for anleggsmidler: verdimodeller og avskrivningstablåer. I Microsoft Dynamics 365 for Operations (1611) er verdimodellfunksjonaliteten og funksjonaliteten for avskrivningstablå slått sammen til ett enkelt konsept som kalles et tablå. Dette emnet inneholder noen ting å ta hensyn til for oppgraderingen. 

Oppgraderingsprosessen flytter eksisterende oppsett og alle eksisterende transaksjoner til den nye tablåstrukturen. Verdimodeller forblir slik de er for øyeblikket, som et tablå som posterer til økonomimodulen. Avskrivningstablåer flyttes til et tablå bok med alternativet **Poster til økonomimodul** satt til **Ingen**. Journalnavn for avskrivningstablå flyttes til et journalnavn for økonomimodul med posteringslaget satt til **Ingen**. Avskrivningstablåtransaksjoner vil bli flyttet til anleggsmiddeltransaksjoner. 

Før du kjører dataoppgraderingen, må du forstå de to alternativene som er tilgjengelige for oppgradering av journallinjer for avskrivningstablå til transaksjonsbilag, og nummerserien som brukes for bilagsserien. 

Alternativ 1: **Systemdefinert nummerserie** – Dette er standardalternativet for å optimalisere ytelsen til dataoppgraderingen. Oppgraderingen kan ikke bruke rammeverket for nummerserie, men vil i stedet tildele bilag med en settbasert tilnærmingsmåte. Etter oppgraderingen vil den nye nummerserien opprettes med **Neste nummerserie** basert på riktig måte på de oppgraderte transaksjonene Nummerserien brukes som standard i formatet FADBUpgr\#\#\#\#\#\#\#\#\#. Det finnes noen få tilgjengelige parametere for å justere formatet når du bruker denne fremgangsmåten:

-   **Nummerseriekode** – Koden for å identifisere nummerserien. Denne nummerseriekoden kan ikke eksistere siden den opprettes av oppgraderingen.
    -   Konstantnavn: **NumberSequenceDefaultCode**
    -   Standardverdi: "FADBUpgr"
-   **Prefiks** – Konstantsstrengverdien som skal brukes som et prefiks for bilagsnumrene.
    -   Konstantnavn: **NumberSequenceDefaultParameterPrefix**
    -   Standardverdi: "FADBUpgr"
-   **Alfanumerisk lengde** – Lengden på det alfanumeriske segmentet i nummerserien.
    -   Konstantnavn: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Standardverdi: 9
-   **Startnummer** – Det første tallet som skal brukes i nummerserien.
    -   Konstantnavn: **NumberSequenceDefaultParameterStartNumber**
    -   Standardverdi: 1

Alternativ 2: **Eksisterende brukerdefinert nummerserie** - Dette alternativet lar deg definere nummerserien som skal brukes for oppgraderingen. Vurder å bruke dette alternativet hvis du har behov for avansert nummerseriekonfigurasjon. Hvis du vil bruke en nummerserie, må du endre oppgraderingsklassen ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans med følgende informasjon:

-   **Nummerseriekode** – Koden til nummerserien.
    -   Konstantnavn: **NumberSequenceExistingCode**
    -   Standardverdi: Ingen standard. Dette må oppdateres til nummerseriekoden.
-   **Felles nummerserie** – En boolsk verdi for å identifisere omfanget for nummerserien. Bruk "true" for nummerserier som deles på tvers av alle firmaer, og "false" for et firmaomfang. Når du bruker "false", må nummerserien med det angitte navnet finnes i hvert firma som inneholder avskrivningstablåtransaksjoner. Det finnes delte nummerserier i hver partisjon som inneholder avskrivningstablåtransaksjoner.
    -   Konstantnavn: **NumberSequenceExistingIsShared**
    -   Standardverdi: true

Parameterne er plassert i begynnelsen av klassen ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

*// Angi en foretrukket metode for fordeling av bilag* 
 *// true, hvis du vil bruke en eksisterende nummerseriekode* 
 *// false, hvis du vil bruke den systemdefinerte nummerserien (standard)* const boolean NumberSequenceUseExistingCode = false;  

*// Hvis bruker fremgangsmåten for systemdefinert nummerserie, angir du parameterne for nummerserien.*
 *// Det opprettes en ny nummerserie med disse parameterne.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Hvis du bruker fremgangsmåten for eksisterende nummerserie, angir du den eksisterende nummerseriekoden.* 
 *// Bilagstilordning går rad for rad for eksisterende nummerserier.* const str NumberSequenceExistingCode = ''; *// Angi omfanget for den eksisterende nummerseriekoden* 
 *// true, hvis den angitte nummerserien er delt* 
 *// false, hvis den angitte nummerserien er per firma* 
 *// Standard systemdefinert nummerserie brukes hvis en nummerseriekode med det angitte omfanget ikke finnes.* const boolean NumberSequenceExistingIsShared = true; 

Bygg på nytt prosjektet som inneholder klassen når konstantene har blitt endret. 

Når du bruker fremgangsmåten for systemgenerert nummerserie (alternativ 1), bruker oppgraderingen settbasert behandling for å tildele bilagsnumrene som er angitt i parameterne for oppgraderingsskriptet. Dette oppretter også en ny nummerserie med angitte parametere etter tildelingen. 

Når du bruker fremgangsmåten for brukerdefinert nummerserie (alternativ 2), sjekker dataoppgraderingen om nummerserien med det angitte omfanget finnes i databasen for hver partisjon og firma med avskrivningstablåtransaksjoner. Hvis den finnes, bruker oppgraderingen rad for rad-behandling for å tildele bilagsnumre som angis av nummerserien ved hjelp av rammeverket for nummerserier. Hvis nummerserien ikke finnes med angitte omfanget, bruker oppgraderingen fremgangsmåten for standard systemdefinert nummerserie for å tildele bilagsnumrene, og det opprettes en ny nummerserie med angitte standardparametere etter tildelingen.

For begge fremgangsmåtene vil skriptet for dataoppgradering også bruke nummerserien for **Bilagsserie**-feltet på de nye journalnavnene for økonomimodulen som er opprettet for de tidligere journalnavnene for avskrivningstablå.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
