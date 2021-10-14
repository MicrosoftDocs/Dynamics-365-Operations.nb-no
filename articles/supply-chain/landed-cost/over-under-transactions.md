---
title: Over-/undertransaksjoner
description: Dette emnet formidler informasjon som vil hjelpe deg med å definere detaljene for policyer for over-/undertransaksjoner, slik at systemet kan bestemme hvordan overbehandlingen og underbehandlingen av varer behandles når de mottas.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 60f4f31e9da762a89b034961a703e1d7b1bbd903
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580750"
---
# <a name="overunder-transactions"></a>Over-/undertransaksjoner

[!include [banner](../../includes/banner.md)]

Når ordrene i en sjøreise behandles, forventer systemet at vareantallet som mottas i det endelige destinasjonslageret, stemmer overens med antallet som er angitt på bestillingslinjene som er knyttet til sjøreisen. Ettersom det nøyaktige antallet på bestillingslinjene ikke alltid er mottatt på lageret, definerer imidlertid modulen **Netto innkjøpspris** et sett med regler som brukes til å håndtere overmottak og undermottak av varer. Disse reglene er spesielt viktige fordi den opprinnelige bestillingen er fakturert og ikke lenger kan endres. Ved å definere detaljene for policyer for over-/undertransaksjoner, kan systemet fastslå hvordan overbehandlingen og underbehandlingen av varer håndteres når de mottas. Du kan også manuelt styre over- og underlager ved å bruke siden **Over-/undertransaksjoner**.

## <a name="overunder-tolerances"></a>Over-/undertoleranser

Du kan angi toleranse for over- og underlevering for å angi over- og undermengder eller volumer som kan behandles for en sjøreise uten å forårsake en feil. Hvis kvitteringen på sjøreiselinjen er utenfor disse toleransene, må den endres og løses før sjøreiselinjen kan lukkes for videre behandling.

Hvis du vil konfigurere toleransene, går du til **Netto innkjøpspris \> Over-/underoppsett \> Over-/undertoleranser**. Der kan du vise, redigere, legge til og fjerne toleranseposter. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Kontokode | <p>Definer omfanget av leverandører som toleransen gjelder, ved å velge én av følgende verdier:</p><ul><li>**Tabell** – Over-/undertoleransen gjelder bare for leverandøren som er valgt for raden.</li><li>**Gruppe** – Over-/undertoleransen gjelder for alle leverandører i leverandørtoleransegruppen som er valgt for raden.</li><li>**Alle** – Over-/undertoleransen gjelder alle leverandører.</li></ul> |
| Kontorelasjon | Velg leverandøren eller leverandørgruppen som over-/undertoleransen gjelder for, avhengig av verdien du har valgt i feltet **Kontokode**. |
| Varekode | <p>Definer omfanget av varer som toleransen gjelder, ved å velge én av følgende verdier:</p><ul><li>**Tabell** – Over-/undertoleransen gjelder bare for varen som er valgt for raden.</li><li>**Gruppe** – Over-/undertoleransen gjelder for alle varene i varetoleransegruppen som er valgt for raden.</li><li>**Alle** – Over-/undertoleransen gjelder alle varer.</li></ul> |
| Varerelasjon | Velg varen eller varegruppen som over-/undertoleransen gjelder for, avhengig av verdien du har valgt i feltet **Varekode**. |
| Beløpstoleranse | Angi beløpstoleransen som skal brukes på en hel bestilling. |
| Prosenttoleranse | Angi prosenttoleransen som skal brukes på en enkelststående bestillingslinje. |

## <a name="overunder-reasons"></a>Over-/underårsaker

Når et over- eller underantall er knyttet til en sjøreiselinje som mottas, kan det hende at du må identifisere årsaken til over- eller underantallet. I dette tilfellet kan du velge overleverings- eller underleveringsårsaken på mottakslinjen når varene mottas.

Hvis du vil definere overleverings- og underleveringsårsaker, kan du gå til **Netto innkjøpspris \> Over-/underoppsett \> Over-/underårsaker**. Der kan du vise, redigere, legge til og fjerne tilgjengelige årsaker til overlevering og underlevering. Følgende tabell beskriver feltene som er tilgjengelige for hver årsak.

| Felt | beskrivelse |
|---|---|
| Over-/underårsak | Angi et unikt navn for årsaken til transaksjonen for over- eller undermottak. |
| beskrivelse | Angi en beskrivelse av over-/underårsaken. |
| Bevegelse | Velg bevegelsesjournalen som er knyttet til over-/underårsaken. Dette feltet viser alle tilgjengelige journaler som journaltypen *Bevegelse* er tilknyttet, på siden **Lagerjournalnavn** (**Lagerstyringsoppsett \> Journalnavn \> Lager**). |

