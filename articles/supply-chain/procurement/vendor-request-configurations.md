---
title: "Leverandørforespørselskonfigurasjoner"
description: "Dette emnet beskriver feltene som må fylles ut i en ny leverandørforespørsel."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: e9b22a6f846607e8afc5d4f01c685f1364b1c01d
ms.contentlocale: nb-no
ms.lasthandoff: 02/08/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="41001-103">Leverandørforespørselskonfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="41001-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="41001-104">For å fullføre en leverandørforespørsel må en kontaktperson for leverandøren fullføre veiviseren for registrering av potensiell leverandør.</span><span class="sxs-lookup"><span data-stu-id="41001-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="41001-105">I skjemaet **Leverandørforespørselskonfigurasjoner** kan du opprette profiler som angir obligatoriske felt og synlige felt i veiviseren for registrering av potensiell leverandør.</span><span class="sxs-lookup"><span data-stu-id="41001-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="41001-106">Registreringsveiviseren for leverandører starter ved å spørre den potensielle leverandørbruker om hvilket land/region som leverandøren gjør forretninger i.</span><span class="sxs-lookup"><span data-stu-id="41001-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="41001-107">Denne informasjonen bestemmer den aktuelle konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="41001-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="41001-108">Hvis ingen bestemt konfigurasjon er definert for et land/region, brukes en standardkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="41001-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="41001-109">Definere en konfigurasjon av leverandørforespørsel</span><span class="sxs-lookup"><span data-stu-id="41001-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="41001-110">Som standard finnes det en leverandørkonfigurasjon i skjemaet Leverandørforespørselskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="41001-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="41001-111">Det er ikke mulig å velge land/regioner for standardkonfigurasjonen, så delen **Land/regioner** kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="41001-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="41001-112">Klikk **Innkjøp og leverandører** > **Oppsett** > **Leverandører**, og klikk deretter på **Leverandørforespørselskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="41001-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="41001-113">Klikk på **Felt**-fanen for å sette statusen til de oppførte feltene.</span><span class="sxs-lookup"><span data-stu-id="41001-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="41001-114">Skjult (ikke synlige)</span><span class="sxs-lookup"><span data-stu-id="41001-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="41001-115">Vises (synlige, men ikke obligatoriske)</span><span class="sxs-lookup"><span data-stu-id="41001-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="41001-116">Obligatorisk (synlig og obligatorisk)</span><span class="sxs-lookup"><span data-stu-id="41001-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="41001-117">Klikk på **Innhold**-fanen for å angi om teksten skal vises i veiviseren, og om det skal være en bekreftelse som den potensielle leverandørbrukeren må godta før neste trinn i veiviseren.</span><span class="sxs-lookup"><span data-stu-id="41001-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="41001-118">Det vil bli bedt om bekreftelse for alle vilkårene som brukeren må godta for å fortsette.</span><span class="sxs-lookup"><span data-stu-id="41001-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="41001-119">Du kan også angi en bekreftelsesmelding som skal vises når veiviseren er ferdig, og du kan legge til ett eller flere spørreskjemaer.</span><span class="sxs-lookup"><span data-stu-id="41001-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="41001-120">Opprette en leverandørkonfigurasjon for et bestemt land/område</span><span class="sxs-lookup"><span data-stu-id="41001-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="41001-121">Klikk **Innkjøp og leverandører** > **Oppsett** > **Leverandører**, og klikk deretter på **Leverandørforespørselskonfigurasjoner**.</span><span class="sxs-lookup"><span data-stu-id="41001-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="41001-122">Klikk på **Ny** for å opprette en ny konfigurasjon, og angi et navn for konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="41001-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="41001-123">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="41001-123">Click **Save**.</span></span>
4.  <span data-ttu-id="41001-124">Åpne fanen **Land/regioner** for å velge landet/regionen som skal brukes for konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="41001-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="41001-125">Fullfør konfigurasjonen ved å følge retningslinjene for standardkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="41001-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


