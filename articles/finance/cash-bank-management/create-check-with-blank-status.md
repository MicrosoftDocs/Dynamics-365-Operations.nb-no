---
title: Opprette sjekker som har tom status
description: Dette emnet beskriver hvordan du oppretter en tom sjekk for en bankkonto på Sjekker-siden.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 94d3a4ac8a3906e48f5a6053c031001c111549ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254041"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="5e3e7-103">Opprette sjekker som har tom status</span><span class="sxs-lookup"><span data-stu-id="5e3e7-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e3e7-104">Dette emnet forklarer hvordan du oppretter tomme sjekker.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="5e3e7-105">Du kan for eksempel opprette en tom sjekk for å registrere en sjekk som er skadet, og som ikke kan brukes til betaling.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="5e3e7-106">På **Sjekker**-siden utfører du vedlikeholdsoppgaver for sjekker.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="5e3e7-107">Du kan for eksempel opprette nye sjekknumre og slette sjekker.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="5e3e7-108">Du kan også opprette sjekker som har statusen **Tom**.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="5e3e7-109">Når tomme sjekker er opprettet, kan de ikke slettes eller brukes på nytt i systemet.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="5e3e7-110">Denne funksjonen er tilgjengelig på **Sjekker**-siden bare hvis du aktiverer funksjonen **Opprett sjekker med tom status på Sjekker-siden** på siden **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="5e3e7-111">Hvis funksjonen ikke er aktivert, kan sjekker som har statusen **Tom**, bare opprettes fra dialogboksen **Betaling med sjekk** under betalingsgenereringsprosessen i Leverandører.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="5e3e7-112">Hvis du vil åpne **Sjekker**-siden, går du til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**, og deretter velger du **Sjekker** i gruppen **Beslektet informasjon** i fanen **Administrer betalinger** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="5e3e7-113">Alternativt kan du gå til **Kontant- og bankbehandling \> Forespørsler og rapporter \> Sjekker**.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="5e3e7-114">Hvis du vil opprette sjekker som har statusen **Tom**, velger du **Opprett tomme sjekker** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="5e3e7-115">Mens systemet oppretter tomme sjekker, er den tilknyttede bankkontoen midlertidig deaktivert.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="5e3e7-116">Denne virkemåten reduserer risikoen for at betalinger blir generert samtidig som tomme sjekker opprettes.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="5e3e7-117">Når behandlingen er fullført, aktiveres den tilknyttede bankkontoen på nytt.</span><span class="sxs-lookup"><span data-stu-id="5e3e7-117">When the processing is completed, the associated bank account is reactivated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]