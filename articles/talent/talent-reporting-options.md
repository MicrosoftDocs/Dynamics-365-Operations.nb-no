---
title: Rapporteringsalternativer i Talent
description: Dette emnet forklarer hvordan du løser problemet der en kunde ønsker å tilpasse Microsoft Dynamics 365 Talent-rapporter eller opprette nye rapporter.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 50342c847200d015a66c6f22007070bb26c6caef
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009358"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="9f3ce-103">Rapporteringsalternativer i Talent</span><span class="sxs-lookup"><span data-stu-id="9f3ce-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f3ce-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="9f3ce-104">**Environment details**</span></span>

<span data-ttu-id="9f3ce-105">Dette problemet gjelder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-105">This issue applies to all environments.</span></span>

<span data-ttu-id="9f3ce-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="9f3ce-106">**Symptom**</span></span>

<span data-ttu-id="9f3ce-107">Kunden ønsker å tilpasse Microsoft Dynamics 365 Talent-rapporter eller opprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="9f3ce-108">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="9f3ce-108">**Issue**</span></span>

<span data-ttu-id="9f3ce-109">Brukeren kan ikke tilpasse de innebygde Microsoft Power BI-rapportene.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="9f3ce-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="9f3ce-110">**Solution**</span></span>

- <span data-ttu-id="9f3ce-111">Core HR-dataene som flyter til Common Data Service, kan rapporteres via PowerApps Common Data Service-koblingen til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="9f3ce-112">Legg merke til at Common Data Service inneholder et delsett med Core HR-data.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="9f3ce-113">Hvis du vil ha mer informasjon om Power BI og instrumentbord, kan du se [Opprette Power BI-rapporter og -instrumentbord med PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="9f3ce-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="9f3ce-114">Elektronisk rapportering (ER) er tilgjengelig for noen av rapportene i Talent.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="9f3ce-115">Kundedrevne tilpasninger kan gjøres via ER-konfigurasjonsalternativene.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="9f3ce-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjelp av ulike dataenheter som leveres av Talent via Microsoft Office-integreringen.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="9f3ce-117">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="9f3ce-117">**Long-term solution**</span></span>

<span data-ttu-id="9f3ce-118">Flere Power BI-alternativer er tilgjengelige, og mer data og enheter vil være en del av Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9f3ce-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
