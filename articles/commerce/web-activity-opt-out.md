---
title: Velge bort samling for webaktivitetshendelse
description: I dette emnet finner du informasjon om hvordan du kan la besøkende på nettstedet velge bort en samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012319"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="b3602-103">Velge bort samling for webaktivitetshendelse</span><span class="sxs-lookup"><span data-stu-id="b3602-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="b3602-104">Dette emnet beskriver hvordan du kan la kundene velge bort samling for webaktivitetshendelse i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3602-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b3602-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="b3602-105">Overview</span></span>

<span data-ttu-id="b3602-106">Dynamics 365 Commerce lar områdeadministratorer analysere webaktiviteten til brukere av sine områder for e-handel.</span><span class="sxs-lookup"><span data-stu-id="b3602-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="b3602-107">På denne måten kan de bedre forstå hvordan områdene brukes, og de kan optimalisere områdene for å gi en forbedret brukeropplevelse og oppfylle forretningsmålene.</span><span class="sxs-lookup"><span data-stu-id="b3602-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="b3602-108">Metoder administratorer kan bruke til å implementere mulighet for brukere å velge bort ting</span><span class="sxs-lookup"><span data-stu-id="b3602-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="b3602-109">Administratorer kan implementere mulighet for brukere å velge bort ting på tre måter.</span><span class="sxs-lookup"><span data-stu-id="b3602-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="b3602-110">Velge bort på vegne av brukeren</span><span class="sxs-lookup"><span data-stu-id="b3602-110">Opt out on behalf of users</span></span>

<span data-ttu-id="b3602-111">I Kontobehandling i Commerce Headquarters (HQ) kan administratorer velge bort på vegne av brukeren.</span><span class="sxs-lookup"><span data-stu-id="b3602-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="b3602-112">I HQ-klienten søker du etter og velger en kunde på siden **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="b3602-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="b3602-113">På siden for kundedetaljer setter du alternativet **Ikke spor webaktivitet** til **Ja** i delen **Personvern** i hurtigkategorien **Detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="b3602-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Personverninnstillinger](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="b3602-115">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="b3602-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="b3602-116">Modulbasert bortvalgsopplevelse</span><span class="sxs-lookup"><span data-stu-id="b3602-116">Module-based opt-out experience</span></span>

<span data-ttu-id="b3602-117">Administratorer kan la godkjente brukere velge bort samling for webaktivitshendelse selv.</span><span class="sxs-lookup"><span data-stu-id="b3602-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="b3602-118">Hvis du vil gi denne bortvalgsopplevelsen, legger du til en bortvalgsmodul for brukerne på profilsidene for kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="b3602-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="b3602-119">Egendefinerte tillegg</span><span class="sxs-lookup"><span data-stu-id="b3602-119">Custom extensions</span></span>

<span data-ttu-id="b3602-120">Administratorer kan opprette egne tillegg for å administrere bortvalgsopplevelsen for brukere.</span><span class="sxs-lookup"><span data-stu-id="b3602-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="b3602-121">Hvis du vil ha mer informasjon, kan du se [Kalle API-er for Retail Server](e-commerce-extensibility/call-retail-server-apis.md) og [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="b3602-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
