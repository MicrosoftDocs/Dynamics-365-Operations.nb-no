---
title: Fordeler med e-postvarsling
description: Denne artikkelen gir en oversikt over e-postvarslingsfunksjonen for fordelsbehandlingsmodulen i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d550cbb2f639535dbb43765c9fb0632a514fbe8c
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229905"
---
# <a name="benefits-email-notification"></a>Fordeler med e-postvarsling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Funksjonen for e-postvarsling gjør det mulig å sende e-postvarslinger og påminnelser til ansatte i følgende scenarioer:

- Registrering av ny ansettelse
- Åpen registrering
- Kvalifiserende levetidshendelser

Du kan opprette og definere flere e-postmaler, og sende varslinger ved hjelp av arbeidsområdet **Fordelsbehandling** og siden **Arbeidsfordeler**. Du kan også spore historikken for varslinger/påminnelser.

## <a name="set-up-human-resources-shared-parameters"></a>Definer delte parametere for personale

På siden **Personaldelte parametere** kan du opprette e-postmaler for fordeler for ulike typer kommunikasjon som sendes til ansatte eller ansattgrupper.

## <a name="create-a-new-email-id-template"></a>Opprette en ny mal for e-post-ID

Hvis du vil opprette en ny mal for e-post-ID, følger du disse trinnene.

1. Gå til **Maler for e-post til system**.
2. Velg **Ny**.
3. Angi et navn i **E-post-ID**-feltet.
4. Angi de andre feltene etter behov.
5. Velg **E-postmelding** for å laste opp malen.
6. På siden **Personaldelte parametere** velger du den nye malen under **Systemmaler**, og flytter den under **Maler for fordeler**.

## <a name="send-email-to-employees"></a>Send e-post til ansatte

Følg denne fremgangsmåten for å sende en e-post til en nyansettelse som ennå ikke er startet.

1. Åpne **Fordelsbehandling**-arbeidsområdet.
2. Velg flisen for gruppen med ansatte som du vil sende e-postmeldingen til.
3. Velg **Send e-post**.
4. Velg ansatte som du vil sende e-postmeldingen til.
5. Velg **Send e-post**.
6. Velg malen du vil bruke.
7. Velg **OK** for å sende e-posten.

    Du kan se gjennom e-postmeldingen og statusen fra den siden **Ansattfordel**, eller ved å velge **E-posthistorikk for fordeler** i **Koblingene**-delen i arbeidsområdet **Fordelsbehandling**. Du kan også sende e-postmeldingen fra siden **Arbeidsfordelsplan**.

8. Hvis du vil vise e-posthistorikk for fordeler, velger du **E-posthistorikk for fordeler** i arbeidsområdet **Fordelsbehandling** i delen **Koblinger**.
9. Vis den fullstendige e-posthistorikken for fordels-e-postmeldinger som er sendt. Hvis du vil se gjennom innholdet i e-postmeldingen, velger du **Vis melding**.
10. Velg **Arbeider**.
11. På siden **Arbeiderfordelsplan** kan du sende e-post og vise e-posthistorikk for fordeler.

Arbeidsområdet **Fordelsbehandling** omfatter ulike fliser. Du kan sende e-postmeldinger ved å velge den tilknyttede malen. Hvis de nye e-postene for ansettelsesregistrering er sendt, velger du kassen **Ny ansettelse ikke startet**, og deretter velger du koblingen **Send påminnelse**. Du kan velge en påminnelsesmal og angi tittelen på meldingen som en første, andre eller tredje påminnelse.
