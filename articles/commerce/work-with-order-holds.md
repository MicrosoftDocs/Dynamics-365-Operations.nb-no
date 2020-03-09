---
title: Konfigurere og arbeide med telefonsenterordresperringer
description: Dette emnet beskriver hvordan du arbeider med sperringer på ordrer ved hjelp av Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 08c0eda418af1aa56c6cc71ca1f7f10460651bc9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023518"
---
# <a name="configure-and-work-with-call-center-order-holds"></a><span data-ttu-id="905ef-103">Konfigurere og arbeide med ordresperrer i telefonsenter</span><span class="sxs-lookup"><span data-stu-id="905ef-103">Configure and work with call center order holds</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="905ef-104">Dette emnet beskriver ordresperrefunksjonene som Dynamics 365 Commerce har for telefonsenterordrer.</span><span class="sxs-lookup"><span data-stu-id="905ef-104">This topic describes the order hold features that Dynamics 365 Commerce has for call center orders.</span></span>

## <a name="configuring-call-center-order-holds"></a><span data-ttu-id="905ef-105">Konfigurere telefonsenterordresperrer</span><span class="sxs-lookup"><span data-stu-id="905ef-105">Configuring call center order holds</span></span>

<span data-ttu-id="905ef-106">For å bruke sperrefunksjonene for telefonsenterordrer må du først angi sperrekoder.</span><span class="sxs-lookup"><span data-stu-id="905ef-106">To use the call center order hold features, you must first define hold codes.</span></span> <span data-ttu-id="905ef-107">Hvis du vil opprette et sett med brukerdefinerte sperrekoder basert på dine forretningskrav, kan du gå til **Salg og markedsføring** \> **Oppsett** \> **Salgsordrer** \> **Ordresperrekoder**.</span><span class="sxs-lookup"><span data-stu-id="905ef-107">To create a set of user-defined hold codes, based on your business requirements, go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Order hold codes**.</span></span> <span data-ttu-id="905ef-108">Du kan eventuelt flagge en av sperrekodene som standard sperrekode ved å sette **Standard for salgsordre**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="905ef-108">You can optionally flag one of the hold codes as the default hold code by setting the **Default for sales order** option to **Yes** for it.</span></span> <span data-ttu-id="905ef-109">Denne sperrekoden vil bli brukt hver gang en salgsordre er satt på vent.</span><span class="sxs-lookup"><span data-stu-id="905ef-109">This hold code will be used any time that a sales order is put on hold.</span></span> <span data-ttu-id="905ef-110">Hvis en salgsordre har reservert lager, og reservasjonene må fjernes automatisk hvis ordren er satt på vent av en bestemt årsak, kan du angi **Fjern beholdningsreservasjoner**-alternativet til **Ja** for årsakskodene.</span><span class="sxs-lookup"><span data-stu-id="905ef-110">If a sales order has reserved inventory, and the reservations must be automatically removed if the order is put on hold for a particular reason, set the **Remove inventory reservations** option to **Yes** for the reason codes.</span></span>

<span data-ttu-id="905ef-111">Hvis du vil angi hvilken type merknad som skal registreres når brukere som plasserer en ordre på vent, angir valgfrie merknader, kan du gå til **Kunder** \> **Oppsett** \> **Kundeparametere**, og på **Salgsoppsett**-hurtigkategorien i **Generelt**-kategorien kan du angi **Merknadstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="905ef-111">To specify the type of note that will be captured when users who put a sales order on hold enter optional notes, go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**, and then, on the **Sales setup** FastTab, on the **General** tab, set the **Note type** field.</span></span> <span data-ttu-id="905ef-112">Bruk **På vent-salgsordrestatus**-feltet for å definere fargen som brukes til å utheve salgsordrer som er på vent når de vises på **Kundeservice**-siden.</span><span class="sxs-lookup"><span data-stu-id="905ef-112">Use the **On Hold sales order status** field to define the color that will be used to highlight sales orders that are on hold when they are viewed on the **Customer service** page.</span></span>

