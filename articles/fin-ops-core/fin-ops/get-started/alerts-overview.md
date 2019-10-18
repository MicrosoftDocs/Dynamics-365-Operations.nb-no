---
title: Oversikt over varsler
description: Dette emnet gir generell informasjon om varsler. Du kan bruke varsler til å holde deg informert om hendelser som du vil spore i løpet av arbeidsdagen.
author: tjvass
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a42e836c0b72798de3375c169e45b121debd55ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191276"
---
# <a name="alerts-overview"></a><span data-ttu-id="89376-104">Oversikt over varsler</span><span class="sxs-lookup"><span data-stu-id="89376-104">Alerts overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a><span data-ttu-id="89376-105">Varsler</span><span class="sxs-lookup"><span data-stu-id="89376-105">About alerts</span></span>
<span data-ttu-id="89376-106">Varsler utgjør et meldingssystem for kritiske hendelser i systemet.</span><span class="sxs-lookup"><span data-stu-id="89376-106">Alerts form a notification system for critical events in the system.</span></span> <span data-ttu-id="89376-107">Du kan bruke varsler til å holde deg informert om hendelser som du vil spore i løpet av arbeidsdagen.</span><span class="sxs-lookup"><span data-stu-id="89376-107">You can use alerts to stay informed about events that you want to track during the workday.</span></span> <span data-ttu-id="89376-108">Du kan enkelt opprette ditt eget sett med varsler slik at du blir varslet om leveringer som er forfalt, ordrer som er slettet, priser som endres eller hendelser du må reagere på.</span><span class="sxs-lookup"><span data-stu-id="89376-108">You can easily create your own set of alert rules so that you're alerted about deliveries that are overdue, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="89376-109">Det finnes flere vanlige scenarier hvor varslingsfunksjonen i Finance and Operations kan brukes.</span><span class="sxs-lookup"><span data-stu-id="89376-109">In enterprise resource planning (ERP), there are several typical scenarios where the alerts feature can be used.</span></span> <span data-ttu-id="89376-110">Her er noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="89376-110">Here are some examples.</span></span>

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a><span data-ttu-id="89376-111">Scenario 1: Opprett en varslingsregel for nye salgsordrer</span><span class="sxs-lookup"><span data-stu-id="89376-111">Scenario 1: Create an alert rule for new sales orders</span></span>

1. <span data-ttu-id="89376-112">Åpne siden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="89376-112">Open the **All sales orders** page.</span></span>
2. <span data-ttu-id="89376-113">Velg **Opprett et egendefinert varsel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89376-113">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
3. <span data-ttu-id="89376-114">Velg **Post er opprettet** i feltet **Hendelse** i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**.</span><span class="sxs-lookup"><span data-stu-id="89376-114">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Event** field, select **Record has been created**.</span></span>

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a><span data-ttu-id="89376-115">Scenario 2: Opprett en varslingsregel for utsettelse av en leveringsdato</span><span class="sxs-lookup"><span data-stu-id="89376-115">Scenario 2: Create an alert rule for postponement of a delivery date</span></span>

1. <span data-ttu-id="89376-116">Åpne siden **Alle kjøpsordrer**.</span><span class="sxs-lookup"><span data-stu-id="89376-116">Open the **All purchase orders** page.</span></span>
2. <span data-ttu-id="89376-117">Velg en bestillings-ID for å få tilgang til bestillingsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="89376-117">Select a purchase order ID to access the purchase order details.</span></span>
3. <span data-ttu-id="89376-118">Utvid hurtigfanen **Bestillingshode**.</span><span class="sxs-lookup"><span data-stu-id="89376-118">Expand the **Purchase order header** FastTab.</span></span>
4. <span data-ttu-id="89376-119">Velg **Opprett et egendefinert varsel** i gruppen **Del** i fanen **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89376-119">On the Action Pane, on the **Options** tab, in the **Share** group, select **Create a custom alert**.</span></span>
5. <span data-ttu-id="89376-120">Velg **Leveringsdato** i feltet **Felt** i hurtigfanen **Varsle meg når** i dialogboksen **Opprett varslingsregel**.</span><span class="sxs-lookup"><span data-stu-id="89376-120">In the **Create alert rule** dialog box, on the **Alert me when** FastTab, in the **Field** field, select **Delivery date**.</span></span>
6. <span data-ttu-id="89376-121">Velg **er utsatt** i feltet **Hendelse**.</span><span class="sxs-lookup"><span data-stu-id="89376-121">In the **Event** field, select **has been postponed**.</span></span>
    
