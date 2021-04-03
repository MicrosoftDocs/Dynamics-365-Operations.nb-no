---
title: Definere arbeidsdeling
description: Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562503"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="0aca5-103">Definere arbeidsdeling</span><span class="sxs-lookup"><span data-stu-id="0aca5-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0aca5-104">Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="0aca5-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="0aca5-105">Dette konseptet kalles arbeidsdeling.</span><span class="sxs-lookup"><span data-stu-id="0aca5-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="0aca5-106">Det kan for eksempel hende at du ikke vil at den samme personen skal bekrefte mottak av varer og behandle betalingen til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="0aca5-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="0aca5-107">Arbeidsdeling hjelper deg med å redusere risikoen for bedrageri, og det hjelper deg å oppdage feil eller uregelmessigheter også.</span><span class="sxs-lookup"><span data-stu-id="0aca5-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="0aca5-108">Du kan også bruke arbeidsdeling til å følge policyer for intern kontroll.</span><span class="sxs-lookup"><span data-stu-id="0aca5-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="0aca5-109">Fullfør fremgangsmåten nedenfor for å opprette en regel.</span><span class="sxs-lookup"><span data-stu-id="0aca5-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="0aca5-110">Du må være en systemansvarlig for å fullføre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="0aca5-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="0aca5-111">Gå til **Systemadministrasjon** > **Sikkerhet** > **Arbeidsdeling** > **Arbeidsdelingsregler**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="0aca5-112">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-112">Click **New**.</span></span>
3. <span data-ttu-id="0aca5-113">Skriv inn en verdi i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="0aca5-114">Klikk på rullegardinknappen i feltet **Første plikt** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0aca5-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0aca5-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="0aca5-116">Velg den første plikten som kontrolleres av regelen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="0aca5-117">Klikk på rullegardinknappen i feltet **Andre plikt** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="0aca5-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="0aca5-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="0aca5-119">Velg den andre plikten som kontrolleres av regelen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="0aca5-120">Velg et alternativ i feltet **Alvorsgrad**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="0aca5-121">Velg viktighet for risikoen som oppstår når den samme brukeren eller rollen utfører begge pliktene.</span><span class="sxs-lookup"><span data-stu-id="0aca5-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="0aca5-122">Skriv inn en verdi i feltet **Sikkerhetsrisiko**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="0aca5-123">Angi en beskrivelse av sikkerhetsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="0aca5-124">Skriv inn en verdi i feltet **Sikkerhetsreduksjon**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="0aca5-125">Angi en beskrivelse av handlingene som du gjøre for å redusere sikkerhetsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="0aca5-126">Du kan for eksempel redusere risikoen ved å utføre mer detaljert gjennomgang av prosessen, utføre en månedlig ledergjennomgang eller ved å dele ressurser med andre avdelinger.</span><span class="sxs-lookup"><span data-stu-id="0aca5-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="0aca5-127">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0aca5-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="0aca5-128">Samsvar med reglene for arbeidsdeling kontrolleres ikke når du oppretter en regel.</span><span class="sxs-lookup"><span data-stu-id="0aca5-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="0aca5-129">Du kan opprette en regel som skaper en konflikt for eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="0aca5-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="0aca5-130">Eksisterende brukerrolletilordninger kan også være i konflikt med den nye regelen.</span><span class="sxs-lookup"><span data-stu-id="0aca5-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="0aca5-131">Du må validere samsvar etter at du har opprettet eller endret en regel.</span><span class="sxs-lookup"><span data-stu-id="0aca5-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="0aca5-132">Hvis du vil ha mer informasjon, kan du se [Identifisere og løse konflikter i arbeidsdeling](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="0aca5-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]