<span data-ttu-id="905ef-113">Hvis du vil opprette et valgfritt sett med På vent-årsakskoder, kan du gå til **Retail og Commerce** \> **Kanaloppsett** \> **Infokoder**.</span><span class="sxs-lookup"><span data-stu-id="905ef-113">To create an optional set of hold reason codes, go to **Retail and Commerce** \> **Channel setup** \> **Info codes**.</span></span> <span data-ttu-id="905ef-114">Disse infokodene kan brukes som sekundær årsakskode for å definere hovedsperrekoden nærmere.</span><span class="sxs-lookup"><span data-stu-id="905ef-114">These info codes can be used as a secondary reason code to further define the main hold code.</span></span> <span data-ttu-id="905ef-115">Velg **Ny** for å opprette et årsakskodesett, og velg deretter **Delkoder** for å definere listen over tilleggsårsaker.</span><span class="sxs-lookup"><span data-stu-id="905ef-115">Select **New** to create a reason code set, and then select **Subcodes** to define the list of additional reasons.</span></span> <span data-ttu-id="905ef-116">Hvis du vil koble infokoder som du definerer til telefonsenterkanalen, kan du gå til **Retail og Commerce** \> **Kanaler** \> **Telefonsentre** \> **Alle telefonsentre**.</span><span class="sxs-lookup"><span data-stu-id="905ef-116">To link any info codes that you define to the call center channel, go to **Retail and Commerce** \> **Channels** \> **Call centers** \> **All call centers**.</span></span> <span data-ttu-id="905ef-117">På **Generelt**-hurtigfanen angir du **Sperrekode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="905ef-117">On the **General** FastTab, set the **Hold code** field.</span></span>

## <a name="putting-orders-on-hold"></a><span data-ttu-id="905ef-118">Sette ordrer på vent</span><span class="sxs-lookup"><span data-stu-id="905ef-118">Putting orders on hold</span></span>

<span data-ttu-id="905ef-119">Ordrer som telefonsenterbrukere oppretter i bakhandelsprogrammet, kan settes på vent manuelt eller automatisk i bestemte situasjoner.</span><span class="sxs-lookup"><span data-stu-id="905ef-119">Orders that call center users create in the back-office Commerce program can be manually put on hold manually or automatically in specific situations.</span></span>

<span data-ttu-id="905ef-120">Under ordreregistrering, men før bestillingen legges inn og bekreftes, ønsker telefonsenterbrukere kanskje å sette en ordre på vent manuelt for å hindre at den blir frigitt til lageret for videre behandling.</span><span class="sxs-lookup"><span data-stu-id="905ef-120">During order entry, but before order submission and confirmation, call center users might want to manually put an order on hold to prevent it from being released to the warehouse for further processing.</span></span> <span data-ttu-id="905ef-121">Kunden som plasserer ordren er eksempelvis kanskje ikke klar til å forplikte seg til den, eller kritiske data som kreves for å behandle ordren, mangler kanskje.</span><span class="sxs-lookup"><span data-stu-id="905ef-121">For example, the customer who is placing the order might not be ready to commit to it, or critical data that is required in order to process the order might be missing.</span></span>

<span data-ttu-id="905ef-122">På siden for ordreregistrering kan telefonsenterbrukeren sette en ordre på vent ved å bruke **Ordresperrer**-alternativet på **Salgsordre**-kategorien på ordreregistreringsmenyen.</span><span class="sxs-lookup"><span data-stu-id="905ef-122">On the order entry page, the call center user can put an order on hold by using the **Order holds** option on the **Sales order** tab of the order entry menu.</span></span> <span data-ttu-id="905ef-123">Brukeren kan også velge **Sperre**-menyelementet på **Salgsordresammendrag**-siden som vises når han eller hun velger **Fullført** på en salgsordre via et telefonsenter.</span><span class="sxs-lookup"><span data-stu-id="905ef-123">Alternatively, the user can select the **Hold** menu item on the **Sales order summary** page that appears when he or she selects **Complete** on a call center sales order.</span></span>

