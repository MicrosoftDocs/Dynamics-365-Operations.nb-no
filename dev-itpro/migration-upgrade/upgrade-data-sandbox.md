---
title: "Dataoppgradering i et sandkassemiljø"
description: "Dette emnet forklarer hvordan du utfører en dataoppgradering fra AX 2012 til Dynamics 365 for Finance and Operations i et sandkassemiljø."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
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
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: nb-no
ms.lasthandoff: 06/15/2017

---

# Dataoppgradering i et sandkassemiljø
<a id="data-upgrade-in-a-sandbox-environment" class="xliff"></a>

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Utdataene for denne aktiviteten er en oppgradert database som du kan bruke i et sandkassemiljø. Et sandkassemiljø er et miljø der bedriftsbrukere og funksjonelle gruppemedlemmer kan validere programfunksjonalitet. Denne funksjonaliteten omfatter tilpasninger og dataene som ble videreført fra Microsoft Dynamics AX 2012.

Vi anbefaler sterkt at du kjører dataoppgraderingsprosessen i et utviklingsmiljø før du kjører den i et delt sandkassemiljø, fordi denne fremgangsmåten vil hjelpe deg med å redusere den totale tiden som kreves for en vellykket dataoppgradering. Hvis du vil ha mer informasjon, kan du se [Oppgradere – Dataoppgradering i et utviklingsmiljø](prepare-data-upgrade.md).

## Oversikt over oppraderingsprosessen for sandkassedataene
<a id="overview-of-the-sandbox-data-upgrade-process" class="xliff"></a>

Før du begynner å oppgradere data i et sandkassemiljø, vil du allerede ha oppgradert data i et utviklingsmiljø, som forklart i [dataoppgradering i et utviklingsmiljø](prepare-data-upgrade.md). De to prosessene er svært like. Den viktigste forskjellen er at et sandkassemiljø bruker Microsoft Azure SQL-Database til lagring av data, mens et utviklingsmiljø bruker Microsoft SQL Server. Denne tekniske forskjellen i databaselaget krever at du endrer dataoppgraderingsprosedyren litt i et sandkassemiljø, fordi en sikkerhetskopi fra AX 2012-databaseforekomsten ikke uten videre kan gjenopprettes til SQL-databasen.

![Oppgraderingsprosess av sandkassedata](./media/data-upgrade-sandbox.png)

Her er trinnene på høyt nivå i oppgraderingsprosessen.

1. Opprett en kopi av AX 2012-databasen. Vi anbefaler sterkt at du bruker en kopi, fordi du må slette noen objekter i kopien som blir eksportert.
2. Eksporter den kopierte databasen til en bacpac-fil ved å bruke et gratis SQL Server-verktøy som heter SQLPackage.exe. Dette verktøyet gir en spesiell type sikkerhetskopi av databasen som kan importeres til SQL-databasen.
3. Laste opp bacpac-filen til lagring i Azure.
4. Last ned bacpac-filen for Application Object Server (AOS)-maskinen i sandkassemiljøet, og importere den deretter ved hjelp av SQLPackage.exe. Deretter må du kjøre et skript mot den importerte databasen for å tilbakestille SQL-databasebrukerne.
5. Kjør MajorVersionDataUpgrade.zip-pakken for å kjøre dataoppgraderingen mot den importerte databasen.

## Opprette en kopi av AX 2012-databasen
<a id="create-a-copy-of-the-ax-2012-database" class="xliff"></a>

Du må opprette en kopi av AX 2012-databasen som du oppgraderer, fordi du må slette noen av objektene fra databasen. Disse objektene omfatter alle brukere med Microsoft Windows-godkjenning. Disse endringene gjør at databasen ikke kan brukes i AX 2012. I dette trinnet, vil du lage en kopi av databasen og slette disse objektene.

Dette trinnet må utføres av databaseadministrator (DBA) eller en person som har lignende kunnskap og erfaring.

Hvis du vil opprette en kopi av databasen, ta en sikkerhetskopi av den opprinnelige databasen og gjenopprette den med et nytt navn. Kontroller at nok diskplass er tilgjengelig for begge databasene. Du kan opprette kopien på en annen server. Versjonen av SQL Server-forekomsten som kjører databasen, er ikke viktig.

Her er et eksempel på koden som oppretter en kopi av databasen. Du må endre dette eksemplet for å gjenspeile de bestemte databasenavnene.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Når kopien er opprettet, kan du kjøre Transact-SQL (T-SQL)-skriptet nedenfor mot den.
TODO 

### Eksportere den kopierte databasen til en bacpac-fil
<a id="export-the-copied-database-to-a-bacpac-file" class="xliff"></a>

'Eksporter den kopierte databasen til en bacpac-fil ved hjelp av verktøyet SQLPackage.exe. Dette trinnet skal utføres av DBA eller gruppemedlemmer som har tilsvarende kunnskaper.

