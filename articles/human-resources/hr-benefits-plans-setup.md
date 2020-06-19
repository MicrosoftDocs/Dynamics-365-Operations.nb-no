---
title: Opprette en fordelsplan
description: Definer fordelsplaner i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bcbf4c1a7f136e5563bf1210b6c09228dad95dea
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429258"
---
# <a name="create-a-benefits-plan"></a>Opprette en fordelsplan

Denne artikkelen viser deg hvordan du definerer fordelsplaner i Dynamics 365 Human Resources.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Ny**.

3. I kategorien **Generelt** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Plan** | En unik ID for planen. |
   | **Beskrivelse** | En beskrivelse av planen. |
   | **Plantype** | Når du oppretter en ny plan, må du angi plantypen. En plantype er en gruppering på høyt nivå av bestemte typer fordeler. Hver plantype angir om en ansatt kan registrere seg i flere planer av denne typen, angir om kontakter er mottakere eller avhengige, og definerer dekningsalternativer. Du kan opprette nye, egendefinerte plantyper for å dekke behovene til fordelstilbudene. De viktigste fordelsplantypene er: <ul><li>401K</li><li>ADD</li><li>Tannpleie</li><li>Helse</li><li>FSA</li><li>Liv</li><li>LTD</li><li>Medisinsk</li><li>PTO</li><li>STD</li><li>Syn</li></ul> |
   | **Kode for plantype** | Plantypekoden for plantypen. |
   | **Programmet** | Angir et program du kan tilordne planen i. |
   | **Bunt** | Angir en bunt du kan tilordne planen i. |
   | **Mester** | Angir om planen er hovedplanen i bunten den er tilordnet til. |
   | **Status** | Viser den gjeldende statusen for fordelsplanen. Standardverdien er Aktiv. Hvis du endrer statusen til Inaktiv, vil ikke planen være tilgjengelig som et valg under registreringen. |
   | **Gyldig fra-dato og -klokkeslett** | Datoen og klokkeslettet når planen starter. Standardverdien er gjeldende systemdato. |
   | **Gyldig til-dato og -klokkeslett** | Datoen og klokkeslettet når planen slutter (statusen settes til Inaktiv). Standardverdien er 12/31/2154, som i praksis betyr aldri. |