<span data-ttu-id="905ef-124">I begge tilfeller vises siden **Ordresperrer**.</span><span class="sxs-lookup"><span data-stu-id="905ef-124">In both cases, the **Order holds** page appears.</span></span> <span data-ttu-id="905ef-125">Deretter kan brukeren velge **Ny** for å opprette en sperring for ordren.</span><span class="sxs-lookup"><span data-stu-id="905ef-125">The user can then select **New** to create a hold for the order.</span></span> <span data-ttu-id="905ef-126">I **Sperrekode**-feltet bør brukeren velge koden som best beskriver årsaken til sperringen.</span><span class="sxs-lookup"><span data-stu-id="905ef-126">In the **Hold code** field, the user should select the code that best describes the reason for the hold.</span></span> <span data-ttu-id="905ef-127">I **Årsakskode**-feltet kan brukeren også velge en tilleggskode for å gi et ekstra nivå for beskrivelsen av sperringen.</span><span class="sxs-lookup"><span data-stu-id="905ef-127">In the **Reason code** field, the user can optionally select an additional code to provide a second level of description of the hold.</span></span>

<span data-ttu-id="905ef-128">I **Merknader**-hurtigkategorien i **Sperremerknader**-feltet kan brukeren angi ytterligere merknader i fritt format for å gi ytterligere kontekst eller informasjon om sperringen.</span><span class="sxs-lookup"><span data-stu-id="905ef-128">On the **Notes** FastTab, in the **Hold Notes** field, the user can enter additional, free-form notes to provide additional context or information about the hold.</span></span> <span data-ttu-id="905ef-129">Disse merknadene kan hjelpe andre brukere som gjennomgår eller arbeider med sperreorden senere.</span><span class="sxs-lookup"><span data-stu-id="905ef-129">These notes can help other users who review or work with the hold order later.</span></span>

<span data-ttu-id="905ef-130">Når sperreinformasjonen er angitt og lagret, kan brukeren lukke **Ordresperrer**-siden.</span><span class="sxs-lookup"><span data-stu-id="905ef-130">After the hold information is entered and saved, the user can close the **Order holds** page.</span></span> <span data-ttu-id="905ef-131">Brukeren returneres deretter til siden for salgsordreregistrering.</span><span class="sxs-lookup"><span data-stu-id="905ef-131">The user is then returned to the sales order entry page.</span></span> <span data-ttu-id="905ef-132">Hvis det ikke kreves flere handlinger på salgsordren, kan du lukke siden salgsordreregistrering.</span><span class="sxs-lookup"><span data-stu-id="905ef-132">If no further actions are required on the sales order, the user can close the sales order entry page.</span></span>

<span data-ttu-id="905ef-133">Hvis **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanal, må ikke betalingen brukes på en ordre som er satt på vent.</span><span class="sxs-lookup"><span data-stu-id="905ef-133">If the **Enable order completion** flag is turned on in the call center channel, payment doesn't have to applied to an order that is put on hold.</span></span> <span data-ttu-id="905ef-134">Men for en salgsordre som ikke er satt på vent, kan ikke brukere forlate siden salgsordreregistrering før betalingen er brukt.</span><span class="sxs-lookup"><span data-stu-id="905ef-134">By contrast, for a sales order that isn't put on hold, users can't leave the sales order entry page until payment is applied.</span></span> <span data-ttu-id="905ef-135">Betalingen vil selvfølgelig være nødvendig før ordrensperren frigis.</span><span class="sxs-lookup"><span data-stu-id="905ef-135">Of course, payment will be required before the order hold is released.</span></span>

