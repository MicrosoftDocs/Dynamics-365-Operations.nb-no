---
title: Planlagt direkteoverføring
description: Denne artikkelen beskriver avansert, planlagt direkteoverføring, hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde. All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: b530cc1403458775fd330e826a32417d3b03bf25
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334573"
---
# <a name="planned-cross-docking"></a>Planlagt direkteoverføring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver avansert, planlagt direkteoverføring. Planlagt direkteoverføring er en lagerprosess hvor lagerantallet som kreves for en ordre, blir dirigert rett fra mottak eller oppretting til riktig utleveringsport eller oppstillingsområde. All gjenværende beholdning fra den inngående kilden dirigeres til den riktige lagringslokasjonen via den vanlige plasseringsprosessen.

Direkteoverføring la arbeiderne hoppe over den inngående plasseringen og utgående plukking av lageret som allerede er merket for en utgående ordre. Derfor reduseres antall ganger beholdningen berøres, der det er mulig. Fordi det i tillegg er mindre samhandling med systemet, økes tids- og plassbesparelsene på lageret.

Før du kan kjøre direkteoverføring, må du konfigurere en ny direkteoverføringsmal der forsyningskilden og andre sett med krav for direkteoverføring er angitt. Når den utgående ordren opprettes, må linjen merkes mot en inngående ordre som inneholder den samme varen. Du kan velge direktivkodefeltet i malen for direkteoverføring, på samme måte som du oppretter etterfylling og bestillinger.

På tidspunktet for mottak av inngående ordre, identifiserer direkteoverføringsoppsettet automatisk behovet for direkteoverføring og oppretter bevegelsesarbeidet for det nødvendige antallet, basert på oppsettet til lokasjonsdirektivet.

> [!NOTE]
> Lagertransaksjoner avregistreres *ikke* når direkteoverføringsarbeid blir avbrutt, selv om innstillingen for denne funksjonen er aktivert i lagestyringsparametere.

## <a name="turn-on-the-planned-cross-docking-features"></a>Aktivere funksjonene for planlagt direkteoverføring

