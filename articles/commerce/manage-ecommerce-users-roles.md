---
title: Behandle brukere og roller for e-handel
description: Dette emnet forklarer hvordan du gir brukere tilgang til redigeringsmiljøet for området for Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255925"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="8c21f-103">Behandle brukere og roller for e-handel</span><span class="sxs-lookup"><span data-stu-id="8c21f-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8c21f-104">Dette emnet forklarer hvordan du gir brukere tilgang til redigeringsmiljøet for området for Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8c21f-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="8c21f-105">For å kontrollere brukertilgang og gi brukere tillatelse til å utføre bestemte oppgaver, bruker områderedigeringsmiljøet sikkerhetsgrupper som du oppretter i Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="8c21f-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="8c21f-106">Du tilordner først en ny eller eksisterende sikkerhetsgruppe fra Azure AD til hver rolle i redigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="8c21f-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="8c21f-107">Deretter kan du gi eller oppheve tillatelser for enkeltbrukere ved å legge til disse brukerne i en passende sikkerhetsgruppe eller fjerne dem fra en sikkerhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c21f-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="8c21f-108">Oversikt over roller i redigeringsmiljøet</span><span class="sxs-lookup"><span data-stu-id="8c21f-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="8c21f-109">Redigeringsmiljøet for Dynamics 365 for Commerce støtter følgende roller.</span><span class="sxs-lookup"><span data-stu-id="8c21f-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="8c21f-110">Rolle</span><span class="sxs-lookup"><span data-stu-id="8c21f-110">Role</span></span>                 | <span data-ttu-id="8c21f-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8c21f-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="8c21f-112">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="8c21f-112">System Administrator</span></span> | <span data-ttu-id="8c21f-113">Brukere som har denne rollen, har alle rettigheter til alle verktøy og til alle vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="8c21f-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="8c21f-114">De kan også opprette områder.</span><span class="sxs-lookup"><span data-stu-id="8c21f-114">They can also create sites.</span></span> |
| <span data-ttu-id="8c21f-115">Administrator</span><span class="sxs-lookup"><span data-stu-id="8c21f-115">Administrator</span></span>   | <span data-ttu-id="8c21f-116">Brukere som har denne rollen, har alle rettigheter for alle verktøy samt vurderinger og omtaler i en gitt områdestruktur.</span><span class="sxs-lookup"><span data-stu-id="8c21f-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="8c21f-117">Nettprodusent</span><span class="sxs-lookup"><span data-stu-id="8c21f-117">Web Producer</span></span>         | <span data-ttu-id="8c21f-118">Brukere som har denne rollen, kan opprette sider, fragmenter og maler, laste opp og administrere aktiva og supplere produkter og kategorier.</span><span class="sxs-lookup"><span data-stu-id="8c21f-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="8c21f-119">Leser</span><span class="sxs-lookup"><span data-stu-id="8c21f-119">Reader</span></span>               | <span data-ttu-id="8c21f-120">Brukere som har denne rollen, kan vise sider, maler, gjenstander, fragmenter, oppsett og innstillinger, men kan ikke utføre endringer.</span><span class="sxs-lookup"><span data-stu-id="8c21f-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="8c21f-121">Moderator for vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="8c21f-121">RnR Moderator</span></span>        | <span data-ttu-id="8c21f-122">Brukere som har denne rollen, kan sensurere produktvurderinger.</span><span class="sxs-lookup"><span data-stu-id="8c21f-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="8c21f-123">Systemansvarlig-rollen</span><span class="sxs-lookup"><span data-stu-id="8c21f-123">System Administrator role</span></span>

<span data-ttu-id="8c21f-124">Når du klargjør Dynamics 365 Commerce i Microsoft Dynamics Lifecycle Services (LCS)-miljøet, blir du bedt om å oppgi en sikkerhetsgruppe for **Systemansvarlig**-rollen.</span><span class="sxs-lookup"><span data-stu-id="8c21f-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="8c21f-125">Denne rollen brukes deretter automatisk på alle områder du oppretter i miljøet du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="8c21f-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="8c21f-126">Sikkerhetsgruppen for denne rollen kan bare oppdateres i LCS.</span><span class="sxs-lookup"><span data-stu-id="8c21f-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="8c21f-127">På siden **Områdeadministrasjon** for alle områder vises den som skrivebeskyttet og er bare til informasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="8c21f-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="8c21f-128">Administrator-rollen</span><span class="sxs-lookup"><span data-stu-id="8c21f-128">Administrator role</span></span>

<span data-ttu-id="8c21f-129">Når du oppretter et nytt område i Commerce, blir du bedt om å angi en sikkerhetsgruppe for **Administrator**-rollen.</span><span class="sxs-lookup"><span data-stu-id="8c21f-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="8c21f-130">Se tabellen tidligere i dette emnet hvis du vil ha en oversikt over hvilke tillatelser denne rollen gir.</span><span class="sxs-lookup"><span data-stu-id="8c21f-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="8c21f-131">Legge til eller oppdatere sikkerhetsgrupper</span><span class="sxs-lookup"><span data-stu-id="8c21f-131">Add or update security groups</span></span>

<span data-ttu-id="8c21f-132">Når området er opprettet, har bare brukere som er i sikkerhetsgruppene som er tilknyttet **Systemansvarlig**- og **Administrator**-rollene, tilgang til redigeringsmiljøet for området.</span><span class="sxs-lookup"><span data-stu-id="8c21f-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="8c21f-133">Hvis du vil tilordne brukere til **Nettprodusent**,- **Moderator for vurderinger og omtaler**- og **Leser** -rollene, må du tilordne sikkerhetsgrupper til disse rollene.</span><span class="sxs-lookup"><span data-stu-id="8c21f-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="8c21f-134">Hvis du vil legge til en sikkerhetsgruppe i en rolle eller oppdatere en sikkerhetsgruppe som for øyeblikket er tilordnet en rolle, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8c21f-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="8c21f-135">Gå til området du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="8c21f-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="8c21f-136">Åpne **Sikkerhet**-siden i **Områdebehandling**.</span><span class="sxs-lookup"><span data-stu-id="8c21f-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="8c21f-137">Velg rollen du vil endre.</span><span class="sxs-lookup"><span data-stu-id="8c21f-137">Select the role to modify.</span></span>
1. <span data-ttu-id="8c21f-138">Legg til sikkerhetsgrupper i roller, eller fjern sikkerhetsgrupper fra roller.</span><span class="sxs-lookup"><span data-stu-id="8c21f-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c21f-139">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8c21f-139">Additional resources</span></span>

[<span data-ttu-id="8c21f-140">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="8c21f-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="8c21f-141">Vurderinger for søkemotoroptimalisering (SEO) for området</span><span class="sxs-lookup"><span data-stu-id="8c21f-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="8c21f-142">Behandle policy for innholdssikkerhet (CSP)</span><span class="sxs-lookup"><span data-stu-id="8c21f-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]