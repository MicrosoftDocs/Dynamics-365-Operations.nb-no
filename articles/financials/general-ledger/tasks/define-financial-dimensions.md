---
title: Definere finansdimensjoner
description: Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5cfe92b8733a0a6d76e074cc31eec3f3935b512
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1530874"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="56b4d-103">Definere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="56b4d-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56b4d-104">Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="56b4d-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="56b4d-105">Veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="56b4d-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="56b4d-106">Opprette en enhetsstøttet finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="56b4d-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="56b4d-107">Gå til Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="56b4d-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="56b4d-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="56b4d-108">Click New.</span></span>
3. <span data-ttu-id="56b4d-109">Velg en systemdefinert enhet som finansdimensjonen baseres på, i feltet Brukerverdier fra.</span><span class="sxs-lookup"><span data-stu-id="56b4d-109">In the User values form field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="56b4d-110">Skriv inn en verdi for å beskrive finansdimensjonen i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="56b4d-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="56b4d-111">Navnet kan være forskjellig fra den systemdefinerte enheten, men kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="56b4d-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="56b4d-112">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="56b4d-112">Click Activate.</span></span>
    * <span data-ttu-id="56b4d-113">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="56b4d-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="56b4d-114">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="56b4d-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="56b4d-115">Klikk Lukk på aktiveringsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="56b4d-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="56b4d-116">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="56b4d-116">Click Activate.</span></span>
    * <span data-ttu-id="56b4d-117">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="56b4d-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="56b4d-118">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="56b4d-118">Click Dimension values.</span></span>
    * <span data-ttu-id="56b4d-119">Noen dimensjonsverdier er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="56b4d-119">Some dimension values are company specific.</span></span> <span data-ttu-id="56b4d-120">Du kan kontrollere om de er firmaspesifikke ved om firmanavnet vises i dimensjonsverdilisten.</span><span class="sxs-lookup"><span data-stu-id="56b4d-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="56b4d-121">Opprette en egendefinert finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="56b4d-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="56b4d-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="56b4d-122">Close the page.</span></span>
2. <span data-ttu-id="56b4d-123">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="56b4d-123">Click New.</span></span>
3. <span data-ttu-id="56b4d-124">I feltet Bruk verdier fra velger du Egendefinert dimensjon.</span><span class="sxs-lookup"><span data-stu-id="56b4d-124">In the Use values from field, select Custom dimension.</span></span>
4. <span data-ttu-id="56b4d-125">Skriv inn en verdi for å beskrive finansdimensjonen i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="56b4d-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="56b4d-126">Navnet kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="56b4d-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="56b4d-127">Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="56b4d-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="56b4d-128">Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek.</span><span class="sxs-lookup"><span data-stu-id="56b4d-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="56b4d-129">Du kan også angi nummertegn (#) og &-tegn som plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes.</span><span class="sxs-lookup"><span data-stu-id="56b4d-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="56b4d-130">Bruk et nummertegn (#) som plassholder for et tall og et &-tegn som plassholder for en bokstav.</span><span class="sxs-lookup"><span data-stu-id="56b4d-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="56b4d-131">Eksempel: Hvis du vil begrense dimensjonsverdien til bokstavene CC og tre tall, kan du angi CC-### som formatmaske.</span><span class="sxs-lookup"><span data-stu-id="56b4d-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="56b4d-132">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="56b4d-132">Click Activate.</span></span>
    * <span data-ttu-id="56b4d-133">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="56b4d-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="56b4d-134">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="56b4d-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="56b4d-135">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="56b4d-135">Click Activate.</span></span>
    * <span data-ttu-id="56b4d-136">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="56b4d-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="56b4d-137">Klikk Dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="56b4d-137">Click Dimension values.</span></span>
8. <span data-ttu-id="56b4d-138">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="56b4d-138">Click New.</span></span>
9. <span data-ttu-id="56b4d-139">Skriv inn et navn for å beskrive finansdimensjonsverdien i feltet Dimensjonsverdi.</span><span class="sxs-lookup"><span data-stu-id="56b4d-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="56b4d-140">Skriv inn en beskrivelse som beskriver finansdimensjonsverdien i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="56b4d-140">In the Description field, type a description that describes your financial dimension value.</span></span>