<span data-ttu-id="89376-122">Når du lukker dialogboksen **Opprett varslingsregel**, vises regelen på siden **Administrer varselregler**.</span><span class="sxs-lookup"><span data-stu-id="89376-122">After you close the **Create alert rule** dialog box, your rule appears on the **Manage alert rules** page.</span></span> <span data-ttu-id="89376-123">Du kan bruke siden **Administrer varselregler** til å oppdatere dine eksisterende varselregler.</span><span class="sxs-lookup"><span data-stu-id="89376-123">You can use the **Manage alert rules** page to update your existing alert rules.</span></span> <span data-ttu-id="89376-124">Du kan for eksempel endre hendelsestriggerne, oppdatere varslinger om systemhendelser, og oppdatere utløpsdatoer.</span><span class="sxs-lookup"><span data-stu-id="89376-124">For example, you can modify event triggers, update event notifications, and update expiration dates.</span></span> <span data-ttu-id="89376-125">Bruk knappen **Varsle meg** i fanen **Alternativer** i handlingsruten for å åpne siden **Administrer varselregler**.</span><span class="sxs-lookup"><span data-stu-id="89376-125">To open the **Manage alert rules** page, use the **Alert me** button on the **Options** tab of the Action Pane.</span></span>

## <a name="what-occurs-when-an-alert-rule-is-created"></a><span data-ttu-id="89376-126">Hva skjer når en varslingsregel opprettes?</span><span class="sxs-lookup"><span data-stu-id="89376-126">What occurs when an alert rule is created?</span></span>

<span data-ttu-id="89376-127">Når du oppretter varselregler, kan du knytte en forhåndsdefinert hendelse til et bestemt felt.</span><span class="sxs-lookup"><span data-stu-id="89376-127">When you create alert rules, you can associate a predefined event with a specific field.</span></span> <span data-ttu-id="89376-128">Datoen som er angitt i feltet, kommer, eller innholdet i feltet endres.</span><span class="sxs-lookup"><span data-stu-id="89376-128">For example, the date that is specified in the field arrives, or the contents of the field change.</span></span> <span data-ttu-id="89376-129">Du kan også knytte en hendelse til postene på en bestemt side.</span><span class="sxs-lookup"><span data-stu-id="89376-129">Alternatively, you can associate an event with the records on a specific page.</span></span> <span data-ttu-id="89376-130">En post opprettes for eksempel eller slettes.</span><span class="sxs-lookup"><span data-stu-id="89376-130">For example, a record is created, or a record is deleted.</span></span>

<span data-ttu-id="89376-131">Når den valgte hendelsen skjer for feltet eller for en post på siden, sendes det et varsel til deg.</span><span class="sxs-lookup"><span data-stu-id="89376-131">When the selected event occurs for the field or for a record on the page, an alert is sent to you.</span></span> <span data-ttu-id="89376-132">Du oppretter for eksempel en regel der du knytter feltet **Leveringsdato** til en bestemt bestillingslinje med hendelsen **tid siden forfall**.</span><span class="sxs-lookup"><span data-stu-id="89376-132">For example, you create a rule where you associate the **Delivery date** field on a specific purchase order line with the **was due this amount of time ago** event.</span></span> <span data-ttu-id="89376-133">Du setter tidsrammen til fem dager.</span><span class="sxs-lookup"><span data-stu-id="89376-133">You set the time frame to five days.</span></span> <span data-ttu-id="89376-134">I dette tilfellet sendes det et varsel fem dager etter leveringsdatoen for bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="89376-134">In this case, an alert is sent five days after the delivery date of that purchase order line.</span></span>

