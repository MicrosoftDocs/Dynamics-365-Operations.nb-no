---
title: Legge til en adresse i en serviceordre
description: Dette emnet beskriver hvordan du legger til en kundeadresse i en serviceordre.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "311916"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="00d28-103">Legge til en adresse i en serviceordre</span><span class="sxs-lookup"><span data-stu-id="00d28-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="00d28-104">Dette emnet beskriver hvordan du legger til en kundeadresse i en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="00d28-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="00d28-105">Når du oppretter en serviceordre, overføres adresseinformasjonen fra prosjektet som serviceordren er knyttet til.</span><span class="sxs-lookup"><span data-stu-id="00d28-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="00d28-106">Du kan imidlertid velge en alternativ lokasjon fra adressene som allerede er angitt i Microsoft Dynamics AX for kunder, leverandører, områder, lagre, serviceordrer og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="00d28-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="00d28-107">Du kan også opprette en ny adresse.</span><span class="sxs-lookup"><span data-stu-id="00d28-107">You can also create a new address.</span></span> <span data-ttu-id="00d28-108">Den nye adressen overføres som standard til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="00d28-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="00d28-109">Du kan imidlertid angi at den nye adressen bare gjelder for denne forekomsten av servicen.</span><span class="sxs-lookup"><span data-stu-id="00d28-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="00d28-110">Hvis du gjør dette, overføres ikke den nye adressen til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="00d28-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="00d28-111">Opprette en kundeadresse for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="00d28-111">Create a customer address for a service order</span></span>

<span data-ttu-id="00d28-112">Hvis du vil legge til en adresse i en serviceordre, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="00d28-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="00d28-113">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="00d28-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="00d28-114">Åpne serviceordren som du vil opprette en adresse for.</span><span class="sxs-lookup"><span data-stu-id="00d28-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="00d28-115">I **handlingsruten** klikker du på **Rediger** og deretter på **Topptekstvisning**.</span><span class="sxs-lookup"><span data-stu-id="00d28-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="00d28-116">På hurtigfanen **Adresse** klikker du på **Legg til adresse**.</span><span class="sxs-lookup"><span data-stu-id="00d28-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="00d28-117">I **Ny adresse**-skjemaet angir du et unikt navn for adressen og fyller ut de gjenstående feltene.</span><span class="sxs-lookup"><span data-stu-id="00d28-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="00d28-118">Hvis du angir samme navn som en eksisterende adresse, overskriver informasjonen du angir i de gjenstående feltene, informasjon for den eksisterende adressen.</span><span class="sxs-lookup"><span data-stu-id="00d28-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="00d28-119">Klikk **OK** for å kopiere den nye adressen til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="00d28-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="00d28-120">Angi en alternativ adresse på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="00d28-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="00d28-121">Hvis du vil legge til en alternativ adresse i en serviceordre, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="00d28-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="00d28-122">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="00d28-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="00d28-123">Åpne serviceordren som du vil angi en alternativ adresse for.</span><span class="sxs-lookup"><span data-stu-id="00d28-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="00d28-124">I **handlingsruten** klikker du på **Rediger** og deretter på **Topptekstvisning**.</span><span class="sxs-lookup"><span data-stu-id="00d28-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="00d28-125">På hurtigfanen **Adresse** klikker du på **Annen adresse**.</span><span class="sxs-lookup"><span data-stu-id="00d28-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="00d28-126">I skjemaet **Adressevalg**, i feltet **Oppføringstype** velger du **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="00d28-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="00d28-127">Velg en adresse, og klikk deretter **OK** for å kopiere den til serviceordren.</span><span class="sxs-lookup"><span data-stu-id="00d28-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


