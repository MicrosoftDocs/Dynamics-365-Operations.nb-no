---
title: Testing av overgang til oppgradering
description: "Dette emnet forklarer hvordan du tester aktiviteter som forekommer når du har slått av AX 2012, men før du aktiverer Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: nb-no
ms.lasthandoff: 06/15/2017

---

# Testing av overgang til oppgradering
<a id="upgrade-cutover-testing" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Overgang* er termen som vi bruker for den endelige prosessen med å aktivere et nytt system. Denne overgangsprosessen består av aktiviteter som forekommer når Microsoft Dynamics AX 2012 er slått av, men før Microsoft Dynamics 365 for Finance and Operations, Enterprise edition er slått på. Formålet med testing av overgang til oppgradering er til å øve på overgangsprosessen, for å sikre en jevnere opplevelse for alle som er involvert i løpet av den faktiske overgangen til aktivering.

Det finnes to primære arbeidsflyter under en overgang:

- **Teknisk arbeidsflyt** – Denne arbeidsflyten omfatter prosessen med å utføre dataoppgraderingen. Firmaet vil håndheve en grense for hvor mye nedetid som er tillatt. I løpet av denne nedetiden vil verken AX 2012 eller Finance and Operations være tilgjengelig. Denne arbeidsflyten må kanskje justere dataoppgraderingsprosedyren for å overholde virksomhetens nedetidsgrense.
- **Funksjonell arbeidsflyt** – Denne arbeidsflyten inneholder konfigurasjonsoppgavene som utføres etter at dataoppgraderingen er fullført. Alle disse oppgavene må dokumenteres og kvantifiseres, og en ressurs må tilordnes til dem, fordi både den funksjonelle arbeidsflyten og den tekniske arbeidsflyten må holdes innenfor virksomhetens nedetidsgrense.

Illustrasjonen nedenfor viser prosessen for overgangen til aktivering slik den foregår i produksjonsmiljøet.

![Overgangsprosess](./media/cutover_1.png)

Denne overgangsprosessen skiller seg fra en grunnleggende dataoppgradering i et sandkassemiljø, på følgende måter:

- AX 2012-databasen kopieres ikke, men det bli bare tatt en sikkerhetskopi, og deretter endres den opprinnelige databasen. Denne metoden er raskere, og sikkerhetskopien gjør tilbakeføring mulig, ved behov.
- Fordi produksjonsmiljøet for økonomi og har begrenset tilgang, utføres nå oppgavene som tidligere ble utført på sandkasseforekomsten av Application Object Server (AOS), av Microsoft DSE-teamet. Disse oppgavene inkluderer nedlasting og import av bacpac-filen og kjøring av MajorversionDataUpgrade.zip-pakken.
- Vi har lagt til følgende oppgaver:

    - Ufør en røyktest.
    - Fullfør oppgaver for oppsett av programmet. Dette trinnet kan være stort, avhengig av hvilke funksjoner som brukes. I dette trinnet konfigurerer det funksjonelle teamet ny programfunksjonalitet, slik at det er klart for bruk i det oppgraderte systemet.
    - Slipp brukerne inn igjen. Varsle brukerbasen om at oppgraderingen er fullført og at de kan bruke systemet på nytt.

## Teknisk arbeidsflyt
<a id="technical-workstream" class="xliff"></a>

Den tekniske arbeidsflyten omfatter forskjellige tekniske gruppemedlemmer: databaseadministrator (DBA), systemansvarlig for AX 2012, server-administratorer og utviklere som har kjennskap til AX 2012 og Finance and Operations. Dette emnet forklarer hvilke aktiviteter som omfatter hvilke roller.

Under overgangstesting fokuserer det tekniske teamet på ytelse- og pålitelighetstesting av dataoppgraderingsprosessen, for å være sikker på at den oppfyller virksomhetens nedetidsgrense. Mange elementer av maskinvare og programvare er involvert i denne prosessen. Noen av disse elementene er lokale, mens andre er i Microsoft-skyen. Dessuten er mange elementer av egendefinert programkode og standardkode involvert. Denne testingen bør gjøre deg trygg på overgangsprosessen for miljøet ditt.

### Slå av AX 2012 AOS-forekomstene
<a id="turn-off-the-ax-2012-aos-instances" class="xliff"></a>

Denne oppgaven involverer systemansvarlig for AX 2012 og serveradministratorene.

