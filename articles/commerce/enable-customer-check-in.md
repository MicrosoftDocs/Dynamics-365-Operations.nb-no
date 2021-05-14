---
title: Aktivere innsjekkingsmeldinger for kunde på salgsstedet
description: Dette emnet beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937606"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="52edc-103">Aktivere innsjekkingsmeldinger for kunde på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="52edc-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="52edc-104">Dette emnet beskriver hvordan du aktiverer innsjekkingsmeldinger for kunde på Microsoft Dynamics 365 Commerce-salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="52edc-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="52edc-105">I e-postene "Ordre klar for henting" kan organisasjoner gi en kobling eller knapp som kundene kan bruke til å varsle butikken om at de er på stedet og venter på at pakken deres skal sendes ut til dem.</span><span class="sxs-lookup"><span data-stu-id="52edc-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="52edc-106">Kundene mottar deretter en innsjekkingsbekreftelse, og butikken mottar et varsel som en oppgave i salgsstedsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="52edc-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="52edc-107">Denne oppgaven fungerer som en ledetekst for en salgsmedarbeider om å levere ordren til kundens kjøretøy.</span><span class="sxs-lookup"><span data-stu-id="52edc-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="52edc-108">Derfor behøver ikke kunden å gå inn i butikken.</span><span class="sxs-lookup"><span data-stu-id="52edc-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="52edc-109">Arbeidsflyten for kundens innsjekking kan også konfigureres til å samle inn tilleggsinformasjon fra kundene, for eksempel parkeringsplassnummeret til kunden, merke, modell og farge på kjøretøyet og leveringsinstruksjoner.</span><span class="sxs-lookup"><span data-stu-id="52edc-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="52edc-110">Deltakeren i detaljhandelen kan bruke denne informasjonen til å legge til rette for innfrielse av ordren.</span><span class="sxs-lookup"><span data-stu-id="52edc-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="52edc-111">Aktivere kundeinnsjekking</span><span class="sxs-lookup"><span data-stu-id="52edc-111">Enable customer check-in</span></span>

<span data-ttu-id="52edc-112">Når innsjekkingsfunksjonen for kunde er aktivert, genererer Commerce en ordrebekreftelses-ID (kalles også kanalreferanse-ID).</span><span class="sxs-lookup"><span data-stu-id="52edc-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="52edc-113">Det genererer også ordrebekreftelses-IDer for ordrer som opprettes via salgsstedet eller telefonsenterkanalene.</span><span class="sxs-lookup"><span data-stu-id="52edc-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="52edc-114">Følg disse trinnene for å slå på kundeinnsjekkingsfunksjonen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="52edc-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="52edc-115">Gå til **Arbeidsområder \> Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="52edc-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="52edc-116">Søk etter funksjonen **Generere et konsekvent kanalreferanse-ID-format på tvers av kanaler**.</span><span class="sxs-lookup"><span data-stu-id="52edc-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="52edc-117">Velg funksjonen, og velg deretter **Aktiver nå** i egenskapsruten.</span><span class="sxs-lookup"><span data-stu-id="52edc-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="52edc-118">Opprette en innsjekkingsbekreftelsesside</span><span class="sxs-lookup"><span data-stu-id="52edc-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="52edc-119">På e-handelområdet må du opprette en ny side som skal fungere som opplevelse for innsjekkingbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="52edc-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="52edc-120">Via tilleggskonfigurasjon kan siden også inkludere et skjema som samler inn tilleggsinformasjon fra kunder for å legge til rette for innfrielse av ordrene.</span><span class="sxs-lookup"><span data-stu-id="52edc-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="52edc-121">Hvis du vil ha mer informasjon om hvordan du setter opp siden og modulen, kan du se [Kundeinnsjekkingsmodul](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="52edc-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="52edc-122">Konfigurere den transaksjonsbaserte e-postmalen</span><span class="sxs-lookup"><span data-stu-id="52edc-122">Configure the transactional email template</span></span>

<span data-ttu-id="52edc-123">Du må legge til en **Jeg er her**-kobling eller -knapp i malen for den transaksjonsbaserte e-posten som kunder mottar når ordren er klar til plukking.</span><span class="sxs-lookup"><span data-stu-id="52edc-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="52edc-124">Kunder vil bruke denne koblingen eller knappen til å varsle butikken om at de er ankommet for å hente ordren.</span><span class="sxs-lookup"><span data-stu-id="52edc-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="52edc-125">Legg til koblingen eller knappen i malen som er tilordnet varslingstypen **Pakking fullført** og leveringsmåten du bruker til innfrielse av bestillinger utenfor butikk.</span><span class="sxs-lookup"><span data-stu-id="52edc-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="52edc-126">I malen oppretter du en HTML-kobling eller -knapp som peker til URL-adressen til innsjekkingsbekreftelsessiden du opprettet.</span><span class="sxs-lookup"><span data-stu-id="52edc-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="52edc-127">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="52edc-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="52edc-128">Hvis du vil ha mer informasjon om hvordan du konfigurerer e-postmaler, kan du se [Tilpasse transaksjons-e-postmeldinger etter leveringsmåte](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="52edc-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="52edc-129">En innsjekkingsbekreftelsesoppgave opprettes på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="52edc-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="52edc-130">Når en kunde har varslet butikken om at de er til stede for plukking, mottar de et varsel om innsjekkingsbekreftelse, og det opprettes en oppgave i oppgavelisten på salgsstedet for butikken der kunden plukker opp ordren.</span><span class="sxs-lookup"><span data-stu-id="52edc-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="52edc-131">Oppgaven inneholder all kunde- og ordreinformasjon som kreves for å oppfylle ordren.</span><span class="sxs-lookup"><span data-stu-id="52edc-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="52edc-132">I oppgaven viser instruksjonersfeltet all informasjon som ble samlet inn fra kunden via tilleggsinformasjonsskjemaet.</span><span class="sxs-lookup"><span data-stu-id="52edc-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="52edc-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="52edc-133">Additional resources</span></span>

[<span data-ttu-id="52edc-134">Innsjekking for plukkmodul</span><span class="sxs-lookup"><span data-stu-id="52edc-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