Hvis du kjører Supply Chain Management, versjon 10.0.28 eller tidligere, kan det hende at du må aktivere planlagt direkteoverføring før du kan bruke den. Gå til [Funksjonsadministrering](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktiver følgende funksjoner i følgende rekkefølge:

1. *Planlagt direkteoverføring*<br>(Denne funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres.)
1. *Kryssoverføringsmaler med lokasjonsdirektiver*<br>(Per Supply Chain Management versjon 10.0.29 er denne funksjonen aktivert som standard.)
    > [!NOTE]
    > Ved hjelp av denne funksjonen kan **Direktivkode**-feltet angis i malen for direkteoverføring, på samme måte som du oppretter etterfyllingsmaler. Hvis du aktiverer denne funksjonen, kan du legge til en direktivkode på arbeidsmallinjene for direkteoverføring for den endelige *Plasser*-linjen. Dette sikrer at den endelige plasseringslokasjonen kan bestemmes under oppretting av arbeidsprosesser før du vurderer arbeidsmaler.

## <a name="setup"></a>Installasjon

### <a name="regenerate-load-posting-methods"></a>Generer lastposteringsmetoder på nytt

Planlagt direkteoverføring er implementert som en lastposteringsmetode. Når du har aktivert funksjonen, må du generere metodene på nytt.

1. Gå til **Lagerstyring \> Oppsett \> Lastposteringsmetoder**.
1. Velg **Regenerer metoder** i handlingsruten.

    Når regenereringen er fullført, skal det vises en metode som har **Metodenavn**-verdien *planCrossDocking*.

1. Lukk siden.

### <a name="create-a-cross-docking-template"></a>Opprett en direkteoverføringsmal

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Direkteoverføringsmaler**.
1. I handlingsruten velger du **Ny** for å opprette en mal.
1. I hodet angir du følgende verdier:

    - **Sekvens:** *1*

        Dette feltet definerer rekkefølgen malene skal evalueres i.

    - **ID for direkteoverføringsmal:** *51*
    - **Beskrivelse:** *Lager 51*
    - **Policy for behovsfrigivelse:** *Før forsyningsmottak*
    - **Lager:** *51*

1. Oppsettet på **Planlegging**-hurtigfanen styrer hvordan malen fungerer. Angi følgende verdier:

    - **Behovskrav:** *Ingen*

        Dette feltet definerer kravene til behovslageret. Hvis behovet må kobles til forsyningen før frigivelse, velger du *Merking*. Hvis behovet må være ordrereservert mot forsyningen før frigivelse, velger *Ordrereservering*.

    - **Lokaliseringstype:** *Forsendelseslokasjoner*

        Dette feltet definerer om direkteoverføringsarbeidet skal bruke oppsamling/lastlokasjoner fra forsendelsen, eller om det skal bruke lokasjonsdirektiver til å finne egne oppsamling/lastlokasjoner.

    - **Arbeidsmal:** La dette feltet stå tomt.

        Dette feltet definerer arbeidsmalen som skal brukes når du oppretter direkteoverføringsarbeid.

    - **Ny validering ved forsyningsmottak:** *Nei*

        Dette alternativet angir om forsyningen skal valideres på nytt under mottak. Hvis dette alternativet er satt til *Ja*, kontrolleres både vinduet maksimal tid og området for utløpsdager.

    - **Direktivkode:** La dette feltet stå tomt

        Dette alternativet aktiveres av malen for direkteoverføring med funksjonen *Kryssoverføringsmaler med lokasjonsdirektiver* (i Supply Chain Management, versjon 10.0.29 er funksjonen aktivert som standard). Systemet bruker lokasjonsdirektiver til å bidra til å finne den beste lokasjonen å flytte lageret for direkteoverføring til. Du kan definere alternativet ved å tilordne en direktivkode til hver relevante direkteoverføringsmal. Hvis en direktivkode er angitt, søker systemet etter lokasjonsdirektiver per direktivkode når arbeid må genereres. På denne måten kan du begrense lokasjonsdirektiver som brukes for en bestemt direkteoverføringsmal.

    - **Validerer tidsvindu:** *Ja*

        Dette alternativet angir om maksimalt tidsvindu skal evalueres når en forsyningskilde velges. Hvis dette alternativet er satt til *Ja*, blir feltene som er relatert til maksimale og minimale tidsvinduer, tilgjengelige.

    - **Maksimalt tidsvindu:** *5*

        Dette feltet definerer maksimal periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.

    - **Enhet for maksimalt tidsvindu:** *Dager*
    - **Minimum tidsvindu** *0*

        Dette feltet definerer minimum periode som er tillatt mellom forsyningsmottak og etterspørselsavreise.

    - **Enhet for minimum tidsvindu:** *Dager*
    - **Utløpsområde (dager):** *0*

        *FEFO-kriterier:* Dette feltet definerer det maksimale antallet dager mellom utløpsdatoen til det første utløpte partiet som for øyeblikket er i lageret, og partiet som mottas.

1. I **Forsyningskilder**-hurtigfanen angir du hvilke typer forsyning som er gyldige for denne malen. Velg **Ny**, og angi deretter følgende verdier:

    - **Sekvensnummer:** *1*
    - **Forsyningskilde:** *Bestilling*

> [!NOTE]
> Du kan definere en spørring til å kontrollere når en bestemt direkteoverføringsmal brukes. Spørringen for maler for direkteoverføring har bare *InventTable*-tabellen (varer) og den internkoblede *WHSInventTable-tabellen* (WMS-varer). Hvis du vil legge til andre tabeller i spørringen, kan du koble dem sammen ved bare å bruke *eksisterende koblinger* eller *ikke-eksisterende koblinger*. Når du filtrerer på de sammenføyde tabellene, blir det hentet en post fra hovedtabellen for hver samsvarende post i den sammenføyde tabellen. Hvis koblingstypen er *kobling finnes*, avsluttes søket etter at det første samsvaret er funnet. Hvis du for eksempel deltar i salgsordrelinjetabellen til varetabellen, validerer og returnerer systemet varer der minst én salgsordrelinje har den definerte betingelsen. I utgangspunktet hentes dataene fra den overordnede tabellen (varer), ikke fra den underordnede tabellen (salgsordrelinje). Derfor kan du ikke filtrere etter kildedokumenter, for eksempel salgsordrelinjer eller kunder, med en gang.

### <a name="create-a-work-class"></a>Opprette en arbeidsklasse

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. I handlingsruten velger du **Ny** for å opprette en arbeidsklasse.
1. Angi følgende verdier:

    - **Arbeidsklasse-ID:** *CrossDock*
    - **Beskrivelse:** *Direkteoverføring*
    - **Arbeidsordretype:** *Direkteoverføring*

### <a name="create-a-work-template"></a>Opprette en arbeidsmal

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Angi *Direkteoverføring* i feltet **Arbeidsordretype**.
1. I handlingsruten velger du **Ny** for å legge til en linje i **Oversikt**-fanen.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** *1*
    - **Arbeidsmal:** *51 Direkteoverføring*
    - **Arbeidsmalbeskrivelse:** *51 Direkteoverføring*

1. Velg **Lagre** for å gjøre **Arbeidsmaldetaljer**-hurtigfanen tilgjengelig.
1. På **Arbeidsmaldetaljer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Arbeidstype:** *Plukk*
    - **Arbeidsklasse-ID:** *CrossDock*

1. Velg **Ny** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Arbeidstype:** *Plasser*
    - **Arbeidsklasse-ID:** *CrossDock*

1. Velg **Lagre**, og Bekreft at det er merket av for **Gyldig** for *51 Direkteoverføring*-malen.
1. Valgfritt: Velg **Rediger spørring** hvis du vil angi kriterier som skal bestemme når og hvor arbeidsmalen skal brukes.

    Du kan definere en spørring til å kontrollere når en bestemt arbeidsmal brukes. Du kan for eksempel angi at en mal bare kan brukes for arbeid på et bestemt sted. Hvis du vil at arbeidsmalen for direkteoverføring skal brukes på en bestemt lokasjon, må du filtrere på **Start lokasjon**-feltet, ikke **Lokasjon**-feltet, fordi arbeidsoppretting for de innkommende prosessene (innkjøp, direkteoverføring og etterfylling) starter fra plasseringslinjen. Når arbeid opprettes, setter lokasjonsdirektivet **Lokasjon**-feltet til plasseringslokasjonen. Plukklokasjonen lagres imidlertid i **Startlokasjon**-feltet.

> [!NOTE]
> Arbeidsklasse-ID-en for *Plukk*- og *Plasser*-arbeidstypene må være like.

### <a name="create-location-directives"></a>Opprette lokasjonsdirektiver

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten setter du **Arbeidsordretype**-feltet til *Direkteoverføring*.
1. Velg **Ny** i handlingsruten, og angi følgende verdier:

    - **Sekvensnummer:** *1*
    - **Navn:** *51 Direkteoverføringsplass*
    - **Arbeidstype:** *Plasser*
    - **Område:** *5*
    - **Lager:** *51*

1. Velg **Lagre** for å gjøre **Linjer**-hurtigfanen tilgjengelig.
1. På **Linjer**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Fra-antall:** *1*
    - **Til-antall:** *1000000*

1. Velg **Lagre** for å gjøre **Lokasjonsdirektivhandlinger**-hurtigfanen tilgjengelig.
1. På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Navn:** *Rampedør*
    - **Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*

1. Velg **Lagre** for å gjøre **Rediger spørring**-knappen på **Lokasjonsdirektivhandlinger**-verktøylinjen tilgjengelig.
1. Velg **Rediger spørring** for å åpne redigeringsprogrammet for spørring.
1. I **Område**-fanen kontrollerer du at følgende to linjer er konfigurert:

    - Linje 1:

        - **Tabell:** *Plasseringer*
        - **Avledet tabell:** *Lokasjoner*
        - **Felt:** *Lager*
        - **Kriterier:** *51*

    - Linje 2:

        - **Tabell:** *Plasseringer*
        - **Avledet tabell:** *Lokasjoner*
        - **Felt:** *Lokasjon*
        - **Kriterier:** *Rampedør*

1. Velg **OK** for å lukke redigeringsprogrammet for spørring.

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. I listen over menyelementer i venstre rute velger du **Kjøpsplassering**.
1. Velg **Rediger**.
1. På **Arbeidsklasser**-hurtigfanen velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Arbeidsklasse-ID:** *CrossDock*
    - **Arbeidsordretype:** *Direkteoverføring*

1. Velg **Lagre**.

## <a name="scenario"></a>Scenario

### <a name="create-a-purchase-order"></a>Opprette en bestilling

Følg disse trinnene for å opprette en bestilling som en forsyningskilde.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett bestilling**-dialogboksen angir du følgende verdier:

    - **Leverandørkonto:** *104*
    - **Lager:** *51*

1. Velg **OK** og noter deg ordrenummeret.
1. Det legges til en ny linje i rutenettet på **Bestillingslinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *5*

### <a name="create-a-sales-order"></a>Opprette en salgsordre

Følg disse trinnene for å opprette en salgsordre som en behovskilde.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-002*
    - **Lager:** *51*

1. Velg **OK**.
1. Det legges til en ny linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *3*

### <a name="create-planned-cross-docking"></a>Opprett planlagt direkteoverføring

Følg disse trinnene for å opprette den planlagte direkteoverføringen fra salgsordren.

1. På **Salgsordredetaljer**-siden for salgsordren du nettopp opprettet, velger du **Frigi til lager** i handlingsruten på **Lager**-fanen i **Handlinger**-gruppen.

    Frigi til lager-handling oppretter en forsendelse og lastlinje for salgsordrelinjen, og prøver å tildele beholdning.
    
    Du får en informasjonsmelding. Du får også følgende advarsel: Ikke no arbeid ble opprettet for bølge XXXX. Se loggen over oppretting av arbeid for detaljer. Denne virkemåten forventes fordi det ikke er noe beholdning i lageret.

1. På **Salgsordrelinjer**-fanen, på **Lager**-menyen, velger du **Forsendelsesdetaljer**.

    **Forsendelsesdetaljer**-siden vises og viser forsendelsen som ble opprettet for salgsordren.

1. I **Lastlinjer**-hurtigfanen legger du merke til at feltet **Planlagt direkteoverføringsantall** er satt til *3*. Fordi det ikke var noe beholdning tilgjengelig på lageret, men en gyldig forsyningskilde vil bli mottatt i tidsvinduet som er definert i direkteoverføringsmalen, ble direkteoverføringsantallet opprettet.
1. I **Lastlinjer**-hurtigfanen velger du **Planlagt direkteoverføring** for å vise detaljene for direkteoverføringen som ble opprettet.

## <a name="process-the-cross-docking"></a>Behandle direkteoverføringen

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Bestilling mottatt på lagermobilappen

Systemet vil motta antallet på 5 fra bestillingen til mottakslokasjonen og opprette to arbeidsdeler.

Den første arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Direkteoverføring* og er koblet til salgsordren. Den har et antall på 3 og dirigeres til den endelige forsendelseslokasjonen, slik at den kan sendes umiddelbart.

Den andre arbeids-ID-en som opprettes, har **Arbeidsordretype**-verdien *Bestillinger* og er koblet til bestillingen. Den har gjenstående antall på 2 som ikke ble direkteoverført, og som sendes til plassering for lageret.

1. Logg på mobilenheten som en bruker i lageret *51*.
1. Gå til **Inngående \> Kjøpsmottak**.
1. I **PONum**-feltet angir du bestillingsnummeret.
1. I feltet **Antall** angi *5*.
1. Velg **OK**.
1. På neste side angir du **Vare**-feltet til *A0001*.
1. Velg **OK**.
1. På neste side kontrollerer du verdiene for **PONum**, **Vare** og **Antall** ved å velge **OK**.

    Du mottar en Arbeid fullført-melding.

1. Velg **Avbryt** for å avslutte.

### <a name="put-away-to-cross-docking-and-bulk"></a>Plassering til direkteoverføring og bulk

For øyeblikket har begge arbeids-ID-ene samme målnummerskilt. Hvis du vil fullføre de neste trinnene, må du hente arbeids-ID-en og målnummerskilt-ID-en. Du kan få denne informasjonen fra arbeidsdetaljene for bestillingslinjen og salgsordrelinjen. Du kan også gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer** og filtrere arbeid der **Lager**-verdien er *51*.

1. Gå til **Inngående \> Kjøpsplassering** på den mobile enheten, og angi målnummerskiltet fra arbeidet.
1. I **ID**-feltet angir du målnummerskilt-ID-en fra arbeidsdetaljene.

    Direkteoverføringsplukking-siden viser plukklokasjonen (*RECV*), målnummerskiltet (*nummerskilt*), vare (*A0001*) og antall (*3*).

1. Velg **OK**.
1. I feltet **mål-LP** angir du et målnummerskilt for nummerskilt-ID-en som skal plasseres (direkteoverføres) til forsendelsesstedet. Du kan velge en hvilken som helst nummerskilt-ID.
1. Velg **OK**.
1. På den neste siden angir du nummerskilt-ID-en i **ID**-feltet.
1. Velg **OK**.
1. Bekreft arbeidet for plukking av det gjenstående antallet på 2, og velg deretter **OK**.
1. På den neste siden velger du **Fullført** for å avslutte plukkprosessen og begynne plasseringsprosessen.

    Mobilappen presenterer lokasjonen og nummerskiltet som varen skal plasseres i.

1. Bekreft masselagringen **Plasser** ved å velge **OK**.
1. Bekreft direkteoverføringen **Plasser** på neste side ved å velge **OK**.

    Du mottar en Arbeid fullført-melding.

1. Velg **Avbryt** for å avslutte.

Illustrasjonen nedenfor viser hvordan det fullførte direkteoverføringsarbeidet kan vises i Microsoft Dynamics 365 Supply Chain Management.

![Direkteoverføringsarbeid fullført.](media/PlannedCrossDockingWork.png "Direkteoverføringsarbeid fullført")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