<span data-ttu-id="89376-135">Du kan også forbedre varselreglene ved å angi betingelser.</span><span class="sxs-lookup"><span data-stu-id="89376-135">Additionally, you can refine alert rules by setting conditions.</span></span> <span data-ttu-id="89376-136">Du kan for eksempel bli varslet om nye bestillinger som opprettes for bestemte leverandørkontoer.</span><span class="sxs-lookup"><span data-stu-id="89376-136">For example, you can be alerted about new purchase orders that are created for specific vendor accounts.</span></span>

## <a name="preparing-for-an-alert"></a><span data-ttu-id="89376-137">Klargjør for et varsel</span><span class="sxs-lookup"><span data-stu-id="89376-137">Preparing for an alert</span></span>

<span data-ttu-id="89376-138">Før du oppretter en varslingsregel, må du vurdere når eller i hvilke situasjoner du vil motta varsler.</span><span class="sxs-lookup"><span data-stu-id="89376-138">Before you set up an alert rule, decide when or in what situations you want to receive alerts.</span></span> <span data-ttu-id="89376-139">Når du vet hvilke hendelser du vil varsles om, kan du finne siden der dataene som forårsaker den hendelsen, vises.</span><span class="sxs-lookup"><span data-stu-id="89376-139">When you know which event you want to be notified about, find the page where the data that causes that event appears.</span></span> <span data-ttu-id="89376-140">Hendelsen kan være en dato som kommer, eller en bestemt endring som forekommer.</span><span class="sxs-lookup"><span data-stu-id="89376-140">The event can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="89376-141">Du må derfor finne siden der datoen er angitt, eller hvor feltet som endres eller den nye posten som opprettes, vises.</span><span class="sxs-lookup"><span data-stu-id="89376-141">Therefore, you must find the page where the date is specified, or where the field that changes or the new record that is created appears.</span></span> <span data-ttu-id="89376-142">Etter at du har denne informasjonen, kan du opprette varslingsregelen.</span><span class="sxs-lookup"><span data-stu-id="89376-142">After you have this information, you can create the alert rule.</span></span>

## <a name="components-of-an-alert-rule"></a><span data-ttu-id="89376-143">Komponentene i en varslingsregel</span><span class="sxs-lookup"><span data-stu-id="89376-143">Components of an alert rule</span></span>

<span data-ttu-id="89376-144">En varslingsregel har fem komponenter:</span><span class="sxs-lookup"><span data-stu-id="89376-144">An alert rule has five components:</span></span>

