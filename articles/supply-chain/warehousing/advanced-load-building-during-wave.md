---
title: Avansert lastplanlegging under en bølge
description: Dette emnet inneholder informasjon om avansert bølgelastplanlegging, som automatisk tilordner forsendelser til eksisterende bølger under bølgekjøring. Du kan derfor opprette meningsfylte laster som representerer lastebiler, uten å måtte bruke arbeidsområdet for lastplanlegging.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0dafac981bcdec307de6dc202f557e7b8837ae2e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670524"
---
# <a name="advanced-load-building-during-wave"></a>Avansert lastplanlegging under en bølge

[!include [banner](../includes/banner.md)]

Avansert bølgelastplanlegging tilordner automatisk forsendelser til eksisterende bølger under bølgekjøring. Du kan derfor opprette meningsfylte laster som representerer lastebiler, uten å måtte bruke arbeidsområdet for lastplanlegging. Denne funksjonen er nyttig for bedrifter som ønsker å bruke konseptet med laster til å spore og planlegge forsendelsen av varer i en lastebil/trailer, men som ikke vil opprette lastene for hver dag manuelt.

Under bølgebehandling oppretter systemet vanligvis en ny last for hver forsendelse som det ikke er tildelt en last til. Når avansert bølgelastplanlegging er aktivert, tilordner imidlertid systemet hver ikke-tilordnede forsendelse til en eksisterende last (hvis det finnes en passende last), og nye laster opprettes bare når det er behov for dem. Avansert bølgelastplanlegging oppretter automatisk de nye lastene, basert på kriteriene du definerer.

Hvis du vil bruke funksjonen, må du definere systemet på følgende måte:

- Opprett *bølgemaler* som inneholder den nye **buildLoads**-metoden. Denne metoden gjør det mulig med avansert bølgelastplanlegging som bruker disse malene.
- Definere *maler for lastplanlegging* for å laste opp alle som er koblet til en bestemt bølgemal og -metode. Malene for lastplanlegging styrer hvilken last (eksisterende eller ny) lastelinjene som blir bølges, legges til. Du kan kombinere eller skille forsendelser, basert på kriterier som lastmal, utstyr og andre feltverdier på lastlinjen.
- Definer *samlegruppe for last* for å kontrollere hvilke varer som skal og ikke skal kombineres på én enkelt last. Du kan også angi om begrensningen skal produsere en advarsel eller en feil, og om volumetrisk begrensningen for lastmalen skal evalueres.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Aktivere avansert bølgelastplanlegging i systemet

Før du kan bruke avansert bølgelastplanlegging, må to funksjoner være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for disse funksjonene og aktivere dem hvis nødvendig. I **Funksjonsadministrering**-arbeidsområdet er funksjonene oppført på følgende måte:

- Funksjon for bygging av bølgelast:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Funksjon for bygging av bølgelast*

- Organisasjonsomfattende bølgetrinnkode:

    - **Modul:** *Lagerstyring*
    - **Funksjonsnavn:** *Organisasjonsomfattende bølgetrinnkode*

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom denne demonstrasjonen ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke denne demonstrasjonen som en veiledning for å bruke denne funksjonen når du arbeider i et produksjonssystem. I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Kontroller at scenariooppsettet omfatter nok tilgjengelig beholdning

Hvis du arbeider med **USMF**-demonstrasjonsdata, må du først kontrollere at systemet er konfigurert slik at det finnes nok beholdning på hver relevante plukklokasjon. For denne demonstrasjonen er forventes det at følgende beholdning er tilgjengelig i lageret: *62*:

- **Vare A0001:** 10 stk
- **Vare A0002:** 10 stk
- **Vare M9200:** 10 ea

Vare **M9200** må legges til i lageret. Fullfør fremgangsmåtene i følgende underinndelinger for å legge til varebeholdningen.

#### <a name="create-a-new-license-plate-id"></a>Opprett en ny nummerskilt-ID

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Nummerskilt**.
1. Velg **Ny** i handlingsruten.
1. I den nye raden i **Nummerskilt**-feltet angir du *LP6203*.
1. Velg **Lagre**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Opprett en standard kostpris for vare M9200 på sted 6

1. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
1. Søk på **M9200**.
1. Velg raden for varen og velg på handlingsruten, på **Styr kostnader**-fanen, i **Definer**-gruppen **Varepris**.
1. På **Varepris**-siden velger du **Ventende priser**-fanen.
1. Velg **Ny** i handlingsruten.
1. På den nye linjen angir du følgende verdier:

    - **Kosttype**: *Planlagt kostnad*
    - **Pristype:** *Kostnad*
    - **Versjon:** *10*
    - **Område:** *6*
    - **Pris:** *1,60*

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du **Aktiver ventende priser**.
1. Velg **Aktive priser**-fanen for å bekrefte at den nye kostprisen for område *6* er lagt til.