## <a name="item-overunder-tolerance-groups"></a>Over-/undertoleransegrupper for vare

Varer som har lignende toleranser, kan grupperes sammen. På denne måten kan du definere over-/undertoleranse for alle varer i denne gruppen samtidig.

Hvis du vil definere over-/undertoleransegrupper for vare, går du til **Netto innkjøpspris \> Over-/underoppsett \> Over-/undertoleransegrupper for vare**. Der kan du vise, redigere, legge til og fjerne poster for over-/undertoleransegrupper. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Gruppe for over-/undertoleranse | Angi et unikt navn for gruppen. Velg et navn som beskriver toleransen, for eksempel *1 % Var*. |
| beskrivelse | Angi en beskrivelse av gruppen. |

## <a name="vendor-overunder-tolerance-groups"></a>Leverandørens over-/undertoleransegrupper for vare

Du kan gruppere leverandører som regelmessig over- eller underlevering. Du kan deretter definere over-/undertoleranse per gruppe.

Hvis du vil definere over-/undertoleransegrupper for leverandør, går du til **Netto innkjøpspris \> Over-/underoppsett \> Over-/undertoleransegrupper for leverandør**. Der kan du vise, redigere, legge til og fjerne poster for over-/undertoleransegrupper. Følgende tabell beskriver feltene som er tilgjengelige for hver post.

| Felt | beskrivelse |
|---|---|
| Over-/undergrupper | Angi et unikt navn for gruppen. Velg et navn som beskriver leverandørtypen som tilhører gruppen. |
| beskrivelse | Angi en beskrivelse av gruppen. |

## <a name="view-and-process-overunder-transactions"></a>Vise og behandle over-/under-transaksjoner

Over- og undertransaksjoner genereres når antallet varer som er plassert, ikke samsvarer med det initialiserte antallet. Antallet i ankomstjournalen bør bare oppdateres med antallet som er lagt bort.

Når mottaket av sjøreiselinjer behandles, kan over-/under-toleranser angis for en leverandør. Varene vil deretter bli gjennomgått og validert. Toleransen kan angis som en prosent, et lokalt beløp eller begge deler.

Hvis en vare som mottas er inni toleransen, genererer systemet en bevegelsesjournal. Denne journalen kan angis på parametersiden for sjøreisen. I tillegg opprettes det en over-/under-transaksjon. Ordreverdien kan for eksempel være 100 dollar, mottaksverdien er 99 dollar, og disse verdiene oppfyller toleransereglene. I dette tilfellet opprettes det en negativ bevegelsesjournal for det undermottatte antallet.

Hvis en vare som mottas, er utenfor toleransen, genererer systemet en over-/under-transaksjon for differansen i antall.

Hvis du vil vise og behandle over-/under-transaksjoner, går du til **Netto innkjøpspris \> Forespørsler \> Over-/undertransaksjoner**. Der vil en over-/under-transaksjon bli knyttet til alle varer for en sjøreise som er overmottatt eller undermottatt. Det anbefales at du bruker siden **Over-/undertransaksjoner** til å løse alle over-/undertransaksjoner som er knyttet til sjøreiser. Det anbefales også at du **ikke** bruker bevegelses- eller opptellingsjournaler til manuelt å løse lagertransaksjoner for underlevering. I stedet bør du bruke siden **Over-/undertransaksjoner** til å administrere lagerantallet for underlevering.

### <a name="upper-overview-tab"></a>Øvre del av fanen Oversikt

Hvis du vil vise over-/undertransaksjoner, velger du fanen **Oversikt** i den øvre delen av siden **Over-/undertransaksjon**. Følgende tabell beskriver feltene som er tilgjengelige i rutenettet.

