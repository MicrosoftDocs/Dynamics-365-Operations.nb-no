---
title: Definere en profil for e-postvarsling
description: Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113811"
---
# <a name="set-up-an-email-notification-profile"></a>Definere en profil for e-postvarsling


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Før du oppretter kanaler, bør du sette opp en profil for å sikre at e-postvarslinger kan sendes ut for ulike hendelser, for eksempel ordreopprettelse, status for odreforsendelse og betalingsfeil.

Hvis du vil ha ytterligere informasjon om e-postkonfigurasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Opprette en profil for e-postvarsling

Hvis du vil opprette en e-postvarslingsprofil, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.
1. I handlingsruten klikker du på **Ny**.
1. I **E-postvarslingsprofil**-feltet angir du et navn for å identifisere profilen.
1. I **Beskrivelse**-feltet angir du en relevant beskrivelse.
1. Sett **Aktiv**-bryteren til **Ja**.

### <a name="create-an-email-template"></a>Opprett en e-postmal

Før du kan opprette en e-postvarsling, må du opprette en e-postmal for organisasjonen som inneholder e-postinformasjonen og e-postmalen for avsenderne.

Hvis du vil opprette en e-postmal, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> E-postmaler for organisasjon**.
1. I handlingsruten velger du **Ny**.
1. I **E-post id**-feltet angir du en ID for å forenkle identifisering av denne malen.
1. I **Avsendernavn**-feltet angir du avsendernavnet.
1. I **E-postbeskrivelse** angir du en meningsfull beskrivelse.
1. I **Avsenderens e-post** angir du avsenderens e-postadresse.
1. I **Generelt**-delen fyller du ut eventuell nødvendig tilleggsinformasjon (for eksempel e-postprioriteten).
1. Utvid **E-postmeldingsinnhold**-delen og velg **Ny** for å opprette malinnholdet. For hvert innholdselement velger du språket og oppgir emnelinjen for e-post. Hvis e-posten skal inneholde brødtekst, må du forsikre deg om at det er merket av i **Har brødtekst**-boksen.
1. I handlingsruten velger du **E-postmelding** for å angi en mal for e-postbrødtekst.

Bildet nedenfor viser noen eksempelinnstillinger for e-postmal.

![Innstillinger for e-postmal](media/email-template.png)

### <a name="create-an-email-event"></a>Opprette en e-posthendelse

Hvis du vil opprette en e-posthendelse, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.
1. Finn og velg ønsket post i listen. 
1. Velg e-postmalen fra **E-post-ID**-rullegardinlisten.
1. Velg aktuell **E-postvarslingstype** fra rullegardinlisten.
1. Merk av i **Aktiv**-avmerkingsboksen.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser noen eksempelinnstillinger for hendelsesvarsling.

![Innstillinger for hendelsesvarsling](media/email-notification-profile.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
