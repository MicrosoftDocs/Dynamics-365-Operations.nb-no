---
title: Klientvarslinger via e-post
description: Dette emnet gir informasjon om hvordan du konfigurerer regler som sender e-postvarsler når forhåndsdefinerte hendelser inntreffer.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2019
ms.locfileid: "373808"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="8b5d8-103">Klientvarslinger via e-post</span><span class="sxs-lookup"><span data-stu-id="8b5d8-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8b5d8-104">I Microsoft Dynamics 365 for Finance and Operations kan du opprette egendefinerte varslingsregler som overvåker filtrerte visninger av data og sender e-postvarslinger automatisk når forhåndsdefinerte hendelser inntreffer.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="8b5d8-105">Alternativet for å sende e-postvarsler er tilgjengelig for alle varseltyper som støttes, og kan også aktiveres for eksisterende varslingsregler.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="8b5d8-106">Du kan bruke innebygde kontroller til å opprette varslingsregler som overvåker de filtrerte visningene av satsvise jobber i systemet.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="8b5d8-107">Ved å overvåke verdien i **Status**-feltet kan du også konfigurere varslingsregler som sender e-post når en satsvis jobb mislykkes.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="8b5d8-108">Når disse varslingsreglene er opprettet, trenger du ikke lenger sjekke rapporter for endringer i forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="8b5d8-109">Du kan i stedet la den intelligente endringsregistreringstjenesten i Finance and Operations utføre overvåkingen for deg.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="8b5d8-110">Klientvarsler avhenger av e-postdelsystemet som leveres gjennom integrasjon med Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="8b5d8-111">Vi anbefaler at du bruker SMTP-leverandøren (Simple Mail Transfer Protocol), slik at e-distribusjonen ikke må være avhengig av en lokal e-postklient.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="8b5d8-112">Hvis varslinger skal sendes via e-post, må kundene konfigurere integrerte e-posttjenester.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="8b5d8-113">E-postvarslinger sendes til mottakere på vegne av varseleiere.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="8b5d8-114">Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post i Finance and Operations, se [Konfigurere og sende e-post](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="8b5d8-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="8b5d8-115">Følgende bilde viser dialogboksen **Opprett varslingsregel**, som nå inneholder alternativet **Send e-post**.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="8b5d8-116">[![Dialogboksen Opprett varslingsregel, der alternativet Send e-post er satt til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="8b5d8-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="8b5d8-117">Når alternativet **Send e-post** er satt til **Ja**, vil varsler fortsatt leveres fra handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="8b5d8-118">E-postmaler for varsler</span><span class="sxs-lookup"><span data-stu-id="8b5d8-118">Alert notification email templates</span></span>

<span data-ttu-id="8b5d8-119">Tjenesten sender e-postvarslinger ved hjelp av forhåndsdefinerte e-postmaler som leverer de grunnleggende opplysningene i varslingen.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="8b5d8-120">Disse opplysningene inkluderer en direkte kobling til siden hvor varslingsregelen ble definert.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="8b5d8-121">Illustrasjonen nedenfor viser strukturen på varslingene når de mottas via e-post.</span><span class="sxs-lookup"><span data-stu-id="8b5d8-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="8b5d8-122">[![Malbaserte varslinger for postoppretting, feltendringer og malsletting](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="8b5d8-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>
