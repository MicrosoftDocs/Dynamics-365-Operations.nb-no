---
title: Rapporteringsalternativer
description: Denne artikkelen forklarer hvordan du løser problemet der en kunde ønsker å tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller opprette nye rapporter.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010143"
---
# <a name="reporting-options"></a><span data-ttu-id="d4c60-103">Rapporteringsalternativer</span><span class="sxs-lookup"><span data-stu-id="d4c60-103">Reporting options</span></span>

<span data-ttu-id="d4c60-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="d4c60-104">**Environment details**</span></span>

<span data-ttu-id="d4c60-105">Dette problemet gjelder for alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="d4c60-105">This issue applies to all environments.</span></span>

<span data-ttu-id="d4c60-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="d4c60-106">**Symptom**</span></span>

<span data-ttu-id="d4c60-107">Kunden ønsker å tilpasse Microsoft Dynamics 365 Human Resources-rapporter eller opprette nye rapporter.</span><span class="sxs-lookup"><span data-stu-id="d4c60-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="d4c60-108">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="d4c60-108">**Issue**</span></span>

<span data-ttu-id="d4c60-109">Brukeren kan ikke tilpasse de innebygde Microsoft Power BI-rapportene.</span><span class="sxs-lookup"><span data-stu-id="d4c60-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="d4c60-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="d4c60-110">**Solution**</span></span>

- <span data-ttu-id="d4c60-111">Human Resources-dataene som flyter til Common Data Service, kan rapporteres via Power Apps Common Data Service-koblingen til Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d4c60-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="d4c60-112">Legg merke til at Common Data Service inneholder et delsett med Human Resources-data.</span><span class="sxs-lookup"><span data-stu-id="d4c60-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="d4c60-113">Hvis du vil ha mer informasjon om Power BI og instrumentbord, kan du se [Opprette Power BI-rapporter og -instrumentbord med Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="d4c60-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="d4c60-114">Elektronisk rapportering (ER) er tilgjengelig for noen av rapportene i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d4c60-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="d4c60-115">Kundedrevne tilpasninger kan gjøres via ER-konfigurasjonsalternativene.</span><span class="sxs-lookup"><span data-stu-id="d4c60-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="d4c60-116">Data kan eksporteres til Microsoft Excel eller Microsoft Word ved hjelp av ulike dataenheter som leveres av Human Resources via Microsoft Office-integreringen.</span><span class="sxs-lookup"><span data-stu-id="d4c60-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="d4c60-117">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="d4c60-117">**Long-term solution**</span></span>

<span data-ttu-id="d4c60-118">Flere Power BI-alternativer er tilgjengelige, og mer data og enheter vil være en del av Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d4c60-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
