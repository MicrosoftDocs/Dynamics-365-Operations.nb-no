---
title: Feilsøke oppgradering og overføring til avansert lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du oppgraderer og overføre til avansert lagerstyring.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993899"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="4b984-103">Feilsøke oppgradering og overføring til avansert lagerstyring</span><span class="sxs-lookup"><span data-stu-id="4b984-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b984-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du oppgraderer og overføre til avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="4b984-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="4b984-105">Jeg får følgende feilmelding: java.security.cert.certPathValidatorException: Finner ikke klareringsanker for sertifiseringsbane.</span><span class="sxs-lookup"><span data-stu-id="4b984-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4b984-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4b984-106">Issue description</span></span>

<span data-ttu-id="4b984-107">Du får denne feilmeldingen i lagerappen, fordi selvsignerte sertifikater ikke er klarerte i lokale Android 8+-miljøer.</span><span class="sxs-lookup"><span data-stu-id="4b984-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4b984-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="4b984-108">Issue resolution</span></span>

<span data-ttu-id="4b984-109">Bruk en ekstern (offentlig) sertifiseringsinstans (CA).</span><span class="sxs-lookup"><span data-stu-id="4b984-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="4b984-110">En hurtigreparasjon for dette problemet er tilgjengelig i versjon 1.9.0.0 av lagerappen.</span><span class="sxs-lookup"><span data-stu-id="4b984-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="4b984-111">Hvis du vil ha mer informasjon om dette problemet og hvordan du løser det, kan du se [Feilsøke tilkoblingsproblemer for lagerapp](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4b984-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="4b984-112">Hva er den godkjente prosessen for flytting fra grunnleggende lager til avansert lagerstyring?</span><span class="sxs-lookup"><span data-stu-id="4b984-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="4b984-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4b984-113">Issue description</span></span>

<span data-ttu-id="4b984-114">Du kjører nå under lagerstyring og bruker grunnleggende lagerfunksjoner, og du vil gå over til avansert lager for å dra nytte av mobilenheter, bølger og arbeid.</span><span class="sxs-lookup"><span data-stu-id="4b984-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="4b984-115">Det oppstår imidlertid problemer når du prøver å utføre denne flyttingen.</span><span class="sxs-lookup"><span data-stu-id="4b984-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="4b984-116">Du kan for eksempel ikke endre produktene, slik at de bruker lagerdimensjoner (område, lager og lokasjon), fordi produktene har transaksjoner mot dem.</span><span class="sxs-lookup"><span data-stu-id="4b984-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="4b984-117">Derfor må du lære den godkjente prosessen for flytting fra grunnleggende lager til avansert lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="4b984-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4b984-118">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="4b984-118">Issue resolution</span></span>

<span data-ttu-id="4b984-119">Hvis du vil ha mer informasjon om prosessen for flytting fra grunnleggende lager til avansert lagerstyring, kan du se følgende blogginnlegg og dokumentasjon:</span><span class="sxs-lookup"><span data-stu-id="4b984-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="4b984-120">Aktiver lagerstyringsprosess for eksisterende varer og lagre</span><span class="sxs-lookup"><span data-stu-id="4b984-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="4b984-121">Overføring av Microsoft Dynamics AX WMS til ny R3-lager- og transportfunksjonalitet</span><span class="sxs-lookup"><span data-stu-id="4b984-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="4b984-122">WMSI/WMS2-vareoverføring</span><span class="sxs-lookup"><span data-stu-id="4b984-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="4b984-123">Oppgradere lagerstyring fra Microsoft Dynamics AX 2012 til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4b984-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
