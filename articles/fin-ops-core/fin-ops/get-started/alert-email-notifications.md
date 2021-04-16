---
title: Klientvarslinger via e-post
description: Dette emnet gir informasjon om hvordan du konfigurerer regler som sender e-postvarsler når forhåndsdefinerte hendelser inntreffer.
author: RichdiMSFT
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d132ed979a84c2906298c05708cef1ee87f47078
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752920"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="7f702-103">Varselmeldinger til klient via e-post</span><span class="sxs-lookup"><span data-stu-id="7f702-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f702-104">Du kan du opprette egendefinerte varslingsregler som overvåker filtrerte visninger av data og sender e-postvarslinger automatisk når forhåndsdefinerte hendelser inntreffer.</span><span class="sxs-lookup"><span data-stu-id="7f702-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="7f702-105">Alternativet for å sende e-postvarsler er tilgjengelig for alle varseltyper som støttes, og du kan også aktivere dem for eksisterende varslingsregler.</span><span class="sxs-lookup"><span data-stu-id="7f702-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="7f702-106">Du kan bruke innebygde kontroller til å opprette varslingsregler som overvåker de filtrerte visningene av satsvise jobber i systemet.</span><span class="sxs-lookup"><span data-stu-id="7f702-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="7f702-107">Ved å overvåke verdien i **Status**-feltet kan du også konfigurere varslingsregler som sender e-post når en satsvis jobb mislykkes.</span><span class="sxs-lookup"><span data-stu-id="7f702-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="7f702-108">Etter at du har opprettet disse varslingsreglene, trenger du ikke lenger å sjekke rapporter for endringer i forretningsdata.</span><span class="sxs-lookup"><span data-stu-id="7f702-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="7f702-109">Du kan i stedet la den intelligente endringsregistreringstjenesten utføre overvåkingen for deg.</span><span class="sxs-lookup"><span data-stu-id="7f702-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="7f702-110">Klientvarsler avhenger av e-postdelsystemet som leveres gjennom integrasjon med Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="7f702-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="7f702-111">Vi anbefaler at du bruker SMTP-leverandøren (Simple Mail Transfer Protocol), slik at e-distribusjonen ikke må være avhengig av en lokal e-postklient.</span><span class="sxs-lookup"><span data-stu-id="7f702-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="7f702-112">Hvis varslinger skal sendes via e-post, må kundene konfigurere integrerte e-posttjenester.</span><span class="sxs-lookup"><span data-stu-id="7f702-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="7f702-113">E-postvarslinger sendes til mottakere på vegne av varseleiere.</span><span class="sxs-lookup"><span data-stu-id="7f702-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="7f702-114">Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post, kan du se [Konfigurere og sende e-post](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="7f702-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="7f702-115">Følgende bilde viser dialogboksen **Opprett varslingsregel**, som nå inneholder alternativet **Send e-post**.</span><span class="sxs-lookup"><span data-stu-id="7f702-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="7f702-116">[![Dialogboksen Opprett varslingsregel, der alternativet Send e-post er satt til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="7f702-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="7f702-117">Når alternativet **Send e-post** er satt til **Ja**, vil varsler fortsatt leveres fra handlingssenteret.</span><span class="sxs-lookup"><span data-stu-id="7f702-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="7f702-118">E-postmaler for varsler</span><span class="sxs-lookup"><span data-stu-id="7f702-118">Alert notification email templates</span></span>

<span data-ttu-id="7f702-119">Tjenesten sender e-postvarslinger ved hjelp av forhåndsdefinerte e-postmaler som leverer de grunnleggende opplysningene i varslingen.</span><span class="sxs-lookup"><span data-stu-id="7f702-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="7f702-120">Illustrasjonen nedenfor viser strukturen på varslingene når de mottas via e-post.</span><span class="sxs-lookup"><span data-stu-id="7f702-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="7f702-121">[![Malbaserte varslinger for postoppretting, feltendringer og malsletting](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="7f702-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]