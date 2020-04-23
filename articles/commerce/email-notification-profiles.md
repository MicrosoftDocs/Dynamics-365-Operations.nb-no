---
title: Definere en profil for e-postvarsling
description: Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180201"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="d363d-103">Definere en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="d363d-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d363d-104">Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d363d-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d363d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="d363d-105">Overview</span></span>

<span data-ttu-id="d363d-106">Før du oppretter kanaler, bør du sette opp en profil for å sikre at e-postvarslinger kan sendes ut for ulike hendelser, for eksempel ordreopprettelse, status for odreforsendelse og betalingsfeil.</span><span class="sxs-lookup"><span data-stu-id="d363d-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="d363d-107">Hvis du vil ha ytterligere informasjon om e-postkonfigurasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d363d-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="d363d-108">Opprette en profil for e-postvarsling</span><span class="sxs-lookup"><span data-stu-id="d363d-108">Create an email notification profile</span></span>

<span data-ttu-id="d363d-109">Hvis du vil opprette en e-postvarslingsprofil, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d363d-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="d363d-110">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="d363d-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d363d-111">I handlingsruten klikker du på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d363d-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="d363d-112">I **E-postvarslingsprofil**-feltet angir du et navn for å identifisere profilen.</span><span class="sxs-lookup"><span data-stu-id="d363d-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="d363d-113">I **Beskrivelse**-feltet angir du en relevant beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d363d-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="d363d-114">Sett **Aktiv**-bryteren til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d363d-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="d363d-115">Opprett en e-postmal</span><span class="sxs-lookup"><span data-stu-id="d363d-115">Create an email template</span></span>

<span data-ttu-id="d363d-116">Før du kan opprette en e-postvarsling, må du opprette en e-postmal for organisasjonen som inneholder e-postinformasjonen og e-postmalen for avsenderne.</span><span class="sxs-lookup"><span data-stu-id="d363d-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="d363d-117">Hvis du vil opprette en e-postmal, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d363d-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="d363d-118">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> E-postmaler for organisasjon**.</span><span class="sxs-lookup"><span data-stu-id="d363d-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="d363d-119">I handlingsruten velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d363d-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d363d-120">I **E-post id**-feltet angir du en ID for å forenkle identifisering av denne malen.</span><span class="sxs-lookup"><span data-stu-id="d363d-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="d363d-121">I **Avsendernavn**-feltet angir du avsendernavnet.</span><span class="sxs-lookup"><span data-stu-id="d363d-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="d363d-122">I **E-postbeskrivelse** angir du en meningsfull beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d363d-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="d363d-123">I **Avsenderens e-post** angir du avsenderens e-postadresse.</span><span class="sxs-lookup"><span data-stu-id="d363d-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="d363d-124">I **Generelt**-delen fyller du ut eventuell nødvendig tilleggsinformasjon (for eksempel e-postprioriteten).</span><span class="sxs-lookup"><span data-stu-id="d363d-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="d363d-125">Utvid **E-postmeldingsinnhold**-delen og velg **Ny** for å opprette malinnholdet.</span><span class="sxs-lookup"><span data-stu-id="d363d-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="d363d-126">For hvert innholdselement velger du språket og oppgir emnelinjen for e-post.</span><span class="sxs-lookup"><span data-stu-id="d363d-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="d363d-127">Hvis e-posten skal inneholde brødtekst, må du forsikre deg om at det er merket av i **Har brødtekst**-boksen.</span><span class="sxs-lookup"><span data-stu-id="d363d-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="d363d-128">I handlingsruten velger du **E-postmelding** for å angi en mal for e-postbrødtekst.</span><span class="sxs-lookup"><span data-stu-id="d363d-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="d363d-129">Bildet nedenfor viser noen eksempelinnstillinger for e-postmal.</span><span class="sxs-lookup"><span data-stu-id="d363d-129">The following image shows some example email template settings.</span></span>

![Innstillinger for e-postmal](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="d363d-131">Opprette en e-posthendelse</span><span class="sxs-lookup"><span data-stu-id="d363d-131">Create an email event</span></span>

<span data-ttu-id="d363d-132">Hvis du vil opprette en e-posthendelse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="d363d-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="d363d-133">I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.</span><span class="sxs-lookup"><span data-stu-id="d363d-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d363d-134">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d363d-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="d363d-135">Velg e-postmalen fra **E-post-ID**-rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="d363d-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="d363d-136">Velg aktuell **E-postvarslingstype** fra rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="d363d-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="d363d-137">Merk av i **Aktiv**-avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="d363d-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="d363d-138">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d363d-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d363d-139">Bildet nedenfor viser noen eksempelinnstillinger for hendelsesvarsling.</span><span class="sxs-lookup"><span data-stu-id="d363d-139">The following image shows some example event notification settings.</span></span>

![Innstillinger for hendelsesvarsling](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="d363d-141">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="d363d-141">Next steps</span></span>

<span data-ttu-id="d363d-142">Før du kan sende e-post, må du konfigurere tjenesten for utgående e-post og sette opp en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="d363d-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="d363d-143">Hvis du vil ha mer informasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d363d-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d363d-144">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d363d-144">Additional resources</span></span>

[<span data-ttu-id="d363d-145">Konfigurere og sende e-post</span><span class="sxs-lookup"><span data-stu-id="d363d-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d363d-146">Oversikt over kanaler</span><span class="sxs-lookup"><span data-stu-id="d363d-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d363d-147">Forutsetninger for kanaloppsett</span><span class="sxs-lookup"><span data-stu-id="d363d-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d363d-148">Oversikt over organisasjoner og organisasjonshierarkier</span><span class="sxs-lookup"><span data-stu-id="d363d-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