<span data-ttu-id="905ef-136">I tillegg kan telefonsenterbrukere legge en manuell svindelsperre på ordrer som er mistenkelige av en eller annen grunn.</span><span class="sxs-lookup"><span data-stu-id="905ef-136">Additionally, call center users can put a manual fraud hold on orders that are suspicious for some reason.</span></span> <span data-ttu-id="905ef-137">Ordrer kan også plasseres på vent automatisk når de oppfyller aktive vilkår og regler for svindel.</span><span class="sxs-lookup"><span data-stu-id="905ef-137">Orders can also be put on hold automatically when they match active fraud criteria and rules.</span></span> <span data-ttu-id="905ef-138">Hvis du vil ha mer informasjon om denne typen ordresperre, se [Konfigurere svindelvarsler](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).</span><span class="sxs-lookup"><span data-stu-id="905ef-138">For more information on about this type of order hold, see [Set up fraud alerts](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).</span></span>

## <a name="viewing-and-managing-orders-that-are-on-hold"></a><span data-ttu-id="905ef-139">Vise og behandle ordrer på vent</span><span class="sxs-lookup"><span data-stu-id="905ef-139">Viewing and managing orders that are on hold</span></span>

### <a name="viewing-hold-information-for-a-single-sales-order"></a><span data-ttu-id="905ef-140">Vise venteinformasjon for én enkelt salgsordre</span><span class="sxs-lookup"><span data-stu-id="905ef-140">Viewing hold information for a single sales order</span></span>

<span data-ttu-id="905ef-141">På **Kundestøtte**-siden kan brukere visuelt identifisere ordrer som er på vent, fordi ordrelinjene er merket med en bestemt farge.</span><span class="sxs-lookup"><span data-stu-id="905ef-141">On the **Customer service** page, users can visually identify orders that are on hold, because the order lines are highlighted in a specific color.</span></span> <span data-ttu-id="905ef-142">Denne fargen er definert av **På vent-salgsordrestatus**-feltet på **Kundeparametere**-siden.</span><span class="sxs-lookup"><span data-stu-id="905ef-142">This color is defined by the **On Hold sales order status** field on the **Accounts receivable parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="905ef-143">Hvis linjen er valgt på siden, kan ikke uthevingsfargen vises.</span><span class="sxs-lookup"><span data-stu-id="905ef-143">If the line is selected on the page, the highlight color isn't visible.</span></span>

<span data-ttu-id="905ef-144">Brukere kan også vise detaljert statusinformasjon for en salgsordre for å finne ut om ordren er på vent.</span><span class="sxs-lookup"><span data-stu-id="905ef-144">Users can also view detailed status information for a sales order to learn whether the order is on hold.</span></span> <span data-ttu-id="905ef-145">Detaljert statusinformasjon kan nås fra siden **Alle salgsordrer** eller **Kundeservice**.</span><span class="sxs-lookup"><span data-stu-id="905ef-145">The detailed status information can be accessed from the **All sales orders** or **Customer service** page.</span></span> <span data-ttu-id="905ef-146">Hvis en ordre er på vent, er **Behandler ikke**-flagget angitt for den, og **Detaljert status**-feltet viser statusen **På vent** eller **Svindelsperre**, avhengig av scenariet.</span><span class="sxs-lookup"><span data-stu-id="905ef-146">If an order is on hold, the **Do not process** flag is set for it, and the **Detailed status** field shows a status of either **On Hold** or **Fraud Hold**, depending on the scenario.</span></span>

<span data-ttu-id="905ef-147">Hvis du vil vise detaljene for en enkelt ordresperre, kan brukere åpne en detaljert visning av **Ordresperre**-siden fra **Kundestøtte**-siden ved hjelp av **Alternativer**-menyen for den valgte ordren.</span><span class="sxs-lookup"><span data-stu-id="905ef-147">To view the details of an individual order hold, users can open a detailed view of the **Order hold** page from the **Customer service** page, by using the **Options** menu for the selected order.</span></span> <span data-ttu-id="905ef-148">Brukere kan også få tilgang til denne visningen fra **Alle salgsordre**-siden ved å velge **Ordresperrer**-menyelementet på **Salgsordre**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="905ef-148">Users can also access this view from the **All sales order** page, by selecting the **Order holds** menu item on the **Sales order** tab.</span></span>

### <a name="viewing-all-orders-that-are-on-hold"></a><span data-ttu-id="905ef-149">Vise alle ordrer på vent</span><span class="sxs-lookup"><span data-stu-id="905ef-149">Viewing all orders that are on hold</span></span>

