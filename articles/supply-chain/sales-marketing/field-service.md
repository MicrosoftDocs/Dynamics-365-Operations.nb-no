---
title: Integrasjon med Microsoft Dynamics 365 for Field Service
description: Dette emnet gir en oversikt over integrasjonen med Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: nb-no
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="c4c66-103">Integrasjon med Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="c4c66-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c4c66-104">Microsoft Dynamics 365 for Finance and Operations gjør det mulig med synkronisering av forretningsprosesser mellom Finance and Operations og Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="c4c66-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="c4c66-105">Intregrasjonsscenarioene konfigureres ved hjelp av utvidbare Dataintegrator-maler og Common Data Service (CDS) for å gjøre det mulig med synkronisering av forretningsprosesser.</span><span class="sxs-lookup"><span data-stu-id="c4c66-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="c4c66-106">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c4c66-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="c4c66-107">Den første fasen av integreringen mellom Field Service og Finance and Operations fokuserer på kunne la arbeidsordrer og avtaler i Field Service faktureres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4c66-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="c4c66-108">Den støttede flyten starter i Field Service, der informasjonen fra arbeidsordrer synkroniseres til Finance and Operations som salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="c4c66-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="c4c66-109">Salgsordrene faktureres i Finance and Operations for å generere fakturadokumenter.</span><span class="sxs-lookup"><span data-stu-id="c4c66-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="c4c66-110">I tillegg synkroniseres informasjonen fra avtalefakturaer i Field Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c4c66-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="c4c66-111">Microsoft Dynamics 365 Data integrator synkroniserer data ved hjelp av prosjekter som kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="c4c66-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="c4c66-112">Standardmaler kan brukes til å lage tilpassede integreringsprosjekter der flere standard og egendefinerte felt, og enheter, kan tilordnes for å justere integreringen og oppfylle spesifikke behov.</span><span class="sxs-lookup"><span data-stu-id="c4c66-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="c4c66-113">Den første fasen av integreringen mellom Field Service og Finance and Operations gjør det mulig med synkronisering av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="c4c66-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="c4c66-114">Produkter i Finance and Operations til produkter i Field Service som inneholder produkttypeinformasjon</span><span class="sxs-lookup"><span data-stu-id="c4c66-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="c4c66-115">Arbeidsordrer i Field Service til salgsordrer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c4c66-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="c4c66-116">Fakturaer i Field Service til fritekstfakturaer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c4c66-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="c4c66-117">Systemkrav for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c4c66-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="c4c66-118">Field Service-integrasjon støtter følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="c4c66-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="c4c66-119">Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) eller senere</span><span class="sxs-lookup"><span data-stu-id="c4c66-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="c4c66-120">Dynamics 365 for Finance and Operations versjon 8.0 (april 2018) ble utgitt i april 2018 og har programbuild-nummer 8.0.30.8020 med plattformoppdatering 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="c4c66-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="c4c66-121">Systemkrav for Field Service</span><span class="sxs-lookup"><span data-stu-id="c4c66-121">System requirements for Field Service</span></span>
<span data-ttu-id="c4c66-122">For å bruke Field Service-integrasjonsløsningen må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="c4c66-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="c4c66-123">Microsoft Dynamics 365 for Field Service 9.0 eller senere</span><span class="sxs-lookup"><span data-stu-id="c4c66-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="c4c66-124">Dynamics 365 for Field Service versjon 1612 (9.0.1.733) (DB 9.0.1.733) online eller en senere versjon.</span><span class="sxs-lookup"><span data-stu-id="c4c66-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="c4c66-125">Prospect to Cash (P2C)-løsningen for Dynamics 365, versjon 1.15.0.1 eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="c4c66-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="c4c66-126">Løsningen er tilgjengelig for nedlasting fra [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="c4c66-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="c4c66-127">Field Service-integrasjonsløsning for Dynamics 365, versjon 1.0.0.0 eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="c4c66-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="c4c66-128">Løsningen er tilgjengelig for nedlasting fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="c4c66-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="c4c66-129">**(VENTER PÅ FRIGIVELSE)**</span><span class="sxs-lookup"><span data-stu-id="c4c66-129">**(PENDING RELEASE)**</span></span>

