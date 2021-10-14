---
title: Lagerhåndtering av innkommende laster for bestillinger
description: Dette emnet beskriver lagerhåndteringsprosessen for innkommende laster for bestillinger.
author: Mirzaab
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: c2d7f140c0199b4b81a7b42220d5800d427be680
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577846"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Lagerhåndtering av innkommende laster for bestillinger

[!include [banner](../includes/banner.md)]

Dette emnet beskriver lagerhåndteringsprosessen for innkommende laster for bestillinger.

For hver innkommende last bør systemet allerede inneholde en tilknyttet salgsordre, og kan også inneholde en relatert lastespesifikasjon og/eller transportplan. Hvis du vil ha mer informasjon om hvordan du oppretter og behandler innkommende laster, kan du se [Forretningsprosess: planlegging av transport for innkommende laster](/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Oversikt: Hvordan innkommende laster opprettes, registreres og mottas

Illustrasjonen nedenfor viser den vanlige flyten for håndtering av innkommende laster som har bestillingsantall når de kommer til lageret.

![Prosessen for behandling av innkommende laster.](media/inbound-process.png "Prosessen for behandling av innkommende laster")

1. **Leverandøren bekrefter bestillingen.**

    Prosessen begynner når en bestilling legges inn i systemet og deretter leveres til en leverandør, som bekrefter ordren. Bestillingen må finnes før du kan opprette en inngående lastepost. Du kan imidlertid opprette den innkommende lasten selv om ordren ikke er bekreftet. For mer informasjon, se [Godkjenne og bekrefte bestillinger](../procurement/purchase-order-approval-confirmation.md).

1. **En inngående lastepost opprettes for å planlegge ankomsten og innholdet.**

    Den innkommende lasteposten representerer en leverandørforsendelse av én eller flere bestillinger. Lasten forventes å ankomme lageret som én fysisk transportenhet (for eksempel et vognlass). Den innkommende lasteposten brukes til planlegging, og logistikkkoordinatoren kan spore lastens fremdrift fra leverandøren. Den brukes også til å registrere ordrelinjeantall og behandle fremdriften via lageroperasjoner, for eksempel ankomst og plasseringsarbeid. Laster kan enten opprettes automatisk eller manuelt, og de kan være basert på enten en bestilling eller en avansert forsendelsesmerknad (ASN) fra leverandøren. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre en innkommende last](/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Leverandøren bekrefter lastfordeling.**

    Når leverandøren fordeler lasten, bekrefter logistikk koordinatoren i det mottakende lageret lasteforsendelsen. Hvis mottaksfirmaet bruker modulen **Transportstyring**, utløser inngående forsendelsesbekreftelse andre lastebehandlingsprosesser som er knyttet til innkommende laster. Hvis du vil ha mer informasjon, se [Bekrefte en last for forsendelse](/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Lasten ankommer lageret, og arbeidere registrerer antall.**

    Når et vognlass mottas på lageret, registrerer lagermedarbeidere antallene i lasten. Når modulen **Lagerstyring** brukes, utfører arbeiderne registreringen med mobilenheter. Hvis du vil ha mer informasjon, kan du se [Mottaksseddel mot bestillinger – registrering](../procurement/product-receipt-against-purchase-orders.md#registration) og delen [Registrere vareantall som kommer i en inngående last](#register-item-quantities-arriving).

1. **Registrerte lasteantall posteres mot bestillinger.**

    Når lasteantallene er registrert som mottatt, må disse antallene posteres mot produktkvitteringen til firmaets lagerfinans for å registrere den fysiske lagerøkningen. Hvis du vil ha mer informasjon, kan du se [Mottaksseddel mot bestillinger – mottaksseddel](../procurement/product-receipt-against-purchase-orders.md#product-receipt) og [Postere registrerte produktantall mot bestillinger](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Registrere vare antall som ankommer i en inngående last

Microsoft Dynamics 365 Supply Chain Management støtter flere av de operative metodene for å registrere ankomsten av bestilte produkter. Derfor kan du konfigurere systemet slik at det samsvarer med dine spesifikke forretningsbehov. Denne delen beskriver hvordan du kan registrere innkommende vareantall ved hjelp av en mobilenhet når avansert lagerstyring er aktivert i systemet. Det finnes imidlertid en alternativ flyt som er basert på bruk av vareankomstjournalen i stedet for en mobilenhet. For mer informasjon om denne flyten kan du se [Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst](tasks/register-items-advanced-warehousing.md).

Når en innkommende last først ankommer lageret, må lagermedarbeidere registrere vareantallene som er inkludert i forsendelsen. Vanligvis bruker de håndholdte skannere. Denne arbeidsflyten er bare tilgjengelig hvis følgende elementer finnes i systemet:

- **En innkommende lastepost som beskriver vareantallene som forventes i forsendelsen**

    Leverandøren bekrefter vanligvis den inngående lasteposten før forsendelsen kommer til lageret. Lasten har derfor statusen _Sendt_. Lagermedarbeidere kan imidlertid også registrere vareantall for laster som har statusen _Åpen_ eller _Mottatt_.

- **En meny for mobilenheter som er konfigurert til å støtte mottak av laster**

    [Mobilappen Lagerstyring](../warehousing/install-configure-warehouse-management-app.md) for mobilenheter støtter følgende arbeidsopprettelsesprosesser:

    - Mottak av lastvare
    - Mottak og plassering av lastvare
    - Mottak av kombinerte skiltnumre, der feltet **Identifikasjonsmåte for kildedokumentlinje** for menyen på mobilenheten er angitt til _Mottak av lastvare_. For mer informasjon, se [Mottak av kombinerte skiltnumre](mixed-license-plate-receiving.md).
    - Mottak og plassering av kombinerte skiltnumre, der feltet **Identifikasjonsmåte for kildedokumentlinje** for menyen på mobilenheten er angitt til _Mottak av lastvare_. For mer informasjon, se [Mottak av kombinerte skiltnumre](mixed-license-plate-receiving.md).

    > [!NOTE]
    > Uansett prosess vil systemet generere arbeid for å ta antall som er registrert i mottakslokasjonen, og plassere dem i den vanlige lagringsplasseringen. Når prosessen _Mottak og plassering av lastvare_ eller _Mottak og plassering av kombinerte skiltnumre_ brukes, blir arbeideren som registrerte lasteantallet, også instruert av enheten om å utføre plasseringsarbeidet som en del av registreringsoppgaven. I motsetning til dette er forutsetningen for prosessene _Mottak av lastvare_ og _Mottak av kombinerte skiltnumre_ at plasseringsarbeidet utføres atskilt fra registreringsoppgaven.

- **En arbeidsmal som definerer plukkings- og plasseringsarbeid for innkommende laster**

    Dette elementet er knyttet til de forrige elementene. Du må ha minst én arbeidsmal for arbeidsordretypen _Bestilling_, og den må inneholde et sett med plukkings-/plasseringsarbeidstyper.

Mobilenheten veileder mottaksassistenten på lageret gjennom flyten for registrering av lasteantall. Som et minumum inkluderer denne flyten følgende trinn for hver last-ID:

1. Angi last-ID-en.
2. Angi varenummeret for en mottatt vare.
3. Angi antallet av varenummeret som er mottatt.
4. Angi skiltnummeret for varens første lokasjon, hvis systemet ikke er konfigurert til å generere dette nummeret automatisk.
5. Trykk på **OK**.

Når arbeideren har fullført disse trinnene, utfører systemet følgende oppdateringer for de aktuelle enhetene, forutsatt at bestillingslinjeantallet ankom i én last, og at alle lastantall er registrert:

| Entity | Oppdateringer | Merk |
|---|---|---|
| Belastning | Feltet **Antall for arbeid opprettet** på lastelinjen oppdateres slik at det viser det registrerte antallet. | Verdien for **Lastestatus** forblir _Sendt_ eller _Åpen_ hvis det ikke er kjørt en forsendelsesbekreftelse for lasten. Hvis minst én linje med plasseringsarbeid er startet, blir dette endret til _Pågår_. |
| Lagertransaksjonen til en bestilling som tilknyttede lasteantall er registrert for |<p>Følgende felt oppdateres:</p><ul><li>Feltet <b>Mottak</b> settes til <i>Registrert.</i></li><li>Feltet <b>Sted</b> oppdateres med stedskoden til mottakssonen. (Denne koden er angitt i feltet <b>Standard mottakssted</b> for hvert lager.)</li><li>Feltet <b>Nummerskilt</b> oppdateres med skiltnummeret som ble angitt eller generert under registreringen.</li><li>Feltet <b>Last-ID</b> oppdateres med nummeret for lasten og antallet den er registrert mot. (Se merknaden.)</li></ul> | Muligheten til å koble mellom bestillingens lagertransaksjon og antallene som er registrert mot lasten, ble innført i versjon 10.0.9 som en valgfri funksjon med navnet _Tilknytt lagertransaksjoner for bestilling med last_. Denne funksjonen er spesielt fordelaktig for driftsflyter der en enkelt ordre av innkjøpte varer leveres som flere laster, eller når en last inneholder antall for flere bestillinger. |
| Lagerplassering | Arbeid opprettes på grunnlag av en arbeidsmal for å instruere arbeideren om å flytte de registrerte antallene fra mottakslokasjonen til et vanlig lagringssted. | Valget av lagringsstedet styres av direktivet for plasseringssted. Hvis det ikke er definert noe stedsdirektiv, er plasseringsstedet for arbeidet tomt. |

Merk at lagermedarbeidere kan registrere mottaket av en bestilling med én eller flere tilknyttede laster uten å bruke prosessen _Mottak av lastvare_. De følgende metodene er tilgjengelige:

- **På mobilenheten:** Bruk prosessene _Mottak av bestillingslinje_ og _Bestillingslinjen er mottatt og plassert_. (Hvis det finnes flere enn én last for bestillingslinjeantallet, kan ikke arbeideren bruke prosessen _Mottak av bestillingslinje_. I stedet vil arbeideren bli bedt om å bruke enhetshandlingen som er knyttet til prosessen _Mottak av lastvare_.)
- **På klienten:** Bruk journalen for vareankomst.
- **På klienten:** Bruk **Registrering**-handlingen som du får tilgang til fra bestillingslinjen.

> [!NOTE]
> Hvis bestillingsmottaket er registrert ved hjelp av noen av metodene ovenfor, opprettes det ingen kobling mellom bestillingens lagertransaksjon og lasten, selv om funksjonen _Tilknytt lagertransaksjoner for bestilling med last_ er aktivert. Ett unntak fra denne regelen er når du bruker alternativet **Mottak av bestillingslinje**, og bare én last har en annen status enn _Mottatt_ for ordre linjen.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Behandle avvik under registrering av inngående lasteantall

Lagerarbeidere kan utføre en delvis registrering av mottak av lasteantall. Hvert delvise mottat av lasteantall oppretter deretter en egen lagertransaksjon som har mottaksstatusen _Registrert_ for det registrerte antallet, og parti-ID-en refererer til den opprinnelige bestillingslinjen.

#### <a name="load-under-receiving"></a>Undermottak av last

Når det kommer en last og vareantallene er mindre enn antallene som er angitt i lasteposten, kan mottakspersonell på lageret arbeide direkte i klienten for å bekrefte dette avviket ved å redusere antallet på lastelinjen, slik at det samsvarer med det faktiske antallet som ble mottatt og registrert.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Overmottak av last

Overmottak skjer når en last ankommer, og vareantallet overskrider forventet lastlinjeantall. Du kan kontrollere om og hvilken grad overmottak er tillatt under registrering av lasten.

Bruk feltet **Overmottak for last** for de relevante menyelementene for mobilenheter for å kontrollere hva som skjer når en lagerarbeider prøver å registrere en overlevering. Dette feltet er tilgjengelig for menyelementer for mobilenheter som bruker følgende typer arbeidsopprettelsesprosesser:

- Mottak av lastvare
- Mottak og plassering av lastvare
- Mottak av kombinerte skiltnumre (når feltet **Identifikasjonsmåte for kildedokumentlinje** er angitt til _Mottak av lastvare_)
- Mottak og plassering av kombinerte skiltnumre (når feltet **Identifikasjonsmåte for kildedokumentlinje** er angitt til _Mottak av lastvare_)

Tabellen nedenfor forklarer hvilke alternativer som er tilgjengelige for feltet **Overmottak for last**.

| Verdi | beskrivelse |
|---|---|
| Tillat | Arbeidere kan registrere mottak av antall som overskrider det gjenstående uregistrerte antallet for en valgt last, men bare hvis det totale registrerte antallet ikke overskrider antallet på bestillingslinjen som er knyttet til lasten (etter justering for overleveringsprosenten). |
| Blokker | <p>Arbeidere kan ikke registrere mottak av antall som overskrider det gjenstående uregistrerte antallet for en valgt last (etter justering for overleveringsprosenten). En arbeider som prøver å registrere mottakene, får en feil og kan ikke fortsette før vedkommende registrerer et antall som er lik eller mindre enn det gjenstående uregistrerte lastantallet.</p><p>Som standard kopieres verdien for overleveringsprosenten på en lastlinje fra den tilknyttede bestillingslinjen. Når feltet <b>Overmottak for last</b> er satt til <i>Blokker</i>, bruker systemet verdien for overleveringsprosent til å beregne det totale antallet som kan registreres for en lastlinje. Denne verdien kan imidlertid overskrives for individuelle laster etter behov. Denne virkemåten blir relevant ved mottaksflyter der noe av eller hele det overskytende antallet som representerer overleveringsprosenten på ordrelinjen, blir distribuert uproporsjonalt på tvers av flere laster. Her er et eksempelscenario:</p><ul><li>Det finnes flere laster for én bestillings linje.</li><li>Bestillingslinjen har en overleveringsprosent som er mer enn 0 (null).</li><li>Antall er allerede registrert mot en eller flere laster uten å ta hensyn til overleveringsprosenten.</li><li>Overleveringsantallet kommer i den siste lasten.</li></ul><p>I dette scenariet kan en mobilenhet brukes til å registrere det ekstra antallet for den siste lasten bare hvis lagersjefen øker overleveringsprosenten for den relevante lastlinjen fra standardverdien til en verdi som er stor nok, slik at hele overleveringen kan registreres med den endelige lasten.</p> |
| Blokker bare for lukkede laster | Arbeidere kan overskride lastlinjeantall for åpne laster, men ikke for laster som har statusen _Mottatt_. |

> [!NOTE]
> Standardverdien for feltet **Overmottak for last** er _Tillatt_. Når denne verdien brukes, samsvarer virkemåten med standard virkemåte som var tilgjengelig før funksjonen _Overmottak av lastantall_ ble introdusert i versjon 10.0.11.

### <a name="put-away-the-registered-quantities"></a>Plassere de registrerte antallene

Når registreringen er fullført på mobilenheten, oppdaterer handlingen _Registrering av mottatt antall_ beholdnings- og lagerpostene for å angi at antallene nå er i mottakssonen og er tilgjengelige for reservering. Et firmas lageroperasjoner krever imidlertid vanligvis at antallene flyttes fra mottakssonen til det vanlige lageret, slik at de påfølgende plukkprosessene kan finne sted. Instruksjoner for plasseringen registreres i plasseringsarbeidet som genereres automatisk når den innkommende lasten registreres som mottatt.

Når lagerarbeideren har fullført plasseringsarbeidet, registrerer og sporer systemet resultatet ved å oppdatere flere enheter, slik det er oppsummert i tabellen nedenfor.

| Entity | Oppdateringer | Merk |
|---|---|---|
| Belastning | <p>Følgende felt oppdateres:</p><ul><li>Verdien for <b>Laststatus</b> endres til <i>Pågår</i>.</li><li>Verdien for <b>Arbeidsstatus</b> endres til <i>100,00 % av arbeid fullført</i>.</li></ul> | Verdien for **Laststatus** endres til _Pågår_ når arbeideren starter plasseringsoppgaven for minst én linje med plasseringsarbeid. |
| ager transaksjoner av arbeid som det tilknyttede antallet er plassert for | Feltene **Mottak** og **Sted**, og andre relevante felt, oppdateres for å gjenspeile bevegelsen fra mottaksstedet til lagringsstedet. | Verdien **Mottaksstatus** for lagertransaksjonen for bestillingen forblir _Registrert_. |
| Lagerplassering | Verdien **Arbeidsstatus** endres til _Lukket_. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Postere registrerte produktantall mot bestillinger

Når inngående produktantall er registrert i systemet, blir de tilgjengelige for reservering i forbindelse med salg og andre utgående og interne operasjoner. Systemet oppdaterer imidlertid ikke lagerkontoene (midlertidige) ennå. Denne oppdateringen kan bare forekomme når operasjonsteamet posterer de registrerte produktkvitteringene.

For å åpne en side der de kan postere en produktkvittering, kan medlemmer av operasjonsteamet følge _ethvert_ av disse trinnene:

- Åpne den relevante lastposten, og velg deretter **Produktkvittering**.
- Gå til **Lagerstyring \> Periodiske oppgaver \> Oppdater produktkvitteringer**, og angi deretter lasten som skal posteres, i feltet **Last-ID**.
- Åpne den relevante bestillingen, og velg deretter **Produktkvittering**.
- Gå til **Innkjøp og leverandører \> Bestillinger \> Mottar produkter \> Postering av produktkvitteringsjobb**.

Handlingen **Produktkvittering** som er tilgjengelig på **Last**-siden (og på den tilsvarende siden for oppdateringsjobben, siden **Oppdater produktkvitteringer**) kan oppdatere produktkvitteringsantall bare på bestillingsantall som har statusen _Registrert_. Handlingen **Produktkvittering** som er tilgjengelig på siden **Bestilling**, kan imidlertid inkludere antall i begge behandlingsstatusene (_Bestilt_ og _Registrert_). Den kan også styre omfanget av produktkvitteringspostering ved hjelp av flere parametere, for eksempel _Motta nå-antall_ og _Registrerte antall og tjenester_.

Bare ordrer med statusen _Bekreftet_ kan være produktkvittering – postert. For ubekreftede bestillinger vil handlingen **Produktkvittering** vises som utilgjengelig.

### <a name="post-registered-quantities-from-the-load-page"></a>Postere registrerte antall fra Last-siden

For produktkvittering – poster registrerte antall fra **Last**-siden må følgende forutsetninger være på plass:

- Lasten må ha minst én antallsenhet som har statusen _Registrert_.
- Laststatusen må være _Sendt_.
- Bestillingen som er knyttet til lasten, må ha statusen _Bekreftet_.

> [!NOTE]
> Hvis laststatusen ikke er satt til _Sendt_, vil systemet automatisk bekrefte lasten før det kjører produktkvitteringsoppdateringen. (Laststatusen settes til _Sendt_ når en bruker registrerer lastens innkommende forsendelse.)

Til ankomstregistreringene av typen produktkvittering – poster som er knyttet til en valgt last, velger arbeideren handlingen **Produktkvittering** på **Last**-siden. Siden som åpnes, har følgende nøkkeldetaljer:

- **Antall**-feltet i **Parametere**-delen i fanen **Innstillinger** viser det _registrerte antallet_. Ingen andre alternativer er tilgjengelig her.
- Rutenettet på hurtigfanen **Oversikt** viser alle bestillingene som er inkludert i den valgte lasten.
- Rute nettet på hurtigfanen **Linjer** viser alle ordrelinjer som har et registrert antall.

> [!NOTE]
> Antall for ordrelinjer som vises i fanen **Linje**, beregnes annerledes, avhengig av om funksjonen _Tillat flere produktkvitteringer per last_ er tilgjengelig og aktivert i din versjon av Supply Chain Management.
>
> | Versjon | Beregning |
> |---|---|
> | Versjoner før versjon 10.0.10, og nyere versjoner der funksjonen _Tillat flere produktkvitteringer per last_ ikke er aktivert | Linjeantallet er summen av alle registrerte antall _for denne bestillingslinjen_, uansett om registreringen ble utført over flere laster, uavhengig av lasten, fra en mobilenhet eller fra klienten. |
> | Versjon 10.0.10 og senere, der funksjonen _Tillat flere produktkvitteringer per last_ er aktivert | Linjeantallet er summen av alle registrerte antall _for lastposten_ som handlingen **Produktkvitteringpostering** ble startet fra. |

Når brukeren velger **OK** for å bekrefte produktkvitteringspostering, utfører systemet følgende nøkkeloppdateringer for de aktuelle enhetene.

| Entity | Oppdateringer |
|---|---|
| Lagertransaksjon for bestillingen som det er inkludert linjeantall for i posteringsomfanget | <p>Følgende felt er oppdatert (men vær oppmerksom på at det også er flere andre oppdateringer):</p><ul><li>Feltet <b>Mottak</b> settes til <i>Mottatt</i>.</li><li>Feltet <b>Fysisk dato</b> oppdateres med datoen for posteringen.</li></ul> |
| Lasten som brukeren posterte produktkvitteringen fra | Oppdateringer for lastene vil være avhengig av versjonen som brukes, og innstillingen i feltet **Tillat flere produktkvitteringer per last**. Reglene er beskrevet i tabellen som vises senere i denne delen. |

Feltet **Tillat flere produktkvitteringer per last** lar selskaper velge en policy for mottak av innkommende last. Avhengig av driftsflytene kan firmaer velge å tillate eller forby flere produktkvitteringsposteringer for den samme lasten. Det anbefales at logistikkansvarlig setter feltet **Tillat flere produktkvitteringer per last** til én av følgende verdier:

- **Nei** – Velg denne verdien hvis lagermottaksassistenter alltid registrerer alle ordreantall som ankommer hver last innenfor en angitt tidsramme. Hvis noen av lastantallene ikke er registrert, forutsetter systemet at de ikke ble mottatt eller ikke var i lasten, og bør derfor ikke betraktes som en del av lasten. Produktkvitteringsposteringen som kjøres fra en last, bruker samme antakelse. I tillegg til produktkvittering – oppdatering av alle de registrerte antallene (hovedfunksjonen), deklarerer det at lasten er komplett og lukket for ytterligere behandling. I dette tilfellet blir alle lastlinjeantall automatisk oppdatert til registrerte antall, lastlinjer som ikke har registrerte antall, blir slettet, og laststatusen endres til _Mottatt_.
- **Ja** – Velg denne verdien hvis lagermottaksassistenter trenger mer tid til å registrere alle antallene i lasten som er ankommet, men i mellomtiden må du produktkvittere – postere antallene som allerede er registrert. I dette tilfellet vil logistikkansvarlig ønske å holde en last åpen, selv etter at produktkvitteringsposteringsjobben er kjørt, slik at gjenstående lastantall kan registreres og produktkvitteringen oppdateres til finans på løpende basis.
- **Spør** – Velg denne verdien hvis prosessen for å motta last er blandet, og det kreves en avgjørelse hver gang produktkvitteringspostering kjøres.

Tabellen nedenfor oppsummerer virkningene av innstillingen **Tillat flere produktkvitteringer per last**.

| Tillat flere produktkvitteringer per last | Lastantall | Laststatus | Merk |
|---|---|---|---|
| Når dette feltet ikke er tilgjengelig (versjoner før 10.0.10) | <p>Lastantallet settes slik at det tilsvarer det registrerte antallet.</p><p>Hvis lastantallet oppdateres til 0 (null), som betyr at det ikke er foretatt noen registrering, slettes lastlinjen.</p><p>Hvis det ikke finnes noen lastlinjer i lasten, blir lasten slettet.</p> | _Mottatt_ | Hvis det finnes flere laster for ordrelinjens registrerte antall, blir bare statusen for lasten som mottaket ble postert fra, oppdatert til _Mottatt_. |
| Nei | <p>Lastantallet settes slik at det tilsvarer det registrerte antallet som er knyttet til last-ID-en.</p><p>Hvis det ikke er registrert noen last-ID for lagertransaksjonen, blir virkemåten den samme som i versjoner før 10.0.10.</p> | _Mottatt_ | |
| Ja | Ingen oppdateringer | _Mottatt_, hvis totalt registrert lastantall er likt eller større enn lastantallet | |
| Ja | Ingen oppdateringer | _Sendt_ eller _Pågår_, hvis totalt registrert lastantall er mindre enn lastantallet | |

Når feltet **Laststatus** er satt til _Mottatt_, kan det ikke foretas flere produktkvitteringsposteringer for denne lasten. Arbeideren kan imidlertid registrere det gjenstående ordreantallet mot den mottatte lasten under følgende betingelser. (Hvis du ha mer informasjon, kan du se delen [Overmottak av last](#load-over-receiving) tidligere i dette emnet.)

- Versjonen av Supply Chain Management er eldre enn versjon 10.0.11.
- Funksjonen _Overmottak av lastantall_ er aktivert, og feltet **Overmottak for lastlinjeantall** på menyen på mobilenheten for lastevarens mottakshandling er satt til _Tillat_.

For produktkvitteringspostering av flere registrerte lastantall mot en last som har statusen _Mottatt_, må brukeren kjøre posteringshandlingen fra den tilknyttede bestillingen.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Postere registrerte antall fra Bestilling-siden

For produktkvitteringspostering av registrerte antall fra **Bestilling**-siden må brukeren fullføre følgende oppgaver før vedkommende velger handlingen **Produktkvittering**:

- Angi **Antall**-feltet i **Parametere**-delen i fanen **Innstillinger** til _Registrert antall_.
- Angir numrene på bestillingene som skal tas med i posteringen, i feltet **Produktkvittering**.

> [!NOTE]
> Linjeantallet som inkluderes i posteringsomfanget, er summen av alle registrerte antall for ordrelinjen, uansett om antallsregistreringen er utført over flere laster, uavhengig av lasten, fra en mobilenhet eller fra klienten. Den samme regelen gjelder når produktkvitteringspostering kjøres fra en last, hvis dette er gjort der feltet **Tillat flere produktkvitteringer per last** enten ikke er tilgjengelig eller ikke er aktivert.

Når brukeren velger **OK** for å bekrefte produktkvitteringspostering, utfører systemet følgende nøkkeloppdateringer for de aktuelle enhetene.

| Entity | Oppdateringer |
|---|---|
| Lagertransaksjon for bestillingen som det er inkludert linjeantall for i posteringsomfanget | <p>Følgende felt er oppdatert (men vær oppmerksom på at det også er flere andre oppdateringer):</p><ul><li>Feltet <b>Mottak</b> settes til <i>Mottatt</i>.</li><li>Feltet <b>Fysisk dato</b> oppdateres med datoen for produktkvitteringsposteringen.</li></ul> |
| Belastning | Oppdateringer for lastene avhenger av om feltet **Tillat flere produktkvitteringer per last** er tilgjengelig og aktivert. Reglene er beskrevet i den neste tabellen. |

Tabellen nedenfor oppsummerer virkningene av innstillingen **Tillat flere produktkvitteringer per last**.

| Tillat flere mottakssedler per belastning | Lastantall | Laststatus | Merk |
|---|---|---|---|
| Når dette feltet enten er deaktivert eller ikke tilgjengelig (i versjoner før 10.0.10) | Ingen oppdateringer | Det utføres ingen oppdateringer. (Statusen forblir _Åpen_, _Sendt_ eller _Pågår_.) | Fordi produktkvitteringsposteringen startes fra en bestilling, har ikke oppdateringslogikken informasjon om tilknytningen mellom de registrerte antallene innenfor sitt omfang og lastene som registreringen ble registrert mot. Derfor kan den ikke velge lasten for statusoppdateringen. |
| Aktivert | Ingen oppdateringer | <p>En av følgende handlinger inntreffer:</p><ul><li>Statusen endres til <i>Mottatt</i> hvis totalt mottatt og kjøpt antall av bestillingslagertransaksjonene er større enn eller lik antallet for lasten de er knyttet til.</li><li>Statusen forblir <i>Åpen</i>, <i>Sendt</i> eller <i>Pågår</i> hvis den forrige betingelsen ikke er oppfylt for alle linjene i lasten.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Velge riktig alternativ for produktkvitteringspostering for logistikkoperasjoner

Som beskrevet tidligere tilbyr systemet to alternativer for produktkvitteringspostering. Du kan få tilgang til alternativene på følgende steder:

- På **Last**-siden eller fra menyen **Lagerstyring \> Periodiske oppgaver** som en oppdateringsjobb
- På siden **Bestilling** eller fra menyen **Innkjøp og leverandører \> Bestillinger \> Mottar produkter** som en oppdateringsjobb

Firmaer som bruker laster til å planlegge og administrere transport og lagerhåndtering av innkommende ordrer, anbefales å bruke følgende funksjoner, som er utformet for å fungere med laster:

- **Mottak av lastvare**-handlinger på mobilenheter for lager, for å registrere ankomsten av produktantallet mot lasten
- **Produktkvitteringpostering**-handlinger som startes fra en last, for å oppdatere lagerfinans

> [!NOTE]
> Andre funksjoner for antallsregistrering produktkvitteringspostering kan brukes til å støtte de tilsvarende inngående driftsprosessene. Hvis du imidlertid bruker dem om hverandre sammen med eller i stedet for de dedikerte funksjonene for laster, kan du redusere nøyaktigheten på dataene til lastpostene og dermed sømløsheten i lasthåndteringsflyter.

## <a name="example-scenarios"></a>Eksempelscenarioer

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Klargjøre systemet for kjøring av eksempelscenarioene

For å gå gjennom eksempelscenarioene som beskrives i denne delen, må du først kontrollere at alle de nødvendige funksjonene er aktivert i systemet. De nødvendige demodataene må også være tilgjengelige i systemet.

#### <a name="turn-on-the-required-features"></a>Aktivere de nødvendige funksjonene

Disse scenarioene krever funksjonen _Flere produktkviteringsposteringer per last_ og dennes forutsetningsfunksjon. Administratorer kan aktivere disse funksjonene ved å følge disse trinnene.

1. Åpne arbeidsområdet **Funksjonsbehandling**. (Hvis du vil ha fullstendig informasjon om hvordan du finner og bruker dette arbeidsområdet, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. Aktiver funksjonen _Tilknytt lagertransaksjoner for bestilling med last_, som er oppført på følgende måte:

    - **Modul:** _Lagerstyring_
    - **Funksjonsnavn:** _Tilknytt lagertransaksjoner for bestilling med last_

1. Aktiver funksjonen _Flere produktkviteringsposteringer per last_, som er oppført på følgende måte:

    - **Modul:** _Lagerstyring_
    - **Funksjonsnavn:** _Flere produktkviteringsposteringer per last_

#### <a name="enable-sample-data"></a>Aktivere eksempeldata

For å arbeide deg gjennom disse scenarioene ved å bruke de angitte eksempelpostene og -verdiene må du bruke et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Legge til et menyelement for mottak av lastvarer når en mobilenhet brukes

Før lagermottaksassistenter kan bruke en mobilenhet til å registrere innkommende beholdning som er knyttet til en last, må du opprette et menyelement for mobilenheter for dette formålet.

I denne delen skal du opprette et menyelement på en mobilenhet og legge det til på en eksisterende meny. En lagerarbeider kan deretter velge menyelementet i mobilappen Lagerstyring.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**, og kontroller at menyen på mobilenheten inkluderer et menyelement med følgende innstillinger:

    - **Modus:** _Arbeid_
    - **Arbeidsopprettelsesprosess:** _Mottak av lastvare_
    - **Generer nummerskilt:** _Ja_

    Du kan la alle andre innstillinger være som standardverdiene.

    ![Innstillinger for menyelementer på mobilenhet.](media/inbound-mobile-menu-items.png "Innstillinger for menyelementer på mobilenhet")

    Hvis du vil ha mer informasjon om hvordan du definerer menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).

2. Når du er ferdig med å definere menyelementet, går du til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten** og legger til elementet i menystrukturen på mobilenhetene.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Eksempelscenario 1: Registrere en last der noen varer mangler

Dette scenarioet viser hvordan du registrerer antall for en inngående last, der ikke alle de forventede antallene finnes. Deretter vises det hvordan du posterer produktkvitteringen for bestillingen.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Opprette en last for å planlegge mottaket av en bestilling

I denne fremgangsmåten oppretter du en bestilling og en tilknyttet last manuelt. Deretter oppdaterer du lasten for å simulere at den er sendt fra leverandøren (som oppdaterer laststatusen). Lagerplanleggere kan deretter filtrere laster etter **laststatus** for å finne forventede innkommende laster.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny**.
1. I dialogboksen **Opprett bestilling** angir du feltet **Leverandørkonto** til _1001_.
1. Velg **OK** for å lukke dialogboksen og opprette bestillingen.
1. Den nye bestillingen inneholder allerede en linje under **Bestillingslinjer**. Angi følgende verdier for denne linjen:

    - **Varenummer:** _A0001_
    - **Lager:** _24_
    - **Antall:** _10_

1. I handlingsruten, i fanen **Kjøp** velger du **Handlinger \> Bekreft**. Ordrestatusen er nå _Bekreftet_.
1. I handlingsruten, i fanen **Lager** velger du **Handlinger \> Arbeidsområde for lastplanlegging**.
1. På siden **Arbeidsområde for lastplanlegging**, i handlingsruten, i fanen **Forsyning og behov**, velger du **Legg til \> Til ny last**.
1. I dialogboksen **Tilordning av lastmal** angir du feltet **Lastmal-ID** til _20' beholder_.
1. Velg **OK** for å lukke dialogboksen og gå tilbake til arbeidsområdet.
1. I **Laster**-delen velger du **Last-ID** for å åpne den nylig opprettede lasten.
1. Gå gjennom lasthodet og linjedetaljene, legg merke til følgende punkt:

    - På hurtigfanen **Last** er feltet **Laststatus** satt til _Åpen_.
    - I delen **Lastlinjer** finnes det en enkelt linje der **Antall**-feltet er satt til _10_ og feltet **Antall for arbeid opprettet** er satt til _0_ (null).

    ![Lastdetaljer.](media/inbound-load-details.png "Lastdetaljer")

1. I handlingsruten, i fanen **Send og motta**, velger du **Bekreft \> Innkomende forsendelse**. Legg merke til at **Laststatus** er endret til _Sendt_.
1. Noter verdien for **Last-ID**, slik at du kan bruke den i neste fremgangsmåte.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Registrere mottak av antallene som ble mottatt i lasten

Når lasten i lagermottakssonen, registrerer en mottaksarbeider lastantallet på en mobilenhet.

1. Bruk mobilenheten til å logge på lager 24. (I standard demodata logger du deg på ved å bruke _24_ som bruker-ID og _1_ som passord.)
1. Velg menyelementet _Mottak av lastvare_, som du opprettet for dette scenarioet.
1. Følg instruksjonene for dataregistrering på skjermen for å angi følgende verdier. (Rekkefølgen kan variere, avhengig av hvilken mobilenhet eller emulator du bruker.)

    - **Last** – Angi last-ID-en du opprettet i den forrige prosedyren.
    - **Vare** – Angi _A0001_, som er varen som forventes for denne belastningen.
    - **Antall** – Angi _9_ som det faktiske antallet som finnes i lasten. Merk at dette antallet er mindre enn forventet antall.

1. Fortsett med å gå gjennom arbeidsflyten, la alle andre felt stå tomme eller settes til standardverdiene, til enheten informerer deg om at arbeidet er fullført.

Lastmottaksoppgaven er nå fullført, og mottaksassistenten kan gå videre til sin neste oppgave. Lagermottakspersonell vil imidlertid til slutt gå gjennom lastposten, og vil kunne se at det mottatte antallet var mindre enn forventet antall. Deretter fullfører de følgende fremgangsmåte ved hjelp av webklienten.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I listen finner du lasten du nettopp mottok. (Du må kanskje merke av for **Vis lukket** for å inkludere innkommende laster med lastestatusen _Sendt_.) Velg deretter koblingen i kolonnen **Last-ID** for å åpne lasten.
1. I lastposten kan du legge merke til at verdien for **Laststatus** forblir _Sendt_, men verdien for **Antall for arbeid opprettet** på lastlinjen er endret til _9_.
1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. I listen finner du innkjøpet du nettopp mottok, og deretter velger du koblingen i **Bestilling**-kolonnen for å åpne ordren.
\
1. I hurtigfanen **Bestillingslinjer** velger du **Beholdning \> Vis \> Transaksjoner**.
1. Se gjennom detaljene for de to bestillingstransaksjonene. (Du må kanskje tilpasse siden **Lagertransaksjoner** for å se feltet **Last-ID** på rutenettet.) Du skal se to transaksjoner:

    - Transaksjonen som har et mottak i _Registrert_-status, representerer registreringsantallet på _9_ som ble kjørt mot en bestemt last ved hjelp av mobilenheten. **Last-ID** er knyttet til den aktuelle transaksjonen.
    - Transaksjonen som har et mottat i _Bestilt_-status, representerer det gjenværende uregistrerte ordrelinjeantallet på _1_.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Produktkvittering – postere de registrerte lastantallene mot bestillinger

I denne fremgangsmåten skal du produktkvittere og postere beholdningen som du har registrert for en last. Som et resultat vil den mottatte beholdningen og de relaterte kostnadene legges til i firmaets økonomimodul.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. I listen finner du lasten du mottok. (Du må kanskje merke av for **Vis lukket** for å inkludere innkommende laster med lastestatusen _Sendt_.) Velg deretter koblingen i kolonnen **Last-ID** for å åpne lasten.
1. I handlingsruten, i fanen **Send og motta**, velger du **Motta \> Produktkvittering**. Hvis du blir bedt om å bekrefte handlingen, velger du **Ja**.
1. I dialogboksen **Posterer produktkvittering**, hurtigfanen **Linjer**, må du inspisere rutenettet. Du skal se bestillingslinjen som antallet er registrert for, mot den valgte lasten.

    > [!NOTE]
    > I versjoner der funksjonen _Flere produktkviteringsposteringer per last_ ikke er tilgjengelig eller aktivert, er standardantallet som vises i rutenettet **Lastlinjer**, det totale antallet som er registrert for alle laster som er knyttet til bestillingslinjen.

1. I hurtigfanen **Oversikt** inspiserer du feltet **Produktkvittering** i rutenettet. Legg merke til at dette er angitt til et tall som inkluderer ID-en til den valgte lasten.
1. Velg **OK** for å postere produktkvitteringen og lukke dialogboksen **Posterer produktkvittering**.
1. Du kommer tilbake til lastdetaljene. Legg merke til følgende punkt:

    - Feltet **Laststatus** er nå satt til _Mottatt_.
    - På lastlinjen er **Antall**-verdien for lasten endret fra _10_ til _9_ stk. for å samsvare med det registrerte antallet, men verdien for **Antall for arbeid opprettet** forblir _9_.

Hvis innkjøpsteamet ikke forventer at leverandøren leverer det gjenstående ordreantallet på 1, kan det lukke ordren ved å oppdatere linjens leveringsrest til _0_. Hvis det derimot snart viser seg at den manglende delen ankom i den opprinnelige lasten, kan lagerpersonell utføre en av følgende handlinger:

- Registrer antallet mot samme last. I dette tilfellet blir feltet **Laststatus** tilbakestilt til _Sendt_, og verdien for **Antall for arbeid opprettet** oppdateres til _10_. Dette valget er bare tilgjengelig i følgende situasjoner:

    - Funksjonen _Overmottak av lastantall_ er ikke tilgjengelig eller er ikke aktivert.
    - Funksjonen _Overmottak av lastantall_ er tilgjengelig og aktivert, og feltet **Overmottak for lastlinjeantall** er satt til _Tillat_.

- Legg til antallet i en ny eller eksisterende last, og behandle den på vanlig måte.
- Registrer og/eller motta antallet på en måte som ikke involverer lasthåndtering.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Eksempelscenario 2: Registrere antall som ankommer på flere innkommende laster der noen varer mangler

I dette scenarioet blir en innkommende levering som er knyttet til en enkelt bestillingslinje, delt inn i to laster. En bestillingslinje kan for eksempel deles opp i flere laster på grunn av fysiske lastbegrensninger på vekt og/eller volum.

Dette scenarioet viser også hvordan du behandler flere produktkvitteringsposteringer for den samme lasten. Du registrerer antall som kommer på flere innkommende laster, men antallene samsvarer ikke med det forventede antallet. Kostnadsoppdateringer som skjer via produktkvitteringsposteringen, utføres flere ganger for samme last.

#### <a name="set-up-load-receiving-policies"></a>Definere policyer for lastmottak

I denne fremgangsmåten skal du aktivere flere produktkvitteringsposteringer fra den samme lasten.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Laster** setter du feltet **Tillat flere produktkvitteringer per last** til _Ja_.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Opprette to laster for å planlegge mottaket av en bestilling

I denne fremgangsmåten oppretter du en bestilling og to laster. Deretter oppdaterer hver last manuelt for å simulere at den er sendt av leverandøren (som oppdaterer laststatusen). Lagerplanleggere kan deretter filtrere laster etter **laststatus** for å finne forventede innkommende laster.

Du vil også lære hvordan du angir bestillingslinjen slik at du kan motta et antall som er 20 prosent høyere enn antallet som er angitt for linjen.

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny**.
1. På hurtigfanen **Leverandør** setter du feltet **Leverandørkonto** til _1001_ og velger deretter **OK**.
1. Den nye bestillingen åpnes, og den inneholder en tom linje i rutenettet **Bestillingslinjer**. Angi følgende verdier for denne ordrelinjen:

    - **Varenummer:** _A0001_
    - **Lager:** _24_
    - **Antall:** _10_

1. På hurtigfanen **Linjedetaljer**, i fanen **Levering**, setter du feltet **Overlevering** til _20_.
1. I handlingsruten, i fanen **Kjøp** velger du **Handlinger \> Bekreft**. Ordrestatusen er nå _Bekreftet_.
1. I handlingsruten, i fanen **Lager** velger du **Handlinger \> Arbeidsområde for lastplanlegging**.
1. På siden **Arbeidsområde for lastplanlegging**, i handlingsruten, i fanen **Forsyning og behov**, velger du **Legg til \> Til ny last**.
1. I dialogboksen **Tilordning av lastmal** angir du feltet **Lastmal-ID** til _20' beholder_. I fanen **Detaljer** endrer du **Antall**-verdien fra _10_ til _5_ for å delvis legge til antallet på bestillingslinjen.
1. Velg **OK** for å bruke innstillingene og lukke dialogboksen.
1. Gjenta trinn 8 til og med 10 for å opprette en ny last. Denne gangen skal **Antall**-feltet allerede være satt til _5_.
1. På siden **Arbeidsområde for lastplanlegging**, i rutenettet **Laster**, velger du verdien for **Last-ID** for den første lasten du opprettet. Siden **Lastdetaljer** vises med den valgte belastningen. Følg disse trinnene:

    1. I handlingsruten, i fanen **Send og motta**, velger du **Bekreft \> Innkomende forsendelse**.
    1. Legg merke til at verdien for **Laststatus** er endret til _Sendt_.
    1. Velg lukkeknappen for å gå tilbake til siden **Arbeidsområde for lastplanlegging**.

1. Gjenta det forrige trinnet for den andre lasten du opprettet.
1. Noter deg de to verdiene for **Last-ID** som vises i rutenettet **Laster**.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>Registrer delvis mottak av antallene som ble ankom i første last, og poster de registrerte lastantallene

Når lasten ankommer lagermottakssonen, registrerer en mottaksarbeider lastantallet på en mobilenhet. Den registrerte beholdningen som er knyttet til en last, blir deretter oppdatert i firmaets økonomimodul ved å postere produktkvitteringen for bestillingen, basert på lasten.

Denne fremgangsmåten viser hvordan en mottaksassistent registrerer lastantall på en mobilenhet.

1. Bruk mobilenheten til å logge på lager 24. (I standard demodata logger du deg på ved å bruke _24_ som bruker-ID og _1_ som passord.)
1. Velg menyelementet _Mottak av lastvare_, som du opprettet for dette scenarioet.
1. Følg instruksjonene for dataregistrering på skjermen for å angi følgende verdier. (Rekkefølgen kan variere, avhengig av hvilken mobilenhet eller emulator du bruker.)

    - **Last** – Angi den første last-ID-en du opprettet i den forrige prosedyren.
    - **Vare** – Angi _A0001_, som er varen som forventes for denne belastningen.
    - **Antall** – Angi _3_. Merk at dette antallet er mindre enn forventet antall. For dette scenarioet må du tenke at du, som mottaksassistent, ikke har tid til å registrere alle antallene for denne lasten. Senere i denne fremgangsmåten skal du registrere de gjenværende delene ved å gjenta dette trinnet og sette **Antall**-feltet til _2_.

1. Fortsett med å gå gjennom arbeidsflyten, la alle andre felt stå tomme eller settes til standardverdiene, til enheten informerer deg om at arbeidet er fullført.
1. I webklienten går du til **Lagerstyring \> Laster \> Alle laster**.
1. I listen finner du lasten du nettopp mottok, og velger **Last ID**-verdien for å åpne lasten. Legg merke til at verdien for **Laststatus** forblir _Sendt_, men verdien for **Antall for arbeid opprettet** på lastlinjen er endret til _3_.
1. I handlingsruten, i fanen **Send og motta**, velger du **Motta \> Produktkvittering**. Hvis du blir bedt om å bekrefte handlingen, velger du **Ja**.
1. I dialogboksen **Posterer produktkvittering** går du gjennom, men endrer ikke verdiene som vises, og deretter velger du **OK**.
1. Du kommer tilbake til siden **Lastdetaljer** for den valgte lasten. Legg merke til følgende punkt:

    - Feltet **Laststatus** forblir satt til _Sendt_.
    - På lastlinjen forblir **Antall**-verdien for lasten _5_ stk., som er det opprinnelige lastantallet, og verdien for **Antall for arbeid opprettet** forblir _3_.

1. Fullfør registreringen av det gjenværende antallet i denne lasten ved å gjenta denne fremgangsmåten. I trinn 3 setter du imidlertid **Antall**-feltet til _2_.

Mottaksoppgaven for den første lasten er nå fullført. Det er opprettet to produktkvitteringsjournaler, én for hver av de to produktkvitteringsoppdateringene som du kjørte.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Registrer mottak av antallene som ble mottatt på den andre lasten, og kontoen for det overførte antallet

I dette scenarioet vil mottaksassistenten registrere inngående et antall som overskrider antallet som finnes i lasten. Overmottak vil være tillatt fordi systemet er konfigurert til å tillate overlevering.

1. Bruk mobilenheten til å logge på lager 24. (I standard demodata logger du deg på ved å bruke _24_ som bruker-ID og _1_ som passord.)
1. Velg menyelementet _Mottak av lastvare_, som du opprettet for dette scenarioet.
1. Følg instruksjonene for dataregistrering på skjermen for å angi følgende verdier. (Rekkefølgen kan variere, avhengig av hvilken mobilenhet eller emulator du bruker.)

    - **Last** – Angi den andre last-ID-en du opprettet tidligere.
    - **Vare** – Angi _A0001_, som er varen som forventes for denne belastningen.
    - **Antall** – Angi _7_, som er det gjenstående antallet som leverandøren har tillatelse til å levere som en del av det totale bestillingsantallet på 12 (der 10 er det opprinnelige ordreantallet, og 2 er det tillatte overleveringsantallet på 20 prosent). Husk at 5 stk. allerede er registrert mot den første lasten.

Den andre lasten er nå oppdatert med antallet 7, og produktkvitteringen kan oppdateres basert på dette antallet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]