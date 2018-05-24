---
title: Definer serviceordrestadier
description: Definer serviceordrestadier.
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
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
ms.openlocfilehash: 6e2556dd8f3f32da16e53bfe46faec7489d84efa
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-service-order-stages"></a><span data-ttu-id="60cdb-103">Definer serviceordrestadier</span><span class="sxs-lookup"><span data-stu-id="60cdb-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="60cdb-104">Klikk **Servicestyring** \> **Oppsett** \> **Serviceordrer** \> **Servicestadier**.</span><span class="sxs-lookup"><span data-stu-id="60cdb-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="60cdb-105">Trykk CTRL+N for å opprette en ny oppføring.</span><span class="sxs-lookup"><span data-stu-id="60cdb-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="60cdb-106">I feltene **Servicestadium** og **Beskrivelse** angir du en servicestadium-ID og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="60cdb-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="60cdb-107">Velg aktuelle parametere for stadiet.</span><span class="sxs-lookup"><span data-stu-id="60cdb-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="60cdb-108">Velg det overordnede stadiet for det gjeldende stadiet, eller la **Overordnet**-feltet være tomt hvis det gjeldende stadiet er det innledende stadiet i stadiumoppsettet.</span><span class="sxs-lookup"><span data-stu-id="60cdb-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="60cdb-109">Du kan ikke endre <STRONG>Overordnet</STRONG>-feltet etter at du har lagret stadiet.</span><span class="sxs-lookup"><span data-stu-id="60cdb-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="60cdb-110">I stedet kan du slette posten og opprette posten på nytt med et annet valg i <STRONG>Overordnet</STRONG>-feltet.</span><span class="sxs-lookup"><span data-stu-id="60cdb-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="60cdb-111">I tillegg kan du bare opprette ett stadium med et tomt <STRONG>Overordnet</STRONG>-felt.</span><span class="sxs-lookup"><span data-stu-id="60cdb-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="60cdb-112">Det vil si at bare ett innledende stadium er tillatt.</span><span class="sxs-lookup"><span data-stu-id="60cdb-112">That is, only one initial stage is permitted.</span></span></P>


  



