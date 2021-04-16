---
title: Innkjøps- og leverandørparametere for Netto innkjøpspris
description: Dette emnet beskriver hvordan du definerer de relevante innkjøps- og leverandørparameterne når du bruker modulen Netto innkjøpspris.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833935"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="d2652-103">Innkjøps- og leverandørparametere for Netto innkjøpspris</span><span class="sxs-lookup"><span data-stu-id="d2652-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2652-104">Siden **Innkjøps- og leverandørparametere** har et par innstillinger som er spesielt relevante når du bruker modulen **Netto innkjøpspris**.</span><span class="sxs-lookup"><span data-stu-id="d2652-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="d2652-105">Bruk dialogboksen **Oppdater ordrelinjer** som åpnes fra siden **Innkjøps- og leverandørparametere** til å angi om bestillingslinjer automatisk skal oppdateres når det gjøres endringer i bestillingshodet.</span><span class="sxs-lookup"><span data-stu-id="d2652-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="d2652-106">Følg fremgangsmåten nedenfor for å fullføre dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="d2652-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="d2652-107">Gå til **Innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører.</span><span class="sxs-lookup"><span data-stu-id="d2652-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="d2652-108">Velg koblingen **Oppdater ordrelinjer** i fanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="d2652-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="d2652-109">Dialogboksen **Oppdater ordrelinjer** viser feltene på ordrehodet, som også kan bruke automatiske oppdateringer for relaterte felt på ordrelinjene.</span><span class="sxs-lookup"><span data-stu-id="d2652-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="d2652-110">Sett hvert felt i listen til en av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="d2652-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="d2652-111">**Alltid** – Ordrelinjene blir oppdatert automatisk når ordrehodet oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d2652-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="d2652-112">**Aldri** – Ordrelinjene blir aldri oppdatert automatisk når ordrehodet oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d2652-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="d2652-113">**Ledetekst** – Brukeren blir bedt om å velge om ordrelinjene skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="d2652-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
