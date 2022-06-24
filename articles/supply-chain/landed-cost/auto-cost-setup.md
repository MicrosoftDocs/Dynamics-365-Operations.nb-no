---
title: Automatisk kosnadsoppsett
description: Denne artikkelen beskriver hvordan du definerer kostnadsregler for forskjellige innkommende sjøreisenivåer. På grunnlag av disse reglene beregner systemet kostnadene og legger dem til automatisk. Brukerne behøver derfor ikke å legge til kostnadene manuelt.
author: Weijiesa
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 02c78789fc7531c267cee936fa30a395e6d0b62f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852396"
---
# <a name="auto-costs-setup"></a>Automatisk kosnadsoppsett

[!include [banner](../../includes/banner.md)]

Du kan bruke siden **Automatiske kostnader** til å definere kostnadsregler for forskjellige kostnadsområder (for eksempel sjøreiser, forsendelsescontainere, elegioer, bestillinger, varer eller overføringsordrelinjer). På grunnlag av reglene, og feltene brukerne velger når de oppretter poster for ett av kostnadsområdene, beregner systemet kostnadene og legger dem til automatisk. Brukerne behøver derfor ikke å legge til kostnadene manuelt.

Hvis du vil arbeide med automatiske kostnader, kan du gå til **Netto innkjøpspris \> Kostnadsoppsett \> Automatiske kostnader**. Deretter setter du opp reglene for automatisk kostpris slik det er beskrevet i resten av denne artikkelen.

## <a name="work-with-cost-areas"></a>Arbeide med kostnadsområder

Automatiske kostnader fungerer som forretningsavtaler eller automatiske tillegg. Hver automatisk kostnadspost tilhører et bestemt kostnadsnivå. Bruk feltet **Kostnadsområde** i listeruten på siden **Automatiske kostnader** til å velge kostnadsområdet du vil arbeide med. Listeruten viser bare automatiske kostnader som tilhører det gjeldende kostnadsområdet som er valgt. Alle automatiske kostnader som du oppretter, tilhører det valgte kostnadsområdet.

Ved bruk av kostnadsområder kan systemet legge til kostnader i løpet av bestillingslinjene i et kostnadsområde. En kostnad for én forsendelsescontainer vil for eksempel verdsette verdien til alle produktene i denne forsendelsescontaineren. Hvis det finnes to eller flere forsendelsescontainere, kan samme kostnadstype angis for hver forsendelsescontainer. Derfor kan containertypen brukes til å finne riktig automatisk kostpris.

## <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruten

Tabellen nedenfor beskriver knappene som er tilgjengelige i handlingsruten på siden **Automatiske kostnader**.

| Knapp | beskrivelse |
|---|---|
| Rediger | Rediger en eksisterende automatisk kostnad. |
| Nye | Opprett en automatisk kostnad. |
| Delete | Slett en automatisk kostnad. |
| Kopier fra | Opprett en ny post for automatisk kostnad som er basert på en eksisterende post. Deretter kan du fritt redigere den nye posten. Ved hjelp av denne knappen kan du raskt opprette nye automatiske kostpriser. |
| Visningsdimensjoner | Åpne en dialogboks der du kan velge lagerdimensjonene som vises for kostnadstransaksjonene du viser. Hvis du fjerner merket i avmerkingsboksene, vil færre lagerdimensjoner vises for kostnadstransaksjonene. Derfor vises detaljer som er mindre detaljerte for transaksjonen. Hvis en lagerdimensjon er angitt for en automatisk kostnad, brukes den automatiske kostnaden bare når den angitte lagerdimensjonen brukes for varen i en sjøreise. |

## <a name="settings-on-the-header"></a>Innstillinger for hodet

Kombinasjonen av innstillinger i hodedelen bestemmer når og hvordan en bestemt automatisk kostnad skal legges til for en sjøreise. En automatisk kostnad vil bare brukes på en sjøreise, forsendelsescontainer eller folio når detaljene i den automatiske kostnaden samsvarer med detaljene i hodet til dette kostnadsområdet. Summen av alle samsvarende automatiske kostnader bestemmer den estimerte, landerte kostnaden for en sjøreise. Denne kostnaden brukes på tvers av alle varene på transportmidlet eller sjøreisen.

Følgende tabell beskriver alle feltene som kan vises i hodedelen. De bestemte feltene som er tilgjengelige, varierer imidlertid avhengig av kostnadsområdet og viser dimensjoner som er valgt.