Du må validere følgende områder:

- **Satsvise jobber som kjører på tidspunktet for overgangen** – en tidkrevende satsvis jobb som allerede har begynt å kjøre, hindrer at systemet stopper. Legg en plan, slik at du kan stoppe AOS-forekomstene på ønsket tidspunktet. Du må kanskje planlegge satsvise jobber slik at de er fullført en stund før du deaktiverer AX 2012.
- **Integrerte systemer** – Det kan hende du har andre systemer som er integrert med AX 2012-miljøet. Du må ta disse systemene med i planen for avstenging av AX 2012. Du må for eksempel kanskje slå av de integrerte systemene en viss tid før du deaktiverer selve AX 2012, slik at eventuelle gjenværende pågående transaksjoner kan fullføres. Kravene for integrerte systemer varierer sterkt fra bedrift til bedrift. Derfor må ekspertteamet planlegge for dette scenariet uavhengig av hverandre.

### Opprett en sikkerhetskopi av AX 2012-databasen.
<a id="create-a-backup-of-the-ax-2012-database" class="xliff"></a>

Denne oppgaven omfatter DBA. Sikkerhetskopien brukes hvis det kreves en tilbakeføring. Det brukes også som et referansepunkt som beholdes i en periode, og viser systemtilstanden på tidspunktet for overgangen.

Du må validere følgende områder:

- Få konkret tidsberegning for sikkerhetskopieringen.
- Juster alternativene for sikkerhetskopiering som brukes (for eksempel komprimering og ikke-komprimering), for å sikre raskest mulig sikkerhetskopiering.

### Eksportere databasen til bacpac
<a id="export-the-database-to-bacpac" class="xliff"></a>

Denne oppgaven omfatter DBA. Utdataene for denne oppgaven er eksportfilen som skal lastes opp til Microsoft Azure for det nye systemet.

Du må validere følgende områder:

- Få konkret tidsberegning for sikkerhetskopieringen.
- Optimaliser eksportprosessen for å garantere raskest mulig opplevelse. Optimaliseringen krever kanskje følgende oppgaver:

    - Mål systemressurser under eksport, for eksempel prosessor, disk i/u og minne.
    - Hvis det finnes ressursflaskehalser, kan du opprette en plan for å redusere dem. Vanligvis vil du redusere disse flaskehalsene ved å tilordne flere av den nødvendige ressursen.

### Laste opp bacpac-filen til lagring i Azure
<a id="upload-the-bacpac-file-to-azure-storage" class="xliff"></a>

Denn oppgaven omfatter DBA eller serveradministratorene. Bacpac-filen flyttes til Azure under denne oppgaven.

Du må validere følgende områder:

- Velg maskinen som skal brukes for opplasting, og kontroller at verktøyet Azure Storage-utforsker er konfigurert og klart til bruk.
- Få konkrete tidsberegninger for opplastingsprosessen ved å måle den flere ganger. Opplastingstidene vil variere, avhengig av hastigheten på Internett-tilkoblingen og den geografiske plasseringen til Azure-datasenteret forhold til lokasjonen.

### Laste ned og importere bacpac-filen til Azure SQL-databasen
<a id="download-and-import-the-bacpac-file-to-the-azure-sql-database" class="xliff"></a>

Når denne oppgaven foregår i aktiveringen, vil den bli utført av Microsoft DSE-gruppen. Under overgangstestingen omfatter den imidlertid din DBA. Resultatet av denne oppgaven er eksportfilen som skal lastes opp til Azure for det nye systemet.

Du må validere følgende områder:

- Få konkret tidsberegning for importprosessen.
- Optimaliser eksportprosessen for å garantere raskest mulig opplevelse. Optimaliseringen krever kanskje følgende oppgaver:

    - Mål systemressurser under eksport. Her er noen eksempler:

        - **På AOS-maskinen:** prosessor, disk i/u- og minne
        - **På Azure SQL-databaseforekomsten:** SQL-databasens produksjon (DTU). Du kan overvåke Azure SQL DTU fra Microsoft SQL Server Management Studio på AOS-maskinen ved å se på sys.dm_resource_stats-systemvisningen.

    - Hvis det finnes ressursflaskehalser, kan du opprette en plan for å redusere dem. Vanligvis vil du redusere disse flaskehalsene ved å tilordne flere av den nødvendige ressursen. Ettersom Microsoft er vert for denne maskinen, må du sende en forespørsel til Microsoft om å øke ressursene hvis du oppdager at de er en flaskehals.

