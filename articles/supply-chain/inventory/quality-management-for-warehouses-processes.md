---
title: Kvalitetsstyring for lagerprosesser
description: Dette emnet inneholder informasjon om funksjonen for kvalitetsstyring for lagerprosesser. Denne funksjonen utvider funksjonaliteten til kvalitetsstyring og lar brukere integrere vareprøvekontroller i lagermottaksprosessen ved hjelp av avansert lagerstyring.
author: Henrikan
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 42280c811e1f4ed5d33c66f5a8634417a61be905
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301335"
---
# <a name="quality-management-for-warehouse-processes"></a>Kvalitetsstyring for lagerprosesser

Med funksjonen _Kvalitetsstyring for lagerprosesser_ kan du integrere vareprøvekontroller i lagermottaksprosessen ved hjelp av avansert lagerstyring. Lagerarbeid kan genereres automatisk for å flytte lager til kvalitetskontroll-lokasjonen, basert på en prosent eller et fast antall, eller basert på hvert *n*-te nummerskilt. Etter at en kvalitetsordre er fullført, kan det genereres arbeid automatisk for å flytte lageret til neste sted i prosessen, avhengig av kvalitetsresultatet.

Funksjonen _Kvalitetsstyring for lagerprosesser_ utvider funksjonaliteten til den grunnleggende kvalitetsstyringsfunksjonen. Her kan du opprette kvalitetsordrer for lageret som er sendt til kvalitetskontroll-lokasjonen, selv om kvalitetsordrer ikke alltid kreves. Derfor er det mulig å kontrollere en lett kvalitetskontrollprosess som er basert på lagerarbeid.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Aktivere funksjonen Kvalitetsstyring for lagerprosesser

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Kvalitetsstyring for lagerprosesser*

## <a name="key-benefits"></a>Hovedfordeler

Funksjonen _Kvalitetsstyring for lagerprosesser_ genererer automatisk arbeid som en del av mottaksprosessen, for å flytte lagerantallet som er nødvendig for kvalitetskontroll til en kvalitetskontroll-lokasjon. Hvis antallet som mottas, overskrider antallet som er nødvendig for kvalitetskontroll (i henhold til vareprøveoppsettet), flyttes det ekstra antallet til en innkommende lokasjon som er definert i oppsettet av lokasjonsdirektiv. Når kvalitetsordren er validert, genereres arbeidet automatisk for å flytte antallet for kvalitetsordren til en ny innkommende eller returlokasjon basert på valideringsresultatet og oppsettet av lokasjonsdirektiv. Den automatiske genereringen av arbeid som bare har det antallet som må flyttes til og fra kvalitetskontroll, gir en integrert prosessopplevelse.

> [!NOTE]
> Når funksjonen _Kvalitetsstyring for lagerprosesser_ er aktivert, kan du fremdeles dra nytte av den manuelle prosessen. I den manuelle prosessen brukes lagerflytting og flytting etter mal for å la en lagerarbeider utløse opprettelsen av lagerarbeid for å flytte lagerbeholdningen fra en kvalitetskontroll-lokasjon til en ny lokasjon. Du kan også fremdeles definere et innkommende lokasjonsdirektiv som flytter lager i sin helhet fra en mottakslokasjon til en kvalitetskontroll-lokasjon uten å vurdere vareprøveoppsettet.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kvalitetsstyring og funksjonen Kvalitetsstyring for lagerprosesser

Når funksjonen _Kvalitetsstyring for lagerprosesser_ er aktivert, endres oppsettet for enheter for styring av nøkkellager og kvalitetsstyring. Illustrasjonen nedenfor gir en oversikt over enhetene som aktiverer kvalitetsordrer for lagerprosesser. Tekst i parentes angir foreslåtte handlinger når kvalitetsstyring ble brukt før funksjonen _Kvalitetsstyring for lagerprosesser_ ble aktivert.

![Kvalitetsstyringsenheter](media/quality-management-entity-diagram.png "Kvalitetsstyringsenheter")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Drivere: Arbeidsordretypene Kvalitetsvareprøver og Kvalitetsordre

Funksjonen _Kvalitetsstyring for lagerprosesser_ introduserer to arbeidsordretyper som aktiverer arbeidsopprettingsprosessen:

- **Kvalitetsvareprøver** – Denne arbeidsordretypen brukes til å opprette arbeid som flytter registrert lager til kvalitetskontroll.
- **Kvalitetsordre** – Denne arbeidsordretypen brukes til å opprette arbeid som flytter lagerbeholdningen fra kvalitetskontroll til en ny lokasjon, basert på oppsettet for lokasjonsdirektiv.

### <a name="work-classes-location-directives-and-work-templates"></a>Arbeidsklasser, lokasjonsdirektiver og arbeidsmaler

Arbeidsordretypene _Kvalitetsvareprøver_ og _Kvalitetsordre_ brukes av lokasjonsdirektiver, arbeidsklasser og arbeidsmaler.

Før lagerarbeidet kan genereres automatisk for å flytte lager til kvalitetskontroll, må du følge disse trinnene for å konfigurere systemet.

1. Opprett separate arbeidsklasser for arbeidsordretypene _Kvalitetsvareprøver_ og _Kvalitetsordre_. På denne måten sikrer du at riktig arbeid kan genereres automatisk basert på de to arbeidsordretypene, og at dette arbeidet kan kjøres ved hjelp av mobilappen Lagerstyring.
1. Definer en arbeidsmal for hver arbeidsordretype:

    - Definer en arbeidsmal som bruker arbeidsordretypen _Kvalitetsvareprøver_ til automatisk å flytte registrert lager til en kvalitetskontroll-lokasjon.
    - Definer en arbeidsmal som bruker arbeidsordretypen _kvalitetsordre_ til å flytte lager til en kvalitetskontroll-lokasjon etter at kvalitetskontrollen er fullført.

1. For hver arbeidsordretype definerer du lokasjonsdirektiver som bruker de riktige kvalitetskontroll-stedene som lageret skal flyttes til. Etter at kvalitetskontroll er fullført, sikrer lokasjonsdirektivet for arbeidsordretypen _kvalitetsordre_ at det blir valgt en ny mållokasjon, slik at lageret kan flyttes ut av kvalitetskontroll-lokasjonen.
1. Definer de relevante menyelementene for mobilenhet for å støtte flytting av mottatt lager til kvalitetskontroll-lokasjonen, og flyttingen av lagerbeholdning som består eller ikke består kvalitetskontroll fra kvalitetskontroll-lokasjonen til en ny lokasjon.

