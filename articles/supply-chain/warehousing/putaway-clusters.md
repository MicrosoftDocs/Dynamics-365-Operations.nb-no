---
title: Plasseringsgrupper
description: Plasseringsgrupper tilbyr en måte for å plukke flere nummerskilter samtidig og deretter ta dem med for plassering på forskjellige steder. De kan være veldig nyttige for detaljhandelsfirmaer, der nummerskilter vanligvis ikke er fulle paller med lager.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5552959068d109bffe32b8074666bcd63b57183a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228447"
---
# <a name="putaway-clusters"></a>Plasseringsgrupper

[!include [banner](../includes/banner.md)]

Plasseringsgrupper tilbyr en måte for å plukke flere nummerskilter samtidig og deretter ta dem med for plassering på forskjellige steder. Denne prosessen blir ofte referert til som en *melkerute*. Plasseringsgrupper kan være veldig nyttige for detaljhandelsfirmaer, der nummerskilter vanligvis ikke er fulle paller med lager. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Aktiver gruppeplasseringsfunksjonen

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Gruppeplasseringsfunksjon*

## <a name="setup-for-the-example-scenario"></a>Konfigurer for eksempelscenarioet

### <a name="cluster-profiles"></a>Gruppeprofiler

Plasseringsgruppeprofilen avgjør hvor en vare skal plasseres, basert på lokasjonen som er tilordnet varen på mottakstidspunktet. Hvis det kreves forskjellige grupper, bør det opprettes andre plasseringsgrupper, én for hvert menyelement for mobilenhet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.
1. Velg **Ny** i handlingsruten.
1. I **Hode**-visning angir du følgende verdier:

    - **ID for plasseringsgruppeprofil:** *Gruppeplassering*
    - **Navn på ID for plasseringsgruppeprofil:** *Gruppeplassering*
    - **Gruppetype:** *Plassering*
    - **Sekvensnummer:** Godta standardverdien.

1. Velg **Lagre** for å gjøre de obligatoriske feltene på **Generelt**-hurtigfanen tilgjengelig.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Tidspunkt for gruppetilordning:** *Ved mottak*

        Dette feltet angir om plasseringsgruppen skal tilordnes umiddelbart når lageret mottas, eller om det skal sorteres senere.

    - **Regel for gruppetilordning:** *Manuell*

        Dette feltet angir om gruppetilordningen skal fastslås automatisk av systemet eller manuelt av brukeren.

    - **Direktivkoden:** La dette feltet stå tomt.
    - **Lokasjon for plasseringsgruppe:** *Mottak*

        Følgende verdier er tilgjengelige:

        - **Mottak** – En lokasjon ble funnet umiddelbart under mottak.
        - **Gruppelukking** – En lokasjon blir funnet når gruppen lukkes.
        - **Brukerrettet** – En lokasjon blir funnet når nummerskiltet plukkes fra gruppen for plassering. I dette tilfellet blir det ikke angitt noen lokasjon når plasseringsarbeidet opprettes. Under selve plasseringen må brukeren skanne nummerskiltet eller arbeids-ID-en for å starte plasseringstrinnet. Systemet finner deretter plasseringslokasjonen på nytt og gir brukeren beskjed om hvor det plukkede antallet skal plasseres.

    - **Plasseringsgruppe per bruker:** *Nei*

        Dette feltet definerer om hver gruppe skal være unik per bruker når grupper tilordnes automatisk. Det er bare tilgjengelig når **Regel for gruppetilordningsregel** er satt til *Automatisk*.

    - **Enhetsbegrensning:** La dette feltet stå tomt.

        Dette feltet definerer enheten som må mottas for at profilen skal være gyldig. Hvis det er tomt, er alle enheter gyldige.

    - **Arbeidsenhetsskift:** *Individuelt*

        Dette feltet definerer om alle lagerbeholdningene skal konsolideres (ved å bruke gruppe-ID-en og nummerskiltet) på ett nummerskilt når en gruppe er lukket, og om den skal plasseres som et enkelt nummerskilt eller separat på nummerskiltene som ble mottatt. Dette feltet er ikke tilgjengelig når feltet **Plasseringsgruppelokasjon** er satt til *Mottak*.

    - **Gruppe vedvarer som overordnet nummerskilt:** *Nei*

        Hvis dette alternativet er angitt til *Ja*, når plasseringstrinnet er fullført, blir gruppe-ID-en et overordnet nummerskilt, og alle varene på gruppe-ID-en blir koblet til det overordnede nummerskiltet.

1. På hurtigfanen **Gruppesortering** kan du definere kriterier for plasseringssortering. Velg **Ny** på verktøylinjen for å legge til en ny linje, og angi deretter følgende verdier:

    - **Sekvensnummer:** Godta standardverdien.
    - **Feltnavn:** *WMSLocationId*

        Dette feltet definerer feltet som denne linjen skal bruke som sorteringskriterium på.

    - **Sortering:** *Stigende*

        Dette feltet angir om sorteringen skal utføres i stigende eller synkende rekkefølge.

