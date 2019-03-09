---
title: Rapporteringsalternativer i Talent
description: Dette emnet forklarer hvordan du løser problemet der en kunde ønsker å tilpasse Microsoft Dynamics 365 for Talent-rapporter eller opprette nye rapporter.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305688"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="cf117-103">Rapporteringsalternativer i Talent</span><span class="sxs-lookup"><span data-stu-id="cf117-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf117-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="cf117-104">**Environment details**</span></span>

<span data-ttu-id="cf117-105">Dette problemet gjelder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="cf117-105">This issue applies to all environments.</span></span>

<span data-ttu-id="cf117-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="cf117-106">**Symptom**</span></span>

<span data-ttu-id="cf117-107">Kunden ønsker å tilpasse Microsoft Dynamics 365 for Talent-rapporter eller opprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="cf117-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="cf117-108">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="cf117-108">**Issue**</span></span>

<span data-ttu-id="cf117-109">Brukeren kan ikke tilpasse de innebygde Microsoft Power BI-rapportene.</span><span class="sxs-lookup"><span data-stu-id="cf117-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="cf117-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="cf117-110">**Solution**</span></span>

- <span data-ttu-id="cf117-111">Core HR-dataene som flyter til Common Data Service for Apps, kan rapporteres via PowerApps CDS-koblingen til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="cf117-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="cf117-112">Legg merke til at Common Data Service for Apps inneholder et delsett med Core HR-data.</span><span class="sxs-lookup"><span data-stu-id="cf117-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="cf117-113">Hvis du vil ha mer informasjon om Power BI og instrumentbord, kan du se [Opprette Power BI-rapporter og -instrumentbord med PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="cf117-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="cf117-114">Elektronisk rapportering (ER) er tilgjengelig for noen av rapportene i Talent.</span><span class="sxs-lookup"><span data-stu-id="cf117-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="cf117-115">Kundedrevne tilpasninger kan gjøres via ER-konfigurasjonsalternativene.</span><span class="sxs-lookup"><span data-stu-id="cf117-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="cf117-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjelp av ulike dataenheter som leveres av Talent via Microsoft Office-integreringen.</span><span class="sxs-lookup"><span data-stu-id="cf117-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="cf117-117">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="cf117-117">**Long-term solution**</span></span>

<span data-ttu-id="cf117-118">Flere Power BI-alternativer er tilgjengelige, og mer data og enheter vil være en del av Common Data Service for Apps.</span><span class="sxs-lookup"><span data-stu-id="cf117-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
