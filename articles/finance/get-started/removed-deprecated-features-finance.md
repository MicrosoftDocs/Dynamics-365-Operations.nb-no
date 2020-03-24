---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127983"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="f71c2-103">Funksjoner som er fjernet eller avskrevet i Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f71c2-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f71c2-104">Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f71c2-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="f71c2-105">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="f71c2-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="f71c2-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="f71c2-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="f71c2-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="f71c2-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="f71c2-108">Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="f71c2-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="f71c2-109">Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="f71c2-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="f71c2-110">Fjernede eller avskrevne funksjoner i Finance 10.0.12</span><span class="sxs-lookup"><span data-stu-id="f71c2-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="f71c2-111">Polske SSRS-rapporter: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014</span><span class="sxs-lookup"><span data-stu-id="f71c2-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="f71c2-112">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="f71c2-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f71c2-113">Ikke lovpålagt.</span><span class="sxs-lookup"><span data-stu-id="f71c2-113">Not legally required.</span></span>  |
| <span data-ttu-id="f71c2-114">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="f71c2-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f71c2-115">Ja (Excel-format for standard revisjonsfil med mva-deklarering - JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="f71c2-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="f71c2-116">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="f71c2-116">**Product areas affected**</span></span>         | <span data-ttu-id="f71c2-117">Søknad</span><span class="sxs-lookup"><span data-stu-id="f71c2-117">Application</span></span> |
| <span data-ttu-id="f71c2-118">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="f71c2-118">**Deployment option**</span></span>              | <span data-ttu-id="f71c2-119">Alle</span><span class="sxs-lookup"><span data-stu-id="f71c2-119">All</span></span> |
| <span data-ttu-id="f71c2-120">**Status**</span><span class="sxs-lookup"><span data-stu-id="f71c2-120">**Status**</span></span>                         | <span data-ttu-id="f71c2-121">Avskrevet: Innen 1. juli 2021 vi planlegger å ikke lenger kunne støtte SSRS-rapportene **: register for utgående mva, register for inngående mva, sammendrag av mva-register for EU – funksjonsreferanser PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="f71c2-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="f71c2-122">Excel-formateringseksempel for standard revisjonsfil med mva-deklarering (JPK_VDEK) blir introdusert i stedet.</span><span class="sxs-lookup"><span data-stu-id="f71c2-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="f71c2-123">Fjernede eller avskrevne funksjoner i Finance 10.0.7</span><span class="sxs-lookup"><span data-stu-id="f71c2-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="f71c2-124">Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg</span><span class="sxs-lookup"><span data-stu-id="f71c2-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="f71c2-125">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="f71c2-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="f71c2-126">Endret til funksjonen med kontogruppevalg.</span><span class="sxs-lookup"><span data-stu-id="f71c2-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="f71c2-127">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="f71c2-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="f71c2-128">Ja</span><span class="sxs-lookup"><span data-stu-id="f71c2-128">Yes</span></span> |
| <span data-ttu-id="f71c2-129">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="f71c2-129">**Product areas affected**</span></span>         | <span data-ttu-id="f71c2-130">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f71c2-130">Workflow</span></span> |
| <span data-ttu-id="f71c2-131">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="f71c2-131">**Deployment option**</span></span>              | <span data-ttu-id="f71c2-132">Alle</span><span class="sxs-lookup"><span data-stu-id="f71c2-132">All</span></span> |
| <span data-ttu-id="f71c2-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="f71c2-133">**Status**</span></span>                         | <span data-ttu-id="f71c2-134">Avskrevet: Etter 1. desember 2020 planlegger vi å ikke lenger støtte kinesiske bilagstyper uten kontogruppevalg.</span><span class="sxs-lookup"><span data-stu-id="f71c2-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="f71c2-135">Finne flere detaljer om den nye utformingen i [Hva er nytt i 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="f71c2-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="f71c2-136">Tidligere kunngjøringer om fjernede eller avskrevne funksjoner</span><span class="sxs-lookup"><span data-stu-id="f71c2-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="f71c2-137">Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="f71c2-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