1. På **Gryppearbeidsmal**-hurtigfanen velger du **Ny** på verktøylinjen for å legge til en linje, og angi deretter følgende verdier:

    - **Arbeidsordretype:** *Bestillinger*
    - **Arbeidsmal:** *61 bestilling direkte*

1. Velg **Lagre** i handlingsruten , og velg deretter **Rediger spørring**.
1. I **Gruppeplassering**-dialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en ny linje i spørringen. Deretter oppdaterer du spørringslinjene som vist i følgende tabell.

    | Tabell | Avledet tabell | Felt | Vilkår |
    |---|---|---|---|
    | Arbeid | Arbeid | Lager | *61* |
    | Arbeid | Arbeid | Arbeids-ID | La dette feltet stå tomt. |

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Lagre** i handlingsruten og lukk siden.

> [!IMPORTANT]
> Felter i gruppeprofilen som vises nedtonet når **Generer gruppe-ID** er satt til *Ja*, er ikke tilgjengelige og vil ikke bli tatt med når denne funksjonen brukes.

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

To nye menyelementer for mobilenheter er tilgjengelige for denne funksjonen. Menyelementet **Motta og sorter gruppe** brukes til å sortere det mottatte lageret til en plasseringsgruppe ved mottak. Menyelementet **Gruppeplassering** brukes til å plassere gruppen etter at den er tilordnet.

#### <a name="receive-and-sort-cluster"></a>Motta og sorter gruppe

Opprett et nytt menyelement for mobilenhet for mottak av lager og sortering i en gruppe. Dette menyelementet vil opprette innkommende arbeid etter at lager er mottatt, som angir at mottaksmenyelementet vil bli brukt for plasseringsgrupper.

> [!NOTE]
> Menyelementet **Motta og sorter gruppe** kan brukes med følgende mottaksmenyelementer:
>
> - Mottak av bestillingslinje
> - Mottak av bestillingsvare
> - Mottak av lastvare

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I **Hode**-visning angir du følgende verdier:

    - **Menyelementnavn:** *Motta og sortere gruppe*
    - **Tittel:** *Motta og sorter gruppe*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Arbeidsopprettingsprosess:** *Mottak av bestillingsvarer*
    - **Generer nummerskilt:** *Ja*
    - **Tilordne plasseringsgruppe:** *Ja*

        > [!NOTE]
        > Alternativet **Tilordne plasseringsgruppe** er bare tilgjengelig for ettrinnsaktiviteten *Arbeidsopprettingsprosess* for mottak.

    Godta standardverdiene for de resterende feltene.

1. Velg **Lagre** i handlingsruten.

#### <a name="cluster-putaway"></a>Gruppeplassering

Opprett et nytt menyelement for mobilenhet for å plassere vekk gruppen etter at den er tilordnet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten.
1. I **Hode**-visning angir du følgende verdier:

    - **Menyelementnavn:** *Gruppeplassering*
    - **Tittel:** *Gruppeplassering*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Ja*

1. På **Generelt**-hurtigfanen settes **Styrt av**-feltet til *Gruppeplassering*. Godta standardverdiene for de resterende feltene.
1. Definer gyldig arbeidsklasse for menyelementet for denne mobilenheten på hurtigfanen **Arbeidsklasser**:

    - **Arbeidsklasse-ID:** *Kjøp*
    - **Arbeidsordretype:** *Bestillinger*

1. Velg **Lagre** i handlingsruten.

### <a name="mobile-device-menu"></a>Meny på mobilenheten

Legg til menyelementene du nettopp opprettet, på innkommende menyen i mobilappen.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. I handlingsruten velger du **Rediger**.
1. Velg **Inngående** i menylisten.
1. I **Tilgjengelige menyer og menyelementer**-listen finner og velger du **Motta og sorter gruppe**.
1. Velg høyre pil for å flytte det valgte menyelementet til **Menystruktur**-listen.
1. Bruk pil opp eller pil ned hvis du vil flytte menyelementet til ønsket plassering på menyen.
1. Velg **Lagre** i handlingsruten.
1. Gjenta trinn 4 til og med 7 for å legge til de gjenværende menyelementene:

    - Tilordne gruppe
    - Gruppeplassering

## <a name="example-scenario"></a>Eksempelscenario

Dette scenarioet simulerer behandling av plasseringsgruppe.

### <a name="create-a-purchase-order"></a>Opprette en bestilling

1. Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett bestilling**-dialogboksen angir du følgende verdier:

    - **Leverandørkonto:** *1001*
    - **Lager:** *61*

1. Velg **OK**.

    Siden **Alle bestillinger** vises.

