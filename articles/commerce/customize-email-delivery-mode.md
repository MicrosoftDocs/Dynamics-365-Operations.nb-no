---
title: Tilpasse transaksjons-e-poster etter leveringsmåte
description: Dette emnet beskriver hvordan du definerer egendefinerte e-postmaler for bestemte meldingstyper og leveringsmåter i Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: d0d96ddb20b2b09751d8c0c0bf8af713de35279a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222639"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="91dd2-103">Tilpasse transaksjons-e-poster etter leveringsmåte</span><span class="sxs-lookup"><span data-stu-id="91dd2-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91dd2-104">Dette emnet beskriver hvordan du definerer egendefinerte e-postmaler for bestemte meldingstyper og leveringsmåter i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91dd2-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91dd2-105">Transaksjons-e-postmeldinger kan nå tilpasses for en kombinasjon av en varslingstype (for eksempel **Ordre opprettet**, **Ordre pakket** eller **Ordre fakturert**) og en leveringsmåte (for eksempel over natten, hent i butikk eller hent utenfor butikk).</span><span class="sxs-lookup"><span data-stu-id="91dd2-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="91dd2-106">Egendefinerte transaksjons-e-poster lar forhandlere levere kundens bestilling med oppfyllelsesfunksjoner som er skreddersydd til ordrens leveringsmåte.</span><span class="sxs-lookup"><span data-stu-id="91dd2-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="91dd2-107">En Ordre pakket-hendelse tilpasses slik at instruksjoner om henting utenfor butikk for kunder som velger henting utenfor butikk.</span><span class="sxs-lookup"><span data-stu-id="91dd2-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="91dd2-108">Den kan også gi informasjon om transportøren og levering for kunder som velger å få bestillingen levert.</span><span class="sxs-lookup"><span data-stu-id="91dd2-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="91dd2-109">Hvis du vil bruke funksjonaliteten for egendefinerte transaksjons-e-postmeldinger, må du først aktivere funksjonen **Tilpass transaksjons-e-postmaler etter leveringsmåte** ved å gå til **Arbeidsområder \> Funksjonsbehandling** i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="91dd2-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="91dd2-110">E-poster kan tilpasses etter leveringsmåte for følgende varslingstyper:</span><span class="sxs-lookup"><span data-stu-id="91dd2-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="91dd2-111">**Ordreannullering** – Denne typen e-postvarsling er ny.</span><span class="sxs-lookup"><span data-stu-id="91dd2-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="91dd2-112">**Ordre opprettet**</span><span class="sxs-lookup"><span data-stu-id="91dd2-112">**Order created**</span></span>
- <span data-ttu-id="91dd2-113">**Ordre bekreftet**</span><span class="sxs-lookup"><span data-stu-id="91dd2-113">**Order confirmed**</span></span>
- <span data-ttu-id="91dd2-114">**Ordre fakturert** – Denne typen e-postvarsling er ny.</span><span class="sxs-lookup"><span data-stu-id="91dd2-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="91dd2-115">Den kan brukes i stedet for varslingstypen **Ordre sendt** som sender en varsling for en hvilken som helst fakturahendelse som har en sendt leveringsmåte (ikke en henting, utbæring eller elektronisk leveringsmåte).</span><span class="sxs-lookup"><span data-stu-id="91dd2-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="91dd2-116">**Ordre plukket**</span><span class="sxs-lookup"><span data-stu-id="91dd2-116">**Order picked**</span></span>
- <span data-ttu-id="91dd2-117">**Ordre pakket**</span><span class="sxs-lookup"><span data-stu-id="91dd2-117">**Order packed**</span></span>
- <span data-ttu-id="91dd2-118">**Ordre klar for henting** – Denne varslingstypen kan tilpasses etter leveringsmåte bare hvis funksjonen **Støtte for flere leveringsmåter** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="91dd2-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="91dd2-119">I så fall tilsvarer denne varslingstypen **Ordre pakket**-varslingstypen.</span><span class="sxs-lookup"><span data-stu-id="91dd2-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="91dd2-120">**Betaling mislyktes**</span><span class="sxs-lookup"><span data-stu-id="91dd2-120">**Payment failed**</span></span>
- <span data-ttu-id="91dd2-121">**Erstatningsordre opprettet**</span><span class="sxs-lookup"><span data-stu-id="91dd2-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="91dd2-122">Konfigurer e-postmaler for bestemte leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="91dd2-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="91dd2-123">I denne fremgangsmåten er forutsetningen at du allerede har opprettet de nye, egendefinerte e-postmalene, og har lagt dem til på siden **E-postmaler for organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="91dd2-124">Hvis du vil ha informasjon om hvordan du oppretter og laster opp e-postmaler, kan du se [Opprett e-postmaler for transaksjonshendelser](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="91dd2-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="91dd2-125">Følg denne fremgangsmåten for å konfigurere e-postmaler for bestemte leveringsmåter i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="91dd2-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="91dd2-126">Gå til **Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="91dd2-127">Under **Varslingsinnstillinger for handelshendelse** velger du en eksisterende varslingstype.</span><span class="sxs-lookup"><span data-stu-id="91dd2-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="91dd2-128">Mens varslingstypen fremdeles er valgt, velger du **Konfigurer leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="91dd2-129">Velg **Ny** i dialogen **Leveringsmåter**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="91dd2-130">Velg en leveringsmåte i feltet **Leveringsmåte**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="91dd2-131">I feltet **E-post-ID** velger du e-postmalen som skal tilordnes leveringsmåten.</span><span class="sxs-lookup"><span data-stu-id="91dd2-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="91dd2-132">Merk av i **Aktiv**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="91dd2-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="91dd2-133">Gjenta trinn 4 til og med 7 for å legge til flere leveringsmåter.</span><span class="sxs-lookup"><span data-stu-id="91dd2-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="91dd2-134">Når du er ferdig, velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="91dd2-135">Når mer enn én leveringsmåte finnes på tvers av linjer i en salgsordre, blir standardmalen brukt.</span><span class="sxs-lookup"><span data-stu-id="91dd2-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="91dd2-136">Standardmalen er malen som er tilordnet til varslingstypen på siden **Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="91dd2-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="91dd2-137">Hvis en salgsordre har en leveringsmåte som ikke er konfigurert for en egendefinert e-postmal, brukes standard e-postmalen.</span><span class="sxs-lookup"><span data-stu-id="91dd2-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91dd2-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="91dd2-138">Additional resources</span></span>

[<span data-ttu-id="91dd2-139">Opprette telefonsenterordrer</span><span class="sxs-lookup"><span data-stu-id="91dd2-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="91dd2-140">Endre leveringsmodus i salgssted</span><span class="sxs-lookup"><span data-stu-id="91dd2-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]