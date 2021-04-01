---
title: Feilsøke innkommende lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250888"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="a482a-103">Feilsøke innkommende lageroperasjoner</span><span class="sxs-lookup"><span data-stu-id="a482a-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a482a-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a482a-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="a482a-105">Jeg får følgende feilmelding: Kvalitetsordre %1 er generert.</span><span class="sxs-lookup"><span data-stu-id="a482a-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="a482a-106">Finner ikke gruppeprofil. Kontroller konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="a482a-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a482a-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a482a-107">Issue description</span></span>

<span data-ttu-id="a482a-108">Denne feilmeldingen er knyttet til en mottaksprosess der kvalitetsstyring (QMS) er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a482a-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="a482a-109">Avhengig av konfigurasjonene i miljøet ditt kan flere detaljer om transaksjonen som genererer feilmeldingen, hjelpe deg med å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="a482a-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a482a-110">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a482a-110">Issue resolution</span></span>

<span data-ttu-id="a482a-111">Først kontrollerer du konfigurasjonen for [gruppeplukking](set-up-cluster-picking.md) og kontrollerer at gruppeprofilene er riktig konfigurert.</span><span class="sxs-lookup"><span data-stu-id="a482a-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="a482a-112">Du kan ikke bruke et menyelement på mobilenheten for gruppeplukking med mindre gruppeprofiler er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="a482a-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="a482a-113">Avhengig av miljøet kan det være at du også må se gjennom andre tilknyttede konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="a482a-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="a482a-114">Mottak av kombinerte nummerskilter virker ikke for noen disposisjonskode, bortsett fra Kredit.</span><span class="sxs-lookup"><span data-stu-id="a482a-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a482a-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a482a-115">Issue description</span></span>

<span data-ttu-id="a482a-116">Når **Handling**-feltet for en disposisjonskode er satt til *Kredit* eller *Svinn*, kan du bare bruke menyelementet [Mottak av kombinerte nummerskilter](mixed-license-plate-receiving.md) til å behandle returnerte varer.</span><span class="sxs-lookup"><span data-stu-id="a482a-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a482a-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a482a-117">Issue resolution</span></span>

<span data-ttu-id="a482a-118">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="a482a-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="a482a-119">For øyeblikket er det bare [disposisjonskoder](../service-management/set-up-disposition-codes.md) der **Handling**-feltet er satt til *Kredit* eller *Svinn*, som støttes for mottak av kombinerte nummerskilter.</span><span class="sxs-lookup"><span data-stu-id="a482a-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="a482a-120">Når jeg kjører den periodiske oppgaven Oppdater produktkvitteringer, bekreftes ubekreftede bestillinger.</span><span class="sxs-lookup"><span data-stu-id="a482a-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a482a-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="a482a-121">Issue description</span></span>

<span data-ttu-id="a482a-122">Når du har kjørt den periodiske oppgaven *Oppdater produktkvitteringer*, bekrefter systemet automatisk ubekreftede bestillinger som har lagertransaksjonsstatusen *Registrert*.</span><span class="sxs-lookup"><span data-stu-id="a482a-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a482a-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="a482a-123">Issue resolution</span></span>

<span data-ttu-id="a482a-124">En ny inngående lastbehandlingsfunksjon, *Overmottak for lastantall*, løser dette problemet.</span><span class="sxs-lookup"><span data-stu-id="a482a-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="a482a-125">Hvis du aktiverer denne funksjonen, går du til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktiverer følgende funksjoner (i rekkefølgen de er oppført):</span><span class="sxs-lookup"><span data-stu-id="a482a-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="a482a-126">Knytt bestillingsbeholdningstransaksjoner til belastning</span><span class="sxs-lookup"><span data-stu-id="a482a-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="a482a-127">Overmottak for belastningsantall</span><span class="sxs-lookup"><span data-stu-id="a482a-127">Over receipt of load quantities</span></span>

<span data-ttu-id="a482a-128">Hvis du vil ha mer informasjon, kan du se [Poster registrerte produktantall mot bestillinger](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="a482a-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]