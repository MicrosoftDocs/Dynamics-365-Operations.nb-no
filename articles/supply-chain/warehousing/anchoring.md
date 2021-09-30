---
title: Forankring
description: Dette emnet beskriver hvordan du aktiverer og bruker forankring.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a17574cccbdf6f26f0453bda67eabaa16d559cd3
ms.sourcegitcommit: 99bde425ade701ef244c6bca6d411aef94a59b3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/20/2021
ms.locfileid: "7505592"
---
# <a name="anchoring"></a>Forankring

[!include [banner](../includes/banner.md)]

Dette emnet inneholder detaljer om forankringsprosessen. Den beskriver konfigurasjonen som kreves, og logikken som kjøres når en lagerarbeider endrer enten oppsamlingslokasjonen eller lastingslokasjonen.

Ved hjelp av forankringsfunksjonen kan du overstyre oppsamlings- eller lastelokasjonen. Alle åpne plasser sendes deretter til den nye oppsamlings- eller innlastingslokasjonen du angir.

Denne funksjonen kan hjelpe arbeidere med å være mer effektive mens de sender varer. Her er noen eksempler:

- En arbeider som må plassere varene for ordre 1 på en oppsamlingslokasjon ved sone 1, kan ikke fullføre denne operasjonen fordi en tidligere last ikke er fjernet fra lokasjonen. I stedet for å vente på at oppsamlingslokasjonen ved sone 1 blir tilgjengelig, bestemmer arbeideren å bruke oppsamlingslokasjonen ved sone 2. Arbeideren overstyrer derfor den foreslåtte oppsamlingslokasjonen. Plasseringslokasjonen hvor alle de andre elementene for arbeidet oppdateres deretter til oppsamlingslokasjonen for sone 2.
- En arbeider som må utføre flere plukkinger for samme levering, kan være sikker på at alle plasserte varer er satt sammen på samme sted. Derfor kreves det mindre tid å laste varene inn i trucken.

Du konfigurerer forankring for menyelementer for mobilenhet ved hjelp av alternativet **Forankring**. Hvis du angir dette alternativet til *Ja*, kan du bruke feltet **Forankre etter** til å angi om du vil forankre etter forsendelse eller last. Hvis du setter Feltet **Forankring etter** til *Forsendelse*, endres etterfølgende åpne plasseringer til den nye lokasjonen for denne forsendelsen. Hvis du setter det til *Last*, endres etterfølgende åpne plasseringer til den nye lokasjonen for denne lasten.

> [!IMPORTANT]
> Lokasjonen for etterfølgende åpne plasser endres bare på arbeidslinjene som genereres fra samme arbeidsmallinje. Systemet vil med andre ord forankre plasseringslinjene som stammer fra samme arbeidsmallinje.

Dette emnet gir et scenario som viser hvordan forankring fungerer. I løpet av scenarioet kan du opprette et sett med salgsordrer og frigi dem til lageret. Du vil deretter overstyre den foreslåtte oppsamlingslokasjonen og kontrollere at alt gjenværende plasseringsarbeid sendes til den nye lokasjonen.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Forutsetning for scenario: Gjør demodata tilgjengelige

 i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til *USMF* før du begynner.

## <a name="scenario-setup"></a>Scenariooppsett

Før du arbeider deg gjennom eksempelscenarioet, må du aktivere forankring for både det aktuelle menyelementet for mobil enhet.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Definere et menyelement for mobilenhet for å aktivere forankring

Følg denne fremgangsmåten for å aktivere forankring for et menyelement for en mobilenhet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg posten som heter *Salgsplukking*, i listeruten. Hvis ingen eksisterende poster har dette navnet, oppretter du det. Bekreft eller angi følgende verdier for posten:

    - **Navn på menyelement:** *Salgsplukking*
    - **Tittel:** *Salgsplukking*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*
    - **Styrt av:** *Brukerstyrt*
    - **Forankring:** *Ja*

        Denne innstillingen gjør at systemet forankrer flere arbeidsordrelinjer sammen under salgsplukkingen.

    - **Forankring etter:** *Last*

        Denne innstillingen fører til at systemet forankres etter last.

    - **Overstyr målnummerskilt:** *Ja*
    - **Overstyr nummerskiltet under plassering:** *Ja*
    - **Hold arbeidet låst av brukeren:** *Ja*
    - **Tillat overplukking:** *Ja*