1. På **Alle bestillinger**-siden i hurtigfanen **Bestillingslinjer** bruker du **Legg til linje**- knappen til å legge til følgende linjer:

    - Bestillingslinje 1:

        - **Varenummer:** *A0001*
        - **Antall:** *10*

    - Bestillingslinje 2:

        - **Varenummer:** *A0002*
        - **Antall:** *20*

    - Bestillingslinje 3:

        - **Varenummer:** *M9215*
        - **Antall:** *30*

1. Velg **Lagre** i handlingsruten.
1. Noter deg bestillingsnummeret.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Motta lager og plasser det fra mobilenheten

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Motta og sorter lageret i en gruppe

1. Logg på lagerappen som en bruker som er konfigurert for lager *61*.
1. I hovedmenyen velger du **Innkommende**.
1. Velg **Motta og sorter gruppe** på **Innkommende**-menyen.
1. I **Ponum**-feltet angir du bestillingsnummeret.
1. Velg **OK** (hakesymbolknappen).
1. Velg **Vare**-feltet, angi varenummeret *A0001* og velg **OK**.
1. Velg **Antall**-feltet, angi *10* ved å bruke talltastaturet, og velg deretter hakesymbolknappen.
1. På oppgavesiden **Antall** velger du **OK** (hakesymbolknappen) for å bekrefte antallet du har angitt.
1. Velg **OK** på oppgavesiden **Vare** for å bekrefte at varen *A0001* ble angitt.
1. Velg **Gruppe-ID**-feltet, og angi en verdi for å tilordne en ID for gruppen du oppretter.

    ID-en du angir her, vil bli brukt når de to gjenværende varene i bestillingen mottas.

1. Velg **OK**.

    Oppgavesiden **Ponum** vises og viser meldingen Arbeid fullført.

    Vare *A0001* er nå mottatt på *RECV*-lokasjonen og tilordnet gruppe-ID-en du angav i trinn 10.

1. Gjenta trinn 4 til og med 11 for å motta de gjenstående to varene fra bestillingen, og tilordne dem til gruppe-ID-en:

    - Et antall på *20* for vare *A0002*
    - Et antall på *30* for vare *M9215*

#### <a name="close-the-cluster"></a>Lukk gruppen

Før varene i gruppen kan plasseres, må gruppen lukkes.

1. I Supply Chain Management går du til **Lagerstyring \> Arbeid \> Utgående \> Arbeidsgrupper**.
1. I delen **Arbeidsgruppe** på siden **Arbeidsgrupper** søker du i **Gruppe-ID**-feltet etter gruppe-ID-en du angav tidligere.
1. Hvis gruppen ikke vises, kan den allerede være lukket. Hvis du vil finne ut om gruppen ble lukket, merker du av for **Vis lukket arbeid** og søker etter gruppe-ID-en du angav tidligere. Følg deretter ett av disse trinnene:

    - Hvis gruppen er lukket, hopper du over resten av fremgangsmåten for å gå videre til neste fremgangsmåte, [Plasser gruppen](#put-the-cluster-away).
    - Hvis gruppen ikke er lukket, følger du resten av denne fremgangsmåten for å lukke gruppen manuelt. Gå deretter videre til neste fremgangsmåte.

1. Velg gruppe-ID-en du angav tidligere, i delen **Arbeidsgruppe**.
1. I handlingsruten velger du **Lukk gruppe**.

    Når gruppen er lukket, vises den ikke lenger i delen **Arbeidsgruppe** (med mindre det er merket av for **Vis lukket arbeid**).

#### <a name="put-the-cluster-away"></a>Plasser gruppen

1. Logg på lagerappen som en bruker som er konfigurert for lager *61*.
1. I hovedmenyen velger du **Innkommende**.
1. I menyen **Innkommende** velger du **Gruppeplassering**.
1. Velg **Gruppe-ID**, og angi gruppe-ID-en du angav tidligere for den lukkede gruppen.
1. Velg **OK**.

    Siden **Gruppeplassering: plukk** vises. Den viser gruppe-ID-en, plukklokasjonen, varene (verdien *Flere* vises) og det totale antallet i gruppen som må plukkes.

1. Velg **OK**.

    Siden **Gruppeplassering: plasser** vises. **Plasser**-instruksjonene identifiserer gruppe-ID-en, plasseringslokasjonen, varene, det totale antallet og nummerskilt-ID-ene for varene som er mottatt i gruppen.

    Du har standardalternativer for å overstyre eller overføre dette trinnet.

    ![Gruppeplassering: plasser-side](media/Cluster_putaway-Put.png "Gruppeplassering: plasser-side")

1. Velg **OK** for å bekrefte plasseringen av gruppen.

    Meldingen Gruppe fullført vises.

## <a name="notes-and-tips"></a>Merknader og tips

For tilfeller der gruppe-ID-en blir det overordnede nummerskiltet for en nestet pall, gis plasseringsposisjonen automatisk når gruppe-ID-en skannes. Det må ikke skannes flere nummerskilter, selv om det er angitt manuell generering av nummerskilter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]