| Felt | beskrivelse |
|---|---|
| **Kontokode** | <p>Velg én av følgende verdier:</p><ul><li>**Tabell** – Kostnadsregelen gjelder bare for en bestemt leverandør.</li><li>**Gruppe** – Kostnadsregelen gjelder bare for en bestemt leverandørgruppe. Systemet vil se etter [leverandørkostnadstypegruppen](costing-parameters-setup.md) som er knyttet til leverandørposten.</li><li>**Alle** – Kostnadsregelen gjelder for alle leverandører. |
| **Forsendelsesfirma** | Velg leverandøren eller leverandørgruppen som kostnadsregelen gjelder for. Dette feltet er bare tilgjengelig hvis du velger *Tabell* eller *Gruppe* i feltet **Kontokode**. |
| **Tollmegler** | Velg leverandøren eller leverandørgruppen som kostnadsregelen gjelder for. Dette feltet er bare tilgjengelig hvis du velger *Tabell* eller *Gruppe* i feltet **Kontokode**. |
| **Varekode** | <p>Velg én av følgende verdier:</p><ul><li>**Tabell** – Kostnadsregelen gjelder bare for en bestemt vare.</li><li>**Gruppe** – Kostnadsregelen gjelder bare for en bestemt varegruppe. Systemet vil se etter [varekostnadstypegruppen](costing-parameters-setup.md) som er knyttet til vareposten.</li><li>**Alle** – Kostnadsregelen gjelder for alle varer.|
| **Varerelasjon** | Velg varen eller varegruppen som kostnadsregelen gjelder for. Dette feltet er bare tilgjengelig hvis du velger *Tabell* eller *Gruppe* i feltet **Varekode**. |
| **Leveringsmiddel** | Velg leveringsmåten (for eksempel flytransport eller sjøtransport) som kostnadsregelen gjelder. |
| **Containertype** | Type forsendelsescontainer som varene skal sendes i. En automatisk kostnad kan bare brukes på en sjøreise hvis containertypen i det automatiske kostnadsoppsettet samsvarer med containertypen for sjøreisen. |
| **Fra-havn** og **Til-havn** | Kildehavnen ("fra") og målhavnen ("til") for sjøreisen. (Noen forsendelsescontainere kan ha ulike "til-havner", fordi det kan hende at sjøreisen stopper ved flere havner.) En automatisk kostnad kan bare brukes på en sjøreise hvis fra- og til-havnene i det automatiske kostnadsoppsettet samsvarer med fra- og til-havnene til disse sjøreisene. |
| **Automatisk kostnadsnummer** | En unik identifikator for regelen for automatisk kostnad. Verdien i dette feltet genereres automatisk basert på nummerserien som er definert på siden **Parametere for netto innkjøpspris**. |
| **Lagerdimensjoner** | I noen kostnadsområder kan du ta med en eller flere varedimensjoner i hodet (for eksempel størrelse, farge, lager og partinummer). Velg **Vis dimensjoner** i handlingsruten for å velge dimensjonene som skal tas med. |

## <a name="settings-on-the-lines-fasttab"></a>Innstillinger i hurtigfanen Linjer

I hurtigfanen **Linjer** legger du til en rad for hver valuta som kan brukes når en kostnad brukes på en bestillingslinje i en bestillingslinje i en sjøreise. 

For varer og bestillinger vil systemet samsvare med valutaen for hver bestillingslinje mot valutaene som er angitt i hurtigfanen **Linjer**. Den vil bare gjelde kostverdien som er angitt for samsvarende linje eller vare. Hvis ingen linje er definert for valutaen til linjen eller varen, blir ikke den automatiske kostnaden brukt på denne linjen eller varen.

For andre typer kostnadsområder gjelder alle linjer i hurtigfanen **Linjer** for hver sjøreise, forsendelsescontainer, folio eller overføringsordrelinje som samsvarer med verdiene som er fastsatt i hodet.

Følgende tabell beskriver alle feltene som kan vises på hver linje. De bestemte feltene som er tilgjengelige, varierer imidlertid avhengig av kostnadsområdet som er valgt.

