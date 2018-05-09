--- 
title: Definere finansdimensjoner
description: "Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 192af4e8a9f77e4728954375d9d9699187137803
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="51831-103">Definere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="51831-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51831-104">Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="51831-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="51831-105">Veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="51831-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="51831-106">Opprette en enhetsstøttet finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="51831-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="51831-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="51831-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="51831-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="51831-108">Click New.</span></span>
3. <span data-ttu-id="51831-109">Velg en systemdefinert enhet som finansdimensjonen baseres på, i feltet Brukerverdier fra.</span><span class="sxs-lookup"><span data-stu-id="51831-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="51831-110">Skriv inn en verdi for å beskrive finansdimensjonen i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="51831-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="51831-111">Navnet kan være forskjellig fra den systemdefinerte enheten, men kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="51831-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="51831-112">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="51831-112">Click Activate.</span></span>
    * <span data-ttu-id="51831-113">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="51831-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="51831-114">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="51831-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="51831-115">Klikk Lukk på aktiveringsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="51831-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="51831-116">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="51831-116">Click Activate.</span></span>
    * <span data-ttu-id="51831-117">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="51831-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="51831-118">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="51831-118">Click Dimension values.</span></span>
    * <span data-ttu-id="51831-119">Noen dimensjonsverdier er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="51831-119">Some dimension values are company specific.</span></span> <span data-ttu-id="51831-120">Du kan kontrollere om de er firmaspesifikke ved om firmanavnet vises i dimensjonsverdilisten.</span><span class="sxs-lookup"><span data-stu-id="51831-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="51831-121">Opprette en egendefinert finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="51831-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="51831-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="51831-122">Close the page.</span></span>
2. <span data-ttu-id="51831-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="51831-123">Click New.</span></span>
3. <span data-ttu-id="51831-124">Velg et alternativ i feltet Bruk verdier fra <Custom dimension>.</span><span class="sxs-lookup"><span data-stu-id="51831-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="51831-125">Skriv inn en verdi for å beskrive finansdimensjonen i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="51831-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="51831-126">Navnet kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="51831-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="51831-127">Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="51831-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="51831-128">Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek.</span><span class="sxs-lookup"><span data-stu-id="51831-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="51831-129">Du kan også angi nummertegn (#) og &-tegn som plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes.</span><span class="sxs-lookup"><span data-stu-id="51831-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="51831-130">Bruk et nummertegn (#) som plassholder for et tall og et &-tegn som plassholder for en bokstav.</span><span class="sxs-lookup"><span data-stu-id="51831-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="51831-131">Eksempel: Hvis du vil begrense dimensjonsverdien til bokstavene CC og tre tall, kan du angi CC-### som formatmaske.</span><span class="sxs-lookup"><span data-stu-id="51831-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="51831-132">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="51831-132">Click Activate.</span></span>
    * <span data-ttu-id="51831-133">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="51831-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="51831-134">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="51831-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="51831-135">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="51831-135">Click Activate.</span></span>
    * <span data-ttu-id="51831-136">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="51831-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="51831-137">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="51831-137">Click Dimension values.</span></span>
8. <span data-ttu-id="51831-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="51831-138">Click New.</span></span>
9. <span data-ttu-id="51831-139">Skriv inn et navn for å beskrive finansdimensjonsverdien i feltet Dimensjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="51831-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="51831-140">Skriv inn en beskrivelse som beskriver finansdimensjonsverdien i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="51831-140">In the Description field, type a description that describes your financial dimension value.</span></span>


