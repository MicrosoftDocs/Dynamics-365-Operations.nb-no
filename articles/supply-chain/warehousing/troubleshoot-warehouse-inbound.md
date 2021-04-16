---
title: Feilsøke innkommende lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828232"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="24d07-103">Feilsøke innkommende lageroperasjoner</span><span class="sxs-lookup"><span data-stu-id="24d07-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24d07-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="24d07-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="24d07-105">Jeg får følgende feilmelding: Kvalitetsordre %1 er generert.</span><span class="sxs-lookup"><span data-stu-id="24d07-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="24d07-106">Finner ikke gruppeprofil. Kontroller konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="24d07-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="24d07-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="24d07-107">Issue description</span></span>

<span data-ttu-id="24d07-108">Denne feilmeldingen er knyttet til en mottaksprosess der kvalitetsstyring (QMS) er aktivert.</span><span class="sxs-lookup"><span data-stu-id="24d07-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="24d07-109">Avhengig av konfigurasjonene i miljøet ditt kan flere detaljer om transaksjonen som genererer feilmeldingen, hjelpe deg med å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="24d07-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="24d07-110">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="24d07-110">Issue resolution</span></span>

<span data-ttu-id="24d07-111">Først kontrollerer du konfigurasjonen for [gruppeplukking](set-up-cluster-picking.md) og kontrollerer at gruppeprofilene er riktig konfigurert.</span><span class="sxs-lookup"><span data-stu-id="24d07-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="24d07-112">Du kan ikke bruke et menyelement på mobilenheten for gruppeplukking med mindre gruppeprofiler er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="24d07-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="24d07-113">Avhengig av miljøet kan det være at du også må se gjennom andre tilknyttede konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="24d07-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="24d07-114">Mottak av kombinerte nummerskilter virker ikke for noen disposisjonskode, bortsett fra Kredit.</span><span class="sxs-lookup"><span data-stu-id="24d07-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="24d07-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="24d07-115">Issue description</span></span>

<span data-ttu-id="24d07-116">Når **Handling**-feltet for en disposisjonskode er satt til *Kredit* eller *Svinn*, kan du bare bruke menyelementet [Mottak av kombinerte nummerskilter](mixed-license-plate-receiving.md) til å behandle returnerte varer.</span><span class="sxs-lookup"><span data-stu-id="24d07-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="24d07-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="24d07-117">Issue resolution</span></span>

<span data-ttu-id="24d07-118">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="24d07-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="24d07-119">For øyeblikket er det bare [disposisjonskoder](../service-management/set-up-disposition-codes.md) der **Handling**-feltet er satt til *Kredit* eller *Svinn*, som støttes for mottak av kombinerte nummerskilter.</span><span class="sxs-lookup"><span data-stu-id="24d07-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="24d07-120">Når jeg kjører den periodiske oppgaven Oppdater produktkvitteringer, bekreftes ubekreftede bestillinger.</span><span class="sxs-lookup"><span data-stu-id="24d07-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="24d07-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="24d07-121">Issue description</span></span>

<span data-ttu-id="24d07-122">Når du har kjørt den periodiske oppgaven *Oppdater produktkvitteringer*, bekrefter systemet automatisk ubekreftede bestillinger som har lagertransaksjonsstatusen *Registrert*.</span><span class="sxs-lookup"><span data-stu-id="24d07-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="24d07-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="24d07-123">Issue resolution</span></span>

<span data-ttu-id="24d07-124">En ny inngående lastbehandlingsfunksjon, *Overmottak for lastantall*, løser dette problemet.</span><span class="sxs-lookup"><span data-stu-id="24d07-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="24d07-125">Hvis du aktiverer denne funksjonen, går du til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktiverer følgende funksjoner (i rekkefølgen de er oppført):</span><span class="sxs-lookup"><span data-stu-id="24d07-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="24d07-126">Knytt bestillingsbeholdningstransaksjoner til belastning</span><span class="sxs-lookup"><span data-stu-id="24d07-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="24d07-127">Overmottak for belastningsantall</span><span class="sxs-lookup"><span data-stu-id="24d07-127">Over receipt of load quantities</span></span>

<span data-ttu-id="24d07-128">Hvis du vil ha mer informasjon, kan du se [Poster registrerte produktantall mot bestillinger](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="24d07-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="24d07-129">Når jeg registrerer innkommende ordrer, får jeg følgende feilmelding: "Antallet er ikke gyldig."</span><span class="sxs-lookup"><span data-stu-id="24d07-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="24d07-130">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="24d07-130">Issue description</span></span>

<span data-ttu-id="24d07-131">Hvis feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert* for et menyelement på en mobilenhet som brukes til å registrere innkommende ordrer, får du en feilmelding ("Antallet er ikke gyldig"), og du kan ikke fullføre registreringen.</span><span class="sxs-lookup"><span data-stu-id="24d07-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="24d07-132">Feilårsak</span><span class="sxs-lookup"><span data-stu-id="24d07-132">Issue cause</span></span>

<span data-ttu-id="24d07-133">Når *Brukerdefinert* brukes som en grupperingspolicy for nummerskilt, deler systemet det innkommende lageret i separate nummerskilt, som angitt av enhetsseriegruppen.</span><span class="sxs-lookup"><span data-stu-id="24d07-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="24d07-134">Hvis parti- eller serienumre brukes til å spore varen som mottas, må antallene i hvert parti eller hver serie angis per nummerskilt som er registrert.</span><span class="sxs-lookup"><span data-stu-id="24d07-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="24d07-135">Hvis antallet som er angitt for et nummerskilt, overskrider antallet som fortsatt må mottas for gjeldende dimensjoner, får du feilmeldingen.</span><span class="sxs-lookup"><span data-stu-id="24d07-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="24d07-136">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="24d07-136">Issue resolution</span></span>

<span data-ttu-id="24d07-137">Når du registrerer en vare ved hjelp av et menyelement for mobilenhet der feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert*, kan systemet kreve at du bekrefter eller angir numre på nummerskilt, partinumre eller serienumre.</span><span class="sxs-lookup"><span data-stu-id="24d07-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="24d07-138">På bekreftelsessiden for nummerskiltet viser systemet antallet som er tilordnet for gjeldende nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="24d07-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="24d07-139">På parti- eller seriebekreftelsessidene vil systemet vise antallet som fortsatt må mottas på gjeldende numerskilt.</span><span class="sxs-lookup"><span data-stu-id="24d07-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="24d07-140">Det inkluderer også et felt der du kan angi antallet som skal registreres for denne kombinasjonen av nummerskilt og parti- eller serienummer.</span><span class="sxs-lookup"><span data-stu-id="24d07-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="24d07-141">I så fall må du sørge for at antallet som blir registrert for nummerskiltet, ikke overskrider antallet som fortsatt må mottas.</span><span class="sxs-lookup"><span data-stu-id="24d07-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="24d07-142">Hvis det genereres for mange lisensavtaler ved innkommende ordreregistrering, kan verdien i feltet **Grupperingspolicy for numerskilt** endres til *Gruppering av nummerskilt*, en ny enhetssekvensgruppe kan tilordnes varen, eller alternativet **Gruppering av nummerskilt** for enhetssekvensgruppen kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="24d07-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
