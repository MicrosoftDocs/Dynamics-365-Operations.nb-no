---
title: Konfigurere rettighetsregler og -alternativer
description: Angi rettighetsregler og alternativer i Fordelsbehandling i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25593bc4d136e403c7ba87e044c95f4fae1e7db9
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558375"
---
# <a name="configure-eligibility-rules-and-options"></a>Konfigurere rettighetsregler og -alternativer 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Når du har konfigurert de nødvendige parameterne for Fordelsbehandling, kan du opprette rettighetsregler, pakker, perioder og programmer som du vil knytte til dine fordelsplaner.

Rettighetsregler brukes til å fastslå om ansatte er kvalifisert for en plan. Ansatte må oppfylle minst én regel for å være kvalifisert for fordelen. Du har for eksempel to regler i en plan. Den første regelen (linje 1) angir at ansatttypen må være **Ansatt**. Den andre regelen (linje 2) angir at ansatttypen må være heltidsansatt. Derfor er ansatte som oppfyller regel 1, kvalifiserte selv om de bare er ansatt på deltid.

Du kan imidlertid definere én enkelt regel som har flere betingelser. Ansatte må da oppfylle alle betingelsene for regelen for å være kvalifisert for fordelen. Du har for eksempel en regel som kalles **Heltidsansatt**. Denne regelen angir at ansattypet må være **Ansatt** *og* den ansatte må være ansatt på heltid. Ansatte må derfor oppfylle begge betingelsene for regelen for å være kvalifisert.

> [!IMPORTANT]
> Minst én rettighetsregel må knyttes til hver fordelsplan. Du kan knytte flere regler til en fordel.

## <a name="create-an-eligibility-rule"></a>Opprette en rettighetsregel

Rettighetsregler definerer hvilke ansatte som kan registrere seg i hver fordelsplan. Når du har definert rettighetsregler, kan du tilordne dem til fordelsplaner. Deretter kan du behandle registreringsrettighetene for å se hvilke ansatte som er berettiget for hver plan. 

Under åpen registrering kan ansatte velge fordelsplaner. Hvis de ikke er berettiget til en fordelsplan basert på rettighetsregler etter at de allerede er registrert, avregistreres de ikke automatisk. Når det oppstår en livshendelse som påvirker planrettighetene, startes en registreringsperiode for den ansatte for å velge planer som de er berettiget til. 

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I kategorien **Rettighetsregler** velger du **Ny** for å opprette en rettighetsregel. Hvis du vil se planer som er knyttet til en rettighetsregel, velger du **Tilknyttede planer**.

3. Angi verdier for de følgende feltene.

   | Felt | beskrivelse |
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
   | **Bruk tidligere ansettelsesstatus** | Angir om en ansatts tidligere ansettelsesstatus skal brukes som en del av regelen for fordelsrettigheten. Du kan for eksempel angi en rettighetsregel som frafaller en dekningsventeperiode for alle ansatte som har gått fra statusen **Lagt bort** til statusen **Ansatt** innen 90 dager etter forrige ansettelse. |

4. Under **Tilleggskriterier** velger du følgende alternativer og legger til informasjon etter behov.

   | Alternativ | beskrivelse |
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
   | **Kvalifisert fagforening** | Angir fagforeningsmedlemskapene som oppfyller rettighetsregelen. For eksempel Forklift Drivers of America.</br></br>Når du bruker en fagforeningsbasert rettighetsregel, må fagforeningsposten ha sluttdatoen fylt ut. Du kan ikke la dette stå tomt. |
   | **Berettiget postnummer** | Angir postnumrene som oppfyller rettighetsregelen. For eksempel 58104. |

5. Under **Flere detaljer** kan du vise følgende tilleggsdetaljer.

   | Felt | beskrivelse |
   | --- | --- |
   | **Felt for kvalifisert bruker** | Angir flere rettighetsregler basert på kundedefinerte felt. |
   | **Rettighetstype** | Angir den valgte kriteriekategorien under **Tilleggskriterier**. |
   | **Rettighetsreferanse** | Angir verdiene du valgte, under **Tilleggskriterier**. |
   | **Beskrivelse** | Beskrivelsen du valgte, under **Tilleggskriterier**. |

6. Velg **Lagre**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Bruke egendefinerte felt i rettighetsregler

[Egendefinerte felt](hr-developer-custom-fields.md) kan opprettes i Human Resources for å spore tilleggsinformasjon. Disse feltene kan legges til direkte i brukergrensesnittet, og en kolonne legges dynamisk til i den underliggende tabellen.  

Egendefinerte felt kan brukes i berettigelsesprosessen. Rettighetsregler kan bruke én eller flere egendefinerte feltverdier til å fastsette en ansatts berettigelse.  Hvis du vil legge til et egendefinert felt i en eksisterende regel eller opprette en ny regel, kan du gå til **Fordelsbehandling > Koblinger > Oppsett > Rettighetsregler > Rettighet for egendefinert felt**. På denne siden kan du opprette en regel som bruker ett eller flere egendefinerte felt, og du kan definere flere verdier for hvert egendefinerte felt for å fastslå berettigelse.

Følgende tabeller støtter egendefinerte felt som kan brukes til berettigelsesbehandling:

- Arbeider (HcmWorker)  
- Jobb (HcmJob)  
- Stilling (HcmPosition)  
- Stillingsdetaljer (HcmPositionDetail)  
- Stillingstilordning  
- Ansettelse (HcmEmployment)  
- Ansettelsesdetaljer (HcmEmploymentDetails)  
- Jobbdetaljer (HcmJobDetails)  

Følgende egendefinerte felttyper støttes i berettigelsesbehandling:

- Tekst  
- Plukkliste  
- Antall  
- Desimal  
- Avmerkingsboks  

