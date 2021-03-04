---
title: Etterfylling over lokasjonskapasitet
description: Dette emnet inneholder informasjon om funksjonen Etterfylling over lokasjonskapasitet. Denne funksjonen aktiverer alt etterfyllingsarbeid som vil være nødvendig å opprette for dagen, og administrerer tilgjengelighet for etterfyllingsarbeidet for å sikre at plukklokasjonen ikke går ut av beholdning eller går over kapasitet.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 8e9ae16fea892d1d6b6a6b5d06137576623e7f5b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434798"
---
# <a name="replenishment-over-location-capacity"></a>Etterfylling over lokasjonskapasitet

[!include [banner](../includes/banner.md)]

Noen lagre med nøy volum eller plassbegrensning må levere mer antall av en vare på en dag enn det er plass til i plukklokasjonen. Funksjonen *v* aktiverer alt etterfyllingsarbeid som vil være nødvendig å opprette for dagen, og administrerer tilgjengelighet for etterfyllingsarbeidet for å sikre at plukklokasjonen ikke går ut av beholdning eller går over kapasitet..

Funksjonen gjør det mulig å opprette mer etterfyllingsarbeid enn det er plass til i en lokasjon, og det forventes at etterfyllingsarbeid ikke fullføres når lokasjonen er full. Når beholdningen plukkstedet faller under en konfigurerbar terskel, gjøres mer etterfyllingsarbeid tilgjengelig.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Aktivere funksjonen Etterfylling over lokasjonskapasitet

For å gjøre denne funksjonen tilgjengelig aktiverer du følgende funksjoner i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (i denne rekkefølgen):

1. Organisasjonsomfattende arbeidsblokkering
1. Etterfylling over lokasjonskapasitet

## <a name="set-up-the-feature-for-the-example-scenario"></a>Konfigurer funksjonen for eksempelscenarioet

Denne delen inneholder retningslinjer og et eksempel som viser hvordan du definerer denne funksjonen og klargjør eksempeldata foreksempel scenarioet som er oppgitt senere i dette emnet.

### <a name="enable-sample-data"></a>Aktivere eksempeldata

For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

### <a name="location-profile"></a>Lokasjonsprofil

Aktiver funksjonaliteten for Etterfylling over kapasitet på lokasjonsprofilen.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **PLUK-06** i venstre rute.
1. I handlingsruten velger du **Rediger**.
1. Angi følgende verdier på **Etterfylling**-hurtigfanen:

    - **Overskrid lokasjonskapasitet:** *Ja*

        Når dette er aktivert, er det tillatt for etterfyllingsarbeid å overskride maksimumskapasiteten til lokasjonen. Dette gjør det også mulig med andre felt på hurtigfanen **Etterfylling**.

    - **Terskeltype for arbeidstilgjengelighet:** *Antall*

        Dette feltet definerer metoden som brukes til å fastslå når mer arbeid skal frigis. Du kan frigi etter antall eller prosent:

        - *Prosent* – Velg dette alternativet for å bruke prosentkapasitet som er basert på beholdningsgrenser eller volummål. Hvis du velger dette alternativet, aktiveres feltet **Overflytprosent**, og de to antallsrelaterte feltene, **Overflytantall** og **Overflytenhet**, deaktiveres.

            Du kan bruke dette alternativet hvis plukklokasjonene bruker volummål.

            Hvis det er merket av for dette alternativet, setter du feltet **Overflytprosent** til prosenten der mer etterfyllingsarbeid blir gjort tilgjengelig.

        - *Antall* – Velg dette alternativet for å bruke en bestemt antallsverdi. Hvis du velger dette alternativet, deaktiveres feltet **Overflytprosent**, og de feltene **Overflytantall** og **Overflytenhet** aktiveres.

            Bruk dette alternativet når du ikke bruker volummål for lokasjoner som etterfylles, eller når du har konsekvente mengder der du vil at mer beholdning skal hentes til lokasjonen.

           Hvis dette alternativet er valgt, angir du feltene **Overflytantall** og **Overflytenhet** til antallet og enheten der mer etterfyllings arbeid skal gjøres tilgjengelig.

    - **Overflytantall:** *0,65*

        Dette feltet definerer antallet lokasjonen overflyter i.

        Arbeid er tilgjengelig så lenge summen av beholdningsantall i lokasjonen og arbeidsmengde er under denne verdien. Etterfyllingsantall over denne verdien blir blokkert, og blokkeringen må oppheves manuelt.

        Lokasjonsbeholdningsgrenser vurderes når arbeidsantallet beregnes.

    - **Overflytenhet:** *PL*

        Dette feltet definerer enheten som er knyttet til overflytantallet.

        I dette tilfellet vil mer etterfyllingsarbeid gjøres tilgjengelig når lokasjonen går ned til 0,65 paller (PL).

    - **Overflytprosent**

        Dette feltet definerer prosenten der lokasjonen overflyter.

        Arbeid er tilgjengelig så lenge summen av beholdningsantall i lokasjonen og arbeidsmengde er under denne prosentverdien. Prosent for etterfyllingsantall over denne verdien blir blokkert, og blokkeringen må oppheves manuelt.

        Lokasjonsbeholdningsgrenser vurderes når arbeidsantallsprosenten beregnes. Hvis det ikke er definert noen lagergrenser for lokasjoner, beregnes arbeidsmengdeprosenten etter volum hvis volumbegrensninger er definert for lokasjonsprofilen.

