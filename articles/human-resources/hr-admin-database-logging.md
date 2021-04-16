---
title: Konfigurere og administrere databaselogging
description: Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801341"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="4e3eb-103">Konfigurere og administrere databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4e3eb-104">Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="4e3eb-105">Dette emnet beskriver hvordan du gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-105">This topic describes how to:</span></span>

- <span data-ttu-id="4e3eb-106">Administrerer sikkerhet og ytelse for databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="4e3eb-107">Definer databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-107">Set up database logging</span></span>
- <span data-ttu-id="4e3eb-108">Rydder opp i databaselogger</span><span class="sxs-lookup"><span data-stu-id="4e3eb-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="4e3eb-109">Oversikt over databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-109">Overview of database logging</span></span>

<span data-ttu-id="4e3eb-110">Databaselogging sporer spesifikke endringer i Microsoft Dynamics 365 Human Resources-tabeller og -felt.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="4e3eb-111">Disse endringene omfatter innsetting, oppdatering eller sletting.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="4e3eb-112">Databaselogging lagrer en post over endringer i tabeller eller felt i databaseloggtabellen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="4e3eb-113">Firmaets bruk av databaselogging omfatter:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="4e3eb-114">Opprett en overvåkingsregistrering for endringer i bestemte tabeller som inneholder sensitiv informasjon.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="4e3eb-115">Spore enkelttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-115">Tracking single transactions.</span></span> <span data-ttu-id="4e3eb-116">Databaselogging er ikke ment for sporing av automatiserte transaksjoner som kjøres i satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="4e3eb-117">Sikkerhet for databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-117">Security for database logging</span></span>

<span data-ttu-id="4e3eb-118">Databaselogger kan inneholde sensitive data.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="4e3eb-119">Begrens tilgangen til å bare inkludere sikkerhetsroller som trenger tilgang til loggdataene.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="4e3eb-120">Databaselogging og ytelse</span><span class="sxs-lookup"><span data-stu-id="4e3eb-120">Database logging and performance</span></span>

<span data-ttu-id="4e3eb-121">Selv om det er verdifullt fra et forretningsperspektiv, kan databaselogging være dyrt i ressursbruk og -behandling.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="4e3eb-122">Ytelseimplikasjonene for databaselogging omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="4e3eb-123">Databaseloggtabellen kan vokse raskt og føre til en økning i størrelsen på databasen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="4e3eb-124">Veksten avhenger av hvor mye loggdata du bestemmer deg for å beholde.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="4e3eb-125">Som standard beholder databaseloggtabellen bare 30 dager med loggdata.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="4e3eb-126">Databaselogging kan påvirke lange automatiserte prosesser negativt, for eksempel lange dataimporter.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="4e3eb-127">Anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="4e3eb-127">Best practices</span></span>

<span data-ttu-id="4e3eb-128">For å forbedre ytelsen begrenses loggoppføringer ved å velge bestemte felt du skal logge i stedet for hele tabeller.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="4e3eb-129">For å opprettholde generell ytelse er databaselogging begrenset til 20 tabeller.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="4e3eb-130">Bare oppdateringer kan logges for individuelle felt.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="4e3eb-131">Definer databaselogging</span><span class="sxs-lookup"><span data-stu-id="4e3eb-131">Set up database logging</span></span>

