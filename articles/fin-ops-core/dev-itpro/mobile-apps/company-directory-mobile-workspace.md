---
title: Mobilt arbeidsområde for firmakatalog
description: Dette emnet gir informasjon om det mobile arbeidsområdet for firmakatalog, som lar brukere vise og kontakte andre ansatte i organisasjonen.
author: jcart1106
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0b397f3a222ff6957ad4904df90c5db218903090
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748203"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="f693d-103">Mobilt arbeidsområde for firmakatalog</span><span class="sxs-lookup"><span data-stu-id="f693d-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f693d-104">Dette emnet gir informasjon om det mobile arbeidsområdet **Firmakatalog**.</span><span class="sxs-lookup"><span data-stu-id="f693d-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="f693d-105">Dette arbeidsområdet lar brukere vise og kontakte andre ansatte i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f693d-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="f693d-106">Dette mobile arbeidsområdet kan brukes med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="f693d-106">This mobile workspace can be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="f693d-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f693d-107">Overview</span></span>
<span data-ttu-id="f693d-108">Det mobile arbeidsområdet **Firmakatalog** lar brukere utføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="f693d-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="f693d-109">Vis en liste over ansatte i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f693d-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="f693d-110">Søk etter ansatte i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f693d-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="f693d-111">Vis kontaktinformasjon for ansatte.</span><span class="sxs-lookup"><span data-stu-id="f693d-111">View contact information for employees.</span></span>
- <span data-ttu-id="f693d-112">Kontakt ansatte fra profilinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="f693d-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f693d-113">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="f693d-113">Prerequisites</span></span>
<span data-ttu-id="f693d-114">Før du kan bruke dette mobile arbeidsområdet, må du oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="f693d-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f693d-115">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="f693d-115">Prerequisite</span></span></th>
<th><span data-ttu-id="f693d-116">Rolle</span><span class="sxs-lookup"><span data-stu-id="f693d-116">Role</span></span></th>
<th><span data-ttu-id="f693d-117">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f693d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f693d-118">Et av følgende produkter må distribueres i organisasjonen:</span><span class="sxs-lookup"><span data-stu-id="f693d-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="f693d-119">En Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="f693d-119">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="f693d-120">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f693d-120">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="f693d-121">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="f693d-121">System administrator</span></span></td>
<td><span data-ttu-id="f693d-122">Hvis du ikke allerede har en Finance and Operations-app distribuert i organisasjonen, kan du se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="f693d-122">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="f693d-123">Hvis du ikke allerede har Human Resources distribuert i organisasjonen, kan systemansvarlig få tilgang til en prøveversjon fra <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources-nettsiden</a>.</span><span class="sxs-lookup"><span data-stu-id="f693d-123">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f693d-124">Det mobile arbeidsområdet <strong>Firmakatalog</strong> må publiseres.</span><span class="sxs-lookup"><span data-stu-id="f693d-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="f693d-125">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="f693d-125">System administrator</span></span></td>
<td><span data-ttu-id="f693d-126">Se <a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="f693d-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="f693d-127">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="f693d-127">Download and install the mobile app</span></span>
<span data-ttu-id="f693d-128">Laste ned og installere Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="f693d-128">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="f693d-129">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="f693d-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="f693d-130">For iPhone</span><span class="sxs-lookup"><span data-stu-id="f693d-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="f693d-131">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="f693d-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="f693d-132">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="f693d-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="f693d-133">Angi URL-adressen for Microsoft Dynamics365.</span><span class="sxs-lookup"><span data-stu-id="f693d-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="f693d-134">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="f693d-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="f693d-135">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="f693d-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="f693d-136">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="f693d-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="f693d-137">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="f693d-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="f693d-138">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="f693d-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="f693d-139">Vise firmakatalogen ved hjelp av det mobile arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="f693d-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="f693d-140">Velg arbeidsområdet **Firmakatalog** i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="f693d-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="f693d-141">Det vises en liste over ansatte.</span><span class="sxs-lookup"><span data-stu-id="f693d-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="f693d-142">Velg en ansatt.</span><span class="sxs-lookup"><span data-stu-id="f693d-142">Select an employee.</span></span> <span data-ttu-id="f693d-143">Siden **Ansattprofil** vises.</span><span class="sxs-lookup"><span data-stu-id="f693d-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="f693d-144">Informasjonen på denne siden inneholder den ansattes fornavn, etternavn, tittel og avdeling.</span><span class="sxs-lookup"><span data-stu-id="f693d-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="f693d-145">Søke etter firmakatalogen ved hjelp av det mobile arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="f693d-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="f693d-146">Velg arbeidsområdet **Firmakatalog** i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="f693d-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="f693d-147">I **Søk**-feltet skriver du inn den ansattes fornavn, etternavn, tittel eller avdeling for å starte søket.</span><span class="sxs-lookup"><span data-stu-id="f693d-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="f693d-148">Velg en ansatt.</span><span class="sxs-lookup"><span data-stu-id="f693d-148">Select an employee.</span></span> <span data-ttu-id="f693d-149">Siden **Ansattprofil** vises.</span><span class="sxs-lookup"><span data-stu-id="f693d-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="f693d-150">Informasjonen på denne siden inneholder den ansattes fornavn, etternavn, tittel og avdeling.</span><span class="sxs-lookup"><span data-stu-id="f693d-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]