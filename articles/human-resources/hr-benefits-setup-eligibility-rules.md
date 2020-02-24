---
title: Konfigurere rettighetsregler og -alternativer
description: Angi rettighetsregler og alternativer i Fordelsbehandling i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 448156a2428e99d8b95de547cb6f1621d49b1c7b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010133"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurere rettighetsregler og -alternativer

[!include [banner](includes/preview-feature.md)]

Når du har konfigurert de nødvendige parameterne for Fordelsbehandling i Microsoft Dynamics 365 Human Resources, kan du opprette rettighetsregler, pakker, perioder og programmer som du vil knytte til dine fordelsplaner.

## <a name="create-an-eligibility-rule"></a>Opprette en rettighetsregel

Rettighetsregler definerer hvilke ansatte som kan registrere seg i hver fordelsplan. Når du har definert rettighetsregler, kan du tilordne dem til fordelsplaner. Deretter kan du behandle registreringsrettighetene for å se hvilke ansatte som er berettiget for hver plan. 

Under åpen registrering kan ansatte velge fordelsplaner. Hvis de ikke er berettiget til en fordelsplan basert på rettighetsregler etter at de allerede er registrert, avregistreres de ikke automatisk. Når det oppstår en livshendelse som påvirker planrettighetene, startes en registreringsperiode for den ansatte for å velge planer som de er berettiget til. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I kategorien **Rettighetsregler** velger du **Ny** for å opprette en rettighetsregel. Hvis du vil se planer som er knyttet til en rettighetsregel, velger du **Tilknyttede planer**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Rettighetsregel** | En unik identifikator for rettighetsregelen. |
   | **Beskrivelse** | En beskrivelse av rettighetsregelen. |
   | **Gyldig fra-dato og -klokkeslett** | Startdatoen for rettighetsregelen. | 
   | **Gyldig til-dato og -klokkeslett** | Sluttdatoen for rettighetsregelen. |
   | **Brukeransattype** | Angir om den ansattes ansattype skal brukes i regelen for fordelsrettigheten. |
   | **Arbeidertype** | Arbeidertypen, hvis **Bruk ansattype** er satt til **Ja**. |
   | **Bruk ansattstatus** | Angir om den ansattes ansettelsesstatus skal brukes i regelen for fordelsrettigheten. |
   | **Status** | Ansattstatusen, hvis **Bruk ansattstatus** er satt til **Ja**. Hvis **Bruk ansattstatus** er satt til to **Nei**, brukes ikke feltet. |
   | **Bruk ansettelseskategori** | Angir om den ansattes verdi for **Ansettelseskategori** skal brukes som en del av regelen for fordelsrettigheten. | 
   | **Ansettelseskategori** | Den ansattes ansettelseskategori hvis **Bruk ansettelseskategori** er satt til **Ja**. |
   | **Bruk ny ansettelsesregel** | Angir om ansettelsesperioden for en ny ansatt skal brukes som en del av regelen for fordelsrettighet. |
   | **Registreringsperiode** | Tidsperioden når ny ansettelsesregistrering tillates. Hvis du også angir dette i parametere, overstyrer parameterinnstillingen dette. |

4. Under **Tilleggskriterier** velger du følgende alternativer og legger til informasjon etter behov:

   | Alternativ | Beskrivelse |
   | --- | --- |
   | **Kvalifisert alder** | Angir aldersområdet eller -områdene som kreves for å oppfylle rettighetsregelen. |
   | **Kvalifisert avdeling** | Angir avdelingen eller avdelingene som en ansatt må være i for å tilfredsstille rettighetsregelen. |
   | **Kvalifisert ansettelsestype** | Angir ansettelsestypen(e) som en ansatt må være kategorisert som, for å tilfredsstille rettighetsregelen. For eksempel fulltid eller deltid. |
   | **Kvalifisert jobb** | Angir jobben eller jobbene som oppfyller rettighetsregelen. Jobber knyttes til stillinger, og stillinger fylles av ansatte. |
   | **Kvalifisert jobbfunksjon** | Angir jobbfunksjonen(e) som oppfyller en rettighetsregel. For eksempel selgere eller teknikere. |
   | **Kvalifisert jobbtype** | Angir jobbtypen(e) som oppfyller rettighetsregelen. For eksempel kontorist eller leder. |
   | **Kvalifisert juridisk enhet** | Angir den juridiske enheten eller de juridiske enhetene som er gyldige for rettighetsregelen. For eksempel Contoso Entertainment System USA. |
   | **Kvalifisert kompensasjonsområde** | Angir ansattlokasjonen som oppfyller rettighetsregelen. For eksempel det sentrale USA. |
   | **Kvalifisert stilling** | Angir stillingen(e) som oppfyller rettighetsregelen. For eksempel personalassistent eller personalsjef. |
   | **Kvalifisert stillingstype** | Angir stillingstypen(e) som oppfyller rettighetsregelen. For eksempel fulltid. |
   | **Kvalifisert stat** | Angir delstatene eller provinsene som oppfyller rettighetsregelen. For eksempel Nord-Dakota USA eller Britisk Columbia, Canada. |
   | **Kvalifiserte ansettelsesbetingelser** | Angir ansettelsesvilkårene som oppfyller rettighetsregelen. For eksempel, frivillig eller gruppekontrakt. |
   | **Kvalifisert fagforening** | Angir fagforeningsmedlemskapene som oppfyller rettighetsregelen. For eksempel Forklift Drivers of America. </br></br>Når du bruker en fagforeningsbasert rettighetsregel, må fagforeningsposten ha sluttdatoen fylt ut. Du kan ikke la dette stå tomt. |
   | **Berettiget postnummer** | Angir postnumrene som oppfyller rettighetsregelen. For eksempel 58104. |

