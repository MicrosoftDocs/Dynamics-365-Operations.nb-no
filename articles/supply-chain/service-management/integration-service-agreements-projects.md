---
title: Integrering for serviceavtaler og prosjekter
description: "Når du jobber med serviceavtaler og serviceavtalelinjer, bruker du data som er definert i områdene delen Prosjektstyring og regnskap."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="a7e89-103">Integrering for serviceavtaler og prosjekter</span><span class="sxs-lookup"><span data-stu-id="a7e89-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a7e89-104">Når du jobber med serviceavtaler og serviceavtalelinjer, bruker du data som er definert i følgende områder i delen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="a7e89-105">Prosjektpriser</span><span class="sxs-lookup"><span data-stu-id="a7e89-105">Project prices</span></span>

<span data-ttu-id="a7e89-106">Kostnaden og salgsprisen for en serviceavtaletransaksjon er avledet fra kostprisoppsettet som gjelder for prosjektet som er knyttet til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="a7e89-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="a7e89-107">Kost- og salgspriser kan settes opp per prosjekt, ansatt og kategori.</span><span class="sxs-lookup"><span data-stu-id="a7e89-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="a7e89-108">Prosjektvalidering</span><span class="sxs-lookup"><span data-stu-id="a7e89-108">Project validation</span></span>

<span data-ttu-id="a7e89-109">Prosjektene, de ansatte og kategoriene som kan velges på en serviceavtalelinje kan begrenses av valideringsoppsettet i delen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="a7e89-110">Ved å bruke valideringsoppsettet kan du kombinere ansatte, prosjekter og kategorier for kontrolltilgang.</span><span class="sxs-lookup"><span data-stu-id="a7e89-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="a7e89-111">Prosjektlinjeegenskaper</span><span class="sxs-lookup"><span data-stu-id="a7e89-111">Project line properties</span></span>

<span data-ttu-id="a7e89-112">En linjeegenskap angis automatisk for en serviceavtalelinje.</span><span class="sxs-lookup"><span data-stu-id="a7e89-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="a7e89-113">Linjeegenskaper opprettes i skjemaet **Linjeegenskaper** i **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="a7e89-114">Linjeegenskapen som er angitt på en serviceavtale knyttes til prosjektet som er valgt for serviceavtalen, og deretter arves av serviceavtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="a7e89-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="a7e89-115">Standard motkontoer</span><span class="sxs-lookup"><span data-stu-id="a7e89-115">Default offset accounts</span></span>

<span data-ttu-id="a7e89-116">Hvis du angir en utgiftstransaksjon, velges en standard motkonto automatisk for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a7e89-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="a7e89-117">Standard motkonto settes opp for prosjektet som er knyttet til gjeldende serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="a7e89-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="a7e89-118">Prosjektkategorier</span><span class="sxs-lookup"><span data-stu-id="a7e89-118">Project categories</span></span>

<span data-ttu-id="a7e89-119">Kategoriene som er tilgjengelige for serviceavtalelinjer er definert i skjemaet **Prosjektkategorier** i delen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="a7e89-120">Kategorier der det er merket av for <STRONG>Aktiv i journaler</STRONG> på fanen <STRONG>Prosjekt</STRONG> i skjemaet <STRONG>Prosjektkategorier</STRONG>, kan velges.</span><span class="sxs-lookup"><span data-stu-id="a7e89-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="a7e89-121">Imidlertid hvis det er merket av for <STRONG>Inaktive kategorier</STRONG> på fanen <STRONG>Journaler</STRONG> i skjemaet <STRONG>Parametere for prosjektstyring og regnskap</STRONG>, alle kategorier er tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="a7e89-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="a7e89-122">Prosjektparametere</span><span class="sxs-lookup"><span data-stu-id="a7e89-122">Project parameters</span></span>

<span data-ttu-id="a7e89-123">Hvis feltet **Fratrådte arbeidere** på fanen **Journaler** i skjemaet **Parametere for prosjektstyring og regnskap** er valgt, kan du velge inaktive ansatte og aktive ansatte i skjemaene **Serviceavtaler** og **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="a7e89-124">Du kan også aktivere feltene **Starttidspunkt** og **Sluttidspunkt** i **Prosjekt**-kategorien i skjemaet **Serviceordrer** for å angi start- og sluttidspunktene på serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="a7e89-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="a7e89-125">Aktivere start- og sluttidspunktfunksjonen for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="a7e89-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="a7e89-126">Klikk på **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="a7e89-127">Klikk fanen **Journaler**, og velg deretter **Vis start/sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="a7e89-128">Klikk **Prosjektstyring og regnskap** \> **Oppsett** \> **Journaler** \> **Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="a7e89-129">Velg journalnavnet som er tilknyttet serviceordren.</span><span class="sxs-lookup"><span data-stu-id="a7e89-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="a7e89-130">Klikk fanen **Generelt**, og velg deretter **Vis start/sluttidspunkt**.</span><span class="sxs-lookup"><span data-stu-id="a7e89-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a7e89-131">Velg journalnavnet for serviceordren i <STRONG>Time</STRONG>-feltet på fanen <STRONG>Journaler</STRONG> i skjemaet <STRONG>Servicestyringsparametere</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a7e89-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>






