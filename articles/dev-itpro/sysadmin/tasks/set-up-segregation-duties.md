---
title: Definere arbeidsdeling
description: Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "318793"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="9ad72-103">Definere arbeidsdeling</span><span class="sxs-lookup"><span data-stu-id="9ad72-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ad72-104">Du kan definere regler for å skille aktiviteter som må utføres av forskjellige brukere.</span><span class="sxs-lookup"><span data-stu-id="9ad72-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="9ad72-105">Dette konseptet kalles arbeidsdeling.</span><span class="sxs-lookup"><span data-stu-id="9ad72-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="9ad72-106">Det kan for eksempel være at du ikke vil at den samme personen både skal bekrefte mottak av varer og til å behandle betalingen til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9ad72-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="9ad72-107">Arbeidsdeling hjelper deg med å redusere risikoen for bedrageri, og det hjelper deg å oppdage feil eller uregelmessigheter også.</span><span class="sxs-lookup"><span data-stu-id="9ad72-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="9ad72-108">Du kan også bruke arbeidsdeling til å følge policyer for intern kontroll.</span><span class="sxs-lookup"><span data-stu-id="9ad72-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="9ad72-109">Fullfør fremgangsmåten nedenfor for å opprette en regel.</span><span class="sxs-lookup"><span data-stu-id="9ad72-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="9ad72-110">Du må være en systemansvarlig for å fullføre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="9ad72-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="9ad72-111">Demonstrasjonsdatafirmaet DAT brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9ad72-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="9ad72-112">Gå til Systemadministrasjon > Sikkerhet > Arbeidsdeling > Arbeidsdelingsregler.</span><span class="sxs-lookup"><span data-stu-id="9ad72-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="9ad72-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="9ad72-113">Click New.</span></span>
3. <span data-ttu-id="9ad72-114">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="9ad72-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="9ad72-115">Angi et navn for regelen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="9ad72-116">Klikk rullegardinknappen i feltet Første plikt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9ad72-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9ad72-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9ad72-118">Velg den første plikten som kontrolleres av regelen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="9ad72-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9ad72-120">Klikk rullegardinknappen i feltet Andre plikt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9ad72-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9ad72-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9ad72-122">Velg den andre plikten som kontrolleres av regelen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="9ad72-123">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="9ad72-124">Velg et alternativ i feltet Alvorlighetsgrad.</span><span class="sxs-lookup"><span data-stu-id="9ad72-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="9ad72-125">Velg viktighet for risikoen som oppstår når den samme brukeren eller rollen utfører begge pliktene.</span><span class="sxs-lookup"><span data-stu-id="9ad72-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="9ad72-126">Skriv inn en verdi i feltet Sikkerhetsrisiko.</span><span class="sxs-lookup"><span data-stu-id="9ad72-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="9ad72-127">Angi en beskrivelse av sikkerhetsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="9ad72-128">Skriv inn en verdi i feltet Sikkerhetsreduksjon.</span><span class="sxs-lookup"><span data-stu-id="9ad72-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="9ad72-129">Angi en beskrivelse av handlingene som du gjøre for å redusere sikkerhetsrisikoen.</span><span class="sxs-lookup"><span data-stu-id="9ad72-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="9ad72-130">Du kan for eksempel redusere risikoen ved å utføre mer detaljert gjennomgang av prosessen, utføre en månedlig ledergjennomgang eller ved å dele ressurser med andre avdelinger.</span><span class="sxs-lookup"><span data-stu-id="9ad72-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="9ad72-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9ad72-131">Click Save.</span></span>