#### <a name="create-inventory-in-warehouse-62"></a>Opprett beholdning i lager 62

1. Gå til **Lagerstyring** \> **Journaloppføringer** \> **Varer** \> **Beholdningsjustering**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett lagerjournal**-dialogboksen på **Oversikt**-hurtigfanen, angir du *62* i **Lager**-feltet. godta standardverdiene i alle de andre feltene.
1. Velg **OK** for å lukke dialogboksen.
1. **Lagerjustering**-siden åpnes. På **Journallinjer**-hurtigfanen velger du **Ny** for å legge til en linje.
1. På den nye linjen angir du følgende verdier. godta standardverdiene i alle de andre feltene.

    - **Varenummer:** *M9200*
    - **Lokasjon** *bulk-003*
    - **Antall:** Endre verdien til *10*.

1. Velg **Lagre** i handlingsruten.
1. I handlingsruten velger du **Valider** for å kontrollere om det er feil.
1. I **Kontroller journal**-dialogboksen velger du **OK** for å starte kontrollen. Du får en melding når sjekken er fullført.
1. Velg **Bokfør** i handlingsruten for å aktivere lagerjusteringen.
1. I **Bokfør journal**-dialogboksen velger du **OK** for å starte bokføringen. Du får en melding når bokføringen er fullført.

## <a name="set-up-advanced-wave-load-building"></a>Konfigurer avansert bølgelastplanlegging

### <a name="regenerate-wave-process-methods"></a>Generere metoder for bølgebehandling på nytt

Det kan hende du må generere metodene for bølgebehandling på nytt for å gjøre metodene for lastplanlegging (**buildLoads**) tilgjengelige.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Bølger** \> **Bølgebehandlingsmetoder**.
2. Kontroller at **buildLoads** er til stede i listen. Hvis den ikke er til stede, velger du **Generer metoder på nytt** i handlingsruten for å legge den til.

### <a name="set-up-wave-templates"></a>Definere bølgemaler

Hvis du vil dra nytte av avansert bølgelastplanlegging, må du inkludere **buildLoads**-metoden i hver relevante [bølgemal](tasks/configure-wave-processing.md).

1. Gå til **Lagerstyring** \> **Oppsett** \> **Bølger** \> **Bølgemaler**.
1. Velg en bølgemal.

    Hvis du arbeider med **USMF**-demonstrasjonsdataene, velger du den **62 Standardforsendelse**-malen.

1. I handlingsruten velger du **Rediger** for å legge siden inn i redigeringsmodus.
1. På **Metoder**-hurtigfaner i **Gjenværende metoder**-rutenett velger du **buildLoads**-metoden.
1. Velg høyre pil for å flytte **buildLoads**-metoden til **Valgte metoder**-rutenettet.
1. Hvis du vil tilordne en verdi for **bølgetrinnkode** for **buildLoads**-metoden, må du først opprette en kode på **Bølgetrinnkoder**-siden. Du kan bruke en hvilken som helst verdi, men husk å skrive den ned, fordi du trenger den senere. Følg denne fremgangsmåten for å opprette koden **WSC2112**:

    1. I raden for **buildLoads** -metoden høyreklikker du pil ned i **Bølgetrinnkode**-feltet og velger **Vis detaljer**.
    1. På **Bølgetrinnkoder**-siden i handlingsruten velger du **Ny**.
    1. I **Bølgetrinnkode**-feltet angir du *WSC2112*.
    1. I **Bølgetrinnbeskrivelse**-feltet angir du *WSC2112*.
    1. I **Bølgetrinntype**-feltet velger du *Lastplanlegging*.

1. Velg **Lagre**, og lukk siden.
1. I raden for **buildLoads**-metoden, i **Bølgetrinnkode**-feltet, velger du koden du nettopp opprettet (**WSC2112**).
1. Velg **Lagre** i handlingsruten.

> [!NOTE]
> Bølgetrinnkoder er koder som brukere kan definere og bruke til å koble bestemte forekomster av bølgemetoder til tilsvarende maler. Malene omfatter maler for etterfylling, containerbruk, etikettutskrift, lastplanlegging og sortering.
>
> Når bølgetrinnkoder ikke brukes, må brukerne angi en fritekst for å referere til en bestemt mal fra den bølgemetodeforekomsten. Fritekst er utsatt for feil fordi brukerne må passe på at bølgestrinnteksten de legger til en bølgemal for en bestemt bølgetrinnmetode, samsvarer nøyaktig med bølgetrinnteksten i målmalen.
>
> Bølgetrinnkoder for en bestemt bølgetrinntype konfigureres på en egen side. For alle bølgetrinnforekomster i en bølgemal som krever en bølgetrinnkode, må du velge bølgetrinnkoden i en rullegardinliste. Valg i en rullegardinliste erstatter fritekstoppføring og reduserer risikoen og innvirkningen av menneskelig feil. Oppsettkoder brukes til å koble en bølgetrinnmetode i en bølgemal til en målmal for metoden.