<span data-ttu-id="4e3eb-132">Du kan bruke veiviseren **Registrerer databaseendringer** til å konfigurere databaselogging.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="4e3eb-133">Veiviseren gir en fleksibel måte å konfigurere logging for tabeller eller felt på.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="4e3eb-134">Gå til **Systemadministrasjon > Koblinger > Database > Oppsett av databaselogg**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="4e3eb-135">Velg **Ny** for å starte veiviseren **Registrerer databaseendringer**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="4e3eb-136">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-136">Select **Next**.</span></span> 
3. <span data-ttu-id="4e3eb-137">På siden **Tabeller og felt** i veiviseren velger du tabellene og feltene du vil aktivere databaselogging på, og velger **Neste**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="4e3eb-138">Databaselogging er ikke tilgjengelig på alle tabeller i Human Resources-databasen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="4e3eb-139">Hvis du velger **Vis alle tabeller** under listen, utvides listen over tabeller og felt som viser alle databasetabeller som det er tilgjengelig databaselogging for, men dette er et delsett av den fullstendige listen over databasetabeller.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="4e3eb-140">På siden **Endringstyper** i veiviseren velger du dataoperasjonene du vil spore endringer for hver av tabellene og feltene for, og velger **Neste**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="4e3eb-141">Se tabellen nedenfor hvis du vil ha en beskrivelse av dataoperasjonene som er tilgjengelige for logging.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="4e3eb-142">På **Fullfør**-siden kan du se gjennom endringene som blir gjort, og velge **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="4e3eb-143">Operasjon</span><span class="sxs-lookup"><span data-stu-id="4e3eb-143">Operation</span></span> | <span data-ttu-id="4e3eb-144">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4e3eb-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="4e3eb-145">Spor nye transaksjoner</span><span class="sxs-lookup"><span data-stu-id="4e3eb-145">Track new transactions</span></span> | <span data-ttu-id="4e3eb-146">Opprett en logg for nye poster som er opprettet i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="4e3eb-147">Oppdatering</span><span class="sxs-lookup"><span data-stu-id="4e3eb-147">Update</span></span> | <span data-ttu-id="4e3eb-148">Opprett en logg for oppdateringer av tabellposter, eller oppdateringer til enkeltvis valgte felt i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="4e3eb-149">Hvis du velger å logge oppdateringer for tabellen, opprettes det en loggpost hver gang det gjøres en oppdatering i et hvilket som helst felt i en hvilken som helst post i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="4e3eb-150">Hvis du velger å logge oppdateringer for bestemte felt, opprettes det bare en loggpost når det gjøres oppdateringer i disse feltene for tabellposter.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="4e3eb-151">Delete</span><span class="sxs-lookup"><span data-stu-id="4e3eb-151">Delete</span></span> | <span data-ttu-id="4e3eb-152">Opprett en logg for poster som er slettet fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="4e3eb-153">Gi nøkkel nytt navn</span><span class="sxs-lookup"><span data-stu-id="4e3eb-153">Rename key</span></span> | <span data-ttu-id="4e3eb-154">Opprett en loggpost når en tabellnøkkel får nytt navn.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="4e3eb-155">Rydder opp i databaselogger</span><span class="sxs-lookup"><span data-stu-id="4e3eb-155">Clean up database logs</span></span>

<span data-ttu-id="4e3eb-156">Du kan slette hele eller deler av databaseloggene ved hjelp av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="4e3eb-157">Velg alle logger for en bestemt tabell.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="4e3eb-158">Velg bestemte typer databaselogg.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-158">Select specific types of database log.</span></span>
- <span data-ttu-id="4e3eb-159">Velg dato og klokkeslett for oppretting av logg.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="4e3eb-160">Gjør følgende for å konfigurere opprydding i databaselogg:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="4e3eb-161">Gå til **Systemadministrasjon > Koblinger > Database > Databaselogg**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="4e3eb-162">Velg **Opprydding i logg**.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="4e3eb-163">Velg en metode for valg av logger du vil slette, ved å angi ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="4e3eb-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="4e3eb-164">Tabell-ID</span><span class="sxs-lookup"><span data-stu-id="4e3eb-164">Table ID</span></span>
   - <span data-ttu-id="4e3eb-165">Loggtype</span><span class="sxs-lookup"><span data-stu-id="4e3eb-165">Type of log</span></span>
   - <span data-ttu-id="4e3eb-166">Opprettingsdato og -klokkeslett</span><span class="sxs-lookup"><span data-stu-id="4e3eb-166">Created date and time</span></span>

3. <span data-ttu-id="4e3eb-167">Bruk kategorien **Opprydding i databaselogg** for å bestemme når du vil kjøre loggoppryddingsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="4e3eb-168">Som standard er databaselogger tilgjengelige i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="4e3eb-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
