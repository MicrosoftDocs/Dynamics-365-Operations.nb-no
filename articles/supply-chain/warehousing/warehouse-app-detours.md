---
title: Konfigurere omveier for trinn i menyelementer for mobilenheter
description: Dette emnet beskriver hvordan du konfigurerer omveier for menyelementer, slik at arbeidere kan endre den gjeldende oppgaven, utføre en annen oppgave og deretter gå tilbake til den opprinnelige oppgaven uten å miste noe informasjon.
author: MarkusFogelberg
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 2c53de92df1ece80f69daf0cc7a4473a2dafd0c9
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678769"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Konfigurere omveier for trinn i menyelementer for mobilenheter

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: GA with 10.0.23 -->

> [!IMPORTANT]
> Funksjonene som er beskrevet i dette emnet, gjelder bare for den nye mobilappen Warehouse Management. De påvirker ikke den gamle lagerappen, som nå er avskrevet.

Dette emnet beskriver hvordan du konfigurerer omveier for menyelementer, slik at arbeidere kan endre den gjeldende oppgaven, utføre en annen oppgave og deretter gå tilbake til den opprinnelige oppgaven uten å miste noe informasjon.

En omvei er et separat menyelement som kan åpnes fra et trinn i en hovedoppgave. På slutten av omveien returneres arbeideren til stedet der de forlot hovedoppgaven. Under konfigurasjonen angir du menyelementet som skal fungere som en omvei. Du velger også hvilke feltverdier fra hovedoppgaven som automatisk skal videresendes (kopieres) til omveien og angis der. Derfor må du forstå hvor i oppgaveflyten du vil at omveien skal være tilgjengelig for ansatte. Du må også sørge for at informasjonen som må kopieres til omveien, er tilgjengelig for det trinnet i oppgaveflyten.

## <a name="enable-detours-in-your-system"></a>Aktivere omveier i systemet

