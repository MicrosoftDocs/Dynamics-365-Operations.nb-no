---
title: Opprett og oppdater tidspunkter for kundehenting
description: Dette emnet beskriver hvordan du oppretter, konfigurerer og oppdaterer hentetidspunkter for kunder i Commerce Headquarters.
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 6dc2be8a6f62ce13068ce2242f92ef17830c2447
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205753"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Opprett og oppdater tidspunkter for kundehenting

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter, konfigurerer og oppdaterer hentetidspunkter for kunder i Commerce Headquarters.

Tidspunktfunksjonen gjør det mulig for forhandlere å definere et tidspunkt for varer som henteleveringsmåten for kunden er aktivert for. Ved hjelp av tidspunkter kan forhandlere definere dagene og klokkeslettene når ordrer kan hentes fra en butikk. Forhandlerne kan også definere antall ordrer som kan hentes i løpet av en gitt periode. På denne måten kan forhandlerne begrense antall ordrer som kan hentes på en bestemt dag, og på et gitt tidspunkt. Resultatet er en bedre kvalitetsopplevelse for kundene.

> [!NOTE]
> Tidspunktfunksjonen er tilgjengelig i Microsoft Dynamics 365 Commerce, versjon 10.0.15 og nyere.

Følgende illustrasjon viser et eksempel på valg av tidspunkt under e-handelsbetaling.