Tabellen nedenfor viser informasjon om skjemafeltet for berettigelse av brukerdefinerte felt.

| Felt  | beskrivelse |
|--------|-------------|
| Navn | Navn på kriteriene som opprettes. |
| Tabellnavn | Tabellnavnet som inneholder det egendefinerte feltet som brukes for rettighetsregelen. |
| Feltnavn | Feltet som skal brukes for rettighetsregelen. |
| Operatortype | Viser operatoren som brukes i konfigurasjonen av berettigelse av egendefinerte felt. |
| Verdi | Viser verdien som brukes i konfigurasjonen av berettigelse av egendefinerte felt. |

## <a name="eligibility-logic"></a>Rettighetslogikk

Følgende deler beskriver hvordan fordelsrettigheter behandles.

### <a name="rules-assigned-to-a-plan"></a>Regler som tilordnes en plan 
Når flere rettighetsregler er tilordnet en fordelsplan, må en ansatt oppfylle minst én regel for å være kvalifisert til å være med i fordelsplanen.  I følgende eksempel må den ansatte enten oppfylle kravene i **Jobbtype**-regelen eller regelen **Aktive ansatte**.

![Den ansatte må enten oppfylle kravene i Jobbtype-regelen eller regelen Aktive ansatte.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Kriterier i en rettighetsregel 
I en regel definerer du kriteriene som utgjør regelen. I eksempelet over er kriteriene for **Jobbtype**-regel der Jobbtype = Direktører. Derfor må den ansatte være et styremedlem for å være kvalifisert. Dette er en regel der det bare er ett kriterium i regelen.

Du kan definere regler som har flere kriterier. Når du definerer flere kriterier i en rettighetsregel, må en ansatt oppfylle hvert kriterium i regelen for å være kvalifisert for fordelsplanen. 

Regelen **Aktive ansatte** over består for eksempel av følgende kriterier. For at den ansatte skal være kvalifisert basert på **Aktiv ansatt**-regelen, må den ansatte være ansatt i juridisk enhet USMF *og* ha stillingstypen heltid.  

![Kriterier i en rettighetsregel.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Flere betingelser innenfor kriterier

Reglene kan utvides ytterligere for å bruke flere betingelser innenfor ett enkelt kriterium. Den ansatte må oppfylle minst én bestemt betingelse for å være kvalifisert. Hvis du vil bygge på eksemplet ovenfor, kan regelen for **Aktive ansatte** utvides ytterligere til å omfatte ansatte som også er deltidsansatte. Derfor må den ansatte nå være en ansatt i USMF *og* enten heltids- eller deltidsansatt.  

![Flere betingelser innenfor kriterier.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Rettighetsbetingelser innenfor et egendefinert feltkriterium 
I likhet ovenstående kan egendefinerte felt brukes ved oppretting av rettighetsregler og arbeid på samme måte. Det kan for eksempel hende at du vil tilby internettrefusjon til de ansatte i Fargo og København som jobber hjemmefra, fordi internettkostnadene er høyere på disse stedene. Du gjør dette ved å opprette to egendefinerte felt: **Kontoradresse** (plukkliste) og **Jobber hjemmefra** (avmerkingsboks). Deretter oppretter du en regel som kalles **WFH-ansatte**. Kriteriet for regelen er der **Kontoradresse = Fargo** eller **København**, *og* der arbeid **Jobber hjemmefra = Ja**.

Egendefinerte rettighetsregler må defineres som angitt i følgende bilde. 

![Rettighetsbetingelser innenfor et egendefinert feltkriterium.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Konfigurere bunter

Bunter er et sett med relaterte fordelsplaner. Du kan bruke fordelsbunter til å gruppere fordelsplaner som en ansatt må velge for å registrere seg i bestemte fordelsplaner som kan være avhengige av andre fordelsplanregistreringer. Eksempler på når du kanskje vil bruke en bunt, omfatter følgende:

- En helseplanbunt som inkluderer høyt fradragsberettiget helseforsikring med en tilknyttet helsesparekonto (HSA).

- En forsikringsplan for livstid med en obligatorisk forsikringsplan for den ansatte, gruppert med en avhengig livsplan. Dette vil sikre at en ansatt ikke kan velge en avhengig dekningstid uten å registrere seg for ansattdekningen.

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Rettighetsregler og alternativer**.

2. I **Bunter**-kategorien velger du **Ny** for å opprette en bunt. Hvis du vil se planer som er knyttet til en bunt, velger du **Tilknyttede planer**.

3. Angi verdier for de følgende feltene.

   | Felt | beskrivelse |
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

3. Angi verdier for de følgende feltene.

   | Felt | beskrivelse |
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

3. Velg et fleksibelt kredittprogram som skal brukes. Feltene inneholder følgende informasjon.

   | Felt | beskrivelse |
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

3. Angi verdier for de følgende feltene.

   | Felt | beskrivelse |
   | --- | --- |
   | **Program** | En unik ID for programmet. |
   | **Beskrivelse** | En beskrivelse av programmet. | 
   | **Gyldig fra-dato og -klokkeslett** | Datoen og klokkeslettet programmet blir aktivt. |
   | **Gyldig til-dato og -klokkeslett** | Datoen og klokkeslettet programmet utløper. Standardverdien er 12/31/2154, som i praksis betyr aldri. |
   | **Venteperiode for dekning** | Perioden en ansatt må vente før dekningen starter for fordelsprogrammet. |
   | **Venteperiode for fradrag** | Perioden en ansatt venter før fradraget starter for fordelsprogrammet. |
   | **Rettighetsregler** | Velg rettighetsreglene som skal brukes for fordelsprogrammet. Du definerer rettighetsreglene i kategorien **Rettighetsregler** på denne siden. |
   
4. Velg **Lagre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