Før du kan definere omveier for trinn i menyelementer på mobilenheten, må du fullføre fremgangsmåten nedenfor for å aktivere de nødvendige funksjonene og generere de nødvendige feltnavnene i mobilappen Warehouse Management.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
1. I [**Funksjonsadministrering**-arbeidsområdet](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiverer du funksjonen som er oppført på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Trinnvise instruksjoner i lagerapp*

    Hvis du vil ha mer informasjon om funksjonen *Trinnvise instruksjoner i lagerapp*, kan du se [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](mobile-app-titles-instructions.md). Denne funksjonen er en forutsetning for funksjonen *Omveier i Warehouse Management-appen*.

1. Aktiver funksjonen som vises på følgende måte:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Omveier i Warehouse Management-appen*

    Denne funksjonen er funksjonen som er beskrevet i dette emnet.

1. Oppdater feltnavnene i mobilappen Warehouse Management ved å gå til **Lagerstyring \> Oppsett \> Mobile device \> Navn på lagerappfelt**, og velg **Opprett standardoppsett**. For mer informasjon, se [Konfigur felter for mobilappen Lagerstyring](configure-app-field-names-priorities-warehouse.md).
1. Gjenta det forrige trinnet for hver juridiske enhet (firma) der du bruker mobilappen Warehouse Management.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigurere en omvei fra en menyspesifikk overstyring

Bruk fremgangsmåten nedenfor til å definere en omvei fra en menyspesifikk overstyring.

1. Opprett en menyspesifikk overstyring for den relevante menyen og trinnet som beskrevet i [Tilpass trinntitler og instruksjoner for mobilappen Warehouse Management](mobile-app-titles-instructions.md).
1. Finn kombinasjonen av verdier for **Trinn-ID** og **Menyelementnavn** som du ønsker å redigere, og velg deretter verdien i kolonnen **Trinn-ID**.
1. I hurtigfanen **Tilgjengelige omveier (menyelementer)** på siden som vises, kan du angi menyelementet som skal fungere som en omvei. Du kan også velge hvilke feltverdier fra hovedoppgaven som automatisk skal kopieres til og fra omveien. Hvis du vil ha eksempler som viser hvordan du bruker disse innstillingene, kan du se scenarioene senere i dette emnet.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>Eksempelscenario 1: Salgsplukking der en lokasjonsforespørsler fungerer som en omvei

Dette scenariet viser hvordan du konfigurerer en lokasjonsforespørsler som en omvei i en arbeiderstyrt oppgaveflyt for salgsplukking. Denne omveien vil gjøre det mulig for arbeidere å slå opp alle nummerskilt på det stedet de plukker fra, og plukke nummerskiltet som de vil bruke til å fullføre plukkingen. Denne typen omvei kan være nyttig hvis strekkoden skades og derfor ikke kan leses av skannerenheten. Alternativt kan det være nyttig hvis en arbeider må lære hva som faktisk er tilgjengelig i systemet. Legg merke til at dette scenariet bare fungerer hvis du plukker fra nummerskiltkontrollerte lokasjoner.

### <a name="enable-sample-data"></a>Aktivere eksempeldata

Hvis du vil bruke de angitte eksempelpostene og verdiene til å arbeide deg gjennom dette scenariet, må du bruke et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Opprette en menyspesifikk overstyring og konfigurere omveien for scenario 1

I denne fremgangsmåten konfigurerer du en omvei for menyelementet **Salgsplukking** i nummerskilttrinnet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.
1. Finn trinn-IDen med navnet *LicensePlateId*, og velg det.
1. Velg **Legg til trinnkonfigurasjon** i handlingsruten.
1. I rullegardinlisten bruker du **Menyelement**-feltet til å finne og velge *Salgsplukking*.
1. Velg **OK**.
1. Detaljsiden for overstyringen som du akkurat opprettet, vises. I hurtigfanen **Tilgjengelige omveier (menyelementer)** velger du **Legg til** på verktøylinjen.
1. I dialogboksen **Legg til omvei** velger du **Lokasjonsforespørsel** som omveien som skal gjøres tilgjengelig som i mobilappen Warehouse Management.
1. Velg **OK**.
1. I hurtigfanen **Tilgjengelige omveier (menyelementer)** velger du omveiene som du akkurat la til, og velger deretter **Velg felter som skal sendes** på verktøylinjen.
1. Angi informasjonen som skal sendes til og fra omveien, i dialogboksen **Velg felter som skal sendes**. I denne situasjonen aktiverer du ansatte slik at de kan bruke lokasjonen de skal plukke fra, som inndata for lokasjonsforespørsler. I delen **Send fra salgsplukking** velger du derfor **Legg til** på verkøylinjen for å legge til en rad eller et rutenett. Angi deretter følgende verdier for den nye raden:

    - **Kopier fra salgsplukking:** *Lokasjon*
    - **Lim inn i lokasjonsforespørsel:** *Lokasjon*

1. Siden omveier i dette scenariet er konfigurert på nummerskilttrinnet, vil det være nyttig hvis arbeidere kan hente nummerskiltet fra forespørselen tilbake til hovedflyten. I delen **Hent tilbake fra lokasjonsforespørsel** velger du derfor **Legg til** på verkøylinjen for å legge til en rad eller et rutenett. Angi deretter følgende verdier for den nye raden:

    - **Kopier fra lokasjonsforespørsel:** *Nummerskilt*
    - **Lime inn i Salgsplukking:** *Nummerskilt*

1. Velg **OK**.

Omveien er nå fullstendig konfigurert. En knapp for å starte omveien **Lokasjonsforespørsel** vises nå i nummerskilttrinnet for menyelementet **Salgsplukking**.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Fullføre en salgsplukking på en mobilenhet og bruke omveien

I denne fremgangsmåten fullfører du en salgsplukking ved hjelp av mobilappen Warehouse Management. Du vil bruke omveien du nettopp konfigurerte, til å finne nummerskiltet som du vil bruke til å fullføre plukktrinnet.

1. I Microsoft Dynamics 365 Supply Chain Management oppretter du en salgsordre som krever et plukktrinn for å plukke fra en lokasjon som spores med nummerskilt. Deretter frigir du salgsordren til lageret. Noter deg arbeids-ID-en som genereres.
1. Åpne mobilappen Warehouse Management, og logg på lager 24. (I standard demodata logger du deg på ved å bruke *24* som bruker-ID og *1* som passord.)
1. Velg **Utgående**-menyen, og velg deretter menyelementet **Salgsplukking**.
1. Følg instruksjonene for dataoppføring på skjermen for å angi arbeids-IDen som ble generert i trinn 1.
1. Åpne Handlinger-menyen i trinnet som inneholder teksten **Skann et nummerskilt**. Du skal se en ny knapp kalt **Lokasjonsforespørsel**. En pil i hjørnet øverst til venstre angir at knappen vil starte en omvei. Velg **Lokasjonsforespørsel**.
1. Omveien startes. På den neste siden bekrefter du lokasjonen som ble kopiert fra hovedflyten.
1. I listen over tilgjengelige nummerskilt på stedet kan du trykke på nummerskiltet som du vil kopiere tilbake til hovedflyten. Deretter velger du **Tilbake**-knappen.
1. Du returneres til hovedflyten for salgsplukking, og nummerskiltet er kopiert tilbake til den fra omveien. Bekreft verdien for å gå videre til neste trinn.
1. Du kan nå fullføre resten av standardflyten ved å angi instruksjonene for ønsket dataregistrering.

Lagerarbeidene er nå fullført. Arbeideren åpnet en omvei for å utføre en sekundær oppgave (lokasjonsforespørsler) uten å miste plassen i hovedoppgaven, og hentet tilbake informasjonen som var nødvendig for å fullføre hovedoppgaven.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Eksempelscenario 2: Vareforespørsler med bevegelse og justeringsomveier

Dette scenariet viser hvordan du konfigurerer bevegelse og justeringer som flere omveier i oppgaveflyten for lokasjonsforespørsler. Denne funksjonen kan være nyttig i situasjoner der en arbeider ankommer et sted, finner ut at lageret på stedet er forskjellig fra det som er registrert i systemet, og derfor må justere eller flytte varer.

Du kan erstatte lokasjonsforespørselen med en forespørsel om nummerskilt eller en vareforespørsel etter behov.

### <a name="enable-sample-data"></a>Aktivere eksempeldata

Hvis du vil bruke de angitte eksempelpostene og verdiene til å arbeide deg gjennom dette scenariet, må du bruke et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Opprette en menyspesifikk overstyring og konfigurere omveien for scenario 2

I denne fremgangsmåten konfigurerer du en omvei for menyelementet **Salgsplukking** i nummerskilttrinnet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Trinn formobilenhet**.
1. Finn og velg trinn-IDen med navnet *LocationInquiryList*.

    > [!NOTE]
    > Hvis du vil bruke en vareforespørsler i stedet for en lokasjonsforespørsel, velger du en rad der trinn-IDen kalles *ItemInquiryList*. Hvis du vil bruke en forespørsel om nummerskilt, velger du en rad der trinn-IDen kalles *LPInquiryList*.

1. Velg **Legg til trinnkonfigurasjon** i handlingsruten.
1. I rullegardinlisten bruker du **Menyelement**-feltet til å finne og velge *Lokasjonsforespørsel*.
1. Velg **OK**.
1. Detaljsiden for overstyringen som du akkurat opprettet, vises. I hurtigfanen **Tilgjengelige omveier (menyelementer)** velger du **Legg til** på verktøylinjen.
1. I dialogboksen **Legg til omvei** velger du **Bevegelse** som omveien som skal gjøres tilgjengelig som i mobilappen Warehouse Management.
1. Velg **OK**.
1. I hurtigfanen **Tilgjengelige omveier (menyelementer)** velger du omveiene som du akkurat la til, og velger deretter **Velg felter som skal sendes** på verktøylinjen.
1. Angi informasjonen som skal sendes til og fra omveien, i dialogboksen **Velg felter som skal sendes**. I dette scenariet forventer du at arbeidere skal lete etter nummerskiltkontrollerte lokasjoner. Derfor vil det være nyttig å kopiere nummerskiltet fra forespørselen til **Bevegelse-**-omveien. I delen **Send fra salgsplukking** velger du **Legg til** på verkøylinjen for å legge til en rad eller et rutenett. Angi deretter følgende verdier for den nye raden:

    - **Kopier fra lokasjonsforespørsel:** *Lokasjon*
    - **Lim inn i bevegelse:** *Loc / LP*

    I denne omveien forventer du ikke at det skal kopieres informasjon tilbake, fordi hovedflyten var en forespørsel der det ikke kreves flere trinn.

1. Velg **OK**.

Omveien er nå fullstendig konfigurert. En knapp for å starte omveien **Bevegelse** vises nå i nummerskilttrinnet for menyelementet **Lokasjonsforespørsel**.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Gjør en lokasjonsforespørsel på en mobilenhet og bruk omveien

I denne fremgangsmåten fullfører du en lokasjonsforespørsel ved hjelp av mobilappen Warehouse Management. Du vil deretter bruke omveien til å fullføre en varebevegelse.

1. Åpne mobilappen Warehouse Management, og logg på lager 24. (I standard demodata logger du deg på ved å bruke *24* som bruker-ID og *1* som passord.)
1. Velg **Lager**-menyen, og velg deretter menyelementet **Lokasjonsforespørsel**.
1. Angi en lokasjon du vil forespørre om, for eksempel *FL-001*.
1. Når listen vises, trykker du og holder på ett av kortene i den for å vise tilgjengelige omveier.
1. Velg **Bevegelse**.
1. Legg merke til at nummerskiltet er kopiert fra kortet du valgte. Bekreft verdien.
1. Du kan nå følge den standard oppgaveflyten for å fullføre bevegelsen. Når arbeidet er fullført, åpner du Handlinger-menyen og velger **Avbryt**.
1. Du returneres til **Lokasjonsforespørsel**-siden. Legg merke til at verdiene ikke oppdateres automatisk. Derfor må du manuelt oppdatere siden for å se endringene fra bevegelsesomveien.