- <span data-ttu-id="89376-145">**Hendelse** – Hendelsen som utløser en varslingsregel kan være en dato som kommer, eller en bestemt endring som forekommer.</span><span class="sxs-lookup"><span data-stu-id="89376-145">**Event** – The event that triggers an alert rule can be a date that arrives or a specific change that occurs.</span></span> <span data-ttu-id="89376-146">Du definerer hendelser i hurtigfanen **Send e-postvarsel når jobbstatus endres** i dialogboksen **Opprett varslingsregel**.</span><span class="sxs-lookup"><span data-stu-id="89376-146">You define events on the **Send email alerts for job status changes** FastTab of the **Create alert rule** dialog box.</span></span>
- <span data-ttu-id="89376-147">**Betingelse** – I hurtigfanen **Varsle meg for** i dialogboksen **Opprett varslingsregel** kan du velge omfanget for betingelsen for å kontrollere når du varsles om hendelser.</span><span class="sxs-lookup"><span data-stu-id="89376-147">**Condition** – On the **Alert me for** FastTab of the **Create alert rule** dialog box, you can select the scope of the condition, to control when you're alerted about events.</span></span> <span data-ttu-id="89376-148">Du kan bruke regelen bare for gjeldende post eller for alle synlige poster på siden.</span><span class="sxs-lookup"><span data-stu-id="89376-148">You can apply the rule either to the current record only or to all visible records on the page.</span></span> <span data-ttu-id="89376-149">Hvis regelen gjelder på tvers av juridiske enheter, kan du sette alternativet **Organisasjonsomfattende** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="89376-149">If the rule applies across legal entities, you can set the **Organization-wide** option to **Yes**.</span></span>
- <span data-ttu-id="89376-150">**Utløp av regel** – I hurtigfanen **Varsle meg inntil** i dialogboksen **Opprett varslingsregel** kan du angi hvor lenge varslingsregelen skal være aktiv.</span><span class="sxs-lookup"><span data-stu-id="89376-150">**Expiry of rule** – On the **Alert me until** FastTab of the **Create alert rule** dialog box, you can specify how long the alert rule should be active.</span></span>
- <span data-ttu-id="89376-151">**Innhold** – I hurtigfanen **Varsle meg med** i dialogboksen **Opprett varslingsregel** kan du angi emneteksten og meldingsteksten som varslingsmeldingene skal bruke.</span><span class="sxs-lookup"><span data-stu-id="89376-151">**Contents** – On the **Alert me with** FastTab of the **Create alert rule** dialog box, you can specify the subject text and message text that the alert messages should use.</span></span>
- <span data-ttu-id="89376-152">**Bruker** – I hurtigfanen **Hvem skal varsles** i dialogboksen **Opprett varslingsregel** kan du angi hvilken bruker som skal motta varslene.</span><span class="sxs-lookup"><span data-stu-id="89376-152">**User** – On the **Alert who** FastTab of the **Create alert rule** dialog box, you can specify which user should receive the alert messages.</span></span> <span data-ttu-id="89376-153">Bruker-IDen er valgt som standard.</span><span class="sxs-lookup"><span data-stu-id="89376-153">By default, your user ID is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="89376-154">Dette alternativet er begrenset til administratorer for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="89376-154">This option is restricted to organization administrators.</span></span>

## <a name="email-notifications-from-alerts"></a><span data-ttu-id="89376-155">E-postmeldinger fra varsler</span><span class="sxs-lookup"><span data-stu-id="89376-155">Email notifications from alerts</span></span>

<span data-ttu-id="89376-156">E-postmeldinger fra varsler er ikke aktivert ennå.</span><span class="sxs-lookup"><span data-stu-id="89376-156">Email notifications from alerts are not yet enabled.</span></span> <span data-ttu-id="89376-157">Dette vil bli aktivert i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="89376-157">This will be enabled in a future update.</span></span>

## <a name="videos"></a><span data-ttu-id="89376-158">Videoer</span><span class="sxs-lookup"><span data-stu-id="89376-158">Videos</span></span>

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a><span data-ttu-id="89376-159">Slik bruker du varsler til å overvåke filtrerte data</span><span class="sxs-lookup"><span data-stu-id="89376-159">How to use alerts to monitor filtered data</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3DWZ3]

<span data-ttu-id="89376-160">Videoen [Slik bruker du varsler til å overvåke filtrerte data](https://youtu.be/ZYKMcv6kl9s) (vises oven) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="89376-160">The [How to use alerts to monitor filtered data](https://youtu.be/ZYKMcv6kl9s) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

### <a name="alert-rule-options"></a><span data-ttu-id="89376-161">Alternativer for varslingsregel</span><span class="sxs-lookup"><span data-stu-id="89376-161">Alert rule options</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3E4PV]

<span data-ttu-id="89376-162">Videoen [Alternativer for varslingsregler](https://youtu.be/cpzimwOjicM) (vises over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="89376-162">The [Alert rule options](https://youtu.be/cpzimwOjicM) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