5. Under **Flere detaljer** kan du vise følgende tilleggsdetaljer:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Felt for kvalifisert bruker** | Angir flere rettighetsregler basert på kundedefinerte felt. |
   | **Rettighetstype** | Angir den valgte kriteriekategorien under **Tilleggskriterier**. |
   | **Rettighetsreferanse** | Angir verdiene du valgte, under **Tilleggskriterier**. |
   | **Beskrivelse** | Beskrivelsen du valgte, under **Tilleggskriterier**. |

6. Velg **Lagre**.

## <a name="configure-bundles"></a>Konfigurere bunter

Bunter er et sett med relaterte fordelsplaner. Du kan bruke fordelsbunter til å gruppere fordelsplaner som en ansatt må velge for å registrere seg i bestemte fordelsplaner som kan være avhengige av andre fordelsplanregistreringer. Eksempler på når du kanskje vil bruke en bunt, omfatter følgende:

- En helseplanbunt som inkluderer høyt fradragsberettiget helseforsikring med en tilknyttet helsesparekonto (HSA).

- En forsikringsplan for livstid med en obligatorisk forsikringsplan for den ansatte, gruppert med en avhengig livsplan. Dette vil sikre at en ansatt ikke kan velge en avhengig dekningstid uten å registrere seg for ansattdekningen.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I **Bunter**-kategorien velger du **Ny** for å opprette en bunt. Hvis du vil se planer som er knyttet til en bunt, velger du **Tilknyttede planer**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Bunt** | En unik ID for bunten. |
   | **Beskrivelse** | En beskrivelse av bunten. |
   | **Mester** | Angir om en av planene i bunten må være merket som hovedplanen. Hovedplanen må velges under åpen registrering som en del av bunten før fordelsadministratoren kan bekrefte de ansattes fordelsvalg. |
   | **Gyldig fra-dato og -klokkeslett** | Datoen og klokkeslettet bunten blir aktiv. |
   | **Gyldig til** | Datoen da bunten utløper. Standardverdien er 12/31/2154, som i praksis betyr aldri. |

4. Velg **Lagre**.

## <a name="configure-periods"></a>Konfigurere perioder

Perioder definerer når fordeler er i kraft, og når ansatte har tillatelse til å registrere seg. Du kan opprette så mange perioder du vil, for å opprettholde åpne perioder for fordelsregistrering og fordelsdekning. Fordelsplanår kan eller kanskje ikke følge et kalenderår. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I **Perioder**-kategorien velger du **Ny** for å opprette en periode. Hvis du vil kjøre en prosess som knytter alle gyldige, aktive fordelsplaner til fordelsperioden, velger du **Tilknytt planer**. Hvis du vil se planer som er knyttet til en bunt, velger du **Tilknyttede planer**. 

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Periode** | En unik ID for perioden. |
   | **Gyldig fra-dato og -klokkeslett** | Startdatoen og klokkeslettet da fordelsperioden er aktiv. |
   | **Gyldig til-dato og -klokkeslett** | Datoen og klokkeslettet da fordelsperioden blir inaktiv. |
   | **Registreringsstart** | Startdatoen for åpen registrering. Åpen registrering er når en ansatt kan lage fordelsvalg i selvbetjeningsfordelene. |
   | **Registreringsslutt** | Sluttdatoen for åpen registrering. |
   | **Åpne** | Angir om perioden er åpen basert på systemdatoen og gyldig fra- og til-dato og -klokkeslett. | 
   | **Forrige periode** | Angir fordelsperioden som kommer før den valgte fordelsperioden. Denne informasjonen brukes under registrering av fordelsrettigheter til å tilordne planer, dekningsalternativer og berettigede fra et tidligere år. |
 
4. Velg **Lagre**.

## <a name="use-a-flex-credit-program"></a>Bruke et fleksibelt kredittprogram

Du kan bruke fleksible kredittprogrammer til å registrere ansatte i fordeler i henhold til et forhåndsdefinert antall fleksible kreditter. Ansatte kan velge hvordan de skal fordele den fleksible kreditten. Hvis for eksempel en ansatt er dekket under sin ektefelles forsikringsplan, ønsker de kanskje å bruke kredittene de ellers ville ha brukt på helsedekning, på andre fordeler.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I kategorien **Perioder** velger du **Fleksible kredittprogrammer**.

