---
title: Listeside for leverandørtransaksjoner
description: Dette emnet gir informasjon om listesiden for leverandørtransaksjoner for Microsoft Dynamics 365 Finance.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 455ff6b2f337af272c63fce08f40de574622ad55c6fb2c3e5b354a9d34843559
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777198"
---
# <a name="vendor-transactions-list-page"></a>Listeside for leverandørtransaksjoner

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vis utligninger

Knappen **Vis utligninger** i handlingsruten gir rask tilgang til utligningshistorikken og detaljert informasjon om utligningstransaksjonen. Du kan også vise flere transaksjoner som er knyttet til den valgte transaksjonen, fordi de var en del av samme utligningen, eller fordi de er betalinger som ble opprettet i samme betalingsjournalen.

1. Velg **Leverandører \> Alle leverandører**.
2. Velg en leverandør som har transaksjoner, og gå deretter til handlingsruten, kategorien **Leverandør**, og velg **Transaksjoner**.
3. Velg en transaksjon til oppslag, og deretter i handlingsruten velger du **Vis utligninger**.

    I dialogboksen **Vis utligninger** vises den valgte transaksjonen og alle dokumenter som er utlignet mot den. Denne dialogboksen ligner på utligningsloggvisningen, men den inneholder alle relaterte dokumenter.

4. Du kan utføre forskjellige oppgaver i denne dialogboksen. Velg ett eller flere bilag, og velg deretter én av følgende knapper:

    - **Vis relatert** – Vis alle betalingsjournaltransaksjoner og økonomijournaltransaksjoner for leverandøren som ble opprettet i journalene der dokumentene som vises i listen, ble opprettet. Hvis for eksempel en betaling vises, vises alle betalingene i betalingsjournalen der den ble opprettet. Hvis en faktura eller betaling vises, og den ble opprettet i en økonomijournal, vil alle dokumentene i økonomijournalen der den ble opprettet, vises. Alle utligninger som er knyttet til listen med dokumenter, vises også. Når du viser relaterte betalinger, endres etiketten for denne knappen til **Vis utligninger**. Velg **Vis utligninger** for å vise bare transaksjonene som ble vist da du åpnet dialogboksen **Vis utligninger** for første gang.
    - **Vis logg** – Vis utligningshistorikken for bilagene. Velg **Lukk** for å lukke dialogboksen.
    - **Vis regnskap** – Vis alle bilagene som er knyttet til de valgte dokumentene. Velg **Lukk** for å lukke dialogboksen.
    - **Eksporter** – eksporter de valgte bilagene til Microsoft Excel.
    - **Utlign transaksjoner** – Denne knappen vises bare hvis det opprinnelige dokumentet som ble valgt, ikke ble helt utlignet. Når du velger denne knappen, vises dialogboksen **Utlign transaksjoner**, der du kan velge transaksjoner for utligning.
    - **Angre utligninger** – Denne knappen vises bare hvis det opprinnelige dokumentet som ble valgt, ble helt utlignet. Når du velger denne knappen, vises dialogboksen **Angre utligninger**, der du kan angre utligningene som er utført for dette dokumentet.

## <a name="global-transactions"></a>Globale transaksjoner

Knappen **Globale transaksjoner** vises også på **Leverandørtransaksjoner**-listesiden. Med denne knappen kan du vise alle transaksjoner for en leverandør på tvers av alle juridiske enheter. Listesiden **Leverandørtransaksjoner** viser transaksjoner bare for de juridiske enhetene som brukeren har tilgang til, basert på vedkommendes sikkerhetsinnstillinger.

Listesiden viser alle transaksjoner for leverandører som har samme part-ID som leverandøren du startet med. Hvis leverandøren US-001 i én juridisk enhet har samme part-ID som leverandør DE-001 i en annen juridisk enhet, vises for eksempel alle transaksjoner for begge leverandør-ID-ene.

Menyer på listesiden **Leverandørtransaksjoner** varierer avhengig av den juridiske enheten for transaksjonen. Hvis for eksempel en funksjon bare er tilgjengelig for sveitsiske juridiske enheter, vises menyalternativene for funksjonen bare når en sveitsisk transaksjon er valgt.

Hvis du vil ha tilgang til funksjonen, kan du følge disse trinnene.

1. Velg **Leverandører** \> **Alle leverandører**.
2. Velg en leverandør som har transaksjoner, og gå deretter til handlingsruten, kategorien **Leverandør**, **Transaksjoner**-gruppen, og velg **Globale transaksjoner**

