---
title: Aktiviteter i prosessene
description: Dette emnet gir informasjon om forskjellige typer aktiviteter som kan brukes i ansettelsesprosessen.
author: 
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 4f59193991420fd9ec05a83049e569058bf81932
ms.contentlocale: nb-no
ms.lasthandoff: 12/07/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aktiviteter i ansettelsesprosessene

[!include[banner](../includes/banner.md)]

Aktiviteter kan legges til som en del av ansettelsesprosessen i Microsoft Dynamics 365 for Talent: Attract. Aktiviteter kan legges til en prosessmal, eller de kan legges direkte til ansettelsesprosessen i jobben. Når en jobb er definert, velges en prosessmal, og aktivitetene som er inkludert i malen, gjelder for jobben. Hvis det ikke er valgt en mal, brukes standardmalen. Ansettelsesprosessen kan også endres i jobben etter at malen er brukt.

> [!NOTE] 
> Prosessmaler er tilgjengelige med tillegget for omfattende ansettelse.

## <a name="prospect-activity"></a>Kundeemneaktivitet

Kundeemneaktiviteten styrer om kundeemner kan legges til en jobb. Kundeemner kan legges til en jobb som standard. Hvis du vil deaktivere aktiviteten for kundeemnet, kan du angi alternativet **Aktiverer kandidater** til **Av**. Når aktiviteten for kundeemnet er aktivert, kan ansettelsesansvarlige legge til og vise kundeemner, og **Kundeemne**-kategorien vises for jobben.

## <a name="application-activity"></a>Søknadsaktivitet

Søknadsaktiviteten er påkrevd i malen for ansettelsesprosess. Hvis du vil sende e-post til kandidater når de sender inn søknaden eller legges til i søknadsstadiet, kan du angi **Send e-post til kandidat** til **På**.

## <a name="scheduler-activity"></a>Planleggeraktivitet

Planleggeraktiviteten er valgfri. Denne aktiviteten har to komponenter: kandidattilgjengelighet og tidsplan. Med komponenten kandidattilgjengelighet kan du bruke e-post til å spørre om en kandidats tilgjengelighet. Tidsplankomponenten gir mulighet å planlegge intervjuer med kandidaten og ansettelsesteamet. Du kan konfigurere følgende alternativer i planleggeraktiviteten: **Spør om kandidattilgjengelighet**, **Nettmøte** og **Send e-post til kandidat**.

- Hvis du vil sende e-post til kandidater for å spørre om de er tilgjengelige, kan du angi alternativet **Spør om kandidattilgjengelighet** til **På**. Hvis du setter alternativet til **Av**, vises ikke dette trinnet i ansettelsesprosessen for jobben.
- Hvis du vil ha en live-stream eller en telefonkonferanse ved hjelp av Skype for Business, setter du **Nettmøte**-feltet til **Skype for Business**. Den riktige **Bli med i Skype-møte**-koblingen legges deretter til i møteinnkallelsen for intervjuet som er sendt til intervjuere.
- Hvis du vil sende e-post til kandidater for å fullføre tidsplanen, angir du alternativet **Send e-post til kandidat** til **På**. Hvis du setter alternativet til **Av**, vil kandidater få intervjuplanen først når de logger på kandidatportalen.

## <a name="feedback-activity"></a>Tilbakemeldingsaktivitet

Tilbakemeldingsaktiviteten er valgfri. I denne aktiviteten kan intervjudeltakere angi anbefalinger for en søker. De kan også angi eventuelle tilbakemeldinger de har. Hvis du aktiverer alternativet **Arv tilbakemeldingsdeltakere fra ansettelsesteam**, angis rekrutterer, ansettelsesansvarlig og intervjuere automatisk i tilbakemeldingsaktiviteten. Organisasjoner kan la intervjuere vise tilbakemeldingen fra andre før de sender sine egen tilbakemelding. Organisasjoner kan også la intervjuerne redigere tilbakemeldingen etter at de har sendt den.

## <a name="interview-activity"></a>Intervjuaktivitet

Intervjuaktiviteten er valgfri. Denne aktiviteten har tre komponenter: kandidattilgjengelighet, tidsplan og tilbakemelding. Med komponenten kandidattilgjengelighet kan du bruke e-post til å spørre om en kandidats tilgjengelighet. Tidsplankomponenten gir mulighet å planlegge intervjuer med kandidaten og ansettelsesteamet. Du kan konfigurere følgende alternativer i planleggeraktiviteten: **Spør om kandidattilgjengelighet**, **Nettmøte** og **Send e-post til kandidat**.

- Hvis du vil sende e-post til kandidater for å spørre om de er tilgjengelige, kan du angi alternativet **Spør om kandidattilgjengelighet** til **På**. Hvis du setter alternativet til **Av**, vises ikke dette trinnet i ansettelsesprosessen for jobben.
- Hvis du vil ha en live-stream eller en telefonkonferanse ved hjelp av Skype for Business, setter du **Nettmøte**-feltet til **Skype for Business**. Den riktige **Bli med i Skype-møte**-koblingen legges deretter til i møteinnkallelsen.
- Hvis du vil sende e-post til kandidater for å fullføre tidsplanen, angir du alternativet **Send e-post til kandidat** til **På**. Hvis du setter alternativet til **Av**, vil kandidater få intervjuplanen først når de logger på kandidatportalen.