### <a name="set-up-a-work-template-to-enable-staging"></a>Definere en arbeidsmal for å aktivere oppsamling

Følg denne fremgangsmåten for å konfigurere en arbeidsmal for å aktivere oppsamling. Denne konfigurasjonen støtter et scenario der en arbeider plasserer varer for en ordre på en oppsamlingslokasjon.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Velg *Salgsordrer* i feltet **Arbeidsordretype**.
1. Velg **61 SO Stadium**-arbeidsmalen i rutenettet.
1. I delen **Arbeidsmaldetaljer** kontrollerer du at følgende linjer finnes og er konfigurert som vist her:

    - Linje 1:

        - **Arbeidstype:** *Plukk*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Arbeidsklasse-ID:** *Salgsordreplukking*

    - Linje 2:

        - **Arbeidstype:** *Plasser*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Direktivkode:** *Stadium*
        - **Arbeidsklasse-ID:** *Salgsordreplukking*

    - Linje 3:

        - **Arbeidstype:** *Plukk*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Stopp arbeid:** *Ja*
        - **Arbeidsklasse-ID:** *Salgsordrelast*

    - Linje 4:

        - **Arbeidstype:** *Plasser*
        - **Obligatorisk:** Valgt (= *Ja*)
        - **Direktivkode:** *Rampedør*
        - **Arbeidsklasse-ID:** *Salgsordrelast*

1. I handlingsruten velger du **Rediger spørring** for å åpne redigeringsprogrammet.
1. I **Område**-fanen kontrollerer du at følgende linje er til stede:

    - **Tabell:** *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
    - **Felt:** *Lager*
    - **Kriterier:** *61*

1. I **Sortering**-fanen kontrollerer du at følgende linje er til stede:

    - **Tabell:** *Midlertidige arbeidstransaksjoner*
    - **Avledet tabell:** *Midlertidige arbeidstransaksjoner*
    - **Felt:** *Leverings-ID*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å bruke innstillingene og lukke redigeringsprogrammet for spørring. Godta endringene hvis du blir bedt om å gjøre det.
1. Velg **Arbeidshodeskift** i handlingsruten.
1. I linjen der **Feltnavn**-feltet er satt til *Forsendelses-ID*, må du kontrollere at avmerkingsboksen **Grupper etter dette feltet** er valgt.

### <a name="set-up-license-plates-locations-and-inventory"></a>Konfigurere nummerskilter, lokasjoner og beholdning

Før du oppretter salgsordrer og forsendelser, må du sørge for at de påkrevde lokasjoner, nummerskilt og beholdninger finnes.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Nummerskilt**, og opprett to nummerskilt:

    - MyLP1
    - MyLP2

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**, og opprett følgende lokasjoner hvis de ikke allerede finnes.

    | Lager | Lokasjon   | Profil-ID for lokasjon | Sone-ID   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PLUKK-06             | GULV     |
    | 61        | 06A01R3S1B | PLUKK-06             | GULV     |
    | 61        | STADIUM01    | STADIUM               | *(Tom)* |
    | 61        | STADIUM02    | STADIUM               | *(Tom)* |
    | 61        | STADIUM03    | STADIUM               | *(Tom)* |
    | 61        | STADIUM04    | STADIUM               | *(Tom)* |

1. Kontroller at følgende beholdning er tilgjengelig. Hvis du må justere beholdninge, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt.

    | Varenummer | Antall | Lager | Lokasjon   | Nummerskilt |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Opprette behov

Før du kan prøve forankringsfunksjonaliteten må du opprette behov. I dette scenariet oppretter du tre salgsordrer for den samme kunden.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette den første salgsordren.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-001*
    - **Lager:** *61*

1. Velg **OK**.
1. Den nye salgsordren åpnes. Det inneholder en tom linje på **Salgsordrelinjer**-hurtigfanen. Angi følgende verdier for denne linjen:

    - **Varenummer:** *A0001*
    - **Antall:** *1*

1. På verktøylinjen velger du **Legg til linje** for å legge til en ny salgsordrelinje, og angi deretter følgende verdier for den:

    - **Varenummer:** *A0002*
    - **Antall:** *1*

