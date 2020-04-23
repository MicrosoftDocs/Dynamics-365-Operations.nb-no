---
title: Mva-tilordning og overstyringer
description: Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til handelskanaler.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74a7eed04648c63c0b19d5de26d2bdbef59aec7d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207606"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="eb843-103"> Mva-tilordning og overstyringer</span><span class="sxs-lookup"><span data-stu-id="eb843-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb843-104">Denne fremgangsmåten beskriver hvordan du tilordner mva-grupper til handelskanaler.</span><span class="sxs-lookup"><span data-stu-id="eb843-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="eb843-105">Den veileder deg også gjennom oppretting av en ny mva-overstyring og tilordning av den til en eksisterende mva-overstyringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb843-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="eb843-106">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="eb843-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="eb843-107">Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.</span><span class="sxs-lookup"><span data-stu-id="eb843-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="eb843-108">I listen klikker du koblingen ID for kanal for Houston.</span><span class="sxs-lookup"><span data-stu-id="eb843-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="eb843-109">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="eb843-109">Click Edit.</span></span>
    * <span data-ttu-id="eb843-110">Feltet Merverdiavgiftsgruppe inneholder en liste over merverdiavgiftsgrupper for gjeldende firma.</span><span class="sxs-lookup"><span data-stu-id="eb843-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="eb843-111">Gjeldende tildelt gruppe er en generisk "Texas"-merverdiavgiftsgruppe.</span><span class="sxs-lookup"><span data-stu-id="eb843-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="eb843-112">Det finnes også mva-grupper for "Washington" og "Washington, King County."</span><span class="sxs-lookup"><span data-stu-id="eb843-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="eb843-113">Mva-grupper kan inneholde gjeldende avgifter for flere områder.</span><span class="sxs-lookup"><span data-stu-id="eb843-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="eb843-114">Feltet Merverdiavgiftoverstyring er der merverdiavgiftoverstyringsgrupper kan tilordnes til kanalen.</span><span class="sxs-lookup"><span data-stu-id="eb843-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="eb843-115">Merverdiavgiftoverstyringsgrupper kan brukes til å gruppere sammen merverdiavgiftoverstyringer som fungerer for flere butikker.</span><span class="sxs-lookup"><span data-stu-id="eb843-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="eb843-116">I stedet for manuell, enkeltvis tilordning av merverdiavgiftoverstyringer, kan gruppen opprettes og tilordnes direkte til kanalene for å spare tid.</span><span class="sxs-lookup"><span data-stu-id="eb843-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="eb843-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eb843-117">Click Save.</span></span>
5. <span data-ttu-id="eb843-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eb843-118">Close the page.</span></span>
6. <span data-ttu-id="eb843-119">Gå til Retail og Commerce > Kanaloppsett > Merverdiavgift > Mva-overstyringer.</span><span class="sxs-lookup"><span data-stu-id="eb843-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="eb843-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eb843-120">Click New.</span></span>
8. <span data-ttu-id="eb843-121">Angi et navn for den nye overstyringen i feltet Mva-overstyring.</span><span class="sxs-lookup"><span data-stu-id="eb843-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="eb843-122">Angi en kort beskrivelse av overstyringen i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb843-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="eb843-123">Sett statusen til Aktiver.</span><span class="sxs-lookup"><span data-stu-id="eb843-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="eb843-124">Vis eller skjul delen Overstyr.</span><span class="sxs-lookup"><span data-stu-id="eb843-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="eb843-125">Velg et alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb843-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="eb843-126">Mva-grupper for vare kan brukes til å overstyre avgifter for bestemte varer som tilhører gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb843-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="eb843-127">Matvarer beskattes for eksempel vanligvis forskjellig fra fastvarer, og vil sannsynligvis ha sin egen mva-gruppe.</span><span class="sxs-lookup"><span data-stu-id="eb843-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="eb843-128">Mva-grupper er grupper med mva som gjelder for en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="eb843-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="eb843-129">Hvis en kanal for eksempel selger både via detaljhandel og bedrift-til-bedrift, kan mva-grupper for ulike varer brukes.</span><span class="sxs-lookup"><span data-stu-id="eb843-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="eb843-130">Alle gjeldende avgifter vil bli tilordnet til mva-gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb843-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="eb843-131">Nå kan du velge Fra- og Til-avgifter eller Fra avgiftsgruppe og Til avgiftsgruppe for å opprette i mva-overstyring.</span><span class="sxs-lookup"><span data-stu-id="eb843-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="eb843-132">I Fra-feltet angir avgiften eller avgiftsgruppen som skal overstyres.</span><span class="sxs-lookup"><span data-stu-id="eb843-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="eb843-133">Overstyring etter merverdiavgiftsgruppen for vare inneholder andre alternativer enn overstyring etter salgsavgiftsgruppen.</span><span class="sxs-lookup"><span data-stu-id="eb843-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="eb843-134">Mva-overstyringer kan defineres til å overstyre avgifter på hele transaksjoner eller bestemte linjer i transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="eb843-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="eb843-135">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eb843-135">Click Save.</span></span>
14. <span data-ttu-id="eb843-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eb843-136">Close the page.</span></span>
15. <span data-ttu-id="eb843-137">Gå til Retail og Commerce > Kanaloppsett > Merverdiavgift > Mva-overstyringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="eb843-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="eb843-138">I dette trinnet vil du tilordnet den nyopprettede mva-overstyringen til mva-overstyringsgruppen som er tilordnet Houston-kanalen.</span><span class="sxs-lookup"><span data-stu-id="eb843-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="eb843-139">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="eb843-139">Click Edit.</span></span>
17. <span data-ttu-id="eb843-140">Vis eller skjul Oppsett-delen.</span><span class="sxs-lookup"><span data-stu-id="eb843-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="eb843-141">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="eb843-141">Click Add.</span></span>
19. <span data-ttu-id="eb843-142">Klikk rullegardinknappen i feltet Mva-overstyringsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eb843-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="eb843-143">Velg den tidligere opprettede mva-overstyringen fra listen.</span><span class="sxs-lookup"><span data-stu-id="eb843-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="eb843-144">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eb843-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="eb843-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eb843-145">Click Save.</span></span>