>[!NOTE]
> - For alle 1:1-intervjuer sendes påminnelser til intervjuerne hvert døgn hvis intervjueren ikke har svart (godtatt eller avslått) på intervjuforespørselen.
> - For alle panelintervjuer finnes det ingen automatiske påminnelser for å svare på intervjuforespørselen. Hvis du vil utløse en påminnelse manuelt, redigerer du intervjuet og bruker **Oppdater og send**-alternativet for å sende forespørselen tilbake til intervjuerne.

Komponenten tilbakemelding lar folk angi anbefalinger for en søker. De kan også angi eventuelle tilbakemeldinger de har. Hvis du aktiverer alternativet **Arv tilbakemeldingsdeltakere fra ansettelsesteam**, angis rekrutterer, ansettelsesansvarlig og intervjuere automatisk i tilbakemeldingskomponenten. Organisasjoner kan la intervjuere vise tilbakemeldingen fra andre før de sender sine egen tilbakemelding. Organisasjoner kan også la intervjuerne redigere tilbakemeldingen etter at de har sendt den.

## <a name="powerapps-activity"></a>PowerApps-aktivitet

PowerApps-aktiviteten lar deg bygge inn en Microsoft PowerApps-app i ansettelsesprosessen. Appen kan være nødvendig for alle søkere, bare interne søkere, bare ekstern søkere eller ingen søkere. Hvis appen er merket som påkrevd, må den fullføres før neste stadium. Hvis appen ikke er merket som påkrevd, er aktiviteten et valgfritt trinn, og stadiet kan endres selv om appen ikke er fullført.

Hvis du vil lagre PowerApps-aktiviteten i ansettelsesprosessen, må du angi en PowerApps-ID. Du kan finne PowerApps-IDen ved å gå til [PowerApps](https://web.powerapps.com), velge **Apper**  og deretter **Detaljer**.

Hvis du velger alternativet **Tillat tilføying av deltakere for denne aktiviteten**, kan flere bidragsytere legges til for et program som bruker PowerApps-aktiviteten. En organisasjon har for eksempel opprettet en PowerApps-app som er et bibliotek med intervjuspørsmål for tekniske roller. Organisasjonen ansetter nå en ny programvareutvikler og har lagt til PowerApps-aktiviteten i ansettelsesprosessen for programvareutvikler-rollen. Hvis alternativet **Tillat tilføying av deltakere for denne aktiviteten** er valgt, kan en rekrutterer eller ansettelsesansvarlig som viser en søker for programvareutvikler-rollen, legge til personer i PowerApps-aktiviteten. Disse personene kan deretter vise appen som har intervjuspørsmålene.

> [!NOTE]
> PowerApps-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

## <a name="youtube-activity"></a>YouTube-aktivitet

YouTube-aktiviteten lar deg dele en YouTube-video som en del av ansettelsesprosessen. Hvis du vil lagre YouTube-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for YouTube-videoen. Du kan tillate at det legges til deltakere i aktiviteten i PowerApps-aktiviteten. Hvis du velger alternativet **Vis bare til kandidat**, vises videoen bare som en del av kandidatopplevelsen. Den vises ikke i ansettelsesprosessen i Attract.

> [!NOTE]
> YouTube-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

## <a name="web-content-activity"></a>Webinnhold-aktivitet

Webinnhold-aktiviteten lar deg bygge inn elektronisk innhold i ansettelsesprosessen. Hvis du vil lagre webinnhold-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for innholdet. Du kan tillate at det legges til deltakere i aktiviteten i PowerApps- og YouTube-aktivitetene. Hvis du velger alternativet **Vis bare til kandidat**, vises innholdet bare som en del av kandidatopplevelsen. Den vises ikke i ansettelsesprosessen i Attract. Du kan velge størrelsen på innholdet som vises.

> [!NOTE]
> Webinnhold-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

## <a name="microsoft-forms-activity"></a>Microsoft Forms-aktivitet

Microsoft Forms-aktiviteten lar deg bygge inn et Microsoft Forms-skjema i ansettelsesprosessen. Med Microsoft Forms kan du opprette tester, undersøkelser og avstemninger. Hvis du vil lagre Microsoft Forms-aktiviteten i ansettelsesprosessen, må du angi URL-adressen for skjemaet. Du kan tillate at det legges til deltakere i aktiviteten i PowerApps-, YouTube- og web-innhold-aktivitetene. Hvis du velger alternativet **Vis bare til kandidat**, vises skjemaet bare som en del av kandidatopplevelsen. Den vises ikke i ansettelsesprosessen i Attract.

I Microsoft Forms kan forfattere endre innstillingene for å la brukere utenfor organisasjonen svare på undersøkelser eller spørsmål. I så fall sender brukerne svar anonymt. Hvis du vil se hvem som har fylt ut undersøkelser eller spørsmål, kan du kreve at respondentene angir navnene sine som en del av undersøkelser eller spørsmål.

> [!NOTE]
> Microsoft Forms-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

