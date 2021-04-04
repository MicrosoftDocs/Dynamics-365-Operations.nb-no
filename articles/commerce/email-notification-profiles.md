---
title: Definere en profil for e-postvarsling
description: Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
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
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555313"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="8a9f2-103">Definere en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="8a9f2-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a9f2-104">Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8a9f2-105">Når du oppretter kanaler, kan du definere en e-postvarslingsprofil.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="8a9f2-106">På den måten kan e-postmeldinger sendes til kunder for ulike transaksjonshendelser, for eksempel opprettelse av ordre, forsendelsesstatus og betalingsfeil.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="8a9f2-107">Hvis du vil ha ytterligere informasjon om e-postkonfigurasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8a9f2-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="8a9f2-108">Opprette en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="8a9f2-108">Create an email notification profile</span></span>

<span data-ttu-id="8a9f2-109">Hvis du vil opprette en e-postvarslingsprofil, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="8a9f2-110">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="8a9f2-111">I handlingsruten klikker du på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="8a9f2-112">I **E-postvarslingsprofil**-feltet angir du et navn for å identifisere profilen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="8a9f2-113">I **Beskrivelse**-feltet angir du en relevant beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="8a9f2-114">Sett **Aktiv**-bryteren til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="8a9f2-115">Opprett en e-postmal</span><span class="sxs-lookup"><span data-stu-id="8a9f2-115">Create an email template</span></span>

<span data-ttu-id="8a9f2-116">Før en e-postvarslingstype kan aktiveres, må du opprette en e-postmal for organisasjonen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="8a9f2-117">Denne malen definerer e-postemnet, avsenderen, standardspråket og e-postteksten for hvert språk du vil støtte.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="8a9f2-118">Hvis du vil opprette en e-postmal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="8a9f2-119">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> E-postmaler for organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="8a9f2-120">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8a9f2-121">I **E-post id**-feltet angir du en ID for å forenkle identifisering av denne malen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="8a9f2-122">I **Avsendernavn**-feltet angir du avsendernavnet.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="8a9f2-123">I **E-postbeskrivelse** angir du en meningsfull beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="8a9f2-124">I **Avsenderens e-post** angir du avsenderens e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="8a9f2-125">I delen **Generelt** velger du et standardspråk for e-postmalen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="8a9f2-126">Standardspråket brukes når det ikke finnes en lokal mal for det angitte språket.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="8a9f2-127">Utvid **E-postmeldingsinnhold**-delen og velg **Ny** for å opprette malinnholdet.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="8a9f2-128">For hvert innholdselement velger du språket og oppgir emnelinjen for e-post.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="8a9f2-129">Hvis e-posten skal inneholde brødtekst, må du forsikre deg om at det er merket av i **Har brødtekst**-boksen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="8a9f2-130">I handlingsruten velger du **E-postmelding** for å angi en mal for e-postbrødtekst.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="8a9f2-131">Bildet nedenfor viser noen eksempelinnstillinger for e-postmal.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-131">The following image shows some example email template settings.</span></span>

![Innstillinger for e-postmal](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="8a9f2-133">Opprette en e-posthendelse</span><span class="sxs-lookup"><span data-stu-id="8a9f2-133">Create an email event</span></span>

<span data-ttu-id="8a9f2-134">Hvis du vil opprette en e-posthendelse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="8a9f2-135">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="8a9f2-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="8a9f2-137">Velg e-postmalen fra **E-post-ID**-rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="8a9f2-138">Velg aktuell **E-postvarslingstype** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="8a9f2-139">Merk av i **Aktiv**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="8a9f2-140">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8a9f2-141">Bildet nedenfor viser noen eksempelinnstillinger for hendelsesvarsling.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-141">The following image shows some example event notification settings.</span></span>

![Innstillinger for hendelsesvarsling](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="8a9f2-143">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="8a9f2-143">Next steps</span></span>

<span data-ttu-id="8a9f2-144">Før du kan sende e-post, må du konfigurere tjenesten for utgående e-post og sette opp en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="8a9f2-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="8a9f2-145">Hvis du vil ha mer informasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="8a9f2-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8a9f2-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8a9f2-146">Additional resources</span></span>

[<span data-ttu-id="8a9f2-147">Konfigurere og sende e-post</span><span class="sxs-lookup"><span data-stu-id="8a9f2-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="8a9f2-148">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="8a9f2-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8a9f2-149">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="8a9f2-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8a9f2-150">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="8a9f2-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
