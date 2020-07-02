---
title: Konfigurere og administrere databaselogging
description: Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443591"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="a9652-103">Konfigurere og administrere databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-103">Configure and manage database logging</span></span>

<span data-ttu-id="a9652-104">Du kan spore endringer i tabeller og felt i Dynamics 365 Human Resources med databaselogging.</span><span class="sxs-lookup"><span data-stu-id="a9652-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="a9652-105">Dette emnet beskriver hvordan du gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="a9652-105">This topic describes how to:</span></span>

- <span data-ttu-id="a9652-106">Administrerer sikkerhet og ytelse for databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="a9652-107">Definer databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-107">Set up database logging</span></span>
- <span data-ttu-id="a9652-108">Rydder opp i databaselogger</span><span class="sxs-lookup"><span data-stu-id="a9652-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="a9652-109">Oversikt over databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-109">Overview of database logging</span></span>

<span data-ttu-id="a9652-110">Databaselogging sporer spesifikke endringer i Microsoft Dynamics 365 Human Resources-tabeller og -felt.</span><span class="sxs-lookup"><span data-stu-id="a9652-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="a9652-111">Disse endringene omfatter innsetting, oppdatering eller sletting.</span><span class="sxs-lookup"><span data-stu-id="a9652-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="a9652-112">Databaselogging lagrer en post over endringer i tabeller eller felt i databaseloggtabellen.</span><span class="sxs-lookup"><span data-stu-id="a9652-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="a9652-113">Firmaets bruk av databaselogging omfatter:</span><span class="sxs-lookup"><span data-stu-id="a9652-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="a9652-114">Opprett en overvåkingsregistrering for endringer i bestemte tabeller som inneholder sensitiv informasjon.</span><span class="sxs-lookup"><span data-stu-id="a9652-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="a9652-115">Spore enkelttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="a9652-115">Tracking single transactions.</span></span> <span data-ttu-id="a9652-116">Databaselogging er ikke ment for sporing av automatiserte transaksjoner som kjøres i satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="a9652-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="a9652-117">Sikkerhet for databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-117">Security for database logging</span></span>

<span data-ttu-id="a9652-118">Databaselogger kan inneholde sensitive data.</span><span class="sxs-lookup"><span data-stu-id="a9652-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="a9652-119">Begrens tilgangen til å bare inkludere sikkerhetsroller som trenger tilgang til loggdataene.</span><span class="sxs-lookup"><span data-stu-id="a9652-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="a9652-120">Databaselogging og ytelse</span><span class="sxs-lookup"><span data-stu-id="a9652-120">Database logging and performance</span></span>

<span data-ttu-id="a9652-121">Selv om det er verdifullt fra et forretningsperspektiv, kan databaselogging være dyrt i ressursbruk og -behandling.</span><span class="sxs-lookup"><span data-stu-id="a9652-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="a9652-122">Ytelseimplikasjonene for databaselogging omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="a9652-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="a9652-123">Databaseloggtabellen kan vokse raskt og føre til en økning i størrelsen på databasen.</span><span class="sxs-lookup"><span data-stu-id="a9652-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="a9652-124">Veksten avhenger av hvor mye loggdata du bestemmer deg for å beholde.</span><span class="sxs-lookup"><span data-stu-id="a9652-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="a9652-125">Som standard beholder databaseloggtabellen bare 30 dager med loggdata.</span><span class="sxs-lookup"><span data-stu-id="a9652-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="a9652-126">Databaselogging kan påvirke lange automatiserte prosesser negativt, for eksempel lange dataimporter.</span><span class="sxs-lookup"><span data-stu-id="a9652-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="a9652-127">Anbefalte fremgangsmåter</span><span class="sxs-lookup"><span data-stu-id="a9652-127">Best practices</span></span>

<span data-ttu-id="a9652-128">For å forbedre ytelsen begrenses loggoppføringer ved å velge bestemte felt du skal logge i stedet for hele tabeller.</span><span class="sxs-lookup"><span data-stu-id="a9652-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="a9652-129">For å opprettholde generell ytelse er databaselogging begrenset til 20 tabeller.</span><span class="sxs-lookup"><span data-stu-id="a9652-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="a9652-130">Bare oppdateringer kan logges for individuelle felt.</span><span class="sxs-lookup"><span data-stu-id="a9652-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="a9652-131">Definer databaselogging</span><span class="sxs-lookup"><span data-stu-id="a9652-131">Set up database logging</span></span>

<span data-ttu-id="a9652-132">Du kan bruke veiviseren **Registrerer databaseendringer** til å konfigurere databaselogging.</span><span class="sxs-lookup"><span data-stu-id="a9652-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="a9652-133">Veiviseren gir en fleksibel måte å konfigurere logging for tabeller eller felt på.</span><span class="sxs-lookup"><span data-stu-id="a9652-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="a9652-134">Gå til **Systemadministrasjon > Koblinger > Database > Oppsett av databaselogg**.</span><span class="sxs-lookup"><span data-stu-id="a9652-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="a9652-135">Velg **Ny** for å starte veiviseren **Registrerer databaseendringer**.</span><span class="sxs-lookup"><span data-stu-id="a9652-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="a9652-136">Fullfør veiviseren.</span><span class="sxs-lookup"><span data-stu-id="a9652-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="a9652-137">Rydder opp i databaselogger</span><span class="sxs-lookup"><span data-stu-id="a9652-137">Clean up database logs</span></span>

<span data-ttu-id="a9652-138">Du kan slette hele eller deler av databaseloggene ved hjelp av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="a9652-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="a9652-139">Velg alle logger for en bestemt tabell.</span><span class="sxs-lookup"><span data-stu-id="a9652-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="a9652-140">Velg bestemte typer databaselogg.</span><span class="sxs-lookup"><span data-stu-id="a9652-140">Select specific types of database log.</span></span>
- <span data-ttu-id="a9652-141">Velg dato og klokkeslett for oppretting av logg.</span><span class="sxs-lookup"><span data-stu-id="a9652-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="a9652-142">Gjør følgende for å konfigurere opprydding i databaselogg:</span><span class="sxs-lookup"><span data-stu-id="a9652-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="a9652-143">Gå til **Systemadministrasjon > Koblinger > Database > Databaselogg**.</span><span class="sxs-lookup"><span data-stu-id="a9652-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="a9652-144">Velg **Opprydding i logg**.</span><span class="sxs-lookup"><span data-stu-id="a9652-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="a9652-145">Velg en metode for valg av logger du vil slette, ved å angi ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="a9652-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="a9652-146">Tabell-ID</span><span class="sxs-lookup"><span data-stu-id="a9652-146">Table ID</span></span>
   - <span data-ttu-id="a9652-147">Loggtype</span><span class="sxs-lookup"><span data-stu-id="a9652-147">Type of log</span></span>
   - <span data-ttu-id="a9652-148">Opprettingsdato og -klokkeslett</span><span class="sxs-lookup"><span data-stu-id="a9652-148">Created date and time</span></span>

3. <span data-ttu-id="a9652-149">Bruk kategorien **Opprydding i databaselogg** for å bestemme når du vil kjøre loggoppryddingsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="a9652-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="a9652-150">Som standard er databaselogger tilgjengelige i 30 dager.</span><span class="sxs-lookup"><span data-stu-id="a9652-150">By default, database logs are available for 30 days.</span></span>