![Eksempel på valg av tidspunkt under e-handelsbetaling](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Egenskaper for tidspunkt

En tidspunkt er et bestemt intervall når en kunde kan velge å hente en ordre fra en bestemt butikk eller et bestemt sted. Funksjonen for tidspunktstyring er bare tilgjengelig når henteleveringsmåten for kunden er konfigurert i Dynamics 365 Commerce.

Et tidspunkt defineres ved hjelp av følgende egenskaper:

- **Leveringsmåte** – Angi henteleveringsmåten som tidspunktet gjelder for.
- **Minimum dager** og **Maksimum dager** – Angi de tidligste og siste datoene som kan velges for henting i forhold til datoen da ordren er bestilt. 

    **Minimum dager**-egenskapen sikrer at forhandleren har nok tid til å behandle ordren før den er klar til henting. **Maksimum dager**-egenskapen sikrer at brukeren ikke kan velge en dato som er for langt inn i fremtiden. Hvis for eksempel minimumsverdien er satt til **1**, og en ordre blir bestilt 20. september, er den første dagen ordren blir tilgjengelig for henting, den neste dagen (21. september). På lignende måte kan du, ved å angi en maksimumsverdi, definere maksimalt antall dager en ordre kan hentes. Når minimums- og maksimumsverdiene er definert, kan områdebrukere se og velge bare et bestemt sett med dager i løpet av utsjekkingen.

    Du kan angi en minimumsverdi til en desimal verdi som er mindre enn 1. Hvis henting for eksempel er tilgjengelig fire timer etter at en ordre er bestilt, setter du minimumsverdien til **0,17** (= 4 ÷ 24, rundet opp til to desimaler). Hvis du imidlertid angir minimumsverdien til en desimalverdi som er større enn 1, avrundes den alltid opp til nærmeste hele tall. Verdien **1,2** vil for eksempel rundes opp til **2**. Hvis du imidlertid angir maksimumsverdien til en desimalverdi, avrundes den alltid opp til nærmeste hele tall. 

- **Startdato** og **Sluttdato** – Angi start- og sluttdatoene for tidspunktet. Hver tidspunktoppføring har en startdato og en sluttdato. Derfor har du fleksibilitet til å legge til ulike tidspunkter gjennom hele året (for eksempel henting i ferier). Hvis tidspunktets startdato og sluttdato endres etter at en ordre er bestilt, gjelder ikke endringene for den ordren. Når du definerer start- og sluttdatoer, må du ta hensyn til datoer når butikken er stengt (for eksempel første juledag), og kontrollere at tidspunktene ikke er definert for disse dagene.
- **Aktive hentetider** – Angi perioden når henting er tillatt. Hentetidene kan for eksempel være mellom 14:00 og 17:00 hver dag. Denne egenskapen gjør at hentetidene er uavhengige av butikkåpningstidene. Derfor kan forhandleren konfigurere hentetidene som oppfyller deres bestemte forretningsbehov. Når du definerer aktive leveringstider, må du vurdere butikken åpningstid og kontrollere at hentetidspunktene ikke er definert for tidspunkt når butikken er stengt.

    > [!NOTE]
    > Tidene for henting i butikk må defineres i tidssonen til den aktuelle butikken.

- **Tidspunktintervall** – Angi varigheten som kan tildeles hvert tidspunkt. Det kan for eksempel hende at varigheten til hver enkelt tidspunkt er i trinn på 15 minutter, 30 minutter eller én time. Hvis tidssporverdien er 0, er tidssporet tilgjengelig for hele varigheten mellom start- og sluttiden.
- **Tidspunkter per intervall** – Angi antall kunder eller ordrer som kan behandles for henting under hvert tidspunktintervall. Du kan for eksempel angi **1**, **2**, **3** eller et annet heltall.
- **Aktive dager** – Angi dagene i uken når hentetidspunkter er aktive. Denne egenskapen gjør at forhandleren definerer dagene den vil støtte henteordrer.
- **Detaljhandelskanaler** – Angi detaljhandelskanalene. Hvert tidspunkt kan knyttes til én eller flere detaljhandelsbutikker. Avhengig av hver butikks åpningstid, kan én eller flere tidspunktoppføringer opprettes og knyttes til en kanal. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Bare én tidspunktmal kan konfigureres per kanal. Disse kanalene omfatter fysiske butikker, telefonsentre, mobile enheter og e-handel-områder.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Konfigurer tidspunktfunksjonen i Commerce Headquarters

Tidspunkter må defineres for hver henteleveringsmåte i Commerce Headquarters, slik at salgsstedet og e-handelskanalene kan referere til dem.

- Bare én tidspunktmal kan knyttes til hver butikk eller kanal.
- Hvert tidspunkt som opprettes, bør være unikt for hver leveringsmåte i hver mal.
- Når tidspunktfunksjonen er konfigurert, blir tidspunktkalenderen tilgjengelig for de valgte butikkene eller butikkgruppene. Den vil også være synlig på salgsstedet, for referanse.

Følg denne fremgangsmåten for å konfigurere tidspunktfunksjonen i Commerce Headquarters.

1. Gå til **Commerce** \> **Kanaloppsett** \> **Hentetidspunkt i butikk**.
1. Velg **Ny** for å opprette en ny tidspunktmal. Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten.
1. Angi verdier i feltene **Tidspunkt-ID** og **Beskrivelse**.
1. Velg **Legg til** i hurtigfanen **Ordrehenting – tidsinnstillinger**.
1. I dialogboksen **Ordrehenting – tidsinnstillinger** definerer du datointervallet, leveringsmåten, aktive leveringstider, aktive dager, tidspunktintervall, tidspunkter per intervall og andre innstillinger.

    Hvis tidspunktene skal være statiske enn så lenge, setter du **Sluttdato**-feltet til **Aldri**.

    > [!NOTE]
    > Du kan opprette flere maler, men bare én mal kan knyttes til én enkelt kanal eller butikk.

    ![Dialogboksen Ordrehenting – tidsinnstillinger](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Når du er ferdig, velg **OK**.
1. Hvis tidspunkt på en dag varierer, oppretter du flere oppføringer i hurtigfanen **Ordrehenting – tidsinnstillinger** for å sikre at datoene og klokkeslettene ikke overlapper hverandre.
1. På hurtigfanen **Detaljhandelskanaler** velger du **Legg til** for å knytte tidspunktmalen til butikkene eller kanalene der den skal brukes.
1. I dialogboksen **Velg organisasjonsnoder** bruker du pilknappene til å velge (eller fjerne valg av) butikkene, områdene og organisasjonene som malen skal knyttes til.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Når du er ferdig, velg **OK**.
1. På siden **Distribusjonsplan** kjører du **1070**- og **1135**-jobber for å synkronisere data til kanalene.

## <a name="time-slot-selection-for-pos-orders"></a>Tidspunktvalg for salgsstedsordrer

Når en ordre eller ordrelinje identifiseres for henting på salgsstedet, kan selgeren velge hentebutikken eller -stedet og dato og klokkeslett. Hvis en kunde har en plukkordre for en annen butikk, kan kassereren velge datoer som plukkingen skal være tilgjengelig på, i denne butikken. Butikkoppslaget vil inneholde en referanse til datoene og åpningstiden.

Følgende illustrasjon viser et eksempel på valg av tidspunkt for en salgsstedsordre.

![Et eksempel på valg av tidspunkt for en salgsstedsordre](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Tidspunktvalg for e-handelsordrer

Hvis du vil ha informasjon om hvordan du gjør valg av tidspunkt tilgjengelig for e-handelsordrer, kan du se [Henteinformasjonsmodul](../pickup-info-module.md).

> [!NOTE]
> Brukere kan vise eller redigere hentetidspunkter på et Commerce-områdes utsjekkingsside bare hvis henteinformasjonsmodulen er lagt til på denne siden. Hvis utsjekkingssiden ikke inneholder henteinformasjonsmodulen, blir ordrene bestilt uten at brukere angir eller viser informasjon om tidspunkt.

Illustrasjonen nedenfor viser et eksempel på en e-handelsordre der et hentetidspunkt er valgt.

![Eksempel på en e-handelsordre der et hentetidspunkt er valgt](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Tidspunktvalg for telefonsenterordrer

I telefonsenterappen kan telefonsenteragenter velge hentebutikken eller -lokasjonen, i tillegg til en dato og et tidspunkt slik det er merket i illustrasjonen nedenfor.

![Eksempel på en telefonsenterordre der et hentetidspunkt er valgt](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Henteinformasjonsmodul](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]