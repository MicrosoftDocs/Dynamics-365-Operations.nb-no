---
title: Definer serviceordrestadier
description: Definer serviceordrestadier.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9774d5f4e97d3f768366ba552e5928929bacf508
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470935"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="0a6ab-103">Definer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="0a6ab-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="0a6ab-104">Gå til **Servicestyring** \> **Oppsett** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-104">Go to **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="0a6ab-105">Velg **Ny** for å opprette en ny post.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-105">Select **New** to create a new record.</span></span>

3.  <span data-ttu-id="0a6ab-106">I feltene **Servicestadium** og **Beskrivelse** angir du en servicestadium-ID og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="0a6ab-107">Velg aktuelle parametere for stadiet.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="0a6ab-108">Velg det overordnede stadiet for det gjeldende stadiet, eller la **Overordnet**-feltet være tomt hvis det gjeldende stadiet er det innledende stadiet i stadiumoppsettet.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0a6ab-109">Du kan ikke endre <STRONG>Overordnet</STRONG>-feltet etter at du har lagret stadiet.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="0a6ab-110">I stedet kan du slette posten og opprette posten på nytt med et annet valg i <STRONG>Overordnet</STRONG>-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="0a6ab-111">I tillegg kan du bare opprette ett stadium med et tomt <STRONG>Overordnet</STRONG>-felt.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="0a6ab-112">Det vil si at bare ett innledende stadium er tillatt.</span><span class="sxs-lookup"><span data-stu-id="0a6ab-112">That is, only one initial stage is permitted.</span></span></P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]