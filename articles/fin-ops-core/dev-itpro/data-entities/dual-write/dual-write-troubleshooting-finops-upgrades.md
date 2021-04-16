---
title: Feilsøke problemer med oppgradering av Finance and Operations-apper
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av Finance and Operations-apper.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 97509ac662fad6181cbd60e5e0a44f674410acb9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754044"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="fae43-103">Feilsøke problemer med oppgradering av Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="fae43-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="fae43-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fae43-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="fae43-105">Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="fae43-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fae43-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="fae43-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="fae43-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fae43-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="fae43-108">Databasesynkroniseringsfeil</span><span class="sxs-lookup"><span data-stu-id="fae43-108">Database synchronization errors</span></span>

<span data-ttu-id="fae43-109">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="fae43-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="fae43-110">Det kan hende du får en feilmelding som ligner på følgende eksempel når du prøver å bruke tabellen **DualWriteProjectConfiguration** til å oppdatere en Finance and Operations-app til Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="fae43-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="fae43-111">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="fae43-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="fae43-112">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="fae43-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="fae43-113">Åpne Visual Studio som administrator, og åpne applikasjonsobjekttreet.</span><span class="sxs-lookup"><span data-stu-id="fae43-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="fae43-114">Søk etter **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="fae43-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="fae43-115">I applikasjonsobjekttreet høyreklikker du **DualWriteProjectConfiguration** og velger **Legg til i nytt prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="fae43-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="fae43-116">Velg **OK** for å opprette det nye prosjektet som bruker standardalternativer.</span><span class="sxs-lookup"><span data-stu-id="fae43-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="fae43-117">I Løsningsutforsker høyreklikker du **Prosjektegenskaper** og setter **Synkroniser database på build** til **Sann**.</span><span class="sxs-lookup"><span data-stu-id="fae43-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="fae43-118">Bygg prosjektet, og bekreft at byggingen er vellykket.</span><span class="sxs-lookup"><span data-stu-id="fae43-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="fae43-119">Velg **Synkroniser database** på **Dynamics 365**-menyen.</span><span class="sxs-lookup"><span data-stu-id="fae43-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="fae43-120">Velg **Synkroniser** for å utføre en fullstendig databasesynkronisering.</span><span class="sxs-lookup"><span data-stu-id="fae43-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="fae43-121">Når den fullstendige databasesynkroniseringen er fullført, kjører du trinnet for databasesynkronisering på nytt i Microsoft Dynamics Lifecycle Services (LCS) og bruker de manuelle oppgraderingsskriptene, slik at du kan fortsette med oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="fae43-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="fae43-122">Problemer med manglende tabellkolonner i tilordninger</span><span class="sxs-lookup"><span data-stu-id="fae43-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="fae43-123">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="fae43-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="fae43-124">På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:</span><span class="sxs-lookup"><span data-stu-id="fae43-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="fae43-125">*Manglende kildefelt feltnavn \<field name\> i skjemaet.*</span><span class="sxs-lookup"><span data-stu-id="fae43-125">*Missing source field \<field name\> in the schema.*</span></span>

![Eksempel på feilmeldingen om manglende kildekolonne](media/error_missing_field.png)

<span data-ttu-id="fae43-127">Du kan løse problemet ved først å følge disse trinnene for å kontrollere at kolonnene finnes i tabellen.</span><span class="sxs-lookup"><span data-stu-id="fae43-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="fae43-128">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="fae43-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="fae43-129">Gå til **Arbeidsområder \> Databehandling**, velg flisen **Rammeverkparametere** og deretter, i fanen **Tabellinnstillinger**, velger du **Oppdater tabelliste** for å oppdatere tabellene.</span><span class="sxs-lookup"><span data-stu-id="fae43-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="fae43-130">Gå til **Arbeidsområder \> Databehandling**, velg fanen **Datatabeller**, og kontroller at tabellen finnes i listen.</span><span class="sxs-lookup"><span data-stu-id="fae43-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="fae43-131">Hvis tabellen ikke er oppført, logger du på den virtuelle maskinen for Finance and Operations-appen og kontrollerer at tabellen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="fae43-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="fae43-132">Åpne **Tabelltilordning**-siden fra **Dobbel skriving**-siden i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="fae43-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="fae43-133">Velg **Oppdater tabelliste** for å fylle ut kolonnene i tabelltilordningene automatisk.</span><span class="sxs-lookup"><span data-stu-id="fae43-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="fae43-134">Hvis problemet fremdeles ikke er løst, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="fae43-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fae43-135">Denne fremgangsmåten fører deg gjennom prosessen med å slette en tabell og deretter legge den til på nytt.</span><span class="sxs-lookup"><span data-stu-id="fae43-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="fae43-136">Hvis du vil unngå problemer, må du følge fremgangsmåten nøye.</span><span class="sxs-lookup"><span data-stu-id="fae43-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="fae43-137">I Finance and Operations-appen går du til **Arbeidsområder \> Databehandling** og velger flisen **Datatabeller**.</span><span class="sxs-lookup"><span data-stu-id="fae43-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="fae43-138">Finn tabellen som mangler attributtet.</span><span class="sxs-lookup"><span data-stu-id="fae43-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="fae43-139">Klikk **Endre måltilordning** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="fae43-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="fae43-140">Klikk på **Generer tilordning** under **Tilordne oppsamling til mål**.</span><span class="sxs-lookup"><span data-stu-id="fae43-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="fae43-141">Åpne **Tabelltilordning**-siden fra **Dobbel skriving**-siden i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="fae43-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="fae43-142">Hvis attributtet ikke fylles ut automatisk på kartet, legger du det til manuelt ved å klikke **Legg til attributt** og deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fae43-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="fae43-143">Velg kartet, og klikk **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="fae43-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]