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
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a0cf8037ba151bb4e68da1cf4609fb2e4806303a
ms.sourcegitcommit: b952b9f9066a5317259b8344db4c5d99eab4bf3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/25/2020
ms.locfileid: "3165781"
---
# <a name="client-alert-notifications-by-email"></a>Varselmeldinger til klient via e-post

[!include [banner](../includes/banner.md)]

Du kan du opprette egendefinerte varslingsregler som overvåker filtrerte visninger av data og sender e-postvarslinger automatisk når forhåndsdefinerte hendelser inntreffer. Alternativet for å sende e-postvarsler er tilgjengelig for alle varseltyper som støttes, og kan også aktiveres for eksisterende varslingsregler.

Du kan bruke innebygde kontroller til å opprette varslingsregler som overvåker de filtrerte visningene av satsvise jobber i systemet. Ved å overvåke verdien i **Status**-feltet kan du også konfigurere varslingsregler som sender e-post når en satsvis jobb mislykkes. Når disse varslingsreglene er opprettet, trenger du ikke lenger sjekke rapporter for endringer i forretningsdata. Du kan i stedet la den intelligente endringsregistreringstjenesten utføre overvåkingen for deg.

Klientvarsler avhenger av e-postdelsystemet som leveres gjennom integrasjon med Microsoft Office. Vi anbefaler at du bruker SMTP-leverandøren (Simple Mail Transfer Protocol), slik at e-distribusjonen ikke må være avhengig av en lokal e-postklient.

Hvis varslinger skal sendes via e-post, må kundene konfigurere integrerte e-posttjenester. E-postvarslinger sendes til mottakere på vegne av varseleiere.

Hvis du vil ha mer informasjon om hvordan du konfigurerer e-post, kan du se [Konfigurere og sende e-post](../organization-administration/configure-email.md).

Følgende bilde viser dialogboksen **Opprett varslingsregel**, som nå inneholder alternativet **Send e-post**.

[![Dialogboksen Opprett varslingsregel, der alternativet Send e-post er satt til Ja](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)

> [!NOTE]
> Når alternativet **Send e-post** er satt til **Ja**, vil varsler fortsatt leveres fra handlingssenteret.

## <a name="alert-notification-email-templates"></a>E-postmaler for varsler

Tjenesten sender e-postvarslinger ved hjelp av forhåndsdefinerte e-postmaler som leverer de grunnleggende opplysningene i varslingen.

Illustrasjonen nedenfor viser strukturen på varslingene når de mottas via e-post.

[![Malbaserte varslinger for postoppretting, feltendringer og malsletting](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)
