---
title: Klientvarslinger via e-post
description: Dette emnet gir informasjon om hvordan du konfigurerer regler som sender e-postvarsler når forhåndsdefinerte hendelser inntreffer.
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a1d520584e331631bb5a6a88ba6c9a8b50b3d29e
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798629"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="413b1-103">Varselmeldinger til klient via e-post</span><span class="sxs-lookup"><span data-stu-id="413b1-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="413b1-104">Du kan du opprette egendefinerte varslingsregler som overvåker filtrerte visninger av data og sender e-postvarslinger automatisk når forhåndsdefinerte hendelser inntreffer.</span><span class="sxs-lookup"><span data-stu-id="413b1-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="413b1-105">Alternativet for å sende e-postvarsler er tilgjengelig for alle varseltyper som støttes, og du kan også aktivere dem for eksisterende varslingsregler.</span><span class="sxs-lookup"><span data-stu-id="413b1-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="413b1-106">Du kan bruke innebygde kontroller til å opprette varslingsregler som overvåker de filtrerte visningene av satsvise jobber i systemet.</span><span class="sxs-lookup"><span data-stu-id="413b1-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="413b1-107">Ved å overvåke verdien i **Status**-feltet kan du også konfigurere varslingsregler som sender e-post når en satsvis jobb mislykkes.</span><span class="sxs-lookup"><span data-stu-id="413b1-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="413b1-108">Etter at du har opprettet disse varslingsreglene, trenger du ikke lenger å sjekke rapporter for endringer i forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="413b1-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="413b1-109">Du kan i stedet la den intelligente endringsregistreringstjenesten utføre overvåkingen for deg.</span><span class="sxs-lookup"><span data-stu-id="413b1-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="413b1-110">Klientvarsler avhenger av e-postdelsystemet som leveres gjennom integrasjon med Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="413b1-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="413b1-111">Vi anbefaler at du bruker SMTP-leverandøren (Simple Mail Transfer Protocol), slik at e-distribusjonen ikke må være avhengig av en lokal e-postklient.</span><span class="sxs-lookup"><span data-stu-id="413b1-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="413b1-112">Hvis varslinger skal sendes via e-post, må kundene konfigurere integrerte e-posttjenester.</span><span class="sxs-lookup"><span data-stu-id="413b1-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="413b1-113">E-postvarslinger sendes til mottakere på vegne av varseleiere.</span><span class="sxs-lookup"><span data-stu-id="413b1-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="413b1-114">Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post, kan du se [Konfigurere og sende e-post](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="413b1-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="413b1-115">Følgende bilde viser dialogboksen **Opprett varslingsregel**, som nå inneholder alternativet **Send e-post**.</span><span class="sxs-lookup"><span data-stu-id="413b1-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="413b1-116">[![Dialogboksen Opprett varslingsregel, der alternativet Send e-post er satt til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="413b1-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="413b1-117">Når alternativet **Send e-post** er satt til **Ja**, vil varsler fortsatt leveres fra handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="413b1-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="413b1-118">E-postmaler for varsler</span><span class="sxs-lookup"><span data-stu-id="413b1-118">Alert notification email templates</span></span>

<span data-ttu-id="413b1-119">Tjenesten sender e-postvarslinger ved hjelp av forhåndsdefinerte e-postmaler som leverer de grunnleggende opplysningene i varslingen.</span><span class="sxs-lookup"><span data-stu-id="413b1-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="413b1-120">Illustrasjonen nedenfor viser strukturen på varslingene når de mottas via e-post.</span><span class="sxs-lookup"><span data-stu-id="413b1-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="413b1-121">[![Malbaserte varslinger for postoppretting, feltendringer og malsletting](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="413b1-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