1. Følg disse trinnene for hver salgslinje i ordren for å reservere lager for den:

    1. På hurtigfanen **Salgsordrelinjer** velger du en salgsordrelinje.
    1. Velg **Lager \> Reservasjon** på verktøylinjen.
    1. På **Reservasjon**-siden velger du **Reserver parti**, og deretter lukker du siden.
    1. Velg **Lagre** i handlingsruten.

1. Gjenta trinn 2 til og med 6 for å opprette en ny salgsordre. Angi følgende verdier for den:

    - I dialogboksen **Opprett salgsordre**:

        - **Kundekonto:** *US-001*
        - **Lager:** *61*

    - På salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *2*

    - På salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *2*

1. Gjenta trinn 7 for å reservere hver linje i salgsordre 2.
1. Gjenta trinn 2 til og med 6 for å opprette en tredje salgsordre. Angi følgende verdier for den:

    - I dialogboksen **Opprett salgsordre**:

        - **Kundekonto:** *US-001*
        - **Lager:** *61*

    - På salgsordrelinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *3*

    - På salgsordrelinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *3*

1. Gjenta trinn 7 for å reservere hver linje i salgsordre 3.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Bruk arbeidsområde for lastplanlegging til å opprette en last og frigi den til lageret

Følg disse trinnene for å opprette en last for ordrene du opprettet for dette scenarioet, og frigi det deretter til lageret.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I kategorien **Salgslinjer** finner og velger du alle salgsordrelinjene for salgsordre 1 og salgsordre 2.
1. I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**.
1. I dialogboksen **Tilordning av lastmal** velger du en lastmal i feltet **Lastmal-ID**, for eksempel *Standard lastmal*.
1. Velg **OK** for å lukke dialogboksen.
1. I delen **Laster** finner og velger du lasten du opprettet.
1. På verktøylinjen velger du **Frigivelse \> Frigi til lager**.
1. I dialogboksen **Frigi last til lager** velger du **OK** for å frigi den valgte lasten til lageret.
1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid** for å vise arbeidet som ble opprettet. Du bør finne to nye arbeids-IDer, én for hver forsendelse. Hver arbeids-ID har plukk- og plasseringslinjer som henter lager fra plukklokasjonene til oppsamlingslokasjonen og fra oppsamlingslokasjonen til rampedøren. Noter **Arbeids-ID**-verdien for den første forsendelsen, fordi du kommer til å få behov for den i neste fremgangsmåte.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Salgsordreplukking til oppsamlingslokasjonen for den første forsendelsen

1. Logg på mobilappen Warehouse Management som en arbeider som er aktivert i lager *61*. (I standard demodata kan du logge deg på ved å bruke _61_ som bruker-ID og _1_ som passord.)
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Salgsplukking**.
1. Velg **ID**-feltet, og angi deretter arbeids-IDen for den første forsendelsen.
1. Bekreft oppføringen.
1. I **LP**-feltet angir du et skiltnummer for den første varen (*MyLP1*).
1. Bekreft oppføringen.
1. I **Mål-LP**-feltet angir du et hvilket som helst tall (målnummerskilt behøver ikke å eksistere allerede).

    Du vil plukke alle linjer som ble opprettet fra den behandlede bølgen, til samme mållisensplate.

1. Bekreft oppføringen.
1. I **LP**-feltet angir du et skiltnummer for den andre varen (*MyLP2*).
1. Bekreft oppføringen.

    Forestill deg at arbeideren nå har samlet inn ordren, men når de kommer til oppsamlingslokasjonen som er angitt i arbeidet, finner de ut at området allerede er opptatt. Arbeideren kan imidlertid se at en annen lokasjon i nærheten (*STADIUM03*) er tilgjengelig. Derfor vil de be om å endre oppsamlingslokasjonen. Fordi forankringsfunksjonen er aktivert, vil systemet automatisk oppdatere oppsamlingsstedet for dette og alt relatert arbeid.