| Felt | beskrivelse |
|---|---|
| **Valuta.** | Velg valutaen som linjen gjelder for. Valutaen er knyttet til bestillingen. Når systemet prøver å finne de automatiske kostnadene som skal brukes på en sjøreise og dens sjøreiselinjer, vil det velge linjen som har samme valuta som bestillingen. Dette feltet er bare tilgjengelig når feltet **Kostnadsområde** er satt til *Bestilling* eller *Vare*. |
| **Kosttypekode** | Kostnadstypen. |
| **Fordelingsmetode** | <p>Metoden som brukes til å distribuere kostnader til linjer. Følgende alternativer er tilgjengelige:</p><ul><li><p>**Prosent** – Verdien i feltet **Kostnadsverdi** er en prosent som gjelder for totalverdien av varer.</p><p>Hvis feltet **Kostnadsverdi** for eksempel er satt til *10* og totalverdien for varer er 800 dollar, blir kostnadsverdien 80 dollar (= 800 dollar × 10 prosent).</p></li><li>**Antall** – Kostnaden vil bli fakturert på grunnlag av vareantallet.</li><li>**Beløp** – Kostnaden vil bli fakturert på grunnlag av verdien på varene.</li><li>**Volum** – Kostnaden vil bli fakturert på grunnlag av volumet til varene. Volum angis i hovedplanleggingen for varen.</li><li>**Vekt** – Kostnaden vil bli fakturert på grunnlag av vekten til varene. Vekt angis i hovedplanleggingen for varen.</li><li>**Volumetrisk** – Kostnaden vil bli fakturert på grunnlag av det volumetriske målet til varene.</li><li><p>**Mål** – Ved hjelp av dette alternativet kan det angis et mål i modulen **Netto innkjøpspris**. Den brukes ofte av organisasjoner som ikke kjenner til det enkelte volumet eller vekten av varene, men som krever en mer nøyaktig fordeling enn alternativene **Beløp** og **Antall** tillater. Fraktforsenderen eller agenten vil gi organisasjonen vekten eller kuben som måler, enten på varenivå eller på bestillingsnivå.</p><p>Frakten vil for eksempel være lik 900 dollar. Vare A har en vekt på 800 kg og et volum på 2 kubikkmeter (m³). Vare B har en vekt på 100 kg og et volum på 1 m³. Her er resultatene når kostnadene prises basert på vekt:</p><ul><li>Vare A = 800 dollar</li><li>Vare B = 100 dollar</li></ul><p>Her er resultatene når kostnadene prises basert på volum:</p><ul><li>Vare A = 600 dollar</li><li>Vare B = 300 dollar</li></ul><p>**Merk:** Når feltet **Fordelingsmetode** er statt til *Mål*, bruker systemet målene som er angitt for både kosnadsområdet (forsendelsescontaineren) og linjene. Disse målene behøver ikke nødvendigvis å legges til den forventede summen. Hvis du imidlertid krever at de legges sammen til den forventede totalen, kan du gjøre en sjekk ved å bruke statistikken til å gå gjennom det totale målet. Innstillingen for målledetekst og automatisk oppdatering av målet på forsendelses- eller containernivå angis i sjøreisehodet.</p></li></ul> |
| **Fra dato** | Angi starten på datoområdet for etterkalkulering, hvis det er et datointervall. Denne datoen er den første datoen da den automatiske kostnaden vil gjelde. |
| **Til dato** | Angi slutten på datoområdet for etterkalkulering, hvis det er et datointervall. Denne datoen er den siste datoen da den automatiske kostnaden vil gjelde. |
| **Kategori** | <p>Velg metoden som bør brukes til å beregne kostnad. Følgende alternativer er tilgjengelige:</p><ul><li>**Fast** – Kostnaden vil bli fordelt basert på fordelingsmetoden.</li><li>**Stykker** – Kostnaden blir tildelt per stykk. Derfor brukes ikke fordelingsmetoden.</li><li>**Prosent** – En prosent av varens verdi legges til. Derfor brukes ikke fordelingsmetoden.</li><li>**Sats** – Velg dette alternativet hvis det finnes nedbryting av antall. Feltet **Fordelingsmetode** for linjen må settes til *Mål*.</li><ul> |
| **Oppdelt etter antall** | <p>Merk av i denne avmerkingsboksen for å gjøre knappen **Antalloppdelinger** tilgjengelig i hurtigfanen **Linjer**. Ved bruk av antalloppdelinger kan kostnaden deles opp og de forskjellige kostnadene kan variere, avhengig av antallet på bestillingslinjen for sjøreisen. Denne funksjonaliteten brukes ofte når leveringsmåten er flytransport. Feltet **Kategori** for linjen må settes til *Sats*.</p><p>Antallet gjelder alternativet som er valgt i feltet **Fordelingsmetode**. Kostverdien vil gå opp til antallet som er angitt i feltet **Kostnadsverdi**.<p>Et antall på 45–100 kg vil for eksempel gi en kostnad 6,00 dollar per mål (for eksempel kg/m³). Antall som overskrider 100, kg vil for eksempel gi en kostnad 5,50 dollar per mål (for eksempel kg/m³).</p> |
| **Kostnadsverdi** | Angi verdien for kostnaden. |
| **Valutakode for kostnad** | Angi valutaen for kostnaden. |
| **Varens mva-gruppe** | Velg mva-koden for kostnaden. |
| **Minimumskostnad** | <p>Dette feltet gjelder bare hvis det er merket av **Delt opp etter antall**. Hvis målet ikke når denne verdien, velges minimumsverdien, uansett hvilke kostnader som er angitt på siden **Antalloppdelinger**.<p>Et antall på 0–45 kg vil for eksempel gi en kostnad 6 dollar per mål (kg/m³). Antall på 46–100 kg vil for eksempel gi en kostnad 5,50 dollar per mål (kg/m³). Hvis 2 kg sendes, vil pauseantallet opprette en kostnadsverdi på 12 dollar. Hvis feltet **Minimumskostnad** derimot er satt til *100 dollar*, vil den endelige kostnaden bli 100 dollar.</p> |
| **Mengde** | Merk av i denne avmerkingsboksen for å gi brukere tillatelse til å flytte denne kostnaden fra forsendelsescontainernivået til sjøreisenivået. I dette tilfellet kan kostnader automatisk beregnes på forsendelsescontainernivå. De kan imidlertid også kombineres og legges sammen på tvers av alle varer i alle containerne for en sjøreise, i stedet for alle varene i de enkelte forsendelsescontainerne. |
| **Koblet kostnadstype** | <p>Koble gjeldende linje til en annen linje i den samme automatiske kostnadsposten ved å angi verdien **Kosttypekode** for linjen du vil koble til. Denne funksjonaliteten er bare tilgjengelig når feltet **Kategori** for den gjeldende linjen er satt til *Prosent*. Når gjeldende linje er koblet til en annen linje, blir kostnaden for den gjeldende linjen basert på kostnaden for den andre linjen.</p><p>Frakt er for eksempel 1 000 dollar, og du vil at drivstofftillegget skal være 10 prosent av fraktkostnaden. I dette tilfellet må linjen ha verdien **Kategori** for *Prosent*, en **Kostnadsverdi**-verdi på *10 %*, og en verdien *Frakt* for **Koblet kostnadstype**.</p> |
| **Verdijustering** og **Justeringsbeløp** | <p>Bruk disse feltene til å justere verdien og beløpet for ulike prosentverdier. De er bare tilgjengelige når feltet **Kostnadsområde** er satt til *Vare*.</p><p>Ulike kostnader kan defineres for ulike komponenter for en vare. Én komponent av en vare kan ha en annen kostnadsprosent enn de andre komponentene for denne varen. Denne fremgangsmåten kreves enkelte ganger for å verdsette en bestemt del av varene til ulike satser.</p><p>Avgiften for en avgift beregnes for eksempel på to satser: én komponent av avgiftskomponenten har en avgiftssats på 10 prosent, og en annen komponent har en avgiftssats på 2 prosent. I dette tilfellet vil etterkalkulering bli delt mellom de to komponentene.</p><p>Kostnaden beregnes for varen, men kostnadsverdien justeres etter verdien på komponentene som har den forskjellige kostnadskategorien. Kostnaden for de gjenværende komponentene kan deretter beregnes ved å bruke beløpet som den forrige beregningen ble justert med.</p><p>Komponent A i komponenten A har for eksempel en kostnad på 9,50 dollar og en avgift på 10 prosent, og komponent B har en kostnad på 0,50 dollar og en avgift på 2 prosent. Derfor er totalkostnaden 10,00 dollar. Den første oppføringen er for 10 prosent-linjen. Det bruker følgende verdier:</p><ul><li>**Kategori:** *Prosent*</li><li>**Kostnadsverdi:** *10*</li><li>**Verdijustert:** *Juster etter*</li><li>**Justert verdi:** *-0,50*</li></ul><p>Dette oppsettet angir at kostnaden for varen (10 dollar) må reduseres med 0,50 dollar (prisen på komponent B) før det beregnes et avgiftstillegg på 10 prosent. Derfor brukes 10 prosent på 9,50 dollar.</p><p>Den andre oppføringen er for linjen med 2 prosent (de 0,50 dollarene den forrige oppføringen ble justert med). Det bruker følgende verdier:</p><ul><li>**Kategori:** *Prosent*</li><li>**Kostnadsverdi:** *2*</li><li>**Verdijustert:** *Bruk*</li><li>**Justering:** *0,50*</li></ul><p>Dette oppsettet beregner gjenværende avgift som betales på komponent B.</p> |
