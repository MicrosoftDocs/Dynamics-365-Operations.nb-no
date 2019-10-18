---
title: Aktivere Broadbean-integrering i Microsoft Dynamics 365 Talent – Attract
description: Dette emnet forklarer hvordan du konfigurerer Microsoft Dynamics 365 Talent – Attract til å postere jobber til eksterne jobbtavler, for eksempel Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008599"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="8a0d6-103">Aktivere Broadbean-integrering</span><span class="sxs-lookup"><span data-stu-id="8a0d6-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8a0d6-104">Du vil gjerne vise ledige stillingene for så mange kvalifiserte kandidater som mulig.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="8a0d6-105">Rekrutteringsområder, for eksempel Broadbean, hjelper deg med å oppnå dette målet.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="8a0d6-106">Microsoft Dynamics 365 Talent: Attract lar deg postere jobber til Broadbean, og Microsoft gir deg kontinuerlig nye tilbud på dette området.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="8a0d6-107">Hvis du vil postere jobber til eksterne områder, må du ha [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="8a0d6-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="8a0d6-108">Hvis du vil postere jobber til Broadbean via Attract, må du ha et Broadbean-abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="8a0d6-109">Denne funksjonen er for øyeblikket i forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-109">This feature is currently in preview.</span></span> <span data-ttu-id="8a0d6-110">Hvis du vil prøve dette, må du [aktiverer funksjonen i innstillingene for administrasjon av Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="8a0d6-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="8a0d6-111">Konfigurere Broadbean-integrering</span><span class="sxs-lookup"><span data-stu-id="8a0d6-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="8a0d6-112">Logge på Attract som en administrator.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="8a0d6-113">Velg **Innstillinger**-knappen (tannhjulsymbolet) i øvre høyre hjørne på siden, og velg deretter **Administrasjonssenter**.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="8a0d6-114">Kontakt Broadbean, og skriv inn informasjonen din i **Brukernavn**, **Klient-ID**, **Krypteringstoken**.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="8a0d6-115">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="8a0d6-116">Broadbean-legitimasjonen din er sensitiv og konfidensiell.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="8a0d6-117">Derfor må du lagre og dele den på en ansvarlig måte.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="8a0d6-118">Alle som har en Administrator-rolle i Attract, kan vise denne legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="8a0d6-119">Microsoft og Attract er ikke er involvert i å opprette og vedlikeholde disse verdiene.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="8a0d6-120">Det er ditt ansvar å holde dem oppdatert i Attract og arbeide sammen med Broadbean for å løse problemer som involverer legitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="8a0d6-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