4. I kategorien **Konfigurasjon** angir du verdier for følgende felt, avhengig av hvilken type plan du oppretter:

   | Plantype | Felt | Beskrivelse |
   | --- | --- | --- |
   | Medisinsk (medisinsk, tannlege, syn, HMO) | COBRA | Angir om planen er COBRA-berettiget (Consolidated Omnibus Budget Reconciliation Act). |
   | Medisinsk (medisinsk, tannlege, syn, HMO) | HIPAA | Angir om planen er HIPAA-berettiget (Health Insurance Portability and Accountability Act). |
   | <ul><li>Medisinsk (medisinsk, tannlege, syn, HMO)</li><li>Annet (PTO, helse)</li><li>Andre</li><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li><li>Sparinger (for eksempel 401(k))</li><li>FSA</li></ul> | Kvalifisert før skatt | Angir om det kan gjøres bidrag til planen før avgifter brukes. |
   | <ul><li>Medisinsk (medisinsk, tannlege, syn, HMO)</li><li>Annet (PTO, helse)</li><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li><li>Sparinger (for eksempel 401(k))</li><li>FSA</li></ul> | Kvalifisert etter skatt | Angir om det kan gjøres bidrag til planen etter avgifter brukes. |
   | <ul><li>Medisinsk (medisinsk, tannlege, syn, HMO)</li><li>Annet (PTO, helse)</li><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li><li>Sparinger (for eksempel 401(k))</li><li>FSA</li></ul> | Bidragsyter | Angir hvem som bidrar til planen – den ansatte, arbeidsgiveren eller begge. |
   | <ul><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li></ul> | Minimumsdekning | Minimumsbeløpet for forsikringsdekning som kreves for planen. |
   | <ul><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li></ul> | Maksimumsdekning | Maksimumsbeløpet for forsikringsdekning som kreves for planen. |
   | <ul><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li></ul> | Bruk dekningstrinn | Angir om det skal bekreftes at dekningsbeløpet samsvarer med et gyldig trinnvis beløp. |
   | <ul><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li></ul> | Trinnvist beløp | Det trinnvise beløpet for forsikringsdekning for planen. Hvis for eksempel det trinnvise beløpet er 1000, kan en ansatt ikke ha forsikring på $200 500 forsikring, de må runde av oppover til $201 000 eller nedover til $200 000. |
   | <ul><li>Langsiktig uførhet</li><li>ADD (enkelt liv, frivillig liv)</li></ul> | Trinnvis retning | Angir avrundingsretningen (opp eller ned) når dekningsbeløpet ikke oppfyller den trinnvise beløpsverdien. |
   | ADD (enkelt liv, frivillig liv) | Forsikringsbarhetsbevis | Angir om en ansatt må oppgi bevis på at vedkommende kan forsikres. |
   | ADD (enkelt liv, frivillig liv) | Beløp | Beløpet i regnskapsvaluta. Dette feltet er bare aktivt hvis det er merket av for Bevis på forsikringsrett. |
   | <ul><li>Sparinger (for eksempel 401(k))</li><li>FSA</li></ul> | Årlig minimumsbidrag | Minimum bidragsbeløp som kreves for planen. |
   | <ul><li>Sparinger (for eksempel 401(k))</li><li>FSA</li></ul> | Årlig maksimumsbidrag | Maksimum bidragsbeløp som kreves for planen. |
   | Sparinger (for eksempel 401(k)) | Årlig maksimumsbeløp for arbeidsgiver | Maksimumsbeløpet en arbeidsgiver kan bidra med mot spareplanen for en ansatt i en fordelsperiode. Du må merke av for Match ansatt for å kunne bruke dette feltet. |
   | Sparinger (for eksempel 401(k)) | Arbeidsgiversamsvar | Angir om arbeidsgiveren bidrar til spareplanen til en ansatt. |
   | Sparinger (for eksempel 401(k)) | Prosent for arbeidsgiversamsvar | Prosentandelen av et ansattbidrag som arbeidsgiveren vil matche. |
   | Sparinger (for eksempel 401(k)) | Grense for arbeidsgiversamsvar | Den maksimale prosentandelen arbeidsgiveren vil matche. Hvis en arbeidsgiver for eksempel vil matche 100 % av ansattbidraget på opptil 6 % av den ansattes lønn, er arbeidsgivers matchtak lik 6 %. |

5. I kategorien **Oppsett** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Tillat/fortsett registrering** | Angir om ansatte kan registrere seg i planen hvis de oppfyller kravene til rettigheter.</br></br>Hvis denne er satt til Nei, vil ikke planen være tilgjengelig for ansatte når du behandler rettigheter. |
   | **Registrer automatisk fra foregående år** | Angir om en kvalifisert ansatt skal registreres automatisk i planen hvis vedkommende ble registrert i løpet av foregående år. |
   | **Registrer automatisk som standard** | Angir om planen skal velges for registrering som standard. Planen er ikke obligatorisk, slik at den ansatte kan endre standardvalget. |
   | **Lukket for nye registreringer** | Angir om planen skal begrenses til bare kvalifiserte ansatte som ble registrert i planen i fjor. |
   | **Obligatorisk plan** | Angir om ansatte skal registreres i planen automatisk. Ansatte kan ikke endre registreringsvalget. |
   | **Startdato** | Datoen da planen ble opprettet i firmaet. |
   | **Leverandørkonto** (fordelsleverandør) | Leverandøren som firmaet betaler bonuser til for planen. |
   | **Navn** (fordelsleverandør) | Navnet på leverandøren. |
   | **Leverandørreferanse** (fordelsleverandør) | Leverandørens referanse for planen. For eksempel firmaets gruppeplannummer. |
   | **Alternativ referanse** (fordelsleverandør) | Leverandørens alternative referanse for planen. For eksempel firmaets kontonummer. |
   | **Valuta** (fordelsleverandør) | Valutaen som brukes til å betale bonuser til leverandøren. |
   | **Utgiftskonto** (fordelsleverandør) | Finanskontoen som brukes som utgiftskonto for planbonuser. |
   | **Leverandørkonto** (fordelsadministrator) | Leverandøren som firmaet betaler for å administrere planen. Hvis planen er selvadministrert, lar du dette feltet stå tomt. |
   | **Navn** (fordelsadministrator) | Navnet på fordelsadministratorleverandøren. |
   | **Leverandørreferanse** (fordelsadministrator) | Administratorleverandørens referanse for planen. |
   | **Alternativ referanse** (fordelsadministrator) | Administratorleverandørens alternative referanse for planen. |
   | **Valuta** (fordelsadministrator) | Valutaen som brukes til å betale fordelsadministratorne. |
   | **Utgiftskonto** (fordelsadministrator) | Finanskontoen som brukes som utgiftskonto for kostnadene som er forbundet med administrasjon av planen. |

