---
title: Legge til aktiviteter i en ansettelsesprosess
description: Dette emnet gir informasjon om forskjellige typer aktiviteter du kan legge til i en ansettelsesprosess i Microsoft Dynamics 365 Talent – Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462145"
---
# <a name="add-activities-to-a-hiring-process"></a>Legge til aktiviteter i en ansettelsesprosess

[!include [banner](includes/banner.md)]

Aktiviteter kan legges til som en del av ansettelsesprosessen i Microsoft Dynamics 365 Talent: Attract. Aktiviteter kan legges til en prosessmal, eller de kan legges direkte til ansettelsesprosessen i jobben. Når en jobb er definert, velges en prosessmal, og aktivitetene som er inkludert i malen, gjelder for jobben. Hvis det ikke er valgt en mal, brukes standardmalen. Ansettelsesprosessen kan også endres i jobben etter at malen er brukt.

> [!NOTE] 
> Prosessmaler er tilgjengelige med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Kundeemneaktivitet

Kundeemneaktiviteten styrer om kundeemner kan legges til en jobb. Kundeemner kan legges til en jobb som standard. Hvis du vil deaktivere aktiviteten for kundeemnet, kan du angi alternativet **Aktiverer kandidater** til **Av**. Når aktiviteten for kundeemnet er aktivert, kan ansettelsesansvarlige legge til og vise kundeemner, og **Kundeemne**-kategorien vises for jobben.

> [!NOTE]
> Hvis du vil la kandidater legge til en jobb fra LinkedIn, må du sette alternativet **Aktiver kandidater** til **På**.

## <a name="application-activity"></a>Søknadsaktivitet

Søknadsaktiviteten er påkrevd i malen for ansettelsesprosess. Hvis du vil sende e-post til kandidater når de sender inn søknaden eller legges til i søknadsstadiet, kan du angi **Send e-post til kandidat** til **På**.

## <a name="interview-schedule-and-feedback-activity"></a>Intervjuvtidsplan og tilbakemeldingsaktivitet

Denne aktiviteten har tre komponenter: forespørsel om kandidattilgjengelighet, tidsplan og tilbakemelding. Bruk intervjuaktiviteten i jobbmalen hvis du vil ta med kandidatens tilgjengelighetsforespørsel, tidsplan og tilbakemelding som en del av prosessen, i stedet for å bruke dem enkeltvis som en del av ansettelsesprosessen. Hvis du vil ha mer informasjon, se [Planlegging og tilbakemelding for intervju](interview-scheduling-feedback.md).

## <a name="power-apps-activity"></a>Power Apps-aktivitet

Power Apps-aktiviteten lar deg bygge inn en Microsoft Power Apps-app i ansettelsesprosessen. Appen kan være nødvendig for alle søkere, bare interne søkere, bare ekstern søkere eller ingen søkere. Hvis appen er merket som påkrevd, må den fullføres før neste stadium. Skal anses som fullført må **JobApplicationStatus**-feltet settes til **Fullført**. Dette feltet er plassert i JobApplicationActivity-enheten, slik at Power Apps-appen må oppdatere dette feltet før neste stadium. Hvis appen ikke er merket som påkrevd, er aktiviteten et valgfritt trinn, og stadiet kan endres selv om appen ikke er fullført.