### <a name="set-up-load-mix-groups"></a>Definere samlegruppe for last

Samlegrupper for last oppretter regler for typen varer som kan kombineres på én enkelt last. Du kan definere så mange samlegrupper for last du trenger. Hvis du vil bruke avansert bølgelastplanlegging, må du imidlertid ha minst én. Følg denne fremgangsmåten for å lage en samlegruppe for last.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Last** \> **Samlegrupper for last**.
1. I handlingsruten velger du **Ny** for å opprette et lastgruppe.
1. I **ID for samlegruppe for last**-feltet angir du et navn på den nye gruppen.

    Hvis du arbeider med **USMF**-demodataene, angir du følgende verdier:

    - **ID for samlegruppe for last:** *TV*
    - **Beskrivelse:** *TV*

1. I handlingsruten velger du **Lagre** for å gjøre **Kriterier for samlegruppe for last**-hurtigfanen tilgjengelig.
1. På **Kriterier for samlegruppe for last**-hurtigfanen velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du ønskede verdier i hvert felt. Disse verdiene bestemmer varegruppene som vurderes for lastblandingen.

    Hvis du arbeider med **USMF**-demodataene, velger du *TV og video* i **Varegruppe**-feltet.

1. I handlingsruten velger du **Lagre** for å gjøre **Begrensninger for samlegruppe for last**-hurtigfanen tilgjengelig.
1. På **Begrensninger for samlegruppe for last**-hurtigfanen velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du ønskede verdier i hvert felt.

    Hvis du arbeider med **USMF**-demodataene, angir du følgende verdier:

    - **Varegruppe:** *CarAudio*
    - **Lastplanleggingshandling:** *Begrens* (Denne verdien vil hindre at varer som tilhører **CarAudio**-varegruppen, er i samme last som varer som tilhører **TV og video**-varegruppen.)

1. Fortsett å arbeide med reglene til du har lagt til alle kriteriene og begrensningene som kreves for samlegruppen for last.

Hvis du arbeider med **USMF**-demodataene, har du nå fullført dette oppsettet.

### <a name="set-up-load-build-templates"></a>Konfigurer lastplanleggingsmaler

Du kan definere så mange lastplanleggingsmaler du trenger. Hvis du vil bruke avansert bølgelastplanlegging, må du imidlertid ha minst én. Følg denne fremgangsmåten for å opprette en lastplanleggingsmal.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Last** \> **Maler for lastplanlegging under en bølge**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende verdier.

    | Felt | beskrivelse | Verdi i USMF-demodataene |
    |---|---|---|
    | Serienummer | Rekkefølgen som malen skal evalueres i. | *1* |
    | Navn på lastplanleggingsmal | Angi den unike identifikator for lastplanleggingsmalen. Du bør skrive inn navnet på malen du opprettet eller oppdaterte tidligere, i dette oppsettet. | *62 Standardforsendelse* |
    | Bølgetrinnkode | Angi bølgetrinnkode du vil bruke for å koble malen til en bølgemetode. Du må angi koden du valgte for **buildLoads**-metoden da du definerer bølgemalen tidligere i dette oppsettet. | *WSC2112* |
    | Lastmal-ID | Velg lastmalen som skal brukes når nye laster opprettes, og å sammenligne med ved tilordning til eksisterende laster. Lastmalen definerer maksimal vekt og volum som er tillatt for hele lasten. | *Stnd. lastmal* |
    | Utstyr | Utstyret å sammenligne med ved tilordning til eksisterende laster, og å fylle ut for nye laster som opprettes. | La dette feltet stå tomt. |
    | Samlegruppe-ID for last | Velg samlegruppen for last som skal brukes hvis varen er tillatt i lasten. Samlegruppen oppretter regler for typen varer som kan kombineres på én enkelt last. Du bør velge en av samlegruppene som du opprettet tidligere, i dette oppsettet. | *TV* |
    | Bruk åpne laster | Velg om eksisterende laster skal legges til. Følgende alternativer er tilgjengelige:<ul><li>**Ingen** – ikke legg til åpne laster i eksisterende laster.</li><li>**Alle** – legg til åpne later i en eksisterende last som er gyldig for linjen.</li><li>**Tilordnet** – legg til åpne laster i lasten som er tilordnet til bølgen.</li></ul> | *Vilkårlig* |
    | Opprett laster | Angi om nye laster skal opprettes hvis ingen eksisterende laster samsvarer med kriteriene. | Valgt (= *Ja*) |
    | Tillat forsendelseslinjedeling | Angi om en enkelt lastlinje kan dele på flere laster hvis hele linjen overskrider maksimumskapasiteten til lastmalen. | Fjernet (= *Nei*) |
    | Valider volummål | Anig om lastplanlegging skal kontrollerer vekten og volumet for hver lastlinje som tilføyes, for å sikre volumetriske grenser for lastmalen overholdes. | Fjernet (= *Nei*) |