## <a name="more-transaction-filters"></a>Flere transaksjonsfiltre

Filteret for å vise åpne transaksjoner er erstattet med et nytt filter som lar deg vise flere kombinasjoner av transaksjoner. Følgende alternativer er tilgjengelige i **Vis**-feltet:

- **Alle** – Vis alle transaksjoner for de valgte leverandørene (åpne og lukkede).
- **Lukket** – Vis bare transaksjoner som er fullstendig utlignet og lukket.
- **Åpen** – Vis bare transaksjoner som ikke er fullstendig utlignet.
- **Åpne inkludert lukket på eller etter dato** – Vis bare transaksjoner som ikke er fullstendig utlignet på eller etter en dato du angir. Når du velger dette alternativet, kan du endre datoen som vises ved siden av filteret. Transaksjoner som har en verdi for **Siste utligningsdato** på eller etter datoen du angir, vises i listen, selv om disse transaksjonene utlignes fullstendig per gjeldende dato. Saldoen representerer imidlertid saldoene per gjeldende dato, ikke per den valgte datoen.

Velg **Skjul revaluering av valuta**-avmerkingsboksen for å skjule valutaomregningstransaksjoner.

## <a name="modify-due-dates-and-discount-dates"></a>Endre forfallsdatoer og rabattdatoer

Du kan oppdatere forfallsdatoer og rabattdatoer for åpne kundetransaksjoner. I versjon 8.1 kan du nå legge til forfallsdatoer på listesiden **Leverandørtransaksjoner**. Ved å klikke på forfallsdatoen på listesiden **Leverandørtransaksjoner** kan du også endre forfallsdatoer, rabattdatoer, betalingsbetingelser og vilkår for kontantrabatt i dialogboksen **Forfallsdato for oppdatering og kontantrabattdatoer**.

### <a name="activate-the-feature"></a>Aktivere funksjonen

Hvis du vil legge til forfallsdatoer på listesiden **Leverandørtransaksjoner** og endre betalingsinnstillinger for en transaksjon ved hjelp av dialogboksen **Forfallsdato for oppdatering og kontantrabattdatoer**, gjør du følgende.

1. Velg **Leverandører \> Oppsett \> Leverandørparametere**.
2. I kategorien **Utligninger** setter du **Vis forfallsdato og tillat redigering** til **Ja**.
3. For å aktivere denne funksjonen er nye felt lagt til i leverandørtransaksjoner. Disse feltene fylles ut når en ny transaksjon er fullført. De vil også fylles ut når du åpner dialogboksen **Forfallsdato for oppdatering og kontantrabattdatoer**. Når du angir **Vis forfallsdato og tillat redigering** til **Ja**, vises dialogboksen **Oppdater betalingsinformasjon**.  Hvis du vil oppdatere eksisterende transaksjoner umiddelbart, velger du **Oppdater alle eksisterende transaksjoner**. Hvis du vil fylle ut feltene bare for nye transaksjoner, kan du også velge **Fortsett uten oppdatering**.

Forfallsdatoen er nå lagt til på listesiden **Leverandørtransaksjoner**, og det er enklere å endre forfallsdatoen og kontantrabattdatoene for transaksjoner.

### <a name="modify-the-payment-settings"></a>Endre betalingsinnstillingene

På listesiden **Leverandørtransaksjoner** vises alle transaksjoner for en leverandør. Når du velger forfallsdatoen for en transaksjon, vises en dialogboks. Denne dialogboksen viser basisdatoen for beregning av forfallsdato og rabatt, forfallsdatoen, betalingsbetingelsene, vilkårene for kontantrabatt og kontantrabattdatoene.

Hvert felt har en forskjellig effekt på transaksjonen når du redigerer det:

- **Rediger basisdatoen:** Forfallsdatoen og rabattdatoene endres som om basisdatoen er dokumentdatoen.
- **Rediger forfallsdatoen** – Bare forfallsdatoen endres
- **Rediger rabattdatoene:** Bare rabattdatoene endres.
- **Rediger betalingsbetingelsene:** Forfallsdatoen endres, basert på basisdatoen og betalingsbetingelsene.
- **Rediger vilkårene for kontantrabatt:** Kontantrabattene endres, basert på basisdatoen og vilkårene for kontantrabatt.

Når du er ferdig med å redigere betalingsinnstillingene, velger du **Lukk** for å lagre endringene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]