Det er svært viktig at du installerer den nyeste versjonen av SQL Server Management Studio før du starter dette trinnet. Selv om SQLPackage finnes i tidligere versjoner av Management Studio, vil det ikke fungere for dette trinnet, med mindre du først installerer den nyeste versjonen.

Dette trinnet er viktig fordi eksporten må utføres på nytt i løpet av nedetiden før aktiveringen. Her er noen tips:

- Bacpac-prosessen er svært I/U- og prosessorintensiv. Kjør derfor eksporten på kraftig maskin.
- SQLPackage bør kjøres lokalt på maskinen som er vert for databasen. Ikke kjør SQLPackage på en lokal bærbar datamaskin som er koblet til databasemaskinen, fordi denne prosessen er også nettverksintensiv.

Deretter åpner du et **ledetekst**-vindu som administrator, og kjører følgende kommandoer:

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Her er en forklaring av parameterne:

- **ksn** (kildeservernavn) – navnet på SQL-serveren det skal eksporteres fra. For vår prosess bør alltid denne parameteren alltid settes til **localhost**.
- **kdn** (kildedatabasenavn) – navnet på databasen du vil eksportere..
- **mf** (målfil) – banen og navnet på filen som det skal eksporteres til. Mappen må finnes fra før, men filen blir opprettet av prosessen.
- **/p:CommandTimeout** – tidsavbruddsverdi per spørring. Med denne parameteren kan større tabeller eksporteres uten tidsavbrudd.

### Laste opp bacpac-filen til lagring i Azure
<a id="upload-the-bacpac-file-to-azure-storage" class="xliff"></a>

Laste opp bacpac-filen til lagring i Azure. Se UsingStorageExplorer.docx TODO

### Importere bacpac-filen i SQL-databasen
<a id="import-the-bacpac-file-into-sql-database" class="xliff"></a>

I dette trinnet vil du importere den eksporterte bacpac-filen til forekomsten av SQL-databasen som sandkassemiljøet ditt bruker. Først må du installere den nyeste versjonen av Management Studio på sandkasse-AOS-maskinen. Deretter vil du importere filen ved hjelp av verktøyet SQLPackage.exe.

Du vil utføre disse oppgavene direkte på AOS-maskinen i sandkassemiljøet ditt, fordi det ikke finnes brannmurregler som begrenser tilgangen til forekomsten av SQL-databasen. Ved hjelp av AOS-maskinen, kan du imidlertid få tilgang.

Som for eksporttrinnet må du ha den nyeste versjonen av Management Studio før du starter importen. Dette trinnet vil ikke fungere hvis du har en eldre versjon.

Av hensyn til ytelsen anbefales det at du plasserer bacpac-filen på stasjon D på AOS-maskinen. På virtuelle Azure-maskiner er stasjon D en fysisk disk som vanligvis har høyere ytelse enn andre tilgjengelige disker.

Åpne et **ledetekst**-vindu som administrator, og kjør følgende kommandoer:

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Her er en forklaring av parameterne:

- **msn** (målservernavn) – navnet på SQL Azure-serveren du vil importere til. Navnet kan finnes i LCS. Gi det suffikset **. database.windows.net**.
- **mdn** (måldatabasenavn) – navnet på databasen du vil importere til. Databasen må ikke finnes allerede. Importprosessen vil opprette den.
- **kf** (kildefil) – banen til og navnet på filen som skal importeres.
- **mp** (målpassord) – SQL-passord for målforekomsten av SQL-databasen.
- **mb** (målbruker) – SQL-brukernavnet for målforekomsten av SQL-databasen. Vi anbefaler at du bruker **sqladmin**. Du kan hente passordet for denne brukeren fra LCS-prosjektet.
- **/p:CommandTimeout** – tidsavbruddsverdi per spørring. Med denne parameteren kan større tabeller eksporteres uten tidsavbrudd.
- **/p:DatabaseServiceObjective** – tjenestelagnivået til databasen som er opprettet. Du kan kontrollere verdien for den eksisterende databasen ved hjelp av Management Studio. Høyreklikk databasen, og velg deretter **Egenskaper**.

Når du har kjørt kommandoen, får du følgende advarsel. Du kan trygt ignorere den.

![Sandkasse-feil](./media/sandbox-2.png)
 
### Kjør MajorVersionDataUpgrade.zip-pakken
<a id="run-the-majorversiondataupgradezip-package" class="xliff"></a>

Kjør den distribuerbare dataoppgraderingspakken som beskrevet i [Oppgrader data i utviklings-, demo- eller sandkassemiljøer](upgrade-data-to-latest-update.md).

### Oppgradere en kopi av databasen i et utviklingsmiljø
<a id="upgrade-a-copy-of-the-database-in-a-development-environment" class="xliff"></a>

Det er nyttig å oppgradere den samme databasen i et utviklingsmiljø. Hvis du har en kopi av databasen tilgjengelig for utviklingsmiljøer, blir det mye enklere å undersøke feil som blir funnet i det oppgraderte sandkassemiljøet.