### Kjør MajorVersiondataUpgrade.zip-pakken
<a id="run-the-majorversiondataupgradezip-package" class="xliff"></a>

Når denne oppgaven foregår i aktiveringen, vil den bli utført av Microsoft DSE-gruppen. Under overgangstestingen omfatter den imidlertid utviklerne. I løpet av denne oppgaven blir den gamle databasestrukturen omgjort til strukturen i det nye systemet.

Databasens synkroniseringsprosess kjører som en del av denne oppgaven. Databasesynkronisering kan ta lang tid i noen tilfeller, for eksempel når en gruppert indeks er endret på en tabell, fordi denne operasjonen er det vanskelig å gjøre i SQL.

Vi anbefaler sterkt at du først utfører en analyse og feilsøkingsprosess i et utviklingsmiljø. I et sandkassemiljø er alternativer for feilsøking og analyser mer begrenset. Målet er å ha få eller ingen problemer som må løses, når du tester overgangen.

Du må validere følgende områder:

- Få konkret tidsberegning for importprosessen.
- Optimalisere prosessen for å garantere den raskest opplevelsen. Optimaliseringen krever kanskje følgende oppgaver:

    - Overvåk ytelsen til individuelle oppgraderingsskript via ReleaseUpdateScriptsExecution-tabellen.
    - Juster skript for å optimalisere ytelsen. Denne oppgaven kan kreve at du tilpasser et skripts X ++-kode for å optimalisere den for datasettet.
    - Overvåk Azure SQL DTU ved hjelp av Microsoft Dynamics Lifecycle Services (LCS)-overvåking eller sys.dm_resources_stats-systemvisningen i Management Studio. Hvis alle ressurser er brukt, må du kanskje be Microsoft DSE-teamet om et høyere nivå i databasen.

### TIlbakeføre til AX 2012
<a id="roll-back-to-ax-2012" class="xliff"></a>

Målet med denne oppgaven er å gjenopprette databasen ved hjelp av sikkerhetskopien som ble gjort da AX 2012 ble slått av, og deretter aktivere AX 2012 på nytt. Det kan hende statusen for integrerte systemer også må gjenopprettes. Men fordi integrerte systemer varierer fra bedrift til bedrift, må du planlegge denne situasjonen hver for seg, basert på de bestemte forholdene. Selv om det er lite sannsynlig at du må tilbakeføre, er det svært viktig at du har en prosess som er testet, i tilfelle du trenger den.

## Funksjonell arbeidsflyt
<a id="functional-workstream" class="xliff"></a>

Etter dataoppgraderingen må flere konfigurasjonsoppgaver gjøres i det nye miljøet. Målet med denne arbeidsflyten er til å dokumentere og telle alle konfigurasjonsoppgaver og tildele en ressurs til hver oppgave, for å garantere at disse oppgavene kan utføres sammen med den tekniske arbeidsflyten under nedetidsvinduet.

Funksjonelle oppgaver omfatter vanligvis endring av verdiene i bestemte systemparametere eller andre konfigurasjonsdata. Disse oppgavene identifiseres gjennom den fullstendige funksjonelle testomgangen, som er en separat aktivitet fra overgangstestingen. Når en oppgave av denne typen er identifisert, bør den gjennomgås sammen med den funksjonelle ressursen og utvikleren.

Større endringer kan kreve at det skrives et nytt egendefinert dataoppgraderingsskript for å oppdatere dataene under dataoppgraderingsprosessen. Den funksjonelle ressursen kan imidlertid manuelt kjøre mindre endringer gjennom det nye systemet etter dataoppgraderingen.

Større endringer som har nye dataoppgraderingsskript, må testes. Én eller flere flere gjentakelser av MajorVersionDataUpgrade.zip-pakken må derfor kjøres. Det er viktig at du kan vurdere kostnaden ved å kjøre pakken på nytt mot kostnaden ved manuell registrering av data.

For hver manuell endring må det legges til en oppgave i overgangsplandokumentet. Denne oppgaven må vise følgende detaljer:

-   Hva er oppgaven, og hva må gjøres?
-   Hvem må gjøre det?
-   Hvor lang tid tar det?

