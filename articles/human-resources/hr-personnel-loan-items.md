---
title: Administrere varer som er lånt ut til arbeidere
description: Utlånsvarer er poster som hjelper ledere med å spore fysiske varer som firmaet låner ut til arbeidere.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: d34551e4a3cc08ce3fe47e8f8fd2c3cc68c0daf7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130139"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="1bd87-103">Administrere varer som er lånt ut til arbeidere</span><span class="sxs-lookup"><span data-stu-id="1bd87-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="1bd87-104">Utlånsvarer er poster som hjelper ledere med å spore fysiske varer som firmaet låner ut til arbeidere.</span><span class="sxs-lookup"><span data-stu-id="1bd87-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="1bd87-105">Punktene nedenfor viser eksempler på elementer som et firma kan låne ut til ansatte:</span><span class="sxs-lookup"><span data-stu-id="1bd87-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="1bd87-106">Mobiltelefoner</span><span class="sxs-lookup"><span data-stu-id="1bd87-106">Mobile telephones</span></span>
-   <span data-ttu-id="1bd87-107">Biler</span><span class="sxs-lookup"><span data-stu-id="1bd87-107">Automobiles</span></span>
-   <span data-ttu-id="1bd87-108">Datamaskinutstyr</span><span class="sxs-lookup"><span data-stu-id="1bd87-108">Computer equipment</span></span>

<span data-ttu-id="1bd87-109">Hver fysiske vare må ha en tilsvarende utlånsvare.</span><span class="sxs-lookup"><span data-stu-id="1bd87-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="1bd87-110">Hver utlånsvarepost må beskrive hva som lånes ut, hvem som er ansvarlig for utlånet, og antall dager varen kan lånes ut til en arbeider.</span><span class="sxs-lookup"><span data-stu-id="1bd87-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="1bd87-111">Du kan opprette flere utlånsvarer for varer som for eksempel nøkler, adgangskort eller uniformer, samtidig.</span><span class="sxs-lookup"><span data-stu-id="1bd87-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="1bd87-112">Når du låner ut en vare, må du registrere datoen da varen ble utlånt, og den planlagte returdatoen.</span><span class="sxs-lookup"><span data-stu-id="1bd87-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="1bd87-113">Når varen returneres, må du registrere den faktiske returdatoen.</span><span class="sxs-lookup"><span data-stu-id="1bd87-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="1bd87-114">Ansatte kan vise postene for varene som er lånt ut til dem, ved hjelp av området for ansattselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="1bd87-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="1bd87-115">De kan også redigere eksisterende poster eller angi nye elementer for lån, hvis de har mottatt flere fysiske elementer.</span><span class="sxs-lookup"><span data-stu-id="1bd87-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="1bd87-116">Arbeidsflyten kan defineres til å Ruteendringer for nye eller eksisterende utlånsvarer gjennom en godkjenningsprosess.</span><span class="sxs-lookup"><span data-stu-id="1bd87-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="1bd87-117">Ledere kan vise utlånte varer til sine direkte underordnede.</span><span class="sxs-lookup"><span data-stu-id="1bd87-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="1bd87-118">De kan også få tilgang til å legge til nye utlånsvarer på vegne av ansatte.</span><span class="sxs-lookup"><span data-stu-id="1bd87-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="1bd87-119"> Konto for utlånsvarer som er mistet eller kommet bort</span><span class="sxs-lookup"><span data-stu-id="1bd87-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="1bd87-120">Hvis en vare skades eller kommer bort, må du registrere en fiktiv returpost.</span><span class="sxs-lookup"><span data-stu-id="1bd87-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="1bd87-121">Deretter kan du enten slette varen eller beholde den i oversikten, og endre beskrivelsen for å vise at varen ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="1bd87-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="1bd87-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1bd87-122">Additional resources</span></span>
--------

[<span data-ttu-id="1bd87-123">Personale</span><span class="sxs-lookup"><span data-stu-id="1bd87-123">Human resources</span></span>](index.md)



