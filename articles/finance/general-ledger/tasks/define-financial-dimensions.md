---
title: Definere finansdimensjoner
description: Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb2dc5df96198f3c9f68fcac70b2e5dcbe8c8832
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175567"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="7d362-103">Definere finansdimensjoner</span><span class="sxs-lookup"><span data-stu-id="7d362-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d362-104">Denne oppgaveveiledningen beskriver hvordan du legger til en enhetsstøttet finansdimensjon og en egendefinert finansdimensjon.</span><span class="sxs-lookup"><span data-stu-id="7d362-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="7d362-105">Veiledningen bruker USMF demo firmaet.</span><span class="sxs-lookup"><span data-stu-id="7d362-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="7d362-106">Opprette en enhetsstøttet finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="7d362-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="7d362-107">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="7d362-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="7d362-108">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7d362-108">Click **New**.</span></span>
3. <span data-ttu-id="7d362-109">Velg en systemdefinert enhet som finansdimensjonen baseres på, i feltet **Brukerverdier fra**.</span><span class="sxs-lookup"><span data-stu-id="7d362-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="7d362-110">Skriv inn en verdi for å beskrive finansdimensjonen i feltet **Dimensjonsnavn**.</span><span class="sxs-lookup"><span data-stu-id="7d362-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="7d362-111">Navnet kan være forskjellig fra den systemdefinerte enheten, men kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="7d362-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="7d362-112">Klikk **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7d362-112">Click **Activate**.</span></span> <span data-ttu-id="7d362-113">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7d362-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="7d362-114">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="7d362-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="7d362-115">Klikk på **Lukk** på aktiveringsmeldingen.</span><span class="sxs-lookup"><span data-stu-id="7d362-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="7d362-116">Klikk **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7d362-116">Click **Activate**.</span></span> <span data-ttu-id="7d362-117">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="7d362-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="7d362-118">I **handlingsruten** klikker du på **Dimensjonsverdier**.</span><span class="sxs-lookup"><span data-stu-id="7d362-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="7d362-119">Noen dimensjonsverdier er firmaspesifikke.</span><span class="sxs-lookup"><span data-stu-id="7d362-119">Some dimension values are company specific.</span></span> <span data-ttu-id="7d362-120">Du kan kontrollere om de er firmaspesifikke ved om firmanavnet vises i dimensjonsverdilisten.</span><span class="sxs-lookup"><span data-stu-id="7d362-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="7d362-121">Opprette en egendefinert finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="7d362-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="7d362-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7d362-122">Close the page.</span></span>
2. <span data-ttu-id="7d362-123">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7d362-123">Click **New**.</span></span>
3. <span data-ttu-id="7d362-124">I feltet **Bruk verdier fra** velger du **Egendefinert dimensjon**.</span><span class="sxs-lookup"><span data-stu-id="7d362-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="7d362-125">Skriv inn en verdi for å beskrive finansdimensjonen i feltet **Dimensjonsnavn**.</span><span class="sxs-lookup"><span data-stu-id="7d362-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="7d362-126">Navnet kan ikke inneholde mellomrom eller spesialtegn.</span><span class="sxs-lookup"><span data-stu-id="7d362-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="7d362-127">Du kan også angi en kontomaske for å begrense mengden og typen informasjon som du kan angi for dimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="7d362-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="7d362-128">Du kan angi tegn som forblir de samme for hver dimensjonsverdi, for eksempel bokstaver eller en bindestrek.</span><span class="sxs-lookup"><span data-stu-id="7d362-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="7d362-129">Du kan også angi nummertegn (#) og &-tegn som plassholdere for bokstaver og tall som vil endres hver gang en dimensjonsverdi opprettes.</span><span class="sxs-lookup"><span data-stu-id="7d362-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="7d362-130">Bruk et nummertegn (#) som plassholder for et tall og et &-tegn som plassholder for en bokstav.</span><span class="sxs-lookup"><span data-stu-id="7d362-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="7d362-131">Eksempel: Hvis du vil begrense dimensjonsverdien til bokstavene CC og tre tall, kan du angi CC-### som formatmaske.</span><span class="sxs-lookup"><span data-stu-id="7d362-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="7d362-132">Klikk **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7d362-132">Click **Activate**.</span></span> <span data-ttu-id="7d362-133">Aktivering av finansdimensjonen oppdaterer tabellen med finansdimensjonsnavnet og fjerner slettede dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7d362-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="7d362-134">Du kan angi dimensjonsverdier før du aktiverer en finansdimensjon, men en finansdimensjon kan ikke brukes før den er aktivert.</span><span class="sxs-lookup"><span data-stu-id="7d362-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="7d362-135">Klikk **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="7d362-135">Click **Activate**.</span></span> <span data-ttu-id="7d362-136">Aktivering av dimensjonen kan planlegges til å kjøre som parti på en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="7d362-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="7d362-137">I **handlingsruten** klikker du på **Dimensjonsverdier**.</span><span class="sxs-lookup"><span data-stu-id="7d362-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="7d362-138">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7d362-138">Click **New**.</span></span>
9. <span data-ttu-id="7d362-139">Skriv inn et navn for å beskrive finansdimensjonsverdien i feltet **Dimensjonsverdi**.</span><span class="sxs-lookup"><span data-stu-id="7d362-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="7d362-140">Skriv inn en beskrivelse som beskriver finansdimensjonsverdien i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7d362-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

