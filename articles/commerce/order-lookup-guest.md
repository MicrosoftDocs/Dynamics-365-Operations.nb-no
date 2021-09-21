---
title: Aktivere ordreoppslag for gjestebetalinger
description: Dette emnet beskriver hvordan du aktiverer ordreoppslag for gjestebetalinger i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0368f567898210f122047a9f298bcb28b7540de1
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472656"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Aktivere ordreoppslag for gjestebetalinger

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan du aktiverer ordreoppslag for gjestebetalinger i Microsoft Dynamics 365 Commerce.

Funksjonen for bestillingsoppslag for gjestebetalinger lar kunder som foretar innkjøp som gjestebrukere, slå opp ordrene sine. Funksjonen for ordreoppslag er nyttig når kunder vil utføre handlinger, for eksempel kontrollere innfrielsesstatusen til produkter i en ordre, kontrollere adressen som en ordre ble sendt til, bestille et produkt på nytt eller bekrefte butikken som en ordre blir hentet fra.

Kunder som legger inn ordrer som registrerte brukere, kan se ordredetaljene når de er logget på, men kunder som bruker gjestebetaling, kan ikke legge inn bestillinger. Når funksjonen for ordreoppslag for gjestebetalinger er aktivert, gir det imidlertid et skjema som kunder kan bruke til å søke etter ordrer de har plassert som gjester. I dette skjemaet angir kunder ordrebekreftelses-IDen og (valgfritt) e-postadressen de angav i betalingsprosessen.

I tillegg kan en kobling eller knapp som tar kunden direkte til ordredetaljer-siden for ordren, inkluderes i alle ordrerelaterte transaksjons-e-poster. Denne koblingen eller knappen fungerer for ordrer som plasseres både av registrerte brukere og gjestebrukere.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Slå på nødvendige funksjoner i Commerce Headquarters

Hvis du vil aktivere ordreoppslag for gjestebetalinger, må du aktivere følgende funksjoner i **Arbeidsområder \> Funksjonsbehandling** i Commerce Headquarters.

| Funksjon | Formål |
|---------|---------|
| Reservasjonsfunksjon for anonym brukersøkeordre for Retail | Denne funksjonen viser brukergrensesnittet i Commerce-parametere, som lar deg aktivere API for ordreoppslag for ikke-godkjente brukere, og konfigurere hvordan personlige data vises. |
| Aktiver generering av en sterkere kanalreferanse-ID | Denne funksjonen genererer en sikrere referanse-ID på 12 tegn (ordrebekreftelses-ID) som kan sendes i spørringsstrengen når en ordre blir sett opp. |
| Generer et konsekvent format for kanalreferanse-ID på tvers av kanaler | Denne funksjonen genererer en sikker kanalreferanse-ID for ordrer som plasseres via et e-handelsområde, salgsstedet eller et telefonsenter. Før du kan aktivere denne funksjonen, må funksjonen **Aktiver generering av en sterkere referanse-ID for kanal** være aktivert. |

Når du har aktivert **funksjonen for anonymt brukersøk etter ordredetaljer i Retail**, må du aktivere API-en som støtter ikke-godkjente ordreoppslag i Commerce Headquarters. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Kundeordre**. På **Kundeordrer**-siden på **Ordresøk**-hurtigfanen angir du alternativet **Aktiver ikke-godkjente ordreoppslag** til **Ja**, som vist i følgende illustrasjon.

## <a name="manage-the-display-of-personal-data"></a>Administrere visningen av personlige data

Hurtigfanen **Ordresøk** på **Kundeordrer**-siden i Commerce Headquarters inneholder feltet **Ta med personlige data i ordreoppslag for gjester** som gir deg mulighet til å bestemme om personlige opplysninger skal vises for kunder. Denne personlige informasjonen omfatter kundens leveringsadresse og de fire siste sifrene i kundens kredittkortnummer. Som standard vises ikke personlige opplysninger for kunder når ikke-godtatt ordreoppslag er aktivert. I tabellen nedenfor beskrives de tilgjengelige alternativene.

| Alternativ | Resultat |
|--------|--------|
| Aldri | Standardverdien. Ingen personlige opplysninger vises i ordreoppslag. Når registrerte brukere som er logget på, søker etter en ordre de opprettet mens de var logget på, kan de se personopplysningene deres. |
| Bare gjesteordrer | Personlige opplysninger vises i ordreoppslag for ordrer som kunder har opprettet som gjester. Hvis en ordre ble opprettet av en registrert bruker, må denne brukeren logge seg på for å se sine personlige opplysninger. |
| Alle ordrer | Personlige opplysninger vises i alle ordreoppslag. |

> [!NOTE]
> Disse alternativene bestemmer når personlige data, for eksempel kundens adresse og de siste fire sifrene i kundens kredittkortnummer, vises for anonyme gjestebrukere. For å beskytte personvernet til registrerte kunder anbefaler vi at du velger alternativet **Bare gjesteordrer**. Det sikreste alternativet er imidlertid **Aldri**.

Når du endrer verdien til feltet **Ta med personlige data i oppslagsfeltet for gjesteordre**, må du kjøre jobb 1070 (**kanalkonfigurasjon**) i Commerce Headquarters ved å gå til **Retail og Commerce \> IT for Retail og Commerce \> Distribusjonsplan**.

## <a name="configure-the-order-lookup-module"></a>Konfigurere ordreoppslagsmodulen

Ordreoppslagsmodulen i Commerce-modulbiblioteket brukes til å lage skjemaet som gjestebrukere bruker til å slå opp ordrer. Ordreoppslagsmodulen kan inkluderes i hovedsporet til en hvilken som helst side som ikke krever kundepålogging. Hvis du vil ha mer informasjon om hvordan du konfigurerer modulen, kan du se [Ordreoppslagsmodul](order-lookup-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Ordreoppslagsmodul](order-lookup-module.md)

[Definere en profil for e-postvarsling](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