Hvis du vil lagre Power Apps-aktiviteten i ansettelsesprosessen, må du angi en Power Apps-ID. Du kan finne Power Apps-ID-en ved å gå til [Power Apps](https://web.powerapps.com), velge **Apper** og deretter **Detaljer**.

Som standard er Power Apps-aktiviteten tilgjengelig for ansettelsesansvarlig, rekrutterer og deres representanter. Hvis du velger alternativet **Tillat tilføying av deltakere for denne aktiviteten**, kan flere deltakere fra rekrutteringsteamet legges til for et program som bruker Power Apps-aktiviteten. En organisasjon har for eksempel opprettet en Power Apps-app som er et bibliotek med intervjuspørsmål for tekniske roller. Organisasjonen ansetter nå en ny programvareutvikler og har lagt til Power Apps-aktiviteten i ansettelsesprosessen for programvareutvikler-rollen. Hvis alternativet **Tillat tilføying av deltakere for denne aktiviteten** er valgt, kan en rekrutterer eller ansettelsesansvarlig som viser en søker for programvareutvikler-rollen, legge til intervjuere i Power Apps-aktiviteten. Disse personene kan deretter vise appen som har intervjuspørsmålene.

> [!NOTE]
> Power Apps-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube-aktivitet

YouTube-aktiviteten lar deg dele en YouTube-video som en del av ansettelsesprosessen. Hvis du vil lagre YouTube-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for YouTube-videoen. Du kan velge å vise innholdet til **Ansettelsesteam**, **Bare interne kandidater**, **Bare eksterne kandidater** eller **Alle kandidater**. Som med Power Apps-aktiviteten kan du tillate at deltakere i rekrutteringsteamet legges til i aktiviteten. Hvis du velger å vise innholdet til kandidater, vises videoen bare som en del av kandidatopplevelsen og ikke i ansettelsesprosessen.

> [!NOTE]
> YouTube-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Webinnhold-aktivitet

Webinnhold-aktiviteten lar deg bygge inn elektronisk innhold i ansettelsesprosessen. Hvis du vil lagre webinnhold-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for innholdet. Du kan velge å vise innholdet til **Ansettelsesteam**, **Bare interne kandidater**, **Bare eksterne kandidater** eller **Alle kandidater**. Som med Power Apps- og YouTube-aktiviteter kan du tillate at deltakere i rekrutteringsteamet legges til i aktiviteten. Hvis du velger å vise innholdet til kandidater, vises webinnholdet bare som en del av kandidatopplevelsen og ikke i ansettelsesprosessen. Du kan velge størrelsen på innholdet som vises.

> [!NOTE]
> Webinnhold-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Microsoft Forms-aktivitet

Microsoft Forms-aktiviteten lar deg bygge inn en Microsoft Forms-aktivitet i ansettelsesprosessen. Med Microsoft Forms kan du opprette tester, undersøkelser og avstemninger. Hvis du vil lagre Microsoft Forms-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for skjemaet. Du kan velge å vise innholdet til **Ansettelsesteam**, **Bare interne kandidater**, **Bare eksterne kandidater** eller **Alle kandidater**. Som med Power Apps-, YouTube- og webinnholdsaktiviteter kan du tillate at deltakere i rekrutteringsteamet legges til i aktiviteten. Hvis du velger å vise innholdet til kandidater, vises skjemaet bare som en del av kandidatopplevelsen og ikke i ansettelsesprosessen.

I Microsoft Forms kan forfattere endre innstillingene for å la brukere utenfor organisasjonen svare på undersøkelser eller spørsmål. I så fall sender brukerne svar anonymt. Hvis du vil se hvem som har fylt ut undersøkelser eller spørsmål, kan du kreve at respondentene angir navnene sine som en del av undersøkelser eller spørsmål.

> [!NOTE]
> Microsoft Forms-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Tilbudsaktivitet

Ansettelsesprosessmalen krever tilbudsaktiviteten. Hvis du vil bruke den integrerte tilbudsadministrasjonsappen, kan du sette **Lanser Offer Management-app under klargjøring av tilbud** til **På**. Hvis denne innstillingen er deaktivert, vises ikke kandidaten i tilbudsappen, så du må spore oppdateringer til en kandidats tilbudsaktivitet manuelt. Hvis du vil definere om ansettelseslederne kan forberede tilbudet til kandidaten i tilbudsappen, kan du sette **Ansettelsesansvarlige kan klargjøre tilbud** til **På**. Hvis jobben har flere stillinger som er knyttet til den, kan du bestemme om du vil lage flere tilbud mot samme stillingsnummeret. Hvis du vil tillate bare ett tilbud per stilling per jobb, setter du **Tillat at stillinger brukes på nytt i jobb** til **Av**.

> [!NOTE]
> Den integrerte tilbudsadministrasjonsappen er bare tilgjengelig med tillegget for omfattende ansettelse. For mer informasjon, se [Hvilken versjon av Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]