Hvis du vil ha et trinnvis eksempel som viser hvordan du fullfører dette oppsettet, kan du se [eksempelscenariet](#example-scenario) på slutten av dette emnet.

## <a name="enable-a-warehouse-for-quality-management"></a>Aktivere et lager for kvalitetsstyring

Før funksjonen _Kvalitetsstyringen for lagerprosesser_ kan brukes for et bestemt lager, må du følge disse trinnene for å gjøre funksjonen tilgjengelig for dette lageret.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
1. Velg lageret som skal aktivereres for kvalitetsstyring.
1. I hurtigfanen **Lager** setter du alternativet **Aktiver kvalitetsordre for lagerprosesser** til _Ja_. (Merk at dette alternativet bare kan settes til _Ja_ for lagre som bruker lagerstyringsprosesser.)

Når alternativet **Aktiver kvalitetsordre for lagerprosesser** er satt til _Ja_, kontrollerer kvalitetstilknytningsoppsettet om funksjonen _Kvalitetsstyring for lagerprosesser_ faktisk brukes for det valgte lageret. Du kan når som helst endre innstillingen for alternativet _Nei_. I så fall gjelder ikke funksjonen lenger for lageret, uansett hvilket kvalitetstilknytningsoppsett som er definert.

## <a name="quality-control"></a>Kvalitetskontroll

Funksjonen _Kvalitetsstyring for lagerprosesser_ styrer flere nøkkelinnstillinger for kvalitetstilknytninger og vareprøver.

### <a name="quality-associations"></a>Kvalitetstilknytninger

Hver [kvalitetstilknytningspost](enable-quality-management.md) definerer dessuten settet med tester, det akseptable kvalitetsnivået og sampling-planen som gjelder for kvalitetsordrene som genereres. Hvis du vil konfigurere en kvalitetstilknytningspost, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetstilknytninger**.
1. Opprett eller velg kvalitetstilknytningsposten for varen eller gruppen du arbeider med, eller for alle varer.
1. I hurtigfanen **Betingelser** angir du **Gjeldende lagertype**-feltet til én av følgende verdier:

    - **Kvalitetsstyring bare for lagerprosesser** – Aktiver funksjonen _Kvalitetsstyring for lagerprosesser_. Du kan bare velge denne verdien hvis referansetypen er enten *Innkjøp* eller *Produksjon*.
    - **Alle** – Deaktiver funksjonen _Kvalitetsstyring for lagerprosesser_. Velg denne verdien for alle referansetyper unntatt *Innkjøp* og *Produksjon*.

> [!NOTE]
> Funksjonen _Kvalitetsstyring for lagerprosesser_ trer bare i kraft hvis varen på kildedokumentlinjen bruker avanserte lagerstyringsprosesser, og hvis alternativet **Aktiver kvalitetsordre for lagerprosesser** er satt til _Ja_ for lageret på kildedokumentlinjen.

Etter hvert som hver vare blir registrert (eller ferdigmeldt), bestemmer systemet hvilke kvalitetstilknytninger som skal gjelde for den.

Når funksjonen _Kvalitetsstyring for lagerprosesser_ er aktivert, blir den aktuelle lagertypen logisk satt inn i den fjerde søkegruppen i søkehierarkiet for kvalitetstilknytning. Tabellen nedenfor gir en logisk representasjon av søkehierarkiet.

| Søkegruppe | beskrivelse |
|---|---|
| Gruppe 1 | For hver kvalitetstilknytning kontrollerer du verdiene **Referansetype**, **Hendelsestype** og **Utførelsessamsvar** mot varen. Hvis det er et samsvar mot kildedokumentlinjen, går du til gruppe 2. |
| Gruppe 2 | For hver kvalitetstilknytning kontrollerer du **Varekode**-verdien (_Tabell_, _Gruppe_ eller _Alle_) mot varen. _Tabell_ er mer spesifikk enn _Gruppe_, og _Gruppe_ er mer spesifikk enn _Alle_. Hvis det er et samsvar for _Tabell_ (en bestemt vare), går du videre til gruppe 3. Hvis det ikke er samsvar for _Tabell_, kan du søke etter et samsvar for _Gruppe_. Hvis det ikke er samsvar for _Gruppe_, gjelder _Alle_. Hvis det finnes et samsvar, går du videre til gruppe 3. |
| Gruppe 3 | For hver kvalitetstilknytning kontrollerer du **Kontokode**- og **Ressurskode**-verdiene mot varen. Logikken som brukes, ligner på logikken som brukes for **Varekode**-verdien. |
| Gruppe 4 | For hver kvalitetstilknytning kontrollerer du **Gjeldende lagertype**-verdi (_Kvalitetsstyring bare for lagerprosesser_ eller _Alle_) mot varen. Hvis alternativet **Aktiver kvalitetsordre for lagerprosesser** er satt til _Ja_ for lageret i kildedokumentet, og varen på kildedokumentlinjen er satt til _Bruk lagerstyringsprosesser_, vil begge tilknytningene der det er et samsvar for _Kvalitetsstyring bare for lagerprosesser_, og tilknytninger der det er et samsvar for _Alle_, bli brukt parallelt, hvis begge finnes. Hvis alternativet **Aktiver kvalitetsordre for lagerprosesser** er satt til _Nei_ for lageret i kildedokumentet, og varen i kildedokumentlinjen er satt til _Bruk lagerstyringsprosesser_, brukes bare kvalitetsstyring. |

Du har for eksempel definert et lager der alternativet **Aktiver kvalitetsordre for lagerprosesser** er satt til _Ja_, og du har to kvalitetstilknytninger som er definert for *Innkjøp*-referansetypen: én for alle varer og én for *Registrering*-hendelsestypen. Den eneste forskjellen mellom de to kvalitetstilknytningene er verdien **Gjeldende lagertype**: Den settes til _Alle_ for én kvalitetstilknytning og _Kvalitetsstyring bare for lagerprosesser_ for den andre. I dette tilfellet er begge kvalitetstilknytningene like spesifikke, og begge kan brukes.

Verdien i **Testgruppe**-feltet for kvalitetstilknytningene er også en faktor. Dette feltet definerer testprosedyren som må utlignes. Hvis **Testgruppe** -verdien er den samme for begge tilknytninger, opprettes bare en kvalitetsordre, for kvalitetstilknytningen der **Gjeldende lagertype**-verdien er _Kvalitetstyring bare for lagerprosesser_. Hvis **Testgruppe**-verdien ikke er det samme for begge tilknytningene, blir det opprettet to kvalitetsordrer. Den første kvalitetsordren opprettes for kvalitetstilknytningen der **Gjeldende lagertype**-verdi er _Kvalitetsstyring bare for lagerprosesser_. Den andre kvalitetsordren opprettes for kvalitetstilknytningen der **Gjeldende lagertype**-verdi er _Alle_.

> [!NOTE]
> Verdien _Kvalitetsstyring for lagerprosesser_ anses for mer spesifikk enn _Alle_ når kriteriene for kvalitetstilknytningene for gruppe 1 og 2 er like, og når testgruppen er den samme. To kvalitetsordrer vil bare bli opprettet når testgruppene er forskjellige.

#### <a name="reference-types"></a>Referansetyper

Når **Referansetype**-verdien er _Innkjøp_, og **Gjeldende lagertype**-verdien er _Kvalitetsstyring bare for lagerprosesser_, må feltet **Hendelsestype** på hurtigfanen **Prosess** settes til _Registrering_. _Registrering_ er den eneste hendelsestypen som støttes for _Innkjøp_-referansetypen når du bruker funksjonen _Kvalitetsstyring for lagerprosesser_.

#### <a name="quality-processing-policy"></a>Policy for kvalitetsbehandling

Funksjonen _Kvalitetsstyring for lagerprosesser_ gjør det mulig å opprette arbeid bare basert på vareprøve. Derfor tillates det for en lett prosess. Lagerbeholdningen som arbeid opprettes for, er avhengig av vareprøven som er knyttet til kvalitetstilknytningen. Når den lette prosessen brukes, kan kvalitetsavdelingen manuelt opprette en kvalitetsordre hvis en kvalitetsordre kreves, når en arbeider setter antallet inn i kvalitetskontroll-lokasjonen.

Feltet **Policy for kvalitetsbehandling** på hurtigfanen **Kvalitetsordreprosess** styrer om en kvalitetsordre også opprettes når det opprettes arbeid for å flytte en vare til kvalitetsstyringslokasjonen. Dette feltet kan defineres til _Opprett kvalitetsordre_ eller _Opprett bare arbeid_. Standardverdien er _Opprett kvalitetsordre_.

> [!NOTE]
> Uansett om du oppretter kvalitetsordrer manuelt eller automatisk, genererer systemet automatisk arbeid for å flytte varer ut av kvalitetskontroll-lokasjonen når kvalitetsordren merkes som validert.

Opprettelsen av kvalitetsordrearbeid er ikke relatert til kvalitetstilknytningsoppsettet. Hvis det finnes en arbeidsmal som har en **Arbeidsordretype**-verdi på *Kvalitetsordre*, og hvis spørringskriteriene er oppfylt for den arbeidsmalen, vil valideringen av en kvalitetsordre utløse opprettelsen av kvalitetsordrearbeid.

#### <a name="referenced-item-sampling"></a>Referert vareprøve

Hver kvalitetstilknytning må referere til en vareprøve. En vareprøve definerer antallet som skal sendes for kvalitetskontroll. Den kan defineres slik at den bare gjelder for kvalitetstilknytninger der **Gjeldende lagertype**-verdi er _Kvalitetsstyring bare for lagerprosesser_. Hvis **Vareprøveområde**-verdien for en vareprøve er _Last_ eller _Forsendelse_, eller **Spesifikasjon av antall**-verdien er _Fullstendig nummerskilt_, kan vareprøven bare refereres til av kvalitetstilknytninger der **Gjeldende lagertype**-verdien er _Kvalitetsstyring bare for lagerprosesser_.

Hvis du definerer en vareprøve som bruker den gjeldende lagertypen _Kvalitetsstyring bare for lagerprosesser_, vil du få en feilmelding hvis du prøver å referere til den fra en kvalitetstilknytning som ikke bruker funksjonen _Kvalitetsstyring for lagerprosesser_.

> [!NOTE]
> Vareprøver som bruker full blokkering, støttes ikke for kvalitetstilknytninger der **Gjeldende lagertype**-feltet er satt til _Kvalitetsstyring bare for lagerprosesser_.

### <a name="item-sampling"></a>Vareprøve

Vareprøver styrer hvor ofte varer sendes for kvalitetskontroll. Funksjonen _Kvalitetsstyring for lagerprosesser_ innfører begrepet _vareprøveområde_. Systemet bruker vareprøveområdet når det vurderer om og hvordan kvalitetsordrer og/eller kvalitetsvareprøver fungerer og kvalitetsordrearbeid skal opprettes.

Hvis du vil definere vareprøve, går du til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Vareprøver**, og angir **Vareprøveområde**-feltet til en av følgende verdier:

- **Ordre** – Kildedokumentlinjen blir grunnlaget for å vurdere om og hvordan kvalitetsordrer og/eller kvalitetsvareprøver fungerer og kvalitetsordrearbeid opprettes. Denne verdien er standardverdien, og når den er valgt, fungerer systemet på samme måte som det fungerer når funksjonen _Kvalitetsstyring for lagerprosesser_ ikke er aktivert.
- **Last** – Laster vil bli brukt som grunnlag for å evaluere om og hvordan en kvalitetsordre og/eller arbeid blir opprettet. Denne verdien er bare tilgjengelig når funksjonen _Kvalitetsstyring for lagerprosesser_ er aktivert.
- **Forsendelse** – Forsendelser vil bli brukt som grunnlag for å evaluere om og hvordan en kvalitetsordre og/eller arbeid blir opprettet. Denne verdien er bare tilgjengelig når funksjonen _Kvalitetsstyring for lagerprosesser_ er aktivert.

> [!NOTE]
> Når feltet **Vareprøveområde** er satt til *Last* eller *Forsendelse*, brukes belastningsenheten og forsendelsesenhetene, hvis de er tilgjengelige. Hvis de ikke er tilgjengelige, vil ordreenheten bli brukt.

Funksjonen _Kvalitetsstyring for lagerprosesser_ introduserer også *Fullstendig nummerskilt*-verdien for **Spesifikasjon av antall**-feltet. Denne verdien støtter oppretting av kvalitetsordrearbeid og samplingsarbeid for kvalitetsvare, basert på nummerskilt. Når du velger denne verdien, skjer følgende endringer:

- Alternativet **Pausetelling etter vare** og feltet **Per n-te nummerskilt** i **Prosess**-hurtigfanen blir tilgjengelige.
- **Verdi**-feltet i hurtigfanen **Prøvemengde** blir utilgjengelig.
- Alternativene **Per oppdatert antall**, **Lokasjon** og **Nummerskilt** er satt til *Ja,* og innstillingene kan ikke endres.

Alternativet **Pausetelling etter vare** kontrollerer om nummerskiltantallet evalueres per vare eller på tvers av alle varer i prøveområdet. Produktvarianter behandles som samme vare. Dette alternativet kontrollerer også om antallet nummerskilt er tilbakestilt for hver vare.

Verdien for feltet **Per n-te nummerskilt** styrer hvor ofte kvalitetsordreropprettes i forbindelse med antall varer som er registrert. Verdien *3* vil for eksempel sende hver tredje vare til kvalitetskontroll, og begynne med den første varen. Verdien må være over 0 (null).

Mens arbeidere mottar varer ved hjelp av mobilappen Lagerstyring, validerer systemet om det er satt opp en kvalitetstilknytning for hver innkommende vare. Hvis en kvalitetstilknytning er definert, bruker systemet vareprøveposten som er konfigurert for denne kvalitetstilknytningen, til å bestemme hvordan den skal opprette kvalitetsordrer, samplingsarbeid for kvalitetsvare og bestillingsarbeid.

> [!NOTE]
> Når mottaksregistrering utføres i webklienten (ved å bruke den lille registreringssiden eller vareankomst-journalen for bestillingslinjer), blir ingen samplingsarbeid for kvalitetsvare eller bestillingsarbeid opprettet, uavhengig av oppsettet. I stedet vil den refererte vareprøven bare brukes til å kontrollere opprettelsen av kvalitetsordrer for varer som samsvarer med en kvalitetstilknytning.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Eksempler på automatisk generering av kvalitetsordrer

Eksemplene nedenfor viser hvordan oppsettet til en kvalitetstilknytning og et tilknyttet vareutvalg påvirker genereringen av kvalitetsordrer når **Gjeldende lagertype**-feltet er satt til _Kvalitetsstyring bare for lagerprosesser_.

Når **Spesifikasjon av antall**-verdien er _Fullstendig nummerskilt_, styrer feltet **Per n-te nummerskilt** hvilke nummerskilt det opprettes en vareprøvearbeid for. Det første nummerskiltet går alltid til kvalitetskontroll, og deretter angir verdien i dette feltet at hvert *n*-te nummerskilt etter dette nummerskiltet også skal gå.

**Referansetype**-verdien for følgende eksempler er _Innkjøp_ og **Hendelsestype**-verdien er *Registrering*.

| Prøveomfang | Spesifikasjon av antall | Per oppdatert mengde | Per lagringsdimensjon | Stopp telling basert på vare | Per n-te nummerskilt | Resultat |
|---|---|---|---|---|---|---|
| Bestilling | Fullstendig nummerskilt | Ja _(låst/ikke redigerbart)_ | <p>Sted: Ja</p><p>Nummerskilt: Ja _(låst/ikke redigerbart)_</p> | Ingen | 3 | <p>**Ordrelinjeantall: 100 EA**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 20 EA</p><p>Kvalitetsordre 1 for 20 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP2<p>Bestillingsarbeid for 20 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP3<p>Bestillingsarbeid for 20 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP4<p>Samplingsarbeid for kvalitetsvare for 20 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP5<p>Bestillingsarbeid for 20 EA (plassering)</p></li></ol> |
| Rekkefølge | Fast antall = 1 | Ja | <p>Sted: Ja</p><p>Nummerskilt: Ja</p> | Nei | Gjelder ikke | <p>**Ordrelinjeantall: 100**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Bestillingsarbeid for 19 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP2<p>Samplingsarbeid for kvalitetsvare for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Bestillingsarbeid for 19 (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP3<p>Samplingsarbeid for kvalitetsvare for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Bestillingsarbeid for 19 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP4<p>Samplingsarbeid for kvalitetsvare for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Bestillingsarbeid for 19 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 20 EA, LP5<p>Samplingsarbeid for kvalitetsvare for 1 EA</p><p>Kvalitetsordre 1 for 1 EA</p><p>Bestillingsarbeid for 19 EA (plassering)</p></li></ol> |
| Bestilling | Prosent = 10 | Nei | <p>Lokasjon: Nei</p><p>Nummerskilt: Nei</p> | Nei | Gjelder ikke | <p>**Ordrelinjeantall: 100 EA**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 10 EA</p><p>Kvalitetsordre 1 for 10 EA</p><p>Bestillingsarbeid for 40 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP2<p>Bestillingsarbeid for 50 EA (plassering)</p></li></ol> |
| Belastning | Prosent = 5 | Ja _(låst/ikke redigerbart)_ | <p>Lokasjon: Nei</p><p>Nummerskilt: Nei</p> | Nei | Gjelder ikke | <p>**Ordrelinjeantall: 500 EA**</p><p>**To laster: første last 200 EA, andre last 300 EA**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for første last for 100 EA<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 95 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for første last for 100 EA<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 95 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for andre last for 300 EA<p>Samplingsarbeid for kvalitetsvare for 15 EA</p><p>Kvalitetsordre 1 for 15 EA</p><p>Bestillingsarbeid for 285 EA (plassering)</p></li></ol> |
| Rekkefølge | Prosent = 10 | Ja | <p>Sted: Ja</p><p>Nummerskilt: Ja</p> | Ingen | Gjelder ikke | <p>**Ordrelinjeantall: 100**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 45 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP2<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 45 (plassering)</p></li></ol> |
| Belastning | Fullstendig nummerskilt | Ja _(låst/ikke redigerbart)_ | <p>Sted: Ja</p><p>Nummerskilt: Ja _(låst/ikke redigerbart)_</p> | Nei | 3 | <p>**To varer:**</p><ul><li>**Ordrelinjeantall for vare A: 120 EA (4 paller)**</li><li>**Ordrelinjeantall for vare B: 90 EA (3 paller)**</li></ul><p>**Én belastning, to belastningslinjer med hver ordrelinje**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP2<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP3<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP4<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare B, 30 EA, LP5<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare B, 30 EA, LP6<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP7<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li></ol> |
| Belastning | Fullstendig nummerskilt | Ja _(låst/ikke redigerbart)_ | <p>Sted: Ja</p><p>Nummerskilt: Ja _(låst/ikke redigerbart)_</p> | Ja | 3 | <p>**To varer:**</p><ul><li>**Ordrelinjeantall for vare A: 120 EA (4 paller)**</li><li>**Ordrelinjeantall for vare B: 90 EA (3 paller)**</li></ul><p>**Én belastning, to belastningslinjer med hver ordrelinje**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP2<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP3<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP4<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare B, 30 EA, LP5<p>Samplingsarbeid for kvalitetsvare for 30 EA</p><p>Kvalitetsordre 1 for 30 EA</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare B, 30 EA, LP6<p>Bestillingsarbeid for 30 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for vare A, 30 EA, LP7<p>Bestillingsarbeid for 30 EA (plassering)</p></li></ol> |
| Belastning | Prosent = 10 | Ja _(låst/ikke redigerbart)_ | <p>Lokasjon: Nei</p><p>Nummerskilt: Nei</p> | Nei | Gjelder ikke | <p>**Ordrelinjeantall: 100 EA**</p><p>**Ingen belastninger opprettes. Ordreområde brukes.**</p><ol><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP1<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 45 EA (plassering)</p></li><li>Registrer mottak i mobilappen Lagerstyring for 50 EA, LP2<p>Samplingsarbeid for kvalitetsvare for 5 EA</p><p>Kvalitetsordre 1 for 5 EA</p><p>Bestillingsarbeid for 45 EA (plassering)</p></li></ol> |

Når en arbeider validerer en av kvalitetsordrene som vises i den forrige tabellen, genererer systemet automatisk kvalitetsordrearbeid for å flytte lagerbeholdningen fra kvalitetskontroll-lokasjonen til lokasjonen som er definert i lokasjonsdirektivet for arbeidsordretypen _Kvalitetsordre_. Du kan definere en hvilken som helst lokasjon for dette formålet, for eksempel en retur- eller lagringslokasjon, avhengig av testresultatet for kvalitetsordren. Hvis du vil ha et eksempel på dette oppsettet, kan du se [eksempelscenarioet](#example-scenario) på slutten av dette emnet.

Du kan åpne en kvalitetsordre som allerede er validert, på nytt, forutsatt at kvalitetsordrearbeidet som er knyttet til flytting av lageret fra kvalitetskontroll-lokasjonen, ikke har **Arbeidsstatus**-verdien *Lukket* eller *Pågår*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Behandle innsikter når flere kvalitetstilknytninger eksisterer

Mer enn én kvalitetstilknytning kan defineres for og brukes på den samme kildedokumentlinjen, og **Gjeldende lagertype**-feltet kan settes til _Kvalitetsstyring bare for lagerprosesser_ for noen av disse kvalitetstilknytningene og _Alle_ for andre.

I følgende eksempel er **Referansetype**-verdien _Innkjøp_.

1. Den første kvalitetstilknytningen er satt opp på følgende måte:

    - **Gjeldende lagertype:** *Kvalitetsstyring bare for lagerprosesser*
    - **Varekode:** *A0001*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Omslutning*
    - **Vareprøve:** *5 stk.*

1. Den andre kvalitetstilknytningen er satt opp på følgende måte:

    - **Gjeldende lagertype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Omslutning*
    - **Vareprøve:** *1 stk.*

1. Den tredje kvalitetstilknytningen er satt opp på følgende måte:

    - **Gjeldende lagertype:** *Kvalitetsstyring bare for lagerprosesser*
    - **Varekode:** *Alle*
    - **Kontokode:** *104*
    - **Testgruppe:** *Impedans*
    - **Vareprøve:** *Hvert andre nummerskilt* (Denne innstillingen betyr at første, tredje, femte og så videre nummerskilt som mottas, vil opprette en kvalitetsordre.)

1. Den fjerde kvalitetstilknytningen er satt opp på følgende måte:

    - **Gjeldende lagertype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Impedans*
    - **Vareprøve:** *5 stk.*

1. Den femte kvalitetstilknytningen er satt opp på følgende måte:

    - **Gjeldende lagertype:** *Alle*
    - **Varekode:** *Alle*
    - **Kontokode:** *Alle*
    - **Testgruppe:** *Kjegle*
    - **Vareprøve:** *10 %*

En bestilling for et antall på 10 av varen A0001 er nå opprettet for leverandør 104. Deretter registreres en bestillingslinje med antallet 10 som mottatt på et nummerskilt, ved hjelp av mobilappen Lagerstyring. Her er resultatet:

- Det er én kvalitetsordre fra den første kvalitetstilknytningen for *Omslutning*-testgruppen. Antallet er 5. Det finnes ingen kvalitetsordre fra den andre kvalitetstilknytningen, fordi kriteriene for den første kvalitetstilknytningen er mer spesifikk i forhold til *Omslutning*-testgruppen.
- Det er én kvalitetsordre fra den tredje kvalitetstilknytningen for *Impedans*-testgruppen. Antallet er 10. Det finnes ingen kvalitetsordre fra den fjerde kvalitetstilknytningen, fordi kriteriene for den første kvalitetstilknytningen er mer spesifikk i forhold til *Impedans*-testgruppen.
- Det er én kvalitetsordre fra den femte kvalitetstilknytningen for *Kjegle*-testgruppen. Antallet er 1.

I forbindelse med opprettelsen av én kvalitetsordre for hver av de tre kvalitetstilknytningene, opprettes også samplingsarbeid for kvalitetsvare. Det registrerte antallet er bare 10. På grunn av vareprøveoppsettet er imidlertid summen av kvalitetsordreantallet som er opprettet for den gjeldende lagertypen *Kvalitetsstyring bare for lagerprosesser* 16, som overskrider det fysisk registrerte antallet på 10. Derfor opprettes ikke arbeid for ordreantallet for full kvalitet (16), fordi bare 10 er fysisk tilgjengelig for flytting til kvalitetskontroll-lokasjonen. Prioriteten som brukes til å opprette samplingsarbeidet for kvalitetsvare, følger rekkefølgen for opprettingen av kvalitetsordre:

- **Første kvalitetsordre (antall = 5):** Samplingsarbeid for kvalitetsvare opprettes for 5. Et antall på 5 (10 – 5) beholdes nå for senere oppretting av samplingsarbeid for kvalitetsvare.
- **Andre kvalitetsordre (antall = 10):** Samplingsarbeid for kvalitetsvare opprettes for 5. Et antall på 0 (null) beholdes nå for senere oppretting av samplingsarbeid for kvalitetsvare.
- **Tredje kvalitetsordre (antall = 1):** Ingen samplingsarbeid for kvalitetsvare opprettes.

Som en del av prosessen med å opprette kvalitetsordrer, opprettes det en lagersperring av et antall på 10. Det blir referert til denne lagerblokkeringen mot hver av de tre kvalitetsordrene. Summen av kvalitetsordreantallet er 16.

Når kvalitetsordrene er validerert, prøver systemet å opprette kvalitetsordrearbeid for hver kvalitetsordre som er validert. Fordi summen av kvalitetsordreantallet overskrider antallet som faktisk er sperret og derfor tilgjengelig for arbeidsopprettelse, kan ikke kvalitetsordrearbeid opprettes for ordreantall i full kvalitet, som vist her. (Dette eksemplet er en fortsettelse av det forrige eksemplet.)

1. **Valider den andre kvalitetsordren som opprettes (antall = 10). Det opprettes kvalitetsordrearbeid for et antall på 4.**

    Opprettelsen av kvalitetsordrearbeid utløses av en endring i lagerblokkeringsantallet. Fordi summen av kvalitetsordreantallet var 16, vil validering av et antall på 10 føre til at gjenstående kvalitetsordreantall valideres som lik 6. Lagerblokkeringsantallet er redusert fra 10 til 6. Det reduserte antallet på 4 er tilordnet til opprettelse av kvalitetsordrearbeid.

2. **Valider den første kvalitetsordren som opprettes (antall = 5). Det opprettes kvalitetsordrearbeid for et antall på 5.**

    Opprettelsen av kvalitetsordrearbeid utløses av en endring i lagerblokkeringsantallet. Fordi summen av kvalitetsordreantallet var 6, vil validering av et antall på 5 føre til at gjenstående kvalitetsordreantall valideres som lik 1. Lagerblokkeringsantallet er redusert fra 6 til 1. Det reduserte antallet på 5 er tilordnet til opprettelse av kvalitetsordrearbeid.

3. **Valider den tredje kvalitetsordren som opprettes (antall = 1). Det opprettes kvalitetsordrearbeid for et antall på 1.**

    Opprettelsen av kvalitetsordrearbeid utløses av en endring i lagerblokkeringsantallet. Fordi summen av kvalitetsordreantallet var 1, vil validering av et antall på 1 føre til at gjenstående kvalitetsordreantall valideres som lik 0 (null). Lagerblokkeringen fjernes (det vil si at lagerblokkeringsantallet reduseres fra 1 til 0). Det reduserte antallet på 1 er tilordnet til opprettelse av kvalitetsordrearbeid.

> [!NOTE]
> Opprettelsen av kvalitetsordrearbeid er avhengig av lagerblokkeringsantallet som refereres mot én eller flere kvalitetsordrer. Hvis summen av kvalitetsordreantallet overskrider det refererte lagerblokkeringsantallet, vil rekkefølgen som kvalitetsordrene valideres i, bestemme opprettelsen av kvalitetsordrearbeid.

## <a name="canceling-quality-item-sampling-work"></a>Avbryte samplingsarbeid for kvalitetsvare

Du kan avbryte arbeidet som er opprettet for sampling for kvalitetsvare. Følg denne fremgangsmåten for å kontrollere hva som skjer når dette arbeidet er avbrutt.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Generelt** i **Arbeid**-hurtigfanen angir du alternativet **Opphev registrering av mottak ved avbryting av arbeid** til en av følgende verdier:

    - **Ja** – Når samplingsarbeidet for kvalitetsvare avbrytes, slettes den tilknyttede kvalitetsordren, og beholdningen avregistreres.
    - **Nei** – Når samplingsarbeidet for kvalitetsvare avbrytes, slettes ikke den tilknyttede kvalitetsordren, og beholdningen avregistreres ikke.

## <a name="cross-docking"></a>Direkteoverføring

Du kan ha et kvalitetstilknytningsoppsett som oppretter vareprøvearbeid. Men når det finnes direkteoverføring i parallell med en kvalitetstilknytning som oppretter samplingsarbeid for kvalitetsvare, hvis det bare er nok mengde til å oppfylle direkteoverføring, opprettes bare vareprøvearbeid. I tilfeller der alternativet **Aktiver kvalitets ordre for lager prosesser** er satt til _Ja_ for det mottakende lageret, og **Gjeldende lagertype**-feltet er satt til _Kvalitetsstyring bare for lagerprosesser_ for en kvalitetstilknytning, vil opprettelsen av samplingsarbeidet for kvalitetsvare ha prioritet over oppretting av direkteoverføringsarbeid. Hvis antallet overstiger kravene for direkteoverføring, oppretter systemet fremdeles bare vareprøvearbeid.

## <a name="destructive-testing"></a>Destruktiv testing

Du kan definere en testgruppe som utfører destruktiv testing. Når det gjelder en destruktiv test, er forutsetningen at, uavhengig av testresultatet, antallet av varen som testes, vil bli ødelagt som en del av testen. Måten funksjonen _Kvalitetsstyring for lagerprosesser_ støtter destruktiv testing på, ligner på måten kvalitetsstyring støtter det på når funksjonen ikke er aktivert. Før kvalitetsordren kan valideres, må kvalitetskontrolløren angi plukklokasjonen for antallet som er ødelagt. Du kan registrere plukking fra kvalitetsordresiden ved å velge **Lager \> Plukk** i handlingsruten. Når plukkingen for kvalitetsordreantallet er registrert, kan valideringen fullføres.

## <a name="example-scenario"></a>Eksempelscenario

### <a name="prepare-the-scenario"></a>Forberede scenariet

Hvis du vil jobbe gjennom dette scenariet, må du klargjøre systemet på følgende måte:

- Kontroller at du har installert demodata på systemet, og velg den juridiske enheten **USMF**.
- Aktivere _Kvalitetsstyring for lagerprosesser_ i [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurer lager 51 til å bruke funksjonen _Kvalitetsstyring for lagerprosesser_ ved å følge disse trinnene:

    1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lagre**.
    1. Velg lager 51.
    1. I hurtigfanen **Lager** setter du alternativet **Aktiver kvalitetsordre for lagerprosesser** til *Ja*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Oppsett av kvalitet inn – Gå til kvalitetskontroll-lokasjonen

Du må nå forberede et grunnleggende oppsett som gjør det mulig for systemet å støtte funksjonen _Kvalitetsstyring for lagerprosesser_ for lager 51. (Demonstrasjonsdataene definerer en lokasjon for kvalitetsstyring som heter *QMS*. Det finnes en referanse til denne plasseringen flere ganger i dette scenariet.) Du vil forberede følgende elementer, som beskrevet i underdelene av denne delen:

- Arbeidsklasse
- Arbeidsmal
- Lokasjonsdirektiv
- Vareprøve
- Kvalitetstilknytning
- Menyelementer på mobilenheten

#### <a name="work-class-for-quality-in"></a>Arbeidsklasse for kvalitet inn

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. Opprett en arbeidsklasse, og angi følgende verdier:

    - **Arbeidsklasse-ID:** _QualityIn_
    - **Beskrivelse:** _Samplingsarbeid for kvalitetsvare_
    - **Arbeidsordretype** _Sampling av kvalitetsvare_

#### <a name="work-template"></a>Arbeidsmal

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Sett **Arbeidsordretype**-feltet til _Samling av kvalitetsvare_.
1. Opprett en arbeidsmal, og angi følgende verdier:

    - **Arbeidsmal:** _51 kvalitet_
    - **Beskrivelse av arbeidsmal:** _51 kvalitet_

1. Legg til en linje i arbeidsmalen, og angi følgende verdier:

    - **Arbeidstype:** _Plukk_
    - **Arbeidsklasse-ID:** _QualityIn_

1. Legg til en ny linje i arbeidsmalen, og angi følgende verdier:

    - **Arbeidstype:** _Plasser_
    - **Arbeidsklasse-ID:** _QualityIn_

#### <a name="location-directive"></a>Lokasjonsdirektiv

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Sett **Arbeidsordretype**-feltet til _Samling av kvalitetsvare_.
1. Opprett et lokasjonsdirektiv, og angi følgende verdier:

    - **Navn:** _51 til kvalitet_
    - **Arbeidstype:** _Plasser_
    - **Område:** 5
    - **Lager:** _51_

1. Legg til en linje for lokasjonsdirektivet, og angi følgende verdier:

    - **Fra-antall:** _1_
    - **Til antall:** _1000000_

1. Opprett en lokasjonsdirektivhandling, og angi følgende verdi:

    - **Navn:** _Kvalitet_

1. Velg **Rediger spørring** for den nye lokasjonsdirektivhandlingen, og angi en **Område**-post med følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Felt:** _ID for lokasjonsprofil_
    - **Vilkår:** *QMS*

1. Velg **OK** for å lagre spørringen, og lagre det nye lokasjonsdirektivet.

Deretter må du endre rekkefølgen til de eksisterende lokasjonsdirektivene for bestilling for lager 51. Demonstrasjonsdataene inneholder to lokasjonsdirektiver som har en **Arbeidsordretype**-verdi på _Innkjøp_: en har navnet _51 QMS_, og den andre kalles _51 PO Direct_ Hvis du vil være sikker på at funksjonen *Kvalitetsstyring for lagerprosesser* brukes på lager 51, må du kontrollere at lokasjonsdirektivet _51 QMS_ ikke brukes. I stedet for å slette dette stedsdirektivet (fordi du kanskje vil bruke det senere), kan du imidlertid bare endre rekkefølgen.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Sett _Arbeidsordretype_-feltet til **Bestilling**.
1. I sekvenslisten velger du sekvensnummer 5 for lokasjonsdirektivet _51 PO Direct_.
1. Flytt den valgte sekvensen opp til sekvensnummer 4.
1. Kontroller at sekvensnummeret til _51 QMS_-lokasjonsdirektivet nå er minst 5.

#### <a name="item-sampling"></a>Vareprøve

Funksjonen _Kvalitetsstyring for lagerprosesser_ legger til noen nye vareprøvefunksjoner. Verdien for **Prøveomfang** kan nå være _Ordre_, _Forsendelse_ eller _Last_, og verdien for **Samplingsantall** kan nå være _Fullstendig nummerskilt_.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Vareprøve**.
1. Opprett en vareprøvepost, og angi følgende verdier:

    - **Vareprøve:** _Tredje LP_
    - **Beskrivelse:** _Hvert tredje nummerskilt_
    - **Prøveomfang:** _Ordre_

1. I hurtigfanen **Samplingsantall** setter du **Spesifikasjon av antall**-feltet til _Fullstendig nummerskilt_.
1. I hurtigfanen **Prosess** setter du feltet **Per n-te nummerskilt** til _3_.
1. I delen **Per lagerdimensjon** aktiverer du både **Lager** og **Lagerstatus**.

#### <a name="quality-associations"></a>Kvalitetstilknytninger

Opprett en kvalitetstilknytning som vil bruke den nye vareprøven.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Kvalitetstilknytninger**.
1. Opprett en kvalitetstilknytningspost, og angi følgende verdier:

    - **Referansetype:** _Innkjøp_
    - **Varekode:** _Tabell_
    - **Vare:** _M9201_
    - **Område:** _5_

1. I hurtigfanen **Prosess** setter du feltet **Hendelstype** til *Registrering*.
1. I hurtigfanen **Betingelser** angir du **Gjeldende lagertype**-feltet til *Kvalitetsstyring bare for lagerprosesser*.
1. I hurtigfanen **Kvalitetsordreprosess** setter du feltet **Policy for kvalitetsbehandling** til _Opprett kvalitetsordre_.
1. I hurtigfanen **Spesifikasjoner** høyreklikker du i **Testgruppe**-feltet, og deretter velger du **Vis detaljer** for å åpne siden **Testgrupper**.
1. Opprett en testgruppe på siden **Testgruppe** i fanen **Oversikt** i det øvre rutenettet, og angi følgende verdier:

    - **Testgruppe:** _QMS_
    - **Beskrivelse:** _QMS-test_
    - **Akseptabelt antall:** _100_
    - **Vareprøve:** _Tredje LP_ (velg)

1. Legg til en post for en test i fanen **Oversikt** i det nedre rutenettet, og angi følgende verdier:

    - **Sekvens:** *1*
    - **Test:** *Omslutningsmåling*

1. I fanen **Test** i det nedre rutenettet angir du følgende verdier:

    - **Testvariabler:** *Bestått/mislykket*
    - **Standardresultat:** *Bestått*

1. Lagre den nye testgruppen, og lukk **Testgrupper**-siden.
1. Tilbake på siden **Kvalitetstilknytninger** i **Testgruppe**-feltet velger du **QMS**.
1. Lagre posten.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Menyelementer for mobilenhet for kvalitet inn

Hvis du vil fullføre oppsettet for å flytte varer til kvalitetskontroll-lokasjonen, må du gjøre samplingsarbeidet for kvalitetsvare tilgjengelig fra et menyelement for mobilenhet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg menyelementet for mobilenhet **Kjøpsplassering**.
1. På hurtigfanen **Arbeidsklasser** legger du til arbeidsklasse-IDen *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Sammendrag: Oppsettet for å flytte varer til kvalitetskontroll

Du har nå definert en kvalitetstilknytning som bruker funksjonen *Kvalitetsstyring for lagerprosesser* til å utløse opprettingen av en kvalitetsordre. Du har definert arbeids- og plasseringsdataene for lager 51 for å sikre at det opprettes bestemt arbeid når innkjøpsregistrering utføres for varen M9201. Dette oppsettet sikrer at hvert tredje nummerskilt som er registrert, blir flyttet til en kvalitetsplassering (_QMS_), og at det vil bli opprettet en kvalitetsordre for antallet nummerskilt. Alt annet vil bli flyttet til plassering i stedet for kvalitetskontroll-lokasjonen.

### <a name="process-quality-management-work"></a>Behandle kvalitetsstyringsarbeid

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Opprett en bestilling, og angi følgende verdier:

    - **Angi leverandørkonto:** *104*
    - **Lager:** *51*

1. Legg til en bestillingslinje, og angi følgende verdier:

    - **Vare:** *M9201*
    - **Antall:** *20*
    - **Enhet:** *ea*
    - **Lager:** *51*

1. Skriv ned bestillingsnummeret, slik at du kan bruke det senere.
1. Gå til en mobilenhet eller emulator som kjører mobilappen Lagerstyring, og logg på lager 51 ved å bruke *51* som bruker-ID og *1* som passord.
1. Gå til **Inngående \> kjøpsmottak**, og angi følgende verdier:

    - **Best.nr.:** Nummeret på bestillingen du nettopp opprettet
    - **Antall:** *5*
    - **Enhet:** *ea*

1. Fortsett å motta mot linjen, *5 ea* om gangen, til linjen er fullstendig mottatt. (Totalt fire nummerskilt blir opprettet.)
1. Logg av mobilappen Lagerstyring.
1. Tilbake i webklienten går du til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Finn og åpne bestillingen.
1. I delen **Bestillingslinjer** velger du linjen for varenummer *M9201*, og deretter velger du **Bestillingslinjer \> Arbeidsdetaljer**.
1. Legg merke til at andre og tredje arbeidshoder som ble opprettet, er vanlig plasseringsarbeid, mens de første og fjerde arbeidshodene er samplingsarbeid for kvalitetsvare. Dette resultatet er konsekvent med vareprøveoppsettet, som er konfigurert til å ta prøver fra hvert tredje nummerskilt.

#### <a name="move-to-the-quality-control-location"></a>Gå til kvalitetskontroll-plasseringen

Du vil nå flytte nummerskiltene til de angitte stedene. De første og fjerde nummerskiltene vil gå til kvalitetskontroll-plasseringen, mens andre og tredje nummerskilt går direkte til lagring.

1. Gå til en mobilenhet eller emulator som kjører mobilappen Lagerstyring, og logg på lager 51 ved å bruke *51* som bruker-ID og *1* som passord.
1. Gå til **Inngående \> Kjøpsplassering**, og plasser hvert nummerskilt fra den forrige fremgangsmåten helt til du har lukket alt arbeidet.

#### <a name="summary-process-quality-management-work"></a>Sammendrag: Behandle kvalitetsstyringsarbeid

Du har nå kjørt vareprøvearbeidet for kvalitetsvarer for første og fjerde nummerskilt ved å flytte dem til kvalitetskontroll-lokasjonen. Du har også plassert det andre og tredje nummerskiltet. Det neste trinnet er å foreta testing og kontroll av kvalitetsordren.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Oppsett av kvalitet: Gå fra kvalitetskontroll-plasseringen til lagring eller retur

Når arbeidere rapporterer resultater for kvalitetsordre, genererer systemet automatisk arbeid.

Du vil nå fortsette med det nødvendige grunnoppsettet for arbeidsklassen, arbeidsmalen og lokasjonsdirektivet for å aktivere kvalitetsstyring for lagerprosesser, slik at det nødvendige arbeidet kan opprettes for å flytte kvalitetsordreantallet fra kvalitetskontroll-lokasjonen til en bestemt lagerlokasjon.

#### <a name="work-class-for-quality-out"></a>Arbeidsklasse for kvalitet-ut

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsklasser**.
1. Opprett en arbeidsklasse, og angi følgende verdier:

    - **Arbeidsklasse-ID:** *QualityOut*
    - **Beskrivelse:** *Kvalitet ut*
    - **Arbeidsordretype:** *Kvalitetsordre*

#### <a name="work-templates"></a>Arbeidsmaler

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Endre verdien for **Arbeidsordretype** til *Kvalitetsordre*.
1. Opprett en arbeidsmal, og angi følgende verdier:

    - **Arbeidsmal:** *51 kvalitet ut*
    - **Beskrivelse av arbeidsmal:** *51 kvalitet ut*

1. Legg til en linje, og angi følgende verdier:

    - **Arbeidstype:** *Plukk*
    - **Arbeidsklasse-ID:** **QualityOut**

1. Legg til en ny linje, og angi følgende verdier:

    - **Arbeidstype:** *Plasser*
    - **Arbeidsklasse-ID:** *QualityOut*

#### <a name="location-directives"></a>Lokasjonsdirektiver

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Endre verdien for **Arbeidsordretype** til *Kvalitetsordre*.
1. Opprett et lokasjonsdirektiv, og angi følgende verdier:

    - **Navn:** *51 bestått*
    - **Arbeidstype:** *Plasser*
    - **Område:** *5*
    - **Lager:** *51*

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogram for spørring.
1. Angi følgende verdier i fanen **Område**:

    - **Tabell:** *Kvalitetsordrer*
    - **Felt:** *Status*
    - **Kriterier:** *bestått*

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Legg til en linje i hurtigfanen **Linjer**, og angi følgende verdier:

    - **Fra-antall:** *1*
    - **Til-antall:** *1000000*

1. Legg til en rad i hurtigfanen **Lokasjonsdirektivhandlinger**, og angi følgende verdi:

    - **Navn:** *bestått*

1. I hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogram for spørring.
1. Angi følgende verdier i fanen **Område**:

    - **Tabell:** *Plasseringer*
    - **Felt:** *Sone-ID*
    - **Vilkår:** *parti*

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Lagre** i handlingsruten for å lagre det nye lokasjonsdirektivet.
1. Opprett et nytt lokasjonsdirektiv, og angi følgende verdier:

    - **Navn:** *51 mislykket*
    - **Arbeidstype:** *Plasser*
    - **Område:** *5*
    - **Lager:** *51*

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogram for spørring.
1. Angi følgende verdier i fanen **Område**:

    - **Tabell:** *Kvalitetsordrer*
    - **Felt:** *Status*
    - **Kriterier:** *mislykket*

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Legg til en linje i hurtigfanen **Linjer**, og angi følgende verdier:

    - **Fra-antall:** *1*
    - **Til-antall:** *1000000*

1. Legg til en rad i hurtigfanen **Lokasjonsdirektivhandlinger**, og angi følgende verdi:

    - **Navn:** *mislykket*

1. I hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Rediger spørring** for å åpne dialogboksen for redigeringsprogram for spørring.
1. Angi følgende verdier i fanen **Område**:

    - **Tabell:** *Plasseringer*
    - **Felt:** *Sone-ID*
    - **Kriterier:** *Retur*

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Lagre** i handlingsruten for å lagre det nye lokasjonsdirektivet.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Menyelementer for mobilenhet for kvalitet ut

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg menyelementet for mobilenhet **QMS-plassering**.
1. På hurtigfanen **Arbeidsklasser** legger du til arbeidsklasse-IDen *QualityPut*.

Lagerarbeidere vil nå kunne plukke kvalitetsordrearbeid ved hjelp av **QMS-plassering**-menyelementet Varer som ikke bestod kvalitetskontrollen, kan legges i en returlokasjon, og varer som bestod kontrollen, kan legges på parti-001-lokasjonen.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Sammendrag: Oppsettet for å flytte varer fra kvalitetskontroll

Du har definert arbeids- og plasseringsdataene for lager 51 for å sikre at arbeid opprettes automatisk når kvalitetsordrer er fullført. Dette oppsettet sørger for at hvert kvalitetskontrollert nummerskilt flyttes til enten en partilokasjon eller en returlokasjon.

### <a name="process-quality-management-work"></a>Behandle kvalitetsstyringsarbeid

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg den første kvalitetsordren for antallene som ble registrert.
1. Velg **Valider**. Statusen for testen oppdateres til *Mislykket*.
1. Gå til **Lagerstyring \> Alt arbeid**.
1. Åpne arbeidet du nettopp opprettet, og legg merke til at **Arbeidsordretype**-verdien er *Kvalitetsordre*. Arbeidet inkluderer en linje der plasseringslokasjonen er *Retur* og statusen er *Mislykket*. (Hvis statusen for kvalitetsordren var *Bestått*, ville plasseringslokasjonen vært *Parti* i stedet.)
1. Gå tilbake til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg den andre kvalitetsordren for varene som ble registrert.
1. Velg **Resultater** over det nedre rutenettet. Oppdater **Resultatantall**-verdien til *5*, og kontroller at **Testresultat**-verdien endres til en avmerking.
1. Velg **Valider**, og lukk siden.
1. Gå tilbake til **Kvalitetsordrer**-siden, velg **Valider**, og utfør valideringen. Statusen oppdateres til *Bestått*.

    > [!NOTE]
    > Valideringshendelsen utløser opprettingen av kvalitetsordrearbeidet for å flytte antallet fra kvalitetskontroll-lokasjonen til en ny lokasjon.

1. Gå til **Lagerstyring \> Alt arbeid**.
1. Velg arbeidet som nettopp ble opprettet, og legg merke til at det er opprettet et ekstra hode for kvalitetsordre, der plasseringslokasjonen er *BULK-001*.
1. Gå til en mobilenhet eller emulator som kjører mobilappen Lagerstyring, og logg på lager 51 ved å bruke *51* som bruker-ID og *1* som passord.
1. Gå til **Kvalitets \> Plassering fra QMS**, og behandle hvert av de to nummerskiltene som er relatert til begge delene av arbeid, slik at alt arbeid er lukket.

> [!NOTE]
> Vurder å legge til kvalitet ut-oppføringen i et menyelement for mobilenhet der aktivitetskoden er *Vis åpen arbeidsliste*. Hvis du vil ha et eksempel, se menyelementet mobilenhet med navnet **Arbeidsliste** i demodataene. Legg først til *Kvalitetsordre*-arbeidsklassen i et brukerstyrt menyelement, fordi denne arbeidsklassen kreves for at arbeid skal vises i arbeidslisten. Legg deretter til *Kvalitetsordre*-arbeidsklassen i menyelementet **Arbeidsliste**. Brukere som har tilgang til arbeidslisten, vil da kunne plukke og behandle arbeidet som genereres automatisk av kvalitetsordrevalidering.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitets- og avviksstyring](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]