| Felt | beskrivelse |
|---|---|
| Over-/undertransaksjonsnummer | Det unike navnet på over-/undertransaksjonsposten som ble opprettet automatisk da ankomstjournalen ble behandlet. |
| Sjøreise | Sjøreisen som innkjøpslinjen var knyttet til. |
| Fraktcontainer | Containeren som innkjøpslinjen var knyttet til. |
| Ankomstjournal | Ankomstjournalen som over-/underlinjen ble generert fra. |
| Referanse | En referanse til enten bestillingen eller overføringsordren som er knyttet til over-/under-transaksjonen. |
| Antall | Bestillingen det refereres til i over-/undertransaksjonen. |
| Leverandørnummer | Leverandøren som over eller under er knyttet til. |
| Nummer for varer i transitt | Eventuelt nummer for varer i transitt. |
| Varenummer | Varenummeret som over eller under er knyttet til. |
| Opprinnelig antall | Det opprinnelige antallet på bestillingslinjen som er knyttet til forsendelsen. |
| Mottatt antall | Antallet som faktisk ble mottatt. |
| Differanse | Differansen mellom det forventede ankomstjournalbeløpet og beløpet som ble postert i ankomstjournalen. En negativ verdi angir en overlevering av varer. |
| Restantall | Antallet som gjenstår på ankomstjournallinjen. |
| Over-/underlevering | En verdi som angir om antallet som ble mottatt, er over eller under. |
| Status | Statusen for over-/undertransaksjonen. Overlevering kan automatisk opprette en bevegelsesjournal for overleveringsbeløpet og postere journalen, avhengig av innstillingene på siden **[Parametere for netto innkjøpspris](landed-cost-parameters.md)**. I dette tilfellet får over-/under-transaksjonen statusen *Fullført*. Hvis det kreves en handling for å flytte varene ut av underleveringslageret, får posten statusen *Pågår*. |
| Over-/underårsak | Årsaken som er knyttet til over-/undertransaksjonen. |
| Andre lagerdimensjoner | Du kan vise kolonner for tilleggsdimensjoner i rutenettet etter behov. Disse dimensjonene inkluderer partinummer, lagerstatus og lager. Velg **Lager \> Visningsdimensjoner** i handlingsruten for å åpne en dialogboks der du kan velge hvilke dimensjoner som skal tas med. |

### <a name="upper-general-tab"></a>Øvre del av fanen Generelt

Hvis du vil vise mer informasjon om linjen som for øyeblikket er valgt i den øvre fanen **Oversikt**, velger du fanen **Generelt** i øvre del av siden **Over-/undertransaksjon**. Informasjonen i denne fanen inkluderer verdiene for alle tilgjengelige dimensjoner. Denne informasjonen hentes fra den opprinnelige bestillingen.

### <a name="lower-overview-tab"></a>Nedre del av fanen Oversikt

Hvis du vil vise dokumenttypen for raden som er valgt i den øvre fanen **Oversikt**, velger du fanen **Oversikt** i nedre del av siden **Over-/undertransaksjon**. Følgende tabell beskriver feltene som er tilgjengelige.

| Felt | beskrivelse |
|---|---|
| Ny dokumenttype | Dette feltet settes til *Bevegelsesjournal* eller *Bestilling*, avhengig av hvilken handling som vises på den valgte over-/under-transaksjonslinjen. |
| Antall | En referanse og kobling til bestillingen eller bevegelsesjournalen som er knyttet til den valgte over-/under-transaksjonslinjen. |
| Over-/underårsak | Årsaken som er knyttet til den valgte over-/undertransaksjonslinjen. |
| Antall | Antallet du valgte for bestillingen eller bevegelsesjournalen som er knyttet til den valgte over-/under-transaksjonslinjen. |

### <a name="lower-general-tab"></a>Nedre del av fanen Generelt

Hvis du vil vise over-/undertransaksjonsnummer, parti-ID og dimensjonsnummer som er knyttet til den valgte over-/undertransaksjonslinjen, velger du fanen **Generelt** i den nedre delen av siden **Over-/under-transaksjoner**. 

### <a name="process-overunder-transactions"></a>Behandle over-/under-transaksjoner

Handlingsruten på siden **Over-/undertransaksjoner** inneholder følgende kommandoer for behandling av transaksjonene som er valgt på siden. Ved hjelp av hver kommando kan du velge hvordan hver transaksjon skal behandles.

- **Opprett \> Bevegelse** – Opprett og poster en bevegelsesjournal for den valgte transaksjonen. For undertransaksjoner opprettes og posteres en bevegelsesjournal automatisk for differansen mellom det forventede og det mottatte antallet. Velg denne kommandoen for overtransaksjoner hvis du vil at leverandøren skal realisere kostdifferansen.
- **Opprett \> Bestilling** – Opprett en bestilling for forskjellen mellom forventet og faktisk mottatt antall for den valgte transaksjonen. Velg denne kommandoen for overtransaksjoner hvis organisasjonen kommer til å realisere kostdifferansen.
- **Opprett \> Overfør til mål** – Denne kommandoen gjelder bare for overføringsordrer. Velg kommandoen hvis du vil overføre over- eller underantallet til mållageret.
- **Opprett \> Overfør til opprinnelse** – Denne kommandoen gjelder bare for overføringsordrer. Velg kommandoen hvis du vil overføre over- eller underantallet til det opprinnelige lageret.
