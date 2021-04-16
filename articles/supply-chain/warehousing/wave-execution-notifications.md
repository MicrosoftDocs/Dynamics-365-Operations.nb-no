---
title: Varslinger for bølgekjøring
description: Dette emnet beskriver varslinger under bølgekjøring og forklarer hvordan du konfigurerer dem.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 0a61aff10234f40f14d603852be30fec3ba83647
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838088"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="ef938-103">Varslinger for bølgekjøring</span><span class="sxs-lookup"><span data-stu-id="ef938-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ef938-104">Funksjonen *Varslinger for bølgekjøring* bruker forretningshendelser og handlingssenteret til å levere varslinger som er knyttet til bølgekjøring.</span><span class="sxs-lookup"><span data-stu-id="ef938-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="ef938-105">Det lar deg angi hendelsestypene som genererer meldinger, lagrene som genererer dem og brukerne som mottar dem.</span><span class="sxs-lookup"><span data-stu-id="ef938-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="ef938-106">Knappen **Vis meldinger** (klokkesymbolet) til høyre på navigasjonslinjen viser når en handlingssentermelding er tilgjengelig for den gjeldende brukeren.</span><span class="sxs-lookup"><span data-stu-id="ef938-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="ef938-107">Brukeren kan velge **Vis meldinger**-knappen for å åpne handlingssenteret og se gjennom meldingene.</span><span class="sxs-lookup"><span data-stu-id="ef938-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="ef938-108">Forretningshendelser forekommer når forretningsprosesser kjøres.</span><span class="sxs-lookup"><span data-stu-id="ef938-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="ef938-109">Forretningsprosesser består av oppgaver.</span><span class="sxs-lookup"><span data-stu-id="ef938-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="ef938-110">Under en forretningsprosess utfører brukerne som deltar i den, forretningshandlinger for å fullføre disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="ef938-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="ef938-111">Forretningshendelser inneholder en mekanisme som gjør at eksterne systemer kan motta varslinger fra Finance and Operations-programmer.</span><span class="sxs-lookup"><span data-stu-id="ef938-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="ef938-112">På denne måten kan systemene utføre forretningshandlinger som svar på forretningshendelsene.</span><span class="sxs-lookup"><span data-stu-id="ef938-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="ef938-113">Hvis du vil ha mer informasjon, kan du se [Oversikt over forretningshendelser](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="ef938-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="ef938-114">Aktiver funksjonen Varslinger for bølgekjøring</span><span class="sxs-lookup"><span data-stu-id="ef938-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="ef938-115">Før du kan bruke funksjonen *Varslinger for bølgekjøring*, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="ef938-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ef938-116">Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="ef938-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ef938-117">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="ef938-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ef938-118">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="ef938-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ef938-119">**Funksjonsnavn:** *Varslinger for bølgekjøring*</span><span class="sxs-lookup"><span data-stu-id="ef938-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="ef938-120">Scenario: Send varslinger om satsvis bølgekjøring til handlingssenteret</span><span class="sxs-lookup"><span data-stu-id="ef938-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="ef938-121">Dette scenariet viser slutt-til-slutt-flyten for sending av meldinger om utførelsesfeil for bølgebunke til en bestemt rolle via handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="ef938-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ef938-122">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="ef938-122">Make demo data available</span></span>

<span data-ttu-id="ef938-123">For å følge dette scenarioet må du ha demonstrasjonsdata installert, og du må velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ef938-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="ef938-124">Kontroller at bølger kjøres i satsvis modus</span><span class="sxs-lookup"><span data-stu-id="ef938-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="ef938-125">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="ef938-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="ef938-126">På hurtigfanen **Bølgebehandling** setter du alternativet **Behandle bølger satsvis** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ef938-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="ef938-127">Hvis du vil deaktivere varslinger for satsvis bølgekjøring, setter du alternativet **Deaktiver varslinger om satsvis bølgebehandling** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="ef938-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="ef938-128">Konfigurer en bølgevarslingspolicy</span><span class="sxs-lookup"><span data-stu-id="ef938-128">Configure a wave notification policy</span></span>

<span data-ttu-id="ef938-129">Policyer for bølgevarsling definerer varslingstypene som sendes og brukerne som blir varslet.</span><span class="sxs-lookup"><span data-stu-id="ef938-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="ef938-130">Gå til **Lagerstyring \> Oppsett \> Bølger \> Policyer for bølgevarsling**.</span><span class="sxs-lookup"><span data-stu-id="ef938-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="ef938-131">Opprett en post som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="ef938-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="ef938-132">**Policy for bølgevarsling:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="ef938-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="ef938-133">**Beskrivelse:** *Lager 24-bølgebunkefeil*</span><span class="sxs-lookup"><span data-stu-id="ef938-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="ef938-134">**Send melding ved:** *Bare feil*</span><span class="sxs-lookup"><span data-stu-id="ef938-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="ef938-135">**Til rolle:** *Systemansvarling*</span><span class="sxs-lookup"><span data-stu-id="ef938-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="ef938-136">Fordi dette scenariet bruker demodata, velges *Systemadministrator*-rollen av hensyn til forenkling.</span><span class="sxs-lookup"><span data-stu-id="ef938-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="ef938-137">Derfor vil du motta meldingene fordi du er logget på som en systemadministratorbruker.</span><span class="sxs-lookup"><span data-stu-id="ef938-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="ef938-138">I praksis bør du imidlertid vanligvis velge en mer spesifikk rolle for å varsle om feil under utføring av bølgeparti, for eksempel *Lagersjef*.</span><span class="sxs-lookup"><span data-stu-id="ef938-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="ef938-139">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef938-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="ef938-140">Konfigurere en bølgemal</span><span class="sxs-lookup"><span data-stu-id="ef938-140">Configure a wave template</span></span>

<span data-ttu-id="ef938-141">Med bølgemaler kan du koble bestemte forekomster av bølgemetoder til tilsvarende bølgeetikettmaler.</span><span class="sxs-lookup"><span data-stu-id="ef938-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="ef938-142">Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.</span><span class="sxs-lookup"><span data-stu-id="ef938-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ef938-143">I listeruten setter du feltet **Bølgemaltype** til *Forsendelse*, og deretter velger du bølgemalen *24 Standardforsendelse* for lager 24.</span><span class="sxs-lookup"><span data-stu-id="ef938-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="ef938-144">I hurtigfanen **Generelt** angir du feltet **Policy for bølgevarsling**-feltet til *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="ef938-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="ef938-145">Konfigurere en arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="ef938-145">Configure a work template</span></span>

<span data-ttu-id="ef938-146">Arbeidsmaler brukes under bølgekjøring for å generere arbeid.</span><span class="sxs-lookup"><span data-stu-id="ef938-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="ef938-147">I dette scenariet skal bølgekjøring utløse en feil.</span><span class="sxs-lookup"><span data-stu-id="ef938-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="ef938-148">Hvis du angir at arbeidsmalspørringen skal bruke et lager som ikke finnes, vil du sikre at bølgeutførelsen mislykkes og derfor sender et varsel.</span><span class="sxs-lookup"><span data-stu-id="ef938-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="ef938-149">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.</span><span class="sxs-lookup"><span data-stu-id="ef938-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ef938-150">I listeruten setter du feltet **Arbeidsmaltype** til *Salgsordrer*, og deretter velger du arbeidsmalen *24 SO stadium* for lager 24.</span><span class="sxs-lookup"><span data-stu-id="ef938-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="ef938-151">I handlingsruten velger du **Rediger spørring**.</span><span class="sxs-lookup"><span data-stu-id="ef938-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ef938-152">I dialogboksen i redigeringsprogrammet for spørringen, på fanen **Område**, redigerer du følgende rad (eller legger den til hvis den ikke finnes):</span><span class="sxs-lookup"><span data-stu-id="ef938-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="ef938-153">**Tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="ef938-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="ef938-154">**Avledet tabell:** *Midlertidige arbeidstransaksjoner*</span><span class="sxs-lookup"><span data-stu-id="ef938-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="ef938-155">**Felt:** *Lager*</span><span class="sxs-lookup"><span data-stu-id="ef938-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="ef938-156">**Kriterier:** Endre verdien fra *24* til *Feil*.</span><span class="sxs-lookup"><span data-stu-id="ef938-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="ef938-157">Velg **OK**, og bekreft endringen.</span><span class="sxs-lookup"><span data-stu-id="ef938-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="ef938-158">Opprette en salgsordre og frigi den til lageret</span><span class="sxs-lookup"><span data-stu-id="ef938-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="ef938-159">Gå til **Salg og markedsføring \> Salgsordre \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="ef938-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="ef938-160">Opprett en salgsordre med følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="ef938-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="ef938-161">**Kundekonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ef938-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ef938-162">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="ef938-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="ef938-163">I hurtigfanen **Salgsordrelinjer** legger du til en salgsordrelinje som har følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="ef938-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="ef938-164">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ef938-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ef938-165">**Antall:** *10*</span><span class="sxs-lookup"><span data-stu-id="ef938-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef938-166">Disse varene og antallene er bare eksempler.</span><span class="sxs-lookup"><span data-stu-id="ef938-166">These items and quantities are only examples.</span></span> <span data-ttu-id="ef938-167">Det angitte lageret må ha nok varer på lager.</span><span class="sxs-lookup"><span data-stu-id="ef938-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="ef938-168">Mens den nye ordrelinjen fremdeles er valgt på hurtigfanen **Salgsordrelinjer**, velger du **Beholdning \> Reservasjon** på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="ef938-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="ef938-169">På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**.</span><span class="sxs-lookup"><span data-stu-id="ef938-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="ef938-170">Lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="ef938-170">Then close the page.</span></span>
1. <span data-ttu-id="ef938-171">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ef938-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="ef938-172">Varslinger fra utføring av satsvis bølgjobb</span><span class="sxs-lookup"><span data-stu-id="ef938-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="ef938-173">Avhengig av oppsettet av forretningshendelsene vil du til slutt få et varsel om mislykket bølgeutførelse.</span><span class="sxs-lookup"><span data-stu-id="ef938-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="ef938-174">Handlingssentermeldingen vil ligne på følgende eksempel, og vil inneholde en kobling til bølgen som mislyktes.</span><span class="sxs-lookup"><span data-stu-id="ef938-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="ef938-175">**Feil under bølgekjøring**</span><span class="sxs-lookup"><span data-stu-id="ef938-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="ef938-176">Det oppstod en feil under utføring av bølgen USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="ef938-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="ef938-177">Siste meldinger: Intet arbeid ble opprettet for bølgen USMF-000000001.</span><span class="sxs-lookup"><span data-stu-id="ef938-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="ef938-178">**STATUS**</span><span class="sxs-lookup"><span data-stu-id="ef938-178">**STATUS**</span></span>  
> <span data-ttu-id="ef938-179">Aktivt</span><span class="sxs-lookup"><span data-stu-id="ef938-179">Active</span></span>
>
> <span data-ttu-id="ef938-180">Åpne bølgedetaljer</span><span class="sxs-lookup"><span data-stu-id="ef938-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
