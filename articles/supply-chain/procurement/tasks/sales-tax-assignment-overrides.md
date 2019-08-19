---
title: Mva-tilordning og overstyringer
description: Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til kanaler for detaljhandel.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f08829bccbaea6fb70563e553f9042300b4d5ea9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838004"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="3f4b3-103">Mva-tilordning og overstyringer</span><span class="sxs-lookup"><span data-stu-id="3f4b3-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f4b3-104">Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til kanaler for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="3f4b3-105">Den veileder deg også gjennom oppretting av en ny mva-overstyring og tilordning av den til en eksisterende mva-overstyringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="3f4b3-106">Denne prosedyren</span><span class="sxs-lookup"><span data-stu-id="3f4b3-106">This procedure</span></span>

<span data-ttu-id="3f4b3-107">bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3f4b3-108">Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="3f4b3-109">I listen klikker du koblingen ID for detaljhandelskanal for Houston.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="3f4b3-110">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-110">Click Edit.</span></span>
    * <span data-ttu-id="3f4b3-111">Feltet Merverdiavgiftsgruppe inneholder en liste over merverdiavgiftsgrupper for gjeldende firma.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="3f4b3-112">Gjeldende tildelt gruppe er en generisk "Texas"-merverdiavgiftsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="3f4b3-113">Det finnes også mva-grupper for "Washington" og "Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="3f4b3-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="3f4b3-114">Mva-grupper kan inneholde gjeldende avgifter for flere områder.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="3f4b3-115">Feltet Merverdiavgiftoverstyring er der merverdiavgiftoverstyringsgrupper kan tilordnes til kanalen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="3f4b3-116">Merverdiavgiftoverstyringsgrupper kan brukes til å gruppere sammen merverdiavgiftoverstyringer som fungerer for flere butikker.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="3f4b3-117">I stedet for manuell, enkeltvis tilordning av merverdiavgiftoverstyringer, kan gruppen opprettes og tilordnes direkte til kanalene for å spare tid.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="3f4b3-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-118">Click Save.</span></span>
5. <span data-ttu-id="3f4b3-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-119">Close the page.</span></span>
6. <span data-ttu-id="3f4b3-120">Gå til Detaljhandel og handel > Kanaloppsett > Merverdiavgift > Mva-overstyringer.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="3f4b3-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-121">Click New.</span></span>
8. <span data-ttu-id="3f4b3-122">Angi et navn for den nye overstyringen i feltet Mva-overstyring.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="3f4b3-123">Angi en kort beskrivelse av overstyringen i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="3f4b3-124">Sett statusen til Aktiver.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="3f4b3-125">Vis eller skjul delen Overstyr.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="3f4b3-126">Velg et alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="3f4b3-127">Mva-grupper for vare kan brukes til å overstyre avgifter for bestemte varer som tilhører gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="3f4b3-128">Matvarer beskattes for eksempel vanligvis forskjellig fra fastvarer, og vil sannsynligvis ha sin egen mva-gruppe.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="3f4b3-129">Mva-grupper er grupper med mva som gjelder for en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="3f4b3-130">Hvis en kanal for eksempel selger både via detaljhandel og bedrift-til-bedrift, kan mva-grupper for ulike varer brukes.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="3f4b3-131">Alle gjeldende avgifter vil bli tilordnet til mva-gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="3f4b3-132">Nå kan du velge Fra- og Til-avgifter eller Fra avgiftsgruppe og Til avgiftsgruppe for å opprette i mva-overstyring.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="3f4b3-133">I Fra-feltet angir avgiften eller avgiftsgruppen som skal overstyres.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="3f4b3-134">Overstyring etter merverdiavgiftsgruppen for vare inneholder andre alternativer enn overstyring etter salgsavgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="3f4b3-135">Mva-overstyringer kan defineres til å overstyre avgifter på hele transaksjoner eller bestemte linjer i transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="3f4b3-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-136">Click Save.</span></span>
14. <span data-ttu-id="3f4b3-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-137">Close the page.</span></span>
15. <span data-ttu-id="3f4b3-138">Gå til Detaljhandel og handel > Kanaloppsett > Merverdiavgift > Mva-overstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="3f4b3-139">I dette trinnet vil du tilordnet den nyopprettede mva-overstyringen til mva-overstyringsgruppen som er tilordnet Houston-kanalen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="3f4b3-140">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-140">Click Edit.</span></span>
17. <span data-ttu-id="3f4b3-141">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="3f4b3-142">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-142">Click Add.</span></span>
19. <span data-ttu-id="3f4b3-143">Klikk rullegardinknappen i feltet Mva-overstyringsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3f4b3-144">Velg den tidligere opprettede mva-overstyringen fra listen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="3f4b3-145">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3f4b3-146">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-146">Click Save.</span></span>

