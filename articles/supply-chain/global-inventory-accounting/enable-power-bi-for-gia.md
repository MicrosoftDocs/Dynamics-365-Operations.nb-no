---
title: Aktivere Power BI for Globalt lagerregnskap
description: Dette emnet beskriver hvordan du aktiverer Microsoft Power BI for Globalt lagerregnskap.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273203"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="c2280-103">Aktivere Power BI for Globalt lagerregnskap</span><span class="sxs-lookup"><span data-stu-id="c2280-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="c2280-104">Du kan feste fliser, instrumentbord og rapporter fra [PowerBI.com](https://powerbi.com/)-kontoen til Microsoft Dynamics 365-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="c2280-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c2280-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="c2280-105">Prerequisites</span></span>

<span data-ttu-id="c2280-106">Følgende forutsetninger må være på plass før du kan aktivere Power BI-rapportering:</span><span class="sxs-lookup"><span data-stu-id="c2280-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="c2280-107">Du må være systemadministrator i Dynamics 365-programmet.</span><span class="sxs-lookup"><span data-stu-id="c2280-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="c2280-108">Du må ha en [PowerBI.com](https://powerbi.com/)-konto.</span><span class="sxs-lookup"><span data-stu-id="c2280-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="c2280-109">Du må ha minst ett instrumentbord og én rapport i Power BI-kontoen.</span><span class="sxs-lookup"><span data-stu-id="c2280-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="c2280-110">Du må ha administratorrettigheter til Azure Active Directory-kontoen (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c2280-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="c2280-111">Domenet Azure AD må være det samme domenet som du brukte for [PowerBI.com](https://powerbi.com/)-kontoen.</span><span class="sxs-lookup"><span data-stu-id="c2280-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="c2280-112">Installasjon</span><span class="sxs-lookup"><span data-stu-id="c2280-112">Setup</span></span>

<span data-ttu-id="c2280-113">Gjør følgende for å konfigurere Power BI-integrasjonen.</span><span class="sxs-lookup"><span data-stu-id="c2280-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="c2280-114">Logg på [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="c2280-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="c2280-115">Gå til **Delt aktivabibliotek**, velg **Power BI-rapportmodell** som anleggsmiddeltype, og last ned pakken **Globalt lagerregnskap**.</span><span class="sxs-lookup"><span data-stu-id="c2280-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="c2280-116">Logg deg på [PowerBI.com](https://app.powerbi.com/), og last opp rapportfilen for **Globalt lagerregnskap** Power BI ved å følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="c2280-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="c2280-117">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c2280-117">Select **New**.</span></span>
    1. <span data-ttu-id="c2280-118">Velg **Last opp en fil**.</span><span class="sxs-lookup"><span data-stu-id="c2280-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="c2280-119">Velg rapportfilen for **Globalt lagerregnskap** Power BI.</span><span class="sxs-lookup"><span data-stu-id="c2280-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="c2280-120">Konfigurer Power BI-rapporten for **Globalt lagerregnskap** ved å følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="c2280-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="c2280-121">Gå til **Mitt arbeidsområde**, finn datasettet for Globalt lagerregnskap, og velg deretter **Innstillinger** på **Alternativer**-menyen.</span><span class="sxs-lookup"><span data-stu-id="c2280-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="c2280-122">I **Innstillinger for Globalt lagerregnskap** utvider du **Parametere** og oppdaterer alle parametere etter behov.</span><span class="sxs-lookup"><span data-stu-id="c2280-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="c2280-123">Registrer programmet som beskrevet i [Konfigurere PowerBI.com-integrering](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="c2280-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="c2280-124">Integrer Power BI-rapportfilen for **Globalt lagerregnskap** i Dynamics 365 Supply Chain Management ved å følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="c2280-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="c2280-125">Gå til **Systemadministrasjon \> Oppsett \> PowerBI.com-konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="c2280-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="c2280-126">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c2280-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="c2280-127">Velg **Aktiver PowerBI.Com-integrering**.</span><span class="sxs-lookup"><span data-stu-id="c2280-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="c2280-128">I feltet **Program-ID** angir du program-IDen.</span><span class="sxs-lookup"><span data-stu-id="c2280-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="c2280-129">I feltet **Programnøkkel** angir du programnøkkelen.</span><span class="sxs-lookup"><span data-stu-id="c2280-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="c2280-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c2280-130">Select **Save**.</span></span>

1. <span data-ttu-id="c2280-131">Oppdater siden slik at Power BI-påloggingsdialogboksen vises.</span><span class="sxs-lookup"><span data-stu-id="c2280-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="c2280-132">Velg **Åpne rapportkatalog** i kategorien **Alternativer**, og velg deretter Power BI-rapportfilen for **Globalt lagerregnskap** som du lastet opp tidligere.</span><span class="sxs-lookup"><span data-stu-id="c2280-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="c2280-133">Oppdater siden.</span><span class="sxs-lookup"><span data-stu-id="c2280-133">Refresh the page.</span></span> <span data-ttu-id="c2280-134">Du skal se at rapporten er lagt til.</span><span class="sxs-lookup"><span data-stu-id="c2280-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="c2280-135">Under **Power BI-rapporter** velger du koblingen **Globalt lagerregnskap**.</span><span class="sxs-lookup"><span data-stu-id="c2280-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="c2280-136">Hvis du vil ha mer informasjon, se [Konfigurere PowerBI.com-integrasjon](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="c2280-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
