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
ms.openlocfilehash: 9545731af20a96c322b4e92c17f3a46b7077295b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546968"
---
# <a name="client-alert-notifications-by-email"></a>Klientvarslinger via e-post

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 for Finance and Operations kan du opprette egendefinerte varslingsregler som overvåker filtrerte visninger av data og sender e-postvarslinger automatisk når forhåndsdefinerte hendelser inntreffer. Alternativet for å sende e-postvarsler er tilgjengelig for alle varseltyper som støttes, og kan også aktiveres for eksisterende varslingsregler.

Du kan bruke innebygde kontroller til å opprette varslingsregler som overvåker de filtrerte visningene av satsvise jobber i systemet. Ved å overvåke verdien i **Status**-feltet kan du også konfigurere varslingsregler som sender e-post når en satsvis jobb mislykkes. Når disse varslingsreglene er opprettet, trenger du ikke lenger sjekke rapporter for endringer i forretningsdata. Du kan i stedet la den intelligente endringsregistreringstjenesten i Finance and Operations utføre overvåkingen for deg.

Klientvarsler avhenger av e-postdelsystemet som leveres gjennom integrasjon med Microsoft Office. Vi anbefaler at du bruker SMTP-leverandøren (Simple Mail Transfer Protocol), slik at e-distribusjonen ikke må være avhengig av en lokal e-postklient.

Hvis varslinger skal sendes via e-post, må kundene konfigurere integrerte e-posttjenester. E-postvarslinger sendes til mottakere på vegne av varseleiere.

Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post i Finance and Operations, se [Konfigurere og sende e-post](../organization-administration/configure-email.md).

Følgende bilde viser dialogboksen **Opprett varslingsregel**, som nå inneholder alternativet **Send e-post**.

[![Dialogboksen Opprett varslingsregel, der alternativet Send e-post er satt til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Når alternativet **Send e-post** er satt til **Ja**, vil varsler fortsatt leveres fra handlingssenteret.

## <a name="alert-notification-email-templates"></a>E-postmaler for varsler

Tjenesten sender e-postvarslinger ved hjelp av forhåndsdefinerte e-postmaler som leverer de grunnleggende opplysningene i varslingen.

Illustrasjonen nedenfor viser strukturen på varslingene når de mottas via e-post.

[![Malbaserte varslinger for postoppretting, feltendringer og malsletting](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
