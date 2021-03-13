---
title: Opprette organisasonsmodellhierarkier for B2B-organisasjoner
description: Dette emnet beskriver hvordan du oppretter organisasjonsmodellhierarkier for bedrift-til-bedrift-organisasjoner (B2B).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035945"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="5d5b5-103">Opprette organisasonsmodellhierarkier for B2B-organisasjoner</span><span class="sxs-lookup"><span data-stu-id="5d5b5-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d5b5-104">Dette emnet beskriver hvordan du oppretter organisasjonsmodellhierarkier for bedrift-til-bedrift-organisasjoner (B2B) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5d5b5-105">I Commerce Headquarters representeres forretningspartnerorganisasjoner av kunde- og kundehierarkienheter.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="5d5b5-106">Forretningspartnerorganisasjonen og dens brukere representeres som kunder, og kundehierarkier brukes til å knytte disse kundene til hverandre.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="5d5b5-107">Når en forretningspartnerforespørsel om å delta i et B2B-e-handelsområde godkjennes, utføres følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="5d5b5-108">To nye kundeposter opprettes i systemet: en **Type Organisasjon**-kundepost for forretningspartnerorganisasjonen og en kundepost av typen **Type Person** for anmoderen (det vil si forretningspartnerbrukeren som sendte forespørselen).</span><span class="sxs-lookup"><span data-stu-id="5d5b5-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="5d5b5-109">Det opprettes en ny kundehierarkipost under **Kunde \> Kundehierarki**.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="5d5b5-110">Denne posten har følgende hodeegenskaper:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="5d5b5-111">**Kundehierarki-ID** – En unik ID for kundehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="5d5b5-112">Denne IDen bruker nummerserien som er definert i Delte handelsparametere i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="5d5b5-113">**Navn** – Organisasjonsnavnet til forretningspartneren, som angitt i forespørselen om pålasting.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="5d5b5-114">**Formål** – Denne egenskapen er satt til den forhåndsdefinerte verdien **B2B-organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="5d5b5-115">**Organisasjon** – Kunde-IDen til forretningspartneren.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="5d5b5-116">Her er detaljene i kundehierarkiposten:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="5d5b5-117">Kundeposten til anmoderen er knyttet til kundehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="5d5b5-118">Administratorrollen er knyttet til anmoderen.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="5d5b5-119">Når administratoren legger til flere brukere i forretningspartnerorganisasjonen på et B2B-område, opprettes det en ny kundepost for hver bruker i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="5d5b5-120">Denne kundeposten legges også til i den relevante kundehierarkiposten for forretningspartneren og har rollen "bruker".</span><span class="sxs-lookup"><span data-stu-id="5d5b5-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="5d5b5-121">I de fleste tilfeller bør tilsvarende egenskapsverdier for alle kundeposter i et hierarki samsvare.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="5d5b5-122">Fordi alle forretningspartnerbrukere for eksempel skal få like priser for produkter, bør prisgruppen og tilknyttede konfigurasjoner samsvare.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="5d5b5-123">Systemet iverksetter imidlertid ikke denne konsistensen.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="5d5b5-124">Derfor er de relevante Commerce Headquarters-brukerne ansvarlige for å sikre at egenskapsverdiene og konfigurasjonene samsvarer for alle kunder i et gitt hierarki.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="5d5b5-125">Commerce Headquarters-brukere kan se på egenskapsverdiene for alle kundeposter i hierarkiet i side-ved-side-visning.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="5d5b5-126">Velg de relevante kundepostegenskapene ved å velge kategorinavnene på rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="5d5b5-127">Brukere kan vise og redigere egenskapsverdiene direkte fra denne visningen.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="5d5b5-128">Hvis du vil bruke alle verdiene fra administratorkundeposten på alle brukerkundepostene, kan du velge **Overstyr** i kundehierarkidetaljene.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d5b5-129">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5d5b5-129">Additional resources</span></span>

[<span data-ttu-id="5d5b5-130">Definere et B2B-e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="5d5b5-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="5d5b5-131">Administrere forretningspartnerbrukere på B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5d5b5-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="5d5b5-132">Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5d5b5-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="5d5b5-133">Angi produktantallsgrenser for B2B-e-handelsområder</span><span class="sxs-lookup"><span data-stu-id="5d5b5-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)