3. Velg et fleksibelt kredittprogram som skal brukes. Feltene inneholder følgende informasjon:

   | Felt | Beskrivelse |
   | --- | --- |
   | ID for fordelskreditt | Den unike ID-en til det fleksible kredittprogrammet. |
   | Beskrivelse | En beskrivelse av det fleksible kredittprogrammet. | 
   | Fra dato | Datoen da de fleksible kreditt programmet blir aktivt. |
   | Til dato | Sluttdatoen for det fleksible kredittprogrammet. Du kan la standardverdien (12/31/2154) bli værende for å angi at det fleksible kredittprogrammet ikke har en planlagt utløpsdato. |
   | Kredittverdi totalt | Antall kreditter som hver ansatt skal ha for deres fordeler. |
   | Fordelingsregel | Regelen som skal brukes for å fordele fleksible kreditter når en ansatt blir ansatt i midt i en periode for fleksibel kreditt. </br></br><ul><li>**Ingen** – den ansatte får ingen fleksibel kreditt hvis de blir ansatt etter at perioden for det fleksible kredittprogrammet begynner.</li><li>**Full kreditt** – den ansatte mottar hele beløpet med fleksibel kreditt, uansett når de er ansatt.</li><li>**Fordelt** – den ansatte får en fordelt mengde fleksibel kreditt, basert på startdatoen.</li></ul> |
   | Fordelingsformel for fleksikreditt | Regelen som skal brukes for å fordele fleksible kreditter for ansatte som blir ansatt i midt i en fordelsperiode for det fleksible kredittprogrammet. Fordelingen er basert på startdatoen for ansettelsen. Feltet brukes bare hvis du velger **Fordeling** i **Fordelingsregel**-feltet. </br></br><ul><li>**Daglig** – Fordeler antallet fleksible kreditter en ansatt mottar til dagsnivået. Det totale antallet fleksible kreditter deles på antall dager i perioden. Hvis fordelsperioden for eksempel er på 400 dager, vil systemet dele det totale antallet fleksible kreditter med 400 for å beregne antallet fleksible kreditter som de ansatte mottar per dag.</li><li>**Gjeldende måned** – Fordeler antallet fleksible kreditter en ansatt mottar til månedsnivået, avrundet til gjeldende måned. Det totale antallet fleksible kreditter deles på antall måneder i perioden. Hvis fordelsperioden for eksempel er på 15 måneder, vil systemet dele det totale antallet fleksible kreditter med 15 for å beregne antallet fleksible kreditter som de ansatte mottar per måned.</li><li>**Følgende måned** – Fordeler antallet fleksible kreditter en ansatt mottar til månedsnivået, avrundet til neste måned. Det totale antallet fleksible kreditter deles på antall måneder i perioden. Hvis fordelsperioden for eksempel er på 15 måneder, deler systemet det totale antallet fleksible kreditter med 15 for å beregne antallet fleksible kreditter som de ansatte mottar per måned.</li></ul> |
   
   Pass på at hver fordelsplan bare registreres i ett fleksibelt kredittprogram per fordelsperiode. Ellers vet ikke systemet hvilket fleksibelt kredittprogram som skal brukes til å gi fleksible kreditter, og du vil få problemer. 

## <a name="configure-programs"></a>Konfigurere programmer

Programmer er et sett med fordelsplaner som deler et felles sett med rettighetsregler. Du kan definere rettighetsregler for hele programmet i stedet for for hver enkelt plan. For eksempel et Contoso Canada FTE-program eller Contoso Europe-program på ledernivå. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I **Programmer**-kategorien velger du **Ny** for å opprette et program. Hvis du vil opprette unntak for ansatte som ikke oppfyller rettighetsregelkravene, velger du **Overstyr rettighetsregler**. Hvis du vil se planer som er knyttet til et program, velger du **Tilknyttede planer**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Programmet** | En unik ID for programmet. |
   | **Beskrivelse** | En beskrivelse av programmet. | 
   | **Gyldig fra-dato og -klokkeslett** | Datoen og klokkeslettet programmet blir aktivt. |
   | **Gyldig til-dato og -klokkeslett** | Datoen og klokkeslettet programmet utløper. Standardverdien er 12/31/2154, som i praksis betyr aldri. |
   | **Venteperiode for dekning** | Perioden en ansatt må vente før dekningen starter for fordelsprogrammet. |
   | **Venteperiode for fradrag** | Perioden en ansatt venter før fradraget starter for fordelsprogrammet. |
   | **Rettighetsregler** | Velg rettighetsreglene som skal brukes for fordelsprogrammet. Du definerer rettighetsreglene i kategorien **Rettighetsregler** på denne siden. |
   
4. Velg **Lagre**.