<span data-ttu-id="905ef-150">Hvis du vil vise alle ordrer som har blitt satt på manuell eller automatisk vent, kan du gå til **Retail og Commerce** \> **Kunder** \> **Ordresperrer**.</span><span class="sxs-lookup"><span data-stu-id="905ef-150">To view all orders that have been put on manual or automatic hold, go to **Retail and Commerce** \> **Customers** \> **Order holds**.</span></span>

<span data-ttu-id="905ef-151">**Ordresperrer**-arbeidsområdet viser en listevisning over alle ordrer som er på vent på grunn av manuelle eller svindelrelaterte sperrehandlinger.</span><span class="sxs-lookup"><span data-stu-id="905ef-151">The **Order holds** workbench provides a list view of all orders that are on hold because of manual or fraud-related hold actions.</span></span> <span data-ttu-id="905ef-152">Ved hjelp av standard filtrerings- og sorteringsalternativer på siden kan brukere opprette visninger som gjør at de kan jobbe med eller administrere bestemte sperrekoder som de er ansvarlige for å gå gjennom.</span><span class="sxs-lookup"><span data-stu-id="905ef-152">By taking advantage of the standard filtering and sorting options on the page, users can create views that let them work with or manage specific hold codes that they are responsible for reviewing.</span></span> <span data-ttu-id="905ef-153">**Ordresperrer**-arbeidsområdet angir også antall dager en ordren har vært på vent.</span><span class="sxs-lookup"><span data-stu-id="905ef-153">The **Order holds** workbench also indicates the number of days that an order has been on hold.</span></span> <span data-ttu-id="905ef-154">Denne informasjonen kan hjelpe brukere med å prioritere køen.</span><span class="sxs-lookup"><span data-stu-id="905ef-154">This information can help users prioritize the queue.</span></span>

<span data-ttu-id="905ef-155">Brukere kan klikke **Ordresperre** på menyen for å få en mer detaljert visning over ordrene som er satt på vent.</span><span class="sxs-lookup"><span data-stu-id="905ef-155">To get a more detailed view of the orders that are on hold, users can click the **Order hold** option on the menu.</span></span> <span data-ttu-id="905ef-156">Denne visningen gir informasjon om kunden, alle merknader som er brukt på ordren, kunden eller sperrehandlingen.</span><span class="sxs-lookup"><span data-stu-id="905ef-156">This view providing information about the customer, any notes that have been applied to the order, customer, or hold action.</span></span> <span data-ttu-id="905ef-157">Visningen inneholder også informasjon om årsaken til en automatisk sperre, hvis bestillingen ble satt på vent fordi den samsvarer med en regel for svindel.</span><span class="sxs-lookup"><span data-stu-id="905ef-157">The view also provides details about the reason for an automatic hold, if the order was put on hold because it matched a fraud rule.</span></span>

<span data-ttu-id="905ef-158">Både fra listevisningen og den detaljerte visningen av **Ordresperrer**-siden kan brukere vise eller redigere bestillingsrelatert tilleggsinformasjon, for eksempel betalinger, totaler og notater.</span><span class="sxs-lookup"><span data-stu-id="905ef-158">From both the list view and the detailed view of the **Order holds** page, users can view or edit additional order-related information, such as payments, totals, and notes.</span></span>

