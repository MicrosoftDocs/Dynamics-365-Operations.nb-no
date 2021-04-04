---
title: Opprette serviceordrer manuelt
description: Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470959"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="a63d5-103">Opprette serviceordrer manuelt</span><span class="sxs-lookup"><span data-stu-id="a63d5-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a63d5-104">Du kan opprette serviceordrer manuelt ved å bruke en serviceavtale eller ved å bruke **Serviceordrer**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a63d5-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="a63d5-105">Du kan også opprette en serviceordre fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a63d5-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="a63d5-106">Du kan bruke automatiserte prosesser til å opprette serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="a63d5-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="a63d5-107">Opprette en serviceordre manuelt fra en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="a63d5-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="a63d5-108">Velg **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a63d5-109">Velg en serviceavtale eller opprett en ny serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="a63d5-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="a63d5-110">Velg fanen **Lever**, og i gruppen **Opprett** velger du **Planlagte serviceordrer** for å åpne skjemaet **Opprett serviceordre**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="a63d5-111">Opprette en serviceordre manuelt i Serviceordrer-skjemaet</span><span class="sxs-lookup"><span data-stu-id="a63d5-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="a63d5-112">Velg **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a63d5-113">Velg **Ny** for å opprette en ny serviceordre.</span><span class="sxs-lookup"><span data-stu-id="a63d5-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="a63d5-114">Opprett serviceordrelinjer for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a63d5-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a63d5-115">Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="a63d5-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a63d5-116">Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="a63d5-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="a63d5-117">Opprette en serviceordre fra et prosjekt</span><span class="sxs-lookup"><span data-stu-id="a63d5-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="a63d5-118">Gå til **Prosjektstyring og regnskap** \> **Felles** \> **Prosjekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="a63d5-119">I skjemaet **Prosjekter** i **handlingsruten** velger du fanen **Administrer** \> og velger **Tjeneste** \> **Tjenesteordrer**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="a63d5-120">Følg forrige fremgangsmåte for å opprette en serviceordre manuelt i **Serviceordrer**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="a63d5-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="a63d5-121">Feltet **Prosjekt-ID** viser prosjektreferansen.</span><span class="sxs-lookup"><span data-stu-id="a63d5-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a63d5-122">Hvis det er merket av for <STRONG>Tillat uten serviceavtale</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>, kan du postere transaksjonene fra serviceordrelinjene uten å knytte serviceordren til en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="a63d5-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a63d5-123">Hvis avmerkingen er fjernet, må du knytte den manuelt opprettede serviceordren til et prosjekt før du posterer serviceordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="a63d5-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="a63d5-124">Opprette en serviceordre fra Salgsordre-skjemaet</span><span class="sxs-lookup"><span data-stu-id="a63d5-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="a63d5-125">Du kan opprette en serviceordre fra skjemaet **Salgsordrer** ved å bruke veiviseren **Opprett en ny serviceordre basert på salgsordren**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="a63d5-126">Gå til **Salg og markedsføring** \> **Vanlig** \> **Salgsordrer** \> **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="a63d5-127">Åpne den relevante salgsordren.</span><span class="sxs-lookup"><span data-stu-id="a63d5-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="a63d5-128">På fanen **Salgsordre** velger du **Serviceordre** for å starte veiviseren **Opprett en ny serviceordre basert på salgsordren**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="a63d5-129">Velg **Neste \>**, og følg trinnene nedenfor på siden **Velg avtale for serviceordre**:</span><span class="sxs-lookup"><span data-stu-id="a63d5-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="a63d5-130">Bruk **Serviceavtale**-feltet til å velge serviceavtalen som den nye serviceordren skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="a63d5-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="a63d5-131">(Valgfritt): Bruk feltet **Prosjekt-ID** til å knytte denne serviceordren til et bestemt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a63d5-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="a63d5-132">Velg **Neste \>**, og følg trinnene nedenfor på siden **Opprett serviceordre**:</span><span class="sxs-lookup"><span data-stu-id="a63d5-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="a63d5-133">Angi en dato og et klokkeslett for servicebesøkets begynnelse i feltet **Foretrukket servicetidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="a63d5-134">Valgfritt: Endre teksten i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="a63d5-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="a63d5-135">Dette feltet inneholder som standard beskrivelsen av serviceavtalen du valgte på forrige side.</span><span class="sxs-lookup"><span data-stu-id="a63d5-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="a63d5-136">I **Ansvarlig**-feltet velger du ID-en til den ansatte som er ansvarlig for avtalen. Hvis du kjenner til den, kan du også angi ID-en til kundens foretrukne tekniker for servicebesøk.</span><span class="sxs-lookup"><span data-stu-id="a63d5-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="a63d5-137">I feltet **Kontakt-ID** velger du personen i kundens firma som skal kontaktes angående serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a63d5-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="a63d5-138">Velg **Neste \>**, og velg deretter **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="a63d5-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="a63d5-139">Se også</span><span class="sxs-lookup"><span data-stu-id="a63d5-139">See also</span></span>

[<span data-ttu-id="a63d5-140">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="a63d5-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="a63d5-141">Opprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="a63d5-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="a63d5-142">[Opprette serviceordrer (klasseskjema)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a63d5-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]