> [!IMPORTANT]
> Hvis du bruker demonstrasjonsdataene for den juridiske enheten **USMF** og tidligere har aktivert funksjonen *Nummerskiltposisjonering for lokasjon*, må du deaktivere innstillingen **Aktiver nummerskiltposisjonering** for lokasjonsprofilen **BULK-06** for å fullføre trinnene for mobil i eksempelscenarioet.

### <a name="wave-step-code"></a>Bølgetrinnkode

> [!NOTE]
> Hvis du vil definere en bølgetrinnskode som beskrevet her, kan det være at du først må bruke [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen *Organisasjonsomfattende bølgetrinnkode*.

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgetrinnkoder**.
1. Velg **Ny**, og angi følgende verdier:

    - **Bølgetrinnkode:** *Etterfyll*
    - **Bølgetrinnbeskrivelse:** *Etterfylling*
    - **Bølgetrinntype:** *Etterfylling*

1. Velg **Lagre**.

### <a name="replenishment-template"></a>Etterfyllingsmal

Etterfyllingsmaler er et sett med regler som bestemmer når og hvordan en lokasjon fylles.

1. Gå til **Lagerstyring \> Oppsett \> Etterfylling \> Etterfyllingsmaler**.
1. I handlingsruten velger du **Rediger**.
1. I **Oversikt**-delen velger du linjen der feltet **Etterfyllingsmal** er satt til *Behovsbasert etterfylling*.
1. Angi følgende verdier:

    - **Bølgetrinnkode:** *Etterfyll*
    - **Tillat at bølgebehov bruker ikke-reservert antall:** *Ja*

1. Velg **Lagre**.

### <a name="wave-template"></a>Bølgemal

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. I den venstre ruten setter du **Bølgemaltype**-feltet til *Forsendelse*.
1. Velg malen **61 Forsendelse** fra listen.
1. I handlingsruten velger du **Rediger**.
1. I hurtigfanen **Generelt** setter du alternativet **Automatiser frigivelse av etterfyllingsarbeid** til *Ja*.

    Sett dette alternativet til *Ja* for å opprette behovsbasert etterfyllingarbeid og frigi det automatisk. Du må legge til etterfyllingsbølgemetoden i bølgemalen og opprette en mal for etterfylling av typen **Bølgebehov**. Angi en mal for etterfylling på siden **Etterfyllingsmaler**. Hvis du vil definere en etterfyllingsmal, må du legge til etterfyllingsmetoden i bølgemalen.

1. På hurtigfanen **Metoder**, i kolonnen **Valgte metoder**, finner du følgende linje:

    - **Metodenavn:** *etterfylle*
    - **Navn:** *Etterfylling*

1. Sett feltet **Bølgetrinnkode** for denne linjen til *Etterfyll*.
1. Velg **Lagre**.

## <a name="example-scenario"></a>Eksempelscenario

Etter at du har gjort alle de tidligere beskrevne eksempeldataene tilgjengelige og konfigurert dem, kan du arbeide deg gjennom dette scenariet for å prøve ut funksjonen *Etterfylling over lokasjonskapasitet*. Verdiene som vises i dette scenariet, antar at du arbeider med standard demonstrasjonsdata, at du har valgt den juridiske enheten **USMF**, og at du klargjorde eksempelpostene som er beskrevet tidligere i dette emnet. Dette scenariet fungerer også som et eksempel som viser hvordan funksjonen kan brukes i et produksjonsmiljø.

### <a name="create-replenishment-work"></a>Opprett etterfyllingsarbeid

#### <a name="create-sales-order-1"></a>Opprett salgsordre 1

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruten velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.
1. Angi følgende verdier i dialogboksen:

    - **Kundekonto:** *US-007*
    - **Lager:** *61*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *T0100*
    - **Antall:** *40*

1. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti**.
1. Lukk siden.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.

    Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet. Det opprettes også en etterfyllingsbølge.

    Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."

#### <a name="create-sales-order-2"></a>Opprett salgsordre 2

1. I handlingsruten på siden **Alle salgsordrer** velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.
1. Angi følgende verdi i dialogboksen:

    - **Kundekonto:** *US-001*
    - **Lager:** *61*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *T0100*
    - **Antall:** *60*

1. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti**.
1. Lukk siden.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.

    Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet. Det opprettes også en etterfyllingsbølge.

    Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."

#### <a name="create-sales-order-3"></a>Opprett salgsordre 3

1. I handlingsruten på siden **Alle salgsordrer** velger du **Ny** for å åpne en dialogboks for oppretting av en ny salgsordre.
1. Angi følgende verdier i dialogboksen:

    - **Kundekonto:** *US-004*
    - **Lager:** *61*

1. Velg **OK** for å opprette salgsorden og lukke dialogboksen.
1. Den nye salgsordren åpnes. Det inneholder en ny, tom linje på **Salgsordrelinjer**-hurtigfanen. På denne linjen angir du følgende verdier:

    - **Varenummer:** *T0100*
    - **Antall:** *30*

1. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti**.
1. Lukk siden.
1. Velg **Frigi til lager** i kategorien **Lager** i handlingsruten.

    Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID som er opprettet. Det opprettes også en etterfyllingsbølge.

    Du får også en advarsel som sier: "Blokkeringen av arbeids-ID XXXX kan ikke oppheves, fordi den ikke har fullført etterfyllingsarbeid."

#### <a name="view-work-details"></a>Vis arbeidsdetaljer

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. I **Oversikt**-delen filtrerer du **Lager**-kolonnen for lager *61*.
1. Du skal se at sju arbeids-ID-er ble opprettet for de tre etterspørselssalgsordrene.

    - Tre av de sju arbeids-ID-ene har **Arbeidsordretype**-verdien *Etterfylling*, og fire har **Arbeidsordretype**-verdien *Salgsordrer*.
    - Alle de tre arbeids-ID-ene som har **Arbeidsordretype**-verdien *Etterfylling*, har de samme *Plukk*- og *Plassering*-stedene i **Linjer**-delen:

        - **Plukk:** *02A01R5S1B*
        - **Plassering:** *06A01R2S1B*

    - Det ble opprettet to arbeids-ID-er for salgsordre 1.

1. Skriv ned arbeids-ID-ene for salgsordrene.

Avhengig av beholdningsantallene kan arbeidsantallene som opprettes, variere noe. Generelt sett bør imidlertid arbeidshodene som opprettes, samsvare med dette scenarioeksemplet.

#### <a name="on-hand-inventory-license-plate-id"></a>Nummerskilt-ID for lagerbeholdning

Senere i dette scenariet skal du bruke lagerappen (eller en emulator), der du må identifisere nummerskiltet for å fullføre plukke- og etterfyllingsscenariene.

Følg denne fremgangsmåten for å finne ID-ene til nummerskiltene som du vil trenge senere.

1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.
1. Velg **Vis filtre**-knappen for å åpne filterruten.
1. Angi følgende filtreringskriterier for å hente nummerskiltene for scenariet. Bruk filteret *begynner med*.

    - **Varenummer:** *T0100*
    - **Lager:** *61*

1. Velg **Bruk**.
1. Klikk på **Dimensjoner** i handlingsruten.
1. I dialogboksen **Dimensjonsvisning**, i delen **Lagringsdimensjoner**, velger du alle verdiene.
1. I **Transaksjoner**-delen velger du **Varenummer** og **Antall \<\> 0**.
1. Når du er ferdig, velger du **OK** for å lukke dialogboksen.
1. Rutenettet **Beholdning** viser skiltnumrene for varen *T0100* i hver lokasjon. Noter deg hvilket nummerskilt som finnes på hver lokasjon, fordi du vil ha behov for denne informasjonen senere.
1. Lukk siden.

### <a name="process-steps"></a>Prosesstrinn

Du vil utføre etterfylling av lagerlokasjon for de to første arbeids-ID-ene. Arbeid på det tredje etterfyllingsarbeidet vil være blokkert til lagernivået på plukklokasjonen faller under terskelen.

#### <a name="replenishment"></a>Etterfylling

1. Logg på lagerappen som en bruker på lageret *61*. (Angi *61* som bruker-ID og *1* som passord.)
1. Gå til **Beholdning \> Etterfylling**.

    Du blir bedt om å fullføre det første etterfyllingsarbeidet. Varenummeret, antallet og lokasjonen det skal plukkes fra, vises.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.
1. Velg **OK**-knappen (hakesymbolet).

    Systemet genererer et målskiltnummer for det nye nummerskiltet for den plukkede varen.

1. Velg **OK** for å bekrefte verdien.

    Plasseringsarbeid vises som instruerer brukeren om å plassere målnummerskiltet på etterfyllingslokasjonen. *Plassering*-lokasjonen skal være **06A01R2S1B**.

1. Bekreft plasseringsdetaljene, og velg **OK**.

    Du får en melding om arbeidet er fullført, og detaljene for neste etterfyllingsplukkoppgave vises: varenummeret, antallet og lokasjonen det skal plukkes fra. Plukklokasjonen vil være den samme som den første etterfyllingslokasjonen. Derfor vil nummerskiltet ha samme nummerskilt-ID som ble brukt for den første etterfyllingsarbeidsoppgaven.

1. Gjenta de foregående trinnene for å fullføre etterfyllingsarbeidet for den andre arbeidsoppgaven. Antallet og målnummerskiltet vil være forskjellig fra antallet og målnummerskiltet i den første arbeidsoppgaven.

Når det andre etter fyllingsarbeidet er fullført, vises en melding om at arbeidet er fullført. Mobilenheten informerer også om at det ikke er noe tilgjengelig arbeid, selv om det gjenstår noe etterfyllingsarbeid. Dette skjer fordi etterfyllingsarbeidet har tilgjengelighetsstatusen *På vent*, og er derfor merket som **Blokkert**.

Statusen *På vent* ble utløst fordi lokasjonsprofilen for plukkelokasjonen som arbeidet tilordnes til, har en **Overflytantall**-verdi på *0,65 PL*. De to forrige etterfyllingsarbeidsoppgavene har fylt lokasjonen nesten til overflytgrensen for varen *T0100*. (Enhetskonverteringen for varen er *1 PL = 100 stk*.) Derfor vil gjenstående etterfyllingsarbeid føre til at lokasjonen overskrider overflytgrensen.

Før nok beholdning er plukket fra lokasjonen for å få den under terskelen for arbeidsfrigivelse på menyen på mobilenheten, vil dette etterfyllingsarbeidet forbli blokkert.

#### <a name="sales-order-pick"></a>Salgsordreplukking

Før den gjenstående etterfyllingsarbeidsoppgaven kan fullføres, må plukklokasjonen tømmes til et nivå der blokkeringen for det gjenstående etterfyllingsarbeidet kan oppheves. Med andre ord kan ikke summen av lagerbeholdningen på lokasjonen og etterfyllingsantallet overskride verdien for **Overflytantall**. Når denne summen er mindre enn overløpsantallet, blir blokkeringen av det gjenstående etterfyllingsarbeidet opphevet.

1. Logg på lagerappen som en bruker på lageret *61*. (Angi *61* som bruker-ID og *1* som passord.)
1. Gå til **Utgående \> Salgsplukking**.
1. Angi den første arbeids-ID-en for salgsordre 1.

    Du kan se arbeids-ID-ene for salgsordrer som du har tatt notat av tidligere, på siden **Arbeidsdetaljer**. Arbeids-ID-en du angir her, vil generere plukkarbeid for et antall på 10 stk. fra to separate lokasjoner.

1. Velg **OK**.

    Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra, for den første lokasjonen.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.
1. Velg **OK**-knappen (hakesymbolet).

    Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra, for den neste lokasjonen.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.
1. Velg **OK**-knappen (hakesymbolet).

    Siden **Salgsordrer: Plasser** instruerer deg om å plassere begge de fullførte plukkarbeidene i den utgående oppsamlingslokasjonen.

1. Velg **OK**.

    Du mottar en Arbeid fullført-melding.

1. Angi den andre arbeids-ID-en for salgsordre 1.

    Det er bare én plukkoppgave for denne arbeids-ID-en.

1. Velg **OK**.

    Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.

    Nummerskiltet du angir, vil være et av de systemgenererte nummerskiltene fra etterfyllingsarbeidsoppgavene. For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.

1. Velg **OK**-knappen (hakesymbolet).
1. Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.
1. Velg **OK**.

    Du mottar en Arbeid fullført-melding.

Salgsordre 2 er sperret for plukking fordi etterfyllingsoppgaven den er koblet til, ikke er fullført. For øyeblikket er det fremdeles et antall på 30 stk. i plukklokasjonen, og etterfyllingsantallet for salgsordre 2 er 60 stk. Summen av lagerbeholdningen og etterfyllingsbeholdningen (90 stk.) overskrider overflytantallet på 0,65 PL (eller 65 stk.). Før etterfyllingsarbeidet kan fullføres, må salgsordre 3 plukkes.

1. Angi den arbeids-ID-en for salgsordre 3.

    Det er bare én plukkoppgave for denne arbeids-ID-en.

1. Velg **OK**.

    Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.

    Nummerskiltet du angir, vil være et av de systemgenererte nummerskiltene fra etterfyllingsarbeidsoppgavene. For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.

1. Velg **OK**-knappen (hakesymbolet).
1. Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.
1. Velg **OK**.

    Du mottar en Arbeid fullført-melding.

Så snart summen av beholdningsantallet i plukklokasjonen og etterfyllingsantallet er under terskelen, vil du kunne behandle gjenstående etterfyllingsarbeid.

Gå tilbake til siden **Arbeidsdetaljer**, og legg merke til at tilgjengeligheten for etterfyllingsarbeidet for den siste delen av etterfyllingen (for salgsordre 2) er *Åpen*, fordi det nå er nok plass på lokasjonen til å godta etterfyllingen.

Nå kan du behandle dette etterfyllingsarbeidet via mobilenheten.

1. Gå til **Beholdning \> Etterfylling**.

    Du blir bedt om å fullføre det resterende etterfyllingsarbeidet. Varenummeret, antallet og lokasjonen det skal plukkes fra, vises.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.
1. Velg **OK**-knappen (hakesymbolet).

    Systemet genererer et målskiltnummer for det nye nummerskiltet for den plukkede varen.

1. Velg **OK** for å bekrefte verdien.

    Plasseringsarbeid vises som instruerer brukeren om å plassere målnummerskiltet på etterfyllingslokasjonen. *Plassering*-lokasjonen skal være **06A01R2S1B**.

1. Bekreft plasseringsdetaljene, og velg **OK**.

    Du får meldingene om fullført arbeid og ikke noe arbeid tilgjengelig.

Nå kan du plukke salgsordre 2. Blokkeringen for den ble fjernet da etter fyllingsarbeidet som er koblet til salgsordren, ble fullført.

1. Angi arbeids-ID-en for salgsordre 2.

    Det er bare én plukkoppgave for denne arbeids-ID-en.

1. Velg **OK**.

    Oppgavesiden **Salgsordrer: Plukk** viser varenummeret, antallet og lokasjonen du skal plukke fra.

1. I **LP**-feltet angir du skiltnummeret for varen i lokasjonen som vises.

    Nummerskiltet du angir, vil være det systemgenererte nummerskiltet fra etterfyllingsarbeidsoppgaven. For å være sikker på at du registrerer riktig nummerskilt-ID, må du kontrollere beholdningen på siden **Beholdningsliste** for varen, lokasjonen og antallet.

1. Velg **OK**-knappen (hakesymbolet).
1. Bekreft instruksjonene for plasseringsoppgaven til plasseringen for utgående oppsamling.
1. Velg **OK**.

    Du mottar en Arbeid fullført-melding.

## <a name="notes-and-tips"></a>Merknader og tips

- Denne funksjonaliteten fungerer med alle typer etterfylling: bølgebehov, min/maks, lastbehov og sporing.
- Du kan manuelt overstyre tilgjengeligheten av etterfyllingsarbeid for hvert arbeidshode fra siden **Arbeidsdetaljer** hvis du vil.
- Når systemet angir tilgjengeligheten for etterfyllingsarbeid, vurderes all beholdning som allerede finnes på lokasjonen før noe som helst arbeid fullføres.
- Hver del av salgsordrearbeid er koblet til et bestemt etterfyllingsarbeid. Det finnes ingen tilsvarende funksjonalitet for tilgjengelighet av salgsarbeid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]