<span data-ttu-id="905ef-159">Alternativene i **Sperre - utsjekking**-kategorien kan være nyttig hvis flere brukere i firmaet arbeider i sperrekøen samtidig.</span><span class="sxs-lookup"><span data-stu-id="905ef-159">The options on the **Hold checkout** tab might be useful if multiple users in your company work on the hold queue at the same time.</span></span> <span data-ttu-id="905ef-160">Ved å velge **Sjekk ut**-alternativet kan brukere angi at de arbeider for å gå gjennom og undersøke ordresperren.</span><span class="sxs-lookup"><span data-stu-id="905ef-160">By selecting the **Check out** option, users can indicate that they are working to review and investigate the order hold.</span></span> <span data-ttu-id="905ef-161">På denne måten kan ikke andre brukere kaste bort tid ved å prøve å gjøre den samme jobben.</span><span class="sxs-lookup"><span data-stu-id="905ef-161">In this way, other users don't waste time by trying to do the same work.</span></span> <span data-ttu-id="905ef-162">Fra detaljert visning av **Ordresperrer**-siden kan brukere vise informasjon om datoen og klokkeslettet for utsjekkingen og brukeren som sjekket ut sperreposten.</span><span class="sxs-lookup"><span data-stu-id="905ef-162">From the detailed view of the **Order holds** page, users can view information about the checkout date and time, and the user who checked out the hold record.</span></span>

<span data-ttu-id="905ef-163">Når en sperrepost er sjekket ut, kan bare brukeren som sjekket den ut, fjerne utsjekkingen.</span><span class="sxs-lookup"><span data-stu-id="905ef-163">After a hold record is checked out, only the user who checked it out can clear the checkout.</span></span> <span data-ttu-id="905ef-164">Denne begrensningen skal hindre at brukere tar poster som andre brukere allerede arbeider på.</span><span class="sxs-lookup"><span data-stu-id="905ef-164">This restriction is intended to prevent users from taking records that other users are already working on.</span></span> <span data-ttu-id="905ef-165">For å frigi en ordre tilbake til køen slik at andre brukere kan arbeide med den, må brukeren som sjekket ut posten, velge **Fjern utsjekking** alternativet.</span><span class="sxs-lookup"><span data-stu-id="905ef-165">To release an order back to the queue so that other users can work on it, the user who checked out the record selects the **Clear checkout** option.</span></span>

> [!NOTE]
> <span data-ttu-id="905ef-166">Sperren er ikke frigitt når utsjekkingen er fjernet.</span><span class="sxs-lookup"><span data-stu-id="905ef-166">The hold isn't released when the checkout is cleared.</span></span>

<span data-ttu-id="905ef-167">I noen tilfeller, for eksempel når en bruker er syk eller har sluttet i firmaet, kan det hende at poster som er sjekket ut til denne brukeren, må tilordnes til en annen bruker på nytt.</span><span class="sxs-lookup"><span data-stu-id="905ef-167">In some situations, such as when a user is out sick or has left the company, records that are checked out to that user might have to be reassigned to another user.</span></span> <span data-ttu-id="905ef-168">En leder kan tilordne poster på nytt ved hjelp av **Overstyr utsjekking**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="905ef-168">A manager can reassign records by using the **Override checkout** option.</span></span>

## <a name="releasing-orders-that-are-on-hold"></a><span data-ttu-id="905ef-169">Frigi ordrer på vent</span><span class="sxs-lookup"><span data-stu-id="905ef-169">Releasing orders that are on hold</span></span>

<span data-ttu-id="905ef-170">I både liste- og detaljert visning av **Ordresperrer**-siden inneholder **Fjern sperre**-kategorien alternativene som brukes til å frigi en ordresperre.</span><span class="sxs-lookup"><span data-stu-id="905ef-170">In both the list view and the detailed view of the **Order holds** page, the **Clear hold** tab contains the options that are used to release an order hold.</span></span> <span data-ttu-id="905ef-171">Bruk **Fjern sperrer**-alternativet til å frigi en bestilling fra den valgte sperrekoden.</span><span class="sxs-lookup"><span data-stu-id="905ef-171">Use the **Clear holds** option to release an order from the selected hold code.</span></span>