1. I handlingsruten velger du **Lagre** for å gjøre **Rediger spørring**-alternativet tilgjengelig.
1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigering av spørringen.
1. I dialogboksen, på **Sortering**-fanen, velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden definerer du sorteringsreglene du vil bruke. Angi for eksempel følgende verdier for å sortere søkeresultatene i stigende rekkefølge etter ordrenummer:

    - **Tabell:** *Lastdetaljer*
    - **Avledet tabell:** *Lastdetaljer*
    - **Felt:** *Ordrenummer*
    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lagre endringene og lukke dialogboksen.
1. På **Bryt etter**-hurtigfanen angir du regler for å kontrollere hvordan lastene deles opp. Vanligvis vil du kunne bryte egendefinerte felt som har blitt utvidet på lastlinjen, for eksempel **Rute**, **Tur** eller **Kjøring**. Hvis du for eksempel vil opprette én last per ordrenummer, merker du **Bryt etter**-avmerkingsboksen som har følgende verdier:

    - **Referansetabellnavn:** *Lastdetaljer*
    - **Referansefeltnavn:** *Ordrenummer*

## <a name="scenario"></a>Scenario

Dette scenariet viser hvordan innstillingene som ble beskrevet tidligere i dette emnet, påvirker lageroperasjoner mens en salgsordre behandles. Dette scenarioet bruker **USMF**-demonstrasjonsdata sammen med andre demoverdier som finnes i disse installasjonsinstruksjonene.

### <a name="create-sales-orders"></a>Opprette salgsordrer

1. Gå til **Salg og markedsføring** \> **Salgsordrer** \> **Alle salgsordrer**.
1. I handlingsruten velger du **Ny** for å åpne **Opprett salgsordre**-dialogboksen.
1. Angi følgende verdier i dialogboksen:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-007*.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Den bør inneholde en ny, tom linje i rutenettet på **Salgsordrelinjer**-hurtigfanen. På denne nye linjen angir du **Varenummer**-feltet til *A0001* og **Antall**-feltet til *1*.
1. Velg **Reservasjon** på **Beholdning**-menyen over rutenettet.
1. På **Reservasjon**-siden i handlingsruten velger du **Reserver parti**.
1. Velg **Lukk**-knappen (**X**) øverst til høyre på siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten. Systemet oppretter en forsendelse og legger den til en ny last, fordi ingen eksisterende last inneholder lastlinjer som har dette ordrenummeret.

    Du mottar informasjonsmeldinger som angir arbeid, bølge og forsendelse som er opprettet for denne ordren.

1. Hvis du vil bekrefte informasjon om last, forsendelse og arbeid på salgslinjen, velger du linjen, og deretter velger du **Lager**-menyen over rutenettet, velger **Lastdetaljer**, **Forsendelsesdetaljer** eller **Arbeidsdetaljer**.
1. I salgsordren du nettopp opprettet, velger du **Legg til** på **Salgsordrelinjer**-hurtigfanen for å legge til en ny linje.
1. På den nye linjen angir du **Varenummer**-feltet til *A0002* og **Antall**-feltet til *1*.
1. Gjenta linjer 6 til og med 9 for å reservere linjen og frigi den til lageret. Systemet oppretter en **ny** forsendelse for linjen du la til. Men fordi du bruker avansert bølgelastplanlegging, legger systemet denne forsendelsen og lastlinjen til i den eksisterende bølgen. Hvis du ikke brukte avansert bølgelastplanlegging, vil systemet opprette en ny last for forsendelsen.
1. I salgsordren du nettopp opprettet, velger du **Legg til** på **Salgsordrelinjer**-hurtigfanen for å legge til en ny linje.
1. På den nye linjen angir du **Varenummer**-feltet til *M9200* og **Antall**-feltet til *1*.
1. Gjenta linjer 6 til og med 9 for å reservere linjen og frigi den til lageret. Som tidligere oppretter systemet en **ny** forsendelse for linjen du la til. Men fordi varen kommer fra **CarAudio**-varegruppen, **kan den ikke overføre betingelsene du angir for samlegruppen for last**. Derfor **legges den til en ny last**. Hvis du ikke hadde angitt en samlegruppe for lastplanleggingsmalen, ville denne forsendelsen ha blitt lagt til i den første lasten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]