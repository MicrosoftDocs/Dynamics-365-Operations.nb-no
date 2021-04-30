---
title: Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering
description: Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908473"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="13cbc-103">Oversikt over Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="13cbc-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13cbc-104">Dette emnet gir en oversikt over Microsoft Dynamics 365 Commerce- og Microsoft Teams-integrering.</span><span class="sxs-lookup"><span data-stu-id="13cbc-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="13cbc-105">Dynamics 365 Commerce integreres med Teams for å hjelpe kundene og de ansatte med å forbedre produktiviteten ved å synkronisere oppgaveadministrasjon mellom de to programmene.</span><span class="sxs-lookup"><span data-stu-id="13cbc-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="13cbc-106">Den sømløse oppgaveadministrasjonen som Commerce- og Teams-integrering gir, lar butikksjefer og ansatte opprette oppgavelister, tilordne oppgaver til flere butikker og spore statusen til oppgaver på tvers av butikker, fra begge programmene.</span><span class="sxs-lookup"><span data-stu-id="13cbc-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="13cbc-107">Commerce- og Teams-integrering er tilgjengelig fra Commerce versjon 10.0.18.</span><span class="sxs-lookup"><span data-stu-id="13cbc-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="13cbc-108">Hovedfunksjoner</span><span class="sxs-lookup"><span data-stu-id="13cbc-108">Key features</span></span>

<span data-ttu-id="13cbc-109">Her er noen av nøkkelfunksjonene som Commerce- og Microsoft Teams-integreringen gir:</span><span class="sxs-lookup"><span data-stu-id="13cbc-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="13cbc-110">Klargjør Teams ved å dra nytte av veldefinert informasjon fra Commerce, for eksempel organisasjonsstrukturen og informasjon om butikker, arbeidere, tillatelser og forretningskontekst.</span><span class="sxs-lookup"><span data-stu-id="13cbc-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="13cbc-111">Du kan enkelt synkronisere pågående endringer (for eksempel tilføyelse av nye butikker eller ansettelse av nye medarbeidere) mellom Commerce og Teams, men beholde Commerce som hovedkilden for organisasjonsstrukturdata.</span><span class="sxs-lookup"><span data-stu-id="13cbc-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="13cbc-112">Integrer oppgaveadministrasjon mellom Commerce og Teams for å hjelpe butikkarbeidere, butikksjefer, regionsjefer og kommunikasjonsledere med å håndtere oppgavebehandling fra begge programmene.</span><span class="sxs-lookup"><span data-stu-id="13cbc-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="13cbc-113">Forutsetninger for å bruke integreringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="13cbc-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="13cbc-114">Følgende forutsetninger må være på plass før du kan begynne å bruke Microsoft Teams-integreringsfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="13cbc-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="13cbc-115">Microsoft 365 Business-standardlisens (Denne lisensen inkluderer Teams.)</span><span class="sxs-lookup"><span data-stu-id="13cbc-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="13cbc-116">Azure Active Directory-kontoer (Azure AD) for alle butikksjefer og arbeidere</span><span class="sxs-lookup"><span data-stu-id="13cbc-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="13cbc-117">Systemer på salgsstedet (POS-systemer) som er konfigurert med Azure AD-godkjenning</span><span class="sxs-lookup"><span data-stu-id="13cbc-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="13cbc-118">Konseptuell arkitektur</span><span class="sxs-lookup"><span data-stu-id="13cbc-118">Conceptual architecture</span></span>

<span data-ttu-id="13cbc-119">Illustrasjonen nedenfor viser den konseptuelle arkitekturen bak Dynamics 365 Commerce- og Microsoft Teams-integrering, ved å bruke en butikk i San Francisco som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="13cbc-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="13cbc-120">Både Teams og Commerce POS-programmet bruker Microsoft Planner som et repositorium, slik at oppgaver som publiseres fra Teams, vises i POS-programmet. og ad hoc-oppgaver som opprettes av butikksjefer i POS-programmet, vises i Teams, noe som resulterer i en sømløs oppgavebehandlingsopplevelse mellom programmene.</span><span class="sxs-lookup"><span data-stu-id="13cbc-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Arkitekturen bak Commerce og Teams-integrering](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="13cbc-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="13cbc-122">Additional resources</span></span>

[<span data-ttu-id="13cbc-123">Aktiver Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="13cbc-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="13cbc-124">Klargjøring av Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="13cbc-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="13cbc-125">Synkroniser oppgavebehandling mellom Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="13cbc-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="13cbc-126">Behandle brukerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="13cbc-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="13cbc-127">Tilordne butikker og grupper hvis det finnes eksisterende grupper i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="13cbc-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="13cbc-128">Vanlige spørsmål om Dynamics 365 Commerce- og Microsoft Teams-integrering</span><span class="sxs-lookup"><span data-stu-id="13cbc-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