<span data-ttu-id="905ef-172">Telefonsenterordrer krever betaling.</span><span class="sxs-lookup"><span data-stu-id="905ef-172">Call center orders require payment.</span></span> <span data-ttu-id="905ef-173">Derfor kan en sperre ikke fullstendig fjernes hvis betalingen ikke er brukt på ordren.</span><span class="sxs-lookup"><span data-stu-id="905ef-173">Therefore, a hold can't be fully cleared if payment hasn't been applied to the order.</span></span> <span data-ttu-id="905ef-174">På **Telefonsenterparametere**-siden, i **Sperrer**-kategorien, må du kontrollere at **Send når fjernet**-parameteren er aktivert.</span><span class="sxs-lookup"><span data-stu-id="905ef-174">On the **Call center parameters** page, on the **Holds** tab, make sure that the **Submit when cleared** parameter is turned on.</span></span> <span data-ttu-id="905ef-175">Denne innstillingen garanterer at en fjernet sperreordre gjennomgår riktig ordreoverføringlogikk for å validere og godkjenne betalinger.</span><span class="sxs-lookup"><span data-stu-id="905ef-175">This setting helps guarantee that a cleared hold order goes through the correct order submission logic to validate and authorize payments.</span></span> <span data-ttu-id="905ef-176">Hvis betalinger mangler, får brukeren en feilmelding, og sperrekoden fjernes ikke.</span><span class="sxs-lookup"><span data-stu-id="905ef-176">If payments are missing, the user receives an error, and the hold code isn't cleared.</span></span>

<span data-ttu-id="905ef-177">Hvis **Send når fjernet**-parameteren ikke er angitt, må brukere velge **Fjern og send**-alternativet på **Fjern sperre**-menyen for å garantere at ordren går gjennom alle nødvendige betalingsvalideringer.</span><span class="sxs-lookup"><span data-stu-id="905ef-177">If the **Submit when cleared** parameter hasn't been set, users should select the **Clear and submit** option on the **Clear hold** menu to help guarantee that the order goes through all the required payment validations.</span></span> <span data-ttu-id="905ef-178">Hvis bestillingen mislykkes når **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanalen, frigis ordren fra sperrestatusen, men **Ikke behandle**-flagget beholdes.</span><span class="sxs-lookup"><span data-stu-id="905ef-178">If order submission fails when the **Enable order completion** flag is turned on in the call center channel, the order is released from its hold status, but the **Do not process** flag remains set.</span></span> <span data-ttu-id="905ef-179">Ordren er derfor ikke frigitt til lageret før riktige betalinger er brukt og godkjent.</span><span class="sxs-lookup"><span data-stu-id="905ef-179">Therefore, the order isn't released to the warehouse until correct payments have been applied and validated.</span></span>

<span data-ttu-id="905ef-180">Hvis brukerne vil fjerne en sperring, men gjør flere endringer i bestillingen før den frigis for videre behandling, kan de velge **Fjern og endre**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="905ef-180">If users want to clear a hold but make additional changes to the order before it's released for further processing, they can select the **Clear and modify** option.</span></span> <span data-ttu-id="905ef-181">Dette alternativet fjerner sperrekoden og åpner salgsordredetaljer, slik at brukere kan gjøre flere endringer i ordren.</span><span class="sxs-lookup"><span data-stu-id="905ef-181">This option removes the hold code and opens the sales order details so that users can make additional changes to the order.</span></span> <span data-ttu-id="905ef-182">Brukere kan også bruke betaling og sende salgsordren til betalingensvalideringlogikken når **Aktiver ordrefullføring**-flagget er aktivert i telefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="905ef-182">Users can also apply payment and submit the sales order through payment validation logic when the **Enable order completion** flag is turned on in the call center channel.</span></span>

## <a name="reporting-options"></a><span data-ttu-id="905ef-183">Rapporteringsalternativer</span><span class="sxs-lookup"><span data-stu-id="905ef-183">Reporting options</span></span>

<span data-ttu-id="905ef-184">Gå til **Retail og Commerce** \> **Forespørsler og rapporter** \> **Telefonsenterrapporter** \> **Rapport for ordresperre** for å kjøre en rapport om ordresperrer etter datointervall, sperrekode eller andre relaterte kriterier.</span><span class="sxs-lookup"><span data-stu-id="905ef-184">Go to **Retail and Commerce** \> **Inquiries and reports** \> **Call center reports** \> **Order holds report** to run a report about order holds by date range, hold code, or other related criteria.</span></span>