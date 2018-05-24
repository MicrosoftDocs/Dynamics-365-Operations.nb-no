---
title: Annuller serviceordrer
description: "Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved å kjøre en periodisk jobb."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="c769e-103">Annuller serviceordrer</span><span class="sxs-lookup"><span data-stu-id="c769e-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c769e-104">Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved å kjøre en periodisk jobb.</span><span class="sxs-lookup"><span data-stu-id="c769e-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c769e-105">Serviceordrer kan ikke annulleres hvis stadiet serviceordren er i, ikke tillater annullering, hvis serviceordren har varebehov, eller hvis seviceordren allerede er postert.</span><span class="sxs-lookup"><span data-stu-id="c769e-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="c769e-106">Annullere en serviceordre fra Serviceordrer-skjemaet</span><span class="sxs-lookup"><span data-stu-id="c769e-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="c769e-107">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="c769e-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="c769e-108">Velg serviceordren, og klikk deretter på **Annuller ordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c769e-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="c769e-109">Annullere en serviceordrelinje</span><span class="sxs-lookup"><span data-stu-id="c769e-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="c769e-110">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="c769e-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="c769e-111">Dobbeltklikk på serviceordren som inneholder linjen du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="c769e-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="c769e-112">Velg serviceordrelinjen du vil annullere, og klikk deretter **Avbryt ordrelinje** for å endre statusen for linjen til **Avbrutt**.</span><span class="sxs-lookup"><span data-stu-id="c769e-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="c769e-113">For å tilbakeføre annullering av en serviceordrelinje og endre statusen tilbake til <STRONG>Opprettet</STRONG>, klikk på <STRONG>Opphev annullering</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c769e-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="c769e-114">Annullere flere serviceordrer</span><span class="sxs-lookup"><span data-stu-id="c769e-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="c769e-115">Klikk på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Annuller serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="c769e-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="c769e-116">Klikk **Velg**-knappen.</span><span class="sxs-lookup"><span data-stu-id="c769e-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="c769e-117">I **Forespørsel**-skjemaet i **Vilkår**-kolonnen velger du serviceordrene du vil annullere.</span><span class="sxs-lookup"><span data-stu-id="c769e-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="c769e-118">Klikk **OK** for å lukke **Forespørsel**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="c769e-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="c769e-119">Merk av for **Vis infologg** for å generere en informasjonslogg som viser de annullerte serviceordrene.</span><span class="sxs-lookup"><span data-stu-id="c769e-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="c769e-120">Merk av for **Opphev annullering** hvis du vil tilbakeføre en serviceordres **Avbrutt**-status.</span><span class="sxs-lookup"><span data-stu-id="c769e-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="c769e-121">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c769e-121">Click **OK**.</span></span>

<span data-ttu-id="c769e-122">De valgte serviceordrene blir enten annullert, eller de får sin fremdriftsstatus **Avbrutt** tilbakeført til **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="c769e-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c769e-123">Hvis du merker av for <STRONG>Opphev annullering</STRONG>, blir serviceordrer med fremdriftsstatusen <STRONG>Avbrutt</STRONG> tilbakeført, og serviceordrer med fremdriftsstatusen <STRONG>Pågår</STRONG> blir ikke annullert.</span><span class="sxs-lookup"><span data-stu-id="c769e-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



