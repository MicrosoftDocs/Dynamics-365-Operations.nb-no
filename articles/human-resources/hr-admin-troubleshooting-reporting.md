---
title: Rapporteringsalternativer
description: Denne artikkelen forklarer hvordan du løser problemet der en kunde ønsker å tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller opprette nye rapporter.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d0fc6b2d4af6ad021943717645bfff7a27797a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803903"
---
# <a name="reporting-options"></a><span data-ttu-id="8e84b-103">Rapporteringsalternativer</span><span class="sxs-lookup"><span data-stu-id="8e84b-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8e84b-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="8e84b-104">**Environment details**</span></span>

<span data-ttu-id="8e84b-105">Dette problemet gjelder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="8e84b-105">This issue applies to all environments.</span></span>

<span data-ttu-id="8e84b-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="8e84b-106">**Symptom**</span></span>

<span data-ttu-id="8e84b-107">Kunden ønsker å tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller opprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="8e84b-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="8e84b-108">**Problem**</span><span class="sxs-lookup"><span data-stu-id="8e84b-108">**Issue**</span></span>

<span data-ttu-id="8e84b-109">Brukeren kan ikke tilpasse de innebygde Microsoft Power BI-rapportene.</span><span class="sxs-lookup"><span data-stu-id="8e84b-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="8e84b-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="8e84b-110">**Solution**</span></span>

- <span data-ttu-id="8e84b-111">Human Resources-dataene som flyter til Dataverse, kan rapporteres via Power Apps Dataverse-koblingen til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="8e84b-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="8e84b-112">Legg merke til at Dataverse inneholder et delsett med Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="8e84b-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="8e84b-113">Hvis du vil ha mer informasjon om Power BI og instrumentbord, kan du se [Opprette Power BI-rapporter og -instrumentbord med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="8e84b-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="8e84b-114">Elektronisk rapportering (ER) er tilgjengelig for noen av rapportene i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8e84b-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="8e84b-115">Kundedrevne tilpasninger kan gjøres via ER-konfigurasjonsalternativene.</span><span class="sxs-lookup"><span data-stu-id="8e84b-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="8e84b-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjelp av ulike dataenheter som leveres av Human Resources via Microsoft Office-integreringen.</span><span class="sxs-lookup"><span data-stu-id="8e84b-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="8e84b-117">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="8e84b-117">**Long-term solution**</span></span>

<span data-ttu-id="8e84b-118">Flere Power BI-alternativer er tilgjengelige, og mer data og enheter vil være en del av Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8e84b-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]