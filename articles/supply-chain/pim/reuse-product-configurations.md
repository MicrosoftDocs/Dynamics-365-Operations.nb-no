---
title: Gjenbruk av produktkonfigurasjoner
description: Du kan angi at du vil bruke en eksisterende konfigurasjon for et produkt på nytt automatisk. Deretter, når en bruker har fullført en konfigurasjonsøkt, kontrollerer systemet om det allerede finnes en konfigurasjon som tilsvarer brukerens valg. Hvis en tilsvarende konfigurasjon blir funnet, brukes konfigurasjons-IDen, den tilsvarende stykklisten og ruten på nytt.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18a3e5fb583ed620c825164f2628a26b6b0cb469
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "359641"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="8a1f6-105">Gjenbruk av produktkonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="8a1f6-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a1f6-106">Du kan angi at du vil bruke en eksisterende konfigurasjon for et produkt på nytt automatisk.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="8a1f6-107">Deretter, når en bruker har fullført en konfigurasjonsøkt, kontrollerer systemet om det allerede finnes en konfigurasjon som tilsvarer brukerens valg.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="8a1f6-108">Hvis en tilsvarende konfigurasjon blir funnet, brukes konfigurasjons-IDen, den tilsvarende stykklisten og ruten på nytt.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="8a1f6-109">Krav for gjenbruk av konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="8a1f6-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="8a1f6-110">Hvis du vil muliggjøre gjenbruk av konfigurasjoner, må du angi følgende informasjon for komponentene og attributtene på siden **Detaljer om produktkonfigurasjonsmodell**:</span><span class="sxs-lookup"><span data-stu-id="8a1f6-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="8a1f6-111">**Komponenter og delkomponenter** – I hurtigfanen **Generelt**, i feltet **Bruk konfigurasjoner på nytt**, velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="8a1f6-112">**Attributter** – I hurtigfanen **Attributter** velger du alternativet **Ta med i gjenbruk**.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="8a1f6-113">Dette alternativet vises bare når den tilknyttede komponenten er aktivert for gjenbruk.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="8a1f6-114">Hvis du ikke velger noen attributter for gjenbruk, brukes konfigurasjonen alltid på nytt, uavhengig av brukerens valg under en konfigurasjonsøkt.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="8a1f6-115">Attributtverdier i den eksisterende konfigurasjonen må samsvare med brukerens valg.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="8a1f6-116">Hvis brukeren for eksempel velger **Blå** som fargen under en konfigurasjonsøkt, kontrollerer systemet om en eksisterende konfigurasjon av komponenten har fargen blå.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="8a1f6-117">Tilbakestilling av gjenbruk av konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="8a1f6-117">Resetting configuration reuse</span></span>
<span data-ttu-id="8a1f6-118">Når du tilbakestiller gjenbruk av konfigurasjon, tas det ikke lenger hensyn til tidligere opprettede konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="8a1f6-119">Du bør tilbakestille gjenbruk av konfigurasjon hvis stykklisten eller ruten ble endret, men ingen attributter ble endret.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="8a1f6-120">Du tilbakestiller gjenbruk av konfigurasjon for hurtigfanen **Generelt** for komponenten.</span><span class="sxs-lookup"><span data-stu-id="8a1f6-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>



