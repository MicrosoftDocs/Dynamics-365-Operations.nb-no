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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477930"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="9f90c-103">Kanaloppsettsforutsetninger</span><span class="sxs-lookup"><span data-stu-id="9f90c-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f90c-104">Dette emnet viser en oversikt over forutsetninger for kanaloppsett i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9f90c-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9f90c-105">Før en Dynamics 365 Commerce-kanal kan opprettes, må du fullføre en rekke nødvendige oppgaver.</span><span class="sxs-lookup"><span data-stu-id="9f90c-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="9f90c-106">Følgende lister over nødvendige oppgaver er ordnet etter kanaltype.</span><span class="sxs-lookup"><span data-stu-id="9f90c-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="9f90c-107">Det skrives fremdeles en del dokumentasjon, og koblingene blir oppdatert etter hvert som nytt innhold publiseres.</span><span class="sxs-lookup"><span data-stu-id="9f90c-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="9f90c-108">Initialisering</span><span class="sxs-lookup"><span data-stu-id="9f90c-108">Initialization</span></span>

- [<span data-ttu-id="9f90c-109">Initialisere utgangsverdidata</span><span class="sxs-lookup"><span data-stu-id="9f90c-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="9f90c-110">Globale forutsetninger kreves for alle kanaltyper</span><span class="sxs-lookup"><span data-stu-id="9f90c-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="9f90c-111">Definere og konfigurere strukturen for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="9f90c-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="9f90c-112">Konfigurere organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="9f90c-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="9f90c-113">Definere et lager</span><span class="sxs-lookup"><span data-stu-id="9f90c-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="9f90c-114">Konfigurere merverdiavgift</span><span class="sxs-lookup"><span data-stu-id="9f90c-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="9f90c-115">Definere en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="9f90c-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="9f90c-116">Definere nummerserier</span><span class="sxs-lookup"><span data-stu-id="9f90c-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="9f90c-117">Definere en standardkunde og adressebok</span><span class="sxs-lookup"><span data-stu-id="9f90c-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="9f90c-118">Forutsetninger for detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="9f90c-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="9f90c-119">Informasjonskoder og informasjonskodegrupper</span><span class="sxs-lookup"><span data-stu-id="9f90c-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="9f90c-120">Definere en funksjonalitetsprofil for detaljhandel</span><span class="sxs-lookup"><span data-stu-id="9f90c-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="9f90c-121">Konfigurere en adressebok for ansatt</span><span class="sxs-lookup"><span data-stu-id="9f90c-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="9f90c-122">Definere et skjermoppsett</span><span class="sxs-lookup"><span data-stu-id="9f90c-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="9f90c-123">Konfigurere en maskinvarestasjon</span><span class="sxs-lookup"><span data-stu-id="9f90c-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="9f90c-124">Forutsetninger for telefonsenterkanal</span><span class="sxs-lookup"><span data-stu-id="9f90c-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="9f90c-125">Telefonsenterparametere</span><span class="sxs-lookup"><span data-stu-id="9f90c-125">Call center parameters</span></span>
- [<span data-ttu-id="9f90c-126">Telefonsenterordrer og refusjonsbetalingsmåter</span><span class="sxs-lookup"><span data-stu-id="9f90c-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="9f90c-127">Leveringsmåter og tillegg for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="9f90c-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="9f90c-128">Forutsetninger for nettkanal</span><span class="sxs-lookup"><span data-stu-id="9f90c-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="9f90c-129">Opprette en nettbasert funksjonalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="9f90c-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="9f90c-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9f90c-130">Additional resources</span></span>

[<span data-ttu-id="9f90c-131">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="9f90c-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9f90c-132">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="9f90c-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9f90c-133">Definere organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="9f90c-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="9f90c-134">Opprett juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="9f90c-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="9f90c-135">Definere en detaljhandelskanal</span><span class="sxs-lookup"><span data-stu-id="9f90c-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="9f90c-136">Definere en Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="9f90c-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
