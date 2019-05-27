---
title: Registrere mottaket av returnerte varer
description: Du kan registrere at returnerte varer er ankommet, ved å bruke Ankomstoversikt-skjemaet eller Registrering-skjemaet.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571081"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="df21f-103">Registrere mottaket av returnerte varer</span><span class="sxs-lookup"><span data-stu-id="df21f-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df21f-104">Det er to metoder for å registrere mottak av returnerte varer.</span><span class="sxs-lookup"><span data-stu-id="df21f-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="df21f-105">Den første metoden er en lagermottaksprosess som bruker **Ankomstoversikt**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="df21f-106">Den andre bruker **Registrering**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="df21f-107">Registrere mottaket av returnerte varer i Ankomstoversikt-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="df21f-108">Du kan bruke **Ankomstoversikt**-skjemaet for å identifisere en returforsendelse ved hjelp av autorisasjonsreturnummeret.</span><span class="sxs-lookup"><span data-stu-id="df21f-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="df21f-109">Hvis det er angitt et journalnavn i kategorien **Oppsett** og det finnes journallinjer som samsvarer med de valgte linjene i **Ankomstoversikt**-skjemaet, blir det opprettete et nytt journalhode når du klikker **Start ankomst**.</span><span class="sxs-lookup"><span data-stu-id="df21f-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="df21f-110">Klikk **Lagerstyring** \> **Periodisk** \> **Ankomstoversikt**.</span><span class="sxs-lookup"><span data-stu-id="df21f-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="df21f-111">I feltet **Oppsettsnavn** velger du **Returordre** og klikker deretter **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="df21f-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="df21f-112">Du kan bruke <STRONG>Område</STRONG>-feltene til å begrense søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="df21f-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="df21f-113">Du kan skrive eller velge autorisasjonsreturnummeret i feltet <STRONG>Autorisasjonsreturnummer</STRONG> for å få et nøyaktig resultat.</span><span class="sxs-lookup"><span data-stu-id="df21f-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="df21f-114">Hvis du vil definere og lagre et sett med filtre som vil begrense hvilke innkommende ankomster som vises, klikker du <STRONG>Oppsett</STRONG>-kategorien. Tilgjengelige filtre omfatter typer, lagre og utleveringsporter.</span><span class="sxs-lookup"><span data-stu-id="df21f-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="df21f-115">Returordre kan ikke blandes med andre ankomsttyper i <STRONG>Ankomstoversikt</STRONG>-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="df21f-116">Referansen vil derfor alltid være salgsordre, men ingen salgsordre-ID vil være angitt i journalhodet.</span><span class="sxs-lookup"><span data-stu-id="df21f-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="df21f-117">I **Mottak**-rutenettet finner du linjen som samsvarer med varen som returneres, og deretter merker du av for avmerkingsboksen i kolonnen **Velg for ankomst**.</span><span class="sxs-lookup"><span data-stu-id="df21f-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="df21f-118">Hvis du vil ekskludere visse linjer fra returmottaket, som for eksempel varer fra den opprinnelige ordren som ikke var inkludert i returforsendelsen, kan du fjerne merket i de tilknyttede **Velg for ankomst**-boksene i **Linjer**-tabellen i nederste del av skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="df21f-119">Klikk **Start ankomst** for å opprette en ankomstjournal.</span><span class="sxs-lookup"><span data-stu-id="df21f-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="df21f-120">Du kan velge flere returordrer og inkludere dem i en enkelt ankomstprosess.</span><span class="sxs-lookup"><span data-stu-id="df21f-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="df21f-121">Hver returordrelinje kopieres til en tilhørende vareankomstjournallinje.</span><span class="sxs-lookup"><span data-stu-id="df21f-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="df21f-122">Du kan også opprette en ankomstjournal manuelt ved hjelp av <STRONG>Vareankomst</STRONG>-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="df21f-123">Klikk **Lagerstyring** \> **Journaler** \> **Vareankomst** \> **Vareankomst**.</span><span class="sxs-lookup"><span data-stu-id="df21f-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="df21f-124">Velg ankomstjournalen du akkurat opprettet, og klikk deretter **Linjer** for å åpne skjemaet **Journallinjer, lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="df21f-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="df21f-125">I kategorien **Generelt** justerer du nummeret i **Antall**-feltet ved behov, og deretter tilordner du en disposisjonskode i **Disposisjonskode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="df21f-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="df21f-126">Du kan også merke av for **Karantenestyring** for å sende de returnerte varene gjennom en inspeksjonsprosess i forbindelse med en karanteneordre.</span><span class="sxs-lookup"><span data-stu-id="df21f-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="df21f-127">Hvis du sender de returnerte varene gjennom karantene, kan du ikke angi en disposisjonskode.</span><span class="sxs-lookup"><span data-stu-id="df21f-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="df21f-128">Klikk **Valider**-knappen.</span><span class="sxs-lookup"><span data-stu-id="df21f-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="df21f-129">Hvis det ikke er noen feil i valideringsprosessen, klikker du **Poster**.</span><span class="sxs-lookup"><span data-stu-id="df21f-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="df21f-130">Registrere mottaket av returnerte varer i registreringsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="df21f-131">I stedet for å bruke **Ankomstoversikt**-skjemaet kan du bruke **Registrering**-skjemaet til å registrere at returnerte varer er ankommet.</span><span class="sxs-lookup"><span data-stu-id="df21f-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="df21f-132">Klikk **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.</span><span class="sxs-lookup"><span data-stu-id="df21f-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="df21f-133">Opprett en ny returordre eller åpne returordren fra listen.</span><span class="sxs-lookup"><span data-stu-id="df21f-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="df21f-134">Velg returordrelinjen i hurtigfanen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="df21f-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="df21f-135">Klikk **Oppdater linje**, og klikk deretter **Registrering**.</span><span class="sxs-lookup"><span data-stu-id="df21f-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="df21f-136">Tilordne en disposisjonskode i **Disposisjonskode**-feltet, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="df21f-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="df21f-137">Det er ikke mulig å sende varen til inspeksjon som en karanteneordre ved hjelp av <STRONG>Registrering</STRONG>-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="df21f-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="df21f-138">I **Transaksjoner**-rutenettet velger du transaksjonen som skal registreres.</span><span class="sxs-lookup"><span data-stu-id="df21f-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="df21f-139">I **Registrer nå**-rutenettet klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="df21f-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="df21f-140">Gjenta de to forrige trinnene til alle returnerte varer vises i **Registrer nå**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="df21f-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="df21f-141">Klikk **Poster alle**.</span><span class="sxs-lookup"><span data-stu-id="df21f-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="df21f-142">Se også</span><span class="sxs-lookup"><span data-stu-id="df21f-142">See also</span></span>

<span data-ttu-id="df21f-143">[Ankomstoversikt (skjema)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="df21f-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