1. Velg **Overstyr plassering** for å overstyre den foreslåtte oppsamlingslokasjonen.
1. Angi **Oppsamlingsfelt er endret** i feltet *Arbeidsunntak*.
1. I **Lokasjon**-feltet angir du en ny oppsamlingslokasjon (*STADIUM03*).
1. Bekreft oppføringen. Du mottar en Arbeid fullført-melding.
1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid**.
1. Åpne arbeids-IDen for den første forsendelsen. Kontroller at oppsamlingslokasjonen ble oppdatert til den nye lokasjonen (*STADIUM03*) som ble definert ved hjelp av mobilenheten.
1. Åpne arbeids-IDen for den andre forsendelsen. Kontroller at oppsamlingslokasjonen ble oppdatert til ny oppsamlingslokasjon (*STADIUM03*) på grunn av forankringsoppsettet.

> [!NOTE]
> Lokasjonen for alle gjenværende åpne arbeidslinjer som har samme oppsamlingslokasjon, og som ble generert fra samme arbeidsmallinje, vil bli oppdatert til den nye lokasjonen.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Bruk arbeidsområdet for lastplanlegging til å legge til den nye salgsordren i den eksisterende belastningen

Følg denne fremgangsmåten for å legge til en ordre i belastningen, og deretter frigi den til lageret.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I kategorien **Salgslinjer** finner og velger du alle salgsordrelinjene for salgsordre 3.
1. I handlingsruten i fanen **Forsyning og behov** i gruppen **Legg til** velger du **Til eksisterende last** for å legge til de valgte ordrelinjene i en eksisterende last.
1. Velg **OK** for å lukke dialogboksen.
1. I delen **Laster** finner og velger du lasten fra de forrige trinnene.
1. Velg **Frigivelse \> Frigi til lager**.
1. I dialogboksen **Frigi last til lager** velger du **OK** for å frigi den valgte lasten til lageret.
1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid** for å vise arbeidet som ble opprettet. Noter verdien for **Arbeids-ID**, fordi du kommer til å få behov for den i neste fremgangsmåte.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Salgsordreplukking til oppsamlingslokasjonen for den tredje forsendelsen

1. Logg på mobilappen som en arbeider i lageret *61*.
1. I hovedmenyen velger du **Utgående**.
1. I **Utgående**-menyen velger du **Salgsplukking**.
1. Velg **ID**-feltet, og angi deretter arbeids-IDen for den tredje forsendelsen.
1. Bekreft oppføringen.
1. I **LP**-feltet angir du et skiltnummer for den første varen (*MyLP1*).
1. Bekreft oppføringen.
1. I **Mål-LP**-feltet angir du et hvilket som helst tall (målnummerskilt behøver ikke å eksistere allerede).
1. Bekreft oppføringen.
1. I **LP**-feltet angir du et skiltnummer for den andre varen (*MyLP2*).
1. Bekreft oppføringen.

    Som for første belastning kan du tenke deg at arbeideren finner ut at den angitte oppsamlingslokasjonsforløpet ikke er tilgjengelig. Derfor ønsker de å bruke en annen oppsamlingslokasjon (*STADIUM04)*.

1. Velg **Overstyr plassering** for å overstyre den foreslåtte oppsamlingslokasjonen.
1. Angi **Oppsamlingsfelt er endret** i feltet *Arbeidsunntak*.
1. I **Lokasjon**-feltet angir du en ny oppsamlingslokasjon (*STADIUM04*).
1. Bekreft oppføringen. Du mottar en Arbeid fullført-melding.
1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid**.
1. Åpne arbeids-IDen for den første forsendelsen. Kontroller at oppsamlingslokasjonen ikke er oppdatert til den nye oppsamlingslokasjonen (*STADIUM04*), fordi den gjenværende åpne plasser-linjen ikke samsvarer med arbeidsmallinjen til den fullførte oppsamlingslinjen.
1. Åpne arbeids-IDen for den andre forsendelsen. Kontroller at oppsamlingslokasjonen ikke er oppdatert til den nye oppsamlingslokasjonen (*STADIUM04*), fordi oppsamlingslokasjonen ikke samsvarer med oppsamlingslokasjonen for den fullførte oppsamlingslinjen. Den fullførte arbeidslinjen og den gjenværende åpne arbeidslinjen har med andre ord ulike oppsamlingslokasjoner, og i dette tilfellet oppdateres bare linjer som har samme oppsamlingslokasjoner.
1. Åpne arbeids-IDen for den tredje forsendelsen. Kontroller at oppsamlingslokasjonen ble oppdatert til den nye oppsamlingslokasjonen (*STADIUM04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
