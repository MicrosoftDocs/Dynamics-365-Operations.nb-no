--- 
title: "Angi søker- og søknadsdata manuelt"
description: "Denne fremgangsmåten viser hvordan du vedlikeholder informasjon om søkere og søknader manuelt."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e0da2c4e308ef377b7657f0905fec56e47f27b99
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="6fa44-103">Angi søker- og søknadsdata manuelt</span><span class="sxs-lookup"><span data-stu-id="6fa44-103">Enter applicant and application data manually</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6fa44-104">Denne fremgangsmåten viser hvordan du vedlikeholder informasjon om søkere og søknader manuelt.</span><span class="sxs-lookup"><span data-stu-id="6fa44-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="6fa44-105">Du kan angi og vedlikeholde personlige opplysninger, intervjudatoer og -klokkeslett, referanser, kompetanser og overnattingsforespørsler for søkere.</span><span class="sxs-lookup"><span data-stu-id="6fa44-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="6fa44-106">Du kan også oppdatere status for søkerens søknader om ansettelse og opprette brev eller e-postmeldinger for å kommunisere med søkere.</span><span class="sxs-lookup"><span data-stu-id="6fa44-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="6fa44-107">Når du oppretter en søkerpost, opprettes en personpost for den søkeren i den globale adresseboken.</span><span class="sxs-lookup"><span data-stu-id="6fa44-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="6fa44-108">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6fa44-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="6fa44-109">Opprette en ny søkerpost</span><span class="sxs-lookup"><span data-stu-id="6fa44-109">Create a new applicant record</span></span>
1. <span data-ttu-id="6fa44-110">Gå til Personale > Rekruttering > Søkere > Søkere.</span><span class="sxs-lookup"><span data-stu-id="6fa44-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="6fa44-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6fa44-111">Click New.</span></span>
3. <span data-ttu-id="6fa44-112">Skriv inn en verdi i feltet Fornavn.</span><span class="sxs-lookup"><span data-stu-id="6fa44-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="6fa44-113">Skriv inn en verdi i feltet Etternavn.</span><span class="sxs-lookup"><span data-stu-id="6fa44-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="6fa44-114">Hvis den er tilgjengelig, kan du angi ytterligere informasjon om søker.</span><span class="sxs-lookup"><span data-stu-id="6fa44-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="6fa44-115">Informasjonen kan for eksempel inkludere søkerens høyeste utdanning, nåværende stilling eller forrige arbeidsgiver.</span><span class="sxs-lookup"><span data-stu-id="6fa44-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="6fa44-116">Aktiver/deaktiver utvidelsen av delen Kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="6fa44-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="6fa44-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="6fa44-117">Click Add.</span></span>
7. <span data-ttu-id="6fa44-118">I Beskrivelse-feltet skriver du inn E-postkommunikasjon.</span><span class="sxs-lookup"><span data-stu-id="6fa44-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="6fa44-119">Velg et alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="6fa44-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="6fa44-120">Angi en verdi i feltet Kontaktnummer/-adresse.</span><span class="sxs-lookup"><span data-stu-id="6fa44-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="6fa44-121">Denne e-postadressen brukes til å generere e-postkommunikasjon med søkeren.</span><span class="sxs-lookup"><span data-stu-id="6fa44-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="6fa44-122">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="6fa44-122">Click Add.</span></span>
11. <span data-ttu-id="6fa44-123">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6fa44-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="6fa44-124">Angi en verdi i feltet Kontaktnummer/-adresse.</span><span class="sxs-lookup"><span data-stu-id="6fa44-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="6fa44-125">Personlige opplysninger om søker.</span><span class="sxs-lookup"><span data-stu-id="6fa44-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="6fa44-126">Du kan angi personlig tilleggsinformasjon for søkeren, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="6fa44-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="6fa44-127">Dette kan for eksempel inkludere fødselsdato, etnisk opprinnelse, kjønn eller sivilstand.</span><span class="sxs-lookup"><span data-stu-id="6fa44-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="6fa44-128">Klikk Kompetanser i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="6fa44-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="6fa44-129">Du kan angi søkerens kompetanseprofil, inkludert ferdigheter, yrkeserfaring, utdannelse, tester eller sertifikater.</span><span class="sxs-lookup"><span data-stu-id="6fa44-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="6fa44-130">Denne informasjonen kan brukes til å tilordne søkerens ferdigheter til kompetansen som er knyttet til prosjekter som er definert i firmaets data.</span><span class="sxs-lookup"><span data-stu-id="6fa44-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="6fa44-131">Opprette en søknad for søkeren</span><span class="sxs-lookup"><span data-stu-id="6fa44-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="6fa44-132">Klikk Søknader.</span><span class="sxs-lookup"><span data-stu-id="6fa44-132">Click Applications.</span></span>
2. <span data-ttu-id="6fa44-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="6fa44-133">Click New.</span></span>
3. <span data-ttu-id="6fa44-134">Klikk rullegardinknappen i feltet Rekrutteringsprosjekt for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6fa44-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6fa44-135">Ved å velge et rekrutteringsprosjekt knyttes søkeren til en bestemt ledig stilling som er inkludert i dette rekrutteringsprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6fa44-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="6fa44-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="6fa44-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6fa44-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6fa44-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6fa44-138">Jobb og avdeling er basert på det valgte rekrutteringsprosjektet som standard.</span><span class="sxs-lookup"><span data-stu-id="6fa44-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="6fa44-139">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="6fa44-139">Click Save.</span></span>
    * <span data-ttu-id="6fa44-140">Etter at søknaden er lagret, kan du legge ved dokumenter til den, inkludert søkerens erfaring, priser og følgebrev.</span><span class="sxs-lookup"><span data-stu-id="6fa44-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  


