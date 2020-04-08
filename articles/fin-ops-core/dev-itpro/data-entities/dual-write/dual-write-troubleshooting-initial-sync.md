---
title: Feilsøke problemer under første synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172720"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="0c5d1-103">Feilsøke problemer under første synkronisering</span><span class="sxs-lookup"><span data-stu-id="0c5d1-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0c5d1-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="0c5d1-105">Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="0c5d1-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0c5d1-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="0c5d1-108">Se etter innledende synkroniseringsfeil i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="0c5d1-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="0c5d1-109">Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="0c5d1-110">Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="0c5d1-111">Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="0c5d1-113">Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel</span><span class="sxs-lookup"><span data-stu-id="0c5d1-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="0c5d1-114">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="0c5d1-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0c5d1-115">Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="0c5d1-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="0c5d1-116">*Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="0c5d1-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="0c5d1-117">Her er et eksempel på hele feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="0c5d1-118">Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="0c5d1-119">Logg på den virtuelle maskinen for Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c5d1-120">Åpne Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="0c5d1-121">I **Tjenester**-ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="0c5d1-122">Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="0c5d1-123">Innledende synkroniseringsfeil: 403 forbudt</span><span class="sxs-lookup"><span data-stu-id="0c5d1-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="0c5d1-124">Du kan få følgende feilmelding under innledende synkronisering:</span><span class="sxs-lookup"><span data-stu-id="0c5d1-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="0c5d1-125">*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*</span><span class="sxs-lookup"><span data-stu-id="0c5d1-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="0c5d1-126">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0c5d1-127">Logg på Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="0c5d1-128">På siden **Azure Active Directory-programmer** sletter du **DtAppID**-klienten, og deretter legger du den til på nytt.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="0c5d1-130">Selvreferansefeil under innledende synkronisering</span><span class="sxs-lookup"><span data-stu-id="0c5d1-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="0c5d1-131">Du kan få en feilmelding som ligner på følgende eksempel hvis noen av tilordningene har selvreferanser:</span><span class="sxs-lookup"><span data-stu-id="0c5d1-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="0c5d1-132">*På leverandører V2, følgende feil: Post-ID: ny post, ErrorMessage: Kunne ikke løse GUIDen for feltet: msdyn\_invoicevendoraccountnumber.msdyn:\_vendoraccountnumber. Oppslagsverdien ble ikke funnet: CN-001. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="0c5d1-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="0c5d1-133">Denne typen feil oppstår under innledende synkronisering av tilordninger som har selvreferanser.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="0c5d1-134">I det foregående eksemplet refererer feltfakturakontoen til leverandørenheten.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="0c5d1-135">Hvis du vil løse problemet, må du kanskje kjøre tilordningen to ganger før den første synkroniseringen er vellykket.</span><span class="sxs-lookup"><span data-stu-id="0c5d1-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