6. Filtrer etter behov i kategorien **Filtre**. Du kan filtrere etter følgende felt:

   - **Forretningsenhet**
   - **Avdeling**
   - **Juridisk enhet**
   - **Lokasjon**
   - **Posisjon**

7. I kategorien **Rettighetsregler** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Linjenummer** | Linjenummeret til rettighetsregelen. |
   | **Rettighetsregel** | En rettighetsregel som skal brukes for fordelsplanen. Denne rettighetsregelen vil bli brukt på den tilsvarende handlingstypen og knyttet til den angitte dekningsventeperioden og fradrag. |
   | **Handlingstype** | Handlingen rettighetsregelen skal brukes på: fordelsregistrering eller fordelsutløp. |
   | **Venteperiode for dekning** | En verdi fra skjemaet Venteperioder. Dekningsventeperioden styrer antall dager eller måneder en ansatt venter på fordelsdekning eller fordelsutløp, basert på kriteriene i rettighetsregelen og handlingstypen. |
   | **Venteperiode for fradrag** | En verdi fra skjemaet Venteperioder. Fradragsventeperioden styrer antall dager eller måneder en ansatt venter på fordelsfradrag fra lønnsslippen, basert på kriteriene i rettighetsregelen og handlingstypen. |

8. Velg **Lagre**.

## <a name="view-enrolled-workers"></a>Vise registrerte arbeidere

Du kan vise de registrerte arbeiderne som er registrert i en valgt fordelsplan.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Registrerte arbeidere**.

## <a name="attach-coverage-options"></a>Tilknytt dekningsalternativer

Du kan legge til dekningsalternativer i den valgte fordelsplanen. Når du legger ved dekningsalternativer, samles satsen og fradragsoppsettet for et dekningsalternativ.  Eksempel: For en medisinsk plan vil brukeren velge et familiedekningsalternativ.  De må da velge familiesatsen for den tilknyttede planen (definert i satsoppsett) og fradraget for den tilknyttede planen (angis i satsoppsett). Dette gir kostnaden for arbeidsgiveren og den ansatte for en valgt dekning. Deretter kan du gjenta prosessen for en ansatt+1-dekning eller ansattdekning.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Legg ved dekningsalternativer**.

## <a name="override-eligibility-rules"></a>Overstyre rettighetsregler

Du kan legge til arbeidere i en plan som unntak i rettighetsreglene. Hver arbeider du legger til, vil være berettiget for fordelsplanen.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Overstyr rettighetsregler**.

## <a name="view-attached-periods"></a>Vise tilknyttede perioder

Du kan vise en liste over de tilgjengelige fordelsperiodene.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Perioder**.

## <a name="view-plan-information"></a>Vise planinformasjon

Du kan gi en beskrivelse av planen for å hjelpe de ansatte med sine fordelsvalg. Planinformasjonen du angir her, vises i Ansattselvbetjening når du holder musepekeren over planen i listen over dekningsalternativer.

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Planinformasjon**.

## <a name="view-flex-credit-programs"></a>Vis fleksikredittprogrammer

1. I arbeidsområdet **Fordelsbehandling**, under **Planer**, velger du **Fordelsplaner**.

2. Velg **Fleksible kredittprogrammer**.
