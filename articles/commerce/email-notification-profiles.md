---
title: Definere en profil for e-postvarsling
description: Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792663"
---
# <a name="set-up-an-email-notification-profile"></a>Definere en profil for e-postvarsling

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en e-postvarslingsprofil i Microsoft Dynamics 365 Commerce.

Når du oppretter kanaler, kan du definere en e-postvarslingsprofil. På den måten kan e-postmeldinger sendes til kunder for ulike transaksjonshendelser, for eksempel opprettelse av ordre, forsendelsesstatus og betalingsfeil.

Hvis du vil ha ytterligere informasjon om e-postkonfigurasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Opprette en profil for e-postvarsling

Hvis du vil opprette en e-postvarslingsprofil, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Handelsprofil for e-postvarsling**.
1. I handlingsruten klikker du på **Ny**.
1. I **E-postvarslingsprofil**-feltet angir du et navn for å identifisere profilen.
1. I **Beskrivelse**-feltet angir du en relevant beskrivelse.
1. Sett **Aktiv**-bryteren til **Ja**.

### <a name="create-an-email-template"></a>Opprett en e-postmal

Før en e-postvarslingstype kan aktiveres, må du opprette en e-postmal for organisasjonen i Commerce Headquarters. Denne malen definerer e-postemnet, avsenderen, standardspråket og e-postteksten for hvert språk du vil støtte.

Hvis du vil opprette en e-postmal, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> E-postmaler for organisasjon**.
1. I handlingsruten velger du **Ny**.
1. I **E-post id**-feltet angir du en ID for å forenkle identifisering av denne malen.
1. I **Avsendernavn**-feltet angir du avsendernavnet.
1. I **E-postbeskrivelse** angir du en meningsfull beskrivelse.
1. I **Avsenderens e-post** angir du avsenderens e-postadresse.
1. I delen **Generelt** velger du et standardspråk for e-postmalen. Standardspråket brukes når det ikke finnes en lokal mal for det angitte språket.
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

### <a name="next-steps"></a>Neste trinn

Før du kan sende e-post, må du konfigurere tjenesten for utgående e-post og sette opp en satsvis jobb. Hvis du vil ha mer informasjon, kan du se [Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere og sende e-post](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Oversikt over organisasjoner og organisasjonshierarkier](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
