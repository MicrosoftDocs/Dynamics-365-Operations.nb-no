---
title: Forutsetninger for kanaloppsett
description: Dette emnet viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113788"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="78643-103">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="78643-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="78643-104">Dette emnet viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="78643-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="78643-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="78643-105">Overview</span></span>

<span data-ttu-id="78643-106">Før en Dynamics 365 Commerce-kanal kan opprettes, må du fullføre en rekke nødvendige oppgaver.</span><span class="sxs-lookup"><span data-stu-id="78643-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="78643-107">Følgende lister over nødvendige oppgaver er ordnet etter kanaltype.</span><span class="sxs-lookup"><span data-stu-id="78643-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="78643-108">Det skrives fremdeles en del dokumentasjon, og koblingene blir oppdatert etter hvert som nytt innhold publiseres.</span><span class="sxs-lookup"><span data-stu-id="78643-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="78643-109">Initialisering</span><span class="sxs-lookup"><span data-stu-id="78643-109">Initialization</span></span>

- [<span data-ttu-id="78643-110">Initialisere utgangsverdidata</span><span class="sxs-lookup"><span data-stu-id="78643-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="78643-111">Globale forutsetninger kreves for alle kanaltyper</span><span class="sxs-lookup"><span data-stu-id="78643-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="78643-112">Definere og konfigurere strukturen for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="78643-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="78643-113">Konfigurere organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="78643-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="78643-114">Definere et lager</span><span class="sxs-lookup"><span data-stu-id="78643-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="78643-115">Konfigurere merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="78643-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="78643-116">Definere en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="78643-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="78643-117">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="78643-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="78643-118">Definere en standardkunde og adressebok</span><span class="sxs-lookup"><span data-stu-id="78643-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="78643-119">Forutsetninger for detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="78643-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="78643-120">Informasjonskoder og informasjonskodegrupper</span><span class="sxs-lookup"><span data-stu-id="78643-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="78643-121">Definere en funksjonalitetsprofil for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="78643-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="78643-122">Konfigurere en adressebok for ansatt</span><span class="sxs-lookup"><span data-stu-id="78643-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="78643-123">Definere et skjermoppsett</span><span class="sxs-lookup"><span data-stu-id="78643-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="78643-124">Konfigurere en maskinvarestasjon</span><span class="sxs-lookup"><span data-stu-id="78643-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="78643-125">Forutsetninger for telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="78643-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="78643-126">Telefonsenterparametere</span><span class="sxs-lookup"><span data-stu-id="78643-126">Call center parameters</span></span>
- [<span data-ttu-id="78643-127">Telefonsenterordrer og refusjonsbetalingsmåter</span><span class="sxs-lookup"><span data-stu-id="78643-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="78643-128">Leveringsmåter og tillegg for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="78643-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="78643-129">Forutsetninger for nettkanal</span><span class="sxs-lookup"><span data-stu-id="78643-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="78643-130">Opprette en nettbasert funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="78643-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="78643-131">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="78643-131">Additional resources</span></span>

[<span data-ttu-id="78643-132">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="78643-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="78643-133">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="78643-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="78643-134">Definere organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="78643-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="78643-135">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="78643-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="78643-136">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="78643-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="78643-137">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="78643-137">Set up an online channel</span></span>](channel-setup-online.md)
