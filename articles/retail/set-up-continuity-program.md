---
title: Definere et kontinuitetsprogram for et telefonsenter
description: Denne artikkelen beskriver hvordan du setter opp et kontinuitetsprogram for et telefonsenter.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 106128399a64afb808c82e9a7b268039f9a3cf32
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="827f7-103">Definere et kontinuitetsprogram for et telefonsenter</span><span class="sxs-lookup"><span data-stu-id="827f7-103">Set up a continuity program for a call center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="827f7-104">Denne artikkelen beskriver hvordan du setter opp et kontinuitetsprogram for et telefonsenter.</span><span class="sxs-lookup"><span data-stu-id="827f7-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="827f7-105">I et kontinuitetsprogram, som også kalles et program for regelmessige ordrer, mottar kunder regelmessige produktforsendelser i henhold til en forhåndsdefinert tidsplan.</span><span class="sxs-lookup"><span data-stu-id="827f7-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="827f7-106">Hver forsendelse kan inneholde et forskjellig produkt, som for eksempel månedens bok i en bokklubb, eller det samme produktet kan sendes gjentatte ganger.</span><span class="sxs-lookup"><span data-stu-id="827f7-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="827f7-107">Du må fullføre følgende oppgaver hvis du vil definere et kontinuitetsprogram.</span><span class="sxs-lookup"><span data-stu-id="827f7-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="827f7-108">Angi kontinuitetsparametere på siden **Telefonsenterparametere**.</span><span class="sxs-lookup"><span data-stu-id="827f7-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="827f7-109">Opprett deretter et kontinuitetsprogram som angir detaljer, for eksempel betalingsplanen, tidfestingen av forsendelsene, og om det faktureres på forhånd.</span><span class="sxs-lookup"><span data-stu-id="827f7-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="827f7-110">Du må også legge til en liste over produkter som er inkludert i kontinuitetsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="827f7-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="827f7-111">Hvert produkt mottar et hendelses-ID-nummer som tilordnes sekvensielt fra 1.</span><span class="sxs-lookup"><span data-stu-id="827f7-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="827f7-112">Hendelses-ID-er bestemmer rekkefølgen som produktene sendes i.</span><span class="sxs-lookup"><span data-stu-id="827f7-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="827f7-113">Hvis kunder mottar forskjellige produkter i hver forsendelse, sendes produktene i rekkefølge basert på deres hendelses-ID fra og med gjeldende hendelse.</span><span class="sxs-lookup"><span data-stu-id="827f7-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="827f7-114">Hvis kunder mottar det samme produktet i hver forsendelse, inneholder listen bare ett produkt som har én hendelses-ID.</span><span class="sxs-lookup"><span data-stu-id="827f7-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="827f7-115">Samme hendelse forekommer gjentatte ganger.</span><span class="sxs-lookup"><span data-stu-id="827f7-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="827f7-116">Du kan angi hvor mange ganger hver hendelse gjentas.</span><span class="sxs-lookup"><span data-stu-id="827f7-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="827f7-117">Opprett et overordnet produkt som representerer kontinuitetsprogrammet du opprettet i oppgave 2.</span><span class="sxs-lookup"><span data-stu-id="827f7-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="827f7-118">Hvis du legger til dette produktet i en salgsordre, åpnes siden **Kontinuitet**.</span><span class="sxs-lookup"><span data-stu-id="827f7-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="827f7-119">Du kan deretter bruke denne siden til å opprette den faktiske kontinuitetsordren.</span><span class="sxs-lookup"><span data-stu-id="827f7-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="827f7-120">Det overordnede produktet angir ikke enkeltproduktene som kunden mottar i hver forsendelse.</span><span class="sxs-lookup"><span data-stu-id="827f7-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="827f7-121">Når du har definert et kontinuitetsprogram som beskrevet ovenfor, kan du opprette en kontinuitetsordre for en kunde.</span><span class="sxs-lookup"><span data-stu-id="827f7-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="827f7-122">Du må kanskje også utføre følgende ekstra vedlikeholdsoppgaver.</span><span class="sxs-lookup"><span data-stu-id="827f7-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="827f7-123">**Oppdatere gjeldende hendelsesperiode for kontinuitet** – Konfigurer en satsvis jobb som angir for systemet hva gjeldende hendelsesperiode er.</span><span class="sxs-lookup"><span data-stu-id="827f7-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="827f7-124">**Opprett underordnede kontinuitetsordrer** – Opprett underordnede ordrer fra den overordnede kontinuitetsordren.</span><span class="sxs-lookup"><span data-stu-id="827f7-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="827f7-125">**Behandle kontinuitetsbetalinger** – Behandle fakturering og varsler for betalinger som er knyttet til kontinuitetssalgsordrer.</span><span class="sxs-lookup"><span data-stu-id="827f7-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="827f7-126">**Utvid kontinuitetslinjer** (om nødvendig) – Utvid antall ganger en kontinuitetshendelse kan gjentas.</span><span class="sxs-lookup"><span data-stu-id="827f7-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="827f7-127">Gjentakelsen av forsendelser kan deretter gå utover grensen som er angitt i feltet **Terskel for kontinuitetsgjentakelse** i telefonsenterparameterne.</span><span class="sxs-lookup"><span data-stu-id="827f7-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="827f7-128">**Utfør en kontinuitetsoppdatering** (om nødvendig) – Synkroniser endringer mellom kontinuitetsprogrammet og de overordnede kontinuitetssalgsordrene.</span><span class="sxs-lookup"><span data-stu-id="827f7-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="827f7-129">**Lukk overordnede kontinuitetslinjer og -ordrer** – Lukk kontinuitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="827f7-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





