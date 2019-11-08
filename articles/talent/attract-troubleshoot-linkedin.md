---
title: Feilsøke integrering med LinkedIn og Microsoft Dynamics 365 Talent – Attract
description: Dette emnet forklarer hvordan du feilsøker problemer når du prøver å postere jobber til LinkedIn fra Microsoft Dynamics 365 Talent – Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: b031fd95d2e7fc8405ad96139779091e00bb4d46
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551478"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="429c0-103">Feilsøke integrering med LinkedIn og Microsoft Dynamics 365 Talent – Attract</span><span class="sxs-lookup"><span data-stu-id="429c0-103">Troubleshoot integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="429c0-104">Bruk følgende informasjon til å feilsøke problemer som kan oppstå når du prøver å postere jobber til LinkedIn fra Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="429c0-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="429c0-105">Du kan ikke logge på LinkedIn fra Attract</span><span class="sxs-lookup"><span data-stu-id="429c0-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="429c0-106">Hvis du har problemer med å logge på LinkedIn fra Attract, kan du prøve disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="429c0-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="429c0-107">Kontroller at LinkedIn-legitimasjonen du har angitt i Attract, er gyldig og korrekt.</span><span class="sxs-lookup"><span data-stu-id="429c0-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="429c0-108">Hvis legitimasjonen er gyldig og korrekt, kan du kontakte [LinkedIn-støtten](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="429c0-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="429c0-109">Hvis problemet vedvarer, kontakter du [Microsoft Kundestøtte](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="429c0-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="429c0-110">Jobbposteringer fra Attract vises ikke på LinkedIn</span><span class="sxs-lookup"><span data-stu-id="429c0-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="429c0-111">Hvis jobben din ikke vises på LinkedIn etter 24 timer, kan du prøve disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="429c0-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="429c0-112">Kontroller at LinkedIn-selskaps-ID-en er tilordnet til LinkedIn-selskapssiden og er korrekt angitt i administrasjonssenteret for Attract.</span><span class="sxs-lookup"><span data-stu-id="429c0-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="429c0-113">Hvis du vil ha mer informasjon om hvordan du endrer LinkedIn-innstillinger i administrasjonssenteret, kan du se [Konfigurere integrering med LinkedIn](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="429c0-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="429c0-114">Hvis du vil ha mer informasjon om firma-ID-er for LinkedIn, kan du se [Knytte LinkedIn-firma-ID-en til LinkedIn-jobbtavlen - Vanlige spørsmål](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="429c0-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="429c0-115">Kontroller jobbdetaljene på LinkedIn for å se at adressen er fullstendig.</span><span class="sxs-lookup"><span data-stu-id="429c0-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="429c0-116">Når du skal postere en jobb, trenger LinkedIn minst byen og landet eller området for jobben.</span><span class="sxs-lookup"><span data-stu-id="429c0-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="429c0-117">Kontroller at jobben ikke dupliserer en annen jobb som er postert på LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="429c0-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="429c0-118">LinkedIn vil ikke legge ut jobber som er duplikater av LinkedIn premium jobbplasser eller begrensede oppføringer fra en annen kilde.</span><span class="sxs-lookup"><span data-stu-id="429c0-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="429c0-119">Kontroller at noen andre i firmaet ikke allerede har postert jobben manuelt.</span><span class="sxs-lookup"><span data-stu-id="429c0-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="429c0-120">Se også</span><span class="sxs-lookup"><span data-stu-id="429c0-120">See also</span></span>

[<span data-ttu-id="429c0-121">Vanlige spørsmål om LinkedIn</span><span class="sxs-lookup"><span data-stu-id="429c0-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="429c0-122">Postere jobber til LinkedIn fra Attract</span><span class="sxs-lookup"><span data-stu-id="429c0-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="429c0-123">Finne kandidater med LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="429c0-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="429c0-124">Opprette jobber</span><span class="sxs-lookup"><span data-stu-id="429c0-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="429c0-125">Feilsøke integrering med LinkedIn</span><span class="sxs-lookup"><span data-stu-id="429c0-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
