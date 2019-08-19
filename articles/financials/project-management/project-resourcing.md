---
title: Prosjektressurser
description: Dette emnet inneholder informasjon om ressursberegning for prosjekter.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f6f9c4a6b89997d3d5223d56a5beb4bc11898bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838445"
---
# <a name="project-resourcing"></a>Prosjektressurser

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om ressursberegning for prosjekter.

En utfordring for prosjektledere og ressursansvarlige i løpet av planleggingsfasen for prosjektet er ressursallokering, der de må finne og reservere den riktige ressursen skal arbeide på et prosjekt. I Microsoft Dynamics 365 for Finance and Operations kan ressursfunksjoner for prosjekter la deg definere roller som skal behandles som midlertidige ressurser som kan reserveres for et spesifikt prosjekt eller en del av et prosjekt. Denne typen ressurser lar prosjektledere og ressursansvarlige utføre følgende oppgaver:

- Definer en rolle som har de nødvendige kompetansene, slik at det er enkelt å matche ressurser.
- Bruk roller til å definere en innledende prosjekttidsplan som er basert på reserverte ressurser.
- Beregne kostnader, og finne et opprinnelig budsjett, basert på tilordnede roller og ressurser for et prosjekt.
- Bruke roller til å beregne hvor mange ressursreservasjoner som kreves for hvert prosjekt.
- Beregn antall ressurser som kreves for hele prosjektets livssyklus.
- Lage en prosjektstrukturplan ved hjelp av de opprinnelige ressurstildelingene.

[![Prosjektets livssyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Etter hvert som prosjektplanleggingen pågår, kan planlagte ressurser erstattes med bemannede ressurser. Prosjektlederen kan også gå tilbake og oppdatere resursreservasjonene i et hvilket som helst prosjektstadium.

## <a name="set-up-project-resources"></a>Definere prosjektressurser
Du må opprette en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet. Under kalenderoppsett kan prosjektledere gjøre ressursnivåering som en del av ressursoptimalisering. Basert på kalenderplanen kan restriksjoner legges på ressurser. Du kan opprette en kalender på siden **Kalendere**.

Når du setter opp en arbeidstaker som en prosjektressurs, kan du velge blant arbeidere som jobber i selskapet som du setter opp ressurser til. Alternativt kan du velge arbeidstakere fra andre selskaper i organisasjonen din. Disse arbeidstakere er kjent som konserninterne ressurser.

Følgende prosedyrer forklarer hvordan du setter opp en arbeidstaker som en prosjektressurs i firmaet ditt, og hvordan du oppretter en konsernintern prosjektressurs.

### <a name="set-up-a-worker-as-a-project-resource"></a>Definere en arbeider som en prosjektressurs

1. I **Arbeidere**-listen på siden **Arbeidere**, velger du arbeideren som du legger til som en prosjektressurs, og åpner arbeiderposten.
2. På Handling-panelet velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.
3. Velg en kalender, og lukk deretter siden.

Du kan også angi standardprosjekter for en ressurs som en type førtilordning. Førtildelinger kan brukes når ressursansvarlig eller prosjektleder vet hvilke prosjekter som ressursen vil arbeide med på forhånd. Førtildelinger kan også være basert på forespørsel fra en prosjektsponsor eller kunde. Hvis du vil førtilordne et prosjekt, på siden **Tilordne prosjekter** i kategorien **Prosjekter** i lsietn **Gjenværende prosjekter**, velger du det aktuelle prosjektet.

### <a name="set-up-an-intercompany-resource"></a>Definere en konsernintern ressurs

Når du setter opp en arbeidstaker som en konsernintern ressurs, må du fullføre oppsettet i både utlånsfirmaet og lånefirmaet.

**I utlånsselskapet**

1. I Finance and Operations, kontroller at utlånsfirmaet er valgt, og fullfør deretter prosedyren i forrige avsnitt, «Sett opp en arbeidstaker som en prosjektressurs».
2. På siden **Konserninternt regnskap**, velg **Ny**.
3. I feltet **ID for juridisk enhet**, velg utlånsselskapet. Fyll ut de resterende feltene etter behov, og velg deretter **Lagre**.
4. På siden **Overføringspris**, velg **Ny**.
5. I feltet **Lånende juridisk enhet**, velg riktig selskap.
6. For å låne kun den ressursen du opprettet i begynnelsen av denne delen fra utlånsselskapet, gå til feltet **Ressurs**, og velg navnet på ressursen du har opprettet. For å gjøre alle ressurser i det lånende selskapet tilgjengelig til utlånsselskapet lar du feltet **Ressurs** være tomt.
7. På siden **Parametere for prosjektledelse og regnskap**, i kategorien **Konsernintern**, velg **Aktiver konsernintern ressursplanlegging og tidsskjemaer**-alternativet som **Ja**.

**I det lånende selskapet**

- I søkefiltere på siden **Ressursliste**, skriv inn navnet på den ressursen du har opprettet for det lånende selskap for å bekrefte at navnet er inkludert i ressurslisten for det lånende selskap.

## <a name="manage-resource-competencies"></a>Administrere ressurskompetanser
Ressurskompetanser er en viktig del av ressursbehandling. Kompetanser kan brukes som et utgangspunkt til å fastsette ressurser som har den riktige balansen mellom ferdigheter, utdanning, sertifisering og prosjekterfaring. Du bør definere denne informasjonen for hver ressurs og oppdatere den med jevne mellomrom. På denne måten kan du maksimere muligheter når bestemte ressurskompetanser sammenlignes under ressurstildeling i prosjektet.

[![Eksempler på ferdigheter, sertifiseringer, utdanning og prosjekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Fremgangsmåtene nedenfor forklarer hvordan du setter opp noen av kompetansetypene for en ressurs.

Hvis du vil definere kompetanse for en arbeider, kan du bruke **Arbeidere**-listesiden i Personale eller **Ressurser**-listesiden i Prosjektstyring og regnskap. For følgende fremgangsmåter brukes **Arbeidere**-listesiden i Personale.

### <a name="set-up-competencies-certificates"></a>Angi kompetanser: Sertifikater

1. På listesiden over **Arbeidstakere**,velg den linjen for den arbeideren som det skal legges til sertifikatinformasjon for.
2. På Handling-panelet, på **Ansatt**-kategorien, i **Kompetanse**-gruppen, velg **Sertifikater**.
3. Velg **Ny**, og deretter i **Sertifikattype**-feltet, velg **PMP**.
4. I feltet **Startdato**, velg **10/01/2015**, og velg **Lagre**.

### <a name="set-up-competencies-skills"></a>Definer kompetanser: Ferdigheter

1. På **Arbeidere**-listesiden må du kontrollere at det fortsatt er merket av for arbeideren som du brukte i forrige fremgangsmåte. Deretter i Handling-panelet, på **Ansatt**-kategorien, i **Kompetanse**-gruppen, velg **Ferdigheter**.
2. Velg **Ny**.
3. I **Ferdighet**-feltet velger du **Prosjektstyring**.
4. I **Nivå**-feltet velger du **5 Ekspert**.
5. I **Nivådato**-feltet velger du **1-/14/2014**.
6. I feltet **År med erfaring** angir du **10**.
7. Velg **Lagre**, og lukk deretter siden.

## <a name="create-a-new-project"></a>Opprett nytt prosjekt
1. På siden **Prosjektledelse**, velg **Nytt prosjekt**, og skriv inn følgende verdier:

    - **Prosjekttype:** Tid og materialer
    - **Prosjektnavn:** XYZ-oppgraderingsfase 2
    - **Prosjektgruppe:** TM\_WIP
    - **Prosjektkontrakt-ID:** 00000002

2. Velg **Opprett prosjekt**.

### <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1. På siden **Arbeidstakere** i listen **Arbeidstakere**, velg den oppføringen for den arbeidstakeren du tidligere har satt opp kompetanse for. Åpne deretter arbeidstakerens oppføring.
2. På Handling-panelet, i kategorien **Prosjekt**, i gruppen **Oppsett**, velg **Tilordne prosjekt**.
3. På siden **Oppgaver for ressursvalideringsprosjekt**, i kategorien **Prosjekter**, i **Legg til prosjektet til valgte prosjekter**-feltet, filtrer på **XYZ oppgraderingsfase 2**-prosjektet.
4. I vinduet **Gjenstående prosjekter**, velg ett prosjekt og velg deretter pilknappen for å legge det til vinduet **Valgte prosjekter**.

Du kan også tildele kategorier for en ressurs etter behov. Kategoritypen er enten **Kostnad** eller **Inntekt**. Kategoritypen bestemmes av organisasjonen. Hvis ingen kategorier er tildelt for en ressurs, finner Finance and Operations standardkategori på timepriser for kostnader og inntekter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Definere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektetressursfunksjonaliteten til å opprette roller som kreves for prosjektet. Roller kan brukes hvis bekreftede ressurser er ukjente når ressursene blir reservert. Roller kan reserveres midlertidig som planlagte ressurser, slik at du kan fortsette prosjektetplanleggingsfasene.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble ansatt for å fullføre et tid og materialer-prosjekt som har et godkjent prosjektdokument. Den underordnede prosjektlederen fullfører fremdeles omfanget av prosjektet. Ressursbehandleren identifiserer de bestemte ressursene som skal reserveres, for å arbeide med det nye prosjektet. På grunn av prosjektets kritiske karakter, forespurte prosjektsponsoren Senior prosjektleder som en av rollene. Den ressursansvarlige må anskaffe den nye ressursen og definere rollen i systemet dersom junior prosjektleder krever ressursinformasjon under prosjektplanlegging.

Følgende fremgangsmåte viser hvordan ressursbehandleren kan definere rollen som overordnet prosjektleder og tilknytte ressursegenskaper til den. Rollen kan senere brukes til å søke etter ressurser som samsvarer med de nødvendige ressurskompetansene.

1. På siden **Oppsett av roller**, velg **Ny** og skriv inn følgende verdier:

    - **Rolle-ID:** Overordnet prosjektleder
    - **Beskrivelse:** Overordnet prosjektleder

2. Velg **Opprett**.
3. Velg rollen **Senior prosjektleder**, og velg deretter **Konfigurer egenskaper**.
4. I feltet **Egenskapstype** velger du **Ferdighet**.
5. I feltet **Tilgjengelige egenskaper**, skriv inn ferdigheten det skal søkes etter.
6. I feltet **Egenskapstype** velger du **Sertifikat**.
7. I feltet **Tilgjengelige egenskaper** angir du sertifikattypen du skal søke etter.

### <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1. På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.
2. I kategorien **Prosjektteam og planlegging**, velg **Legg til**.
3. I **Rolle**-feltet velger du **Teammedlem**.
4. Velg **Bestill fra kalender**.
5. På siden **Ressurstilgjengelighet**, velg **Vis innstillinger**.
6. På siden **Juster visningsinnstillinger** angir du følgende verdier:

    - **Format for visning av datoområde:** Dag
    - **Vis tilgjengelighetsbeskrivelser:** Ja
    - **Vis gjenstående kapasitet:** Ja

7. Velg en ressurs i listen over ressurser.
8. Velg **Forpliktende bestilling** og **Full kapasitet**.


### <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe prosjektledere eller ressursforvaltere å gå videre med ressursene som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig anskaffet ressurs. Eksempel: Da Daniel ble ansatt, hadde han erfaring og ferdigheter til å fylle rollen som forretningsanalytiker. Ressursbehandleren tilordnet denne rollen som Daniels standardrolle. Derfor la ressursbehandleren Daniel til i et utvalg av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.

Under ressursreservering kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter. De kan bruke denne informasjonen som én av betingelsene når de utfører analyse av beslutninger med flere kriterier under ressursoppfyllelse. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har bestemte ferdigheter, utdanning og erfaring for et bestemt prosjekt.

**Scenario:** Et godkjent prosjekt er startet, og rollen Overordnet prosjektstyrer ble reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen. Ressurslederen har nå anskaffet seg en ressurs for å oppfylle rollen Overordnet prosjektleder.

1. På siden **Ressursliste**, velg **Daniel Goldschmidt**.
2. På siden **Ressursrolle**, velg **Ny** og skriv inn følgende verdier:

    - **Gjelder fra:** Skriv inn gjeldende dato.
    - **Utløper:** Skriv inn **Aldri**.
    - **Rolle:** Skriv inn **Senior prosjektleder**.

3. Velg **Lagre**, og lukk deretter siden.
4. I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og **PMP**-sertifikatet.

## <a name="set-up-role-based-pricing"></a>Definere rollebasert prising
Alle kostnader, salg, og overføringspriser kan defineres for roller.

1. På siden **Salgspris (time)**, velg **Ny** og skriv inn datoen den gjelder fra.
2. Velg en rolle i **Rolle**-kolonnen.
3. I **Prising**-kolonnen, angi en pris for den valgte ressursrollen.

## <a name="form-a-project-team"></a>Danne et prosjektteam
Hvis du vil bruke rollene som tidligere ble angitt i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Et prosjekt kan få tildelt flere roller. For å unngå forvirring merker Finance and Operations automatisk disse rollene under reservasjon. For eksempel, hvis prosjektlederen behøver tre programvareingeniører, genereres automatisk tre programvareingeniører som har **programvareingeniør 1**, **programvareingeniør 2** og **programvareingeniør 3** som etiketter. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter ved søking etter en ressurs. Du kan legge flere egenskaper etter behov for å spesifisere søket ytterligere.

Visningsinnstillinger kan også tilpasses for å få en bedre oversikt over tilgjengelige ressurser. Det finnes alternativer for å vise tilgjengelighet for hver time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenværende kapasitet i ressurser. Dette alternativet er nyttig for tidsstyring, når du estimerer tilgjengelig tid for aktiviteter eller ressurstilgjengelighet.

Prosjektlederen kan velge en rolle på siden, og hvis det finnes en tilgjengelig ressurs som passer til behovet, velge å reservere en ressurs til å fylle rollen. Vær oppmerksom på at ressursene ikke må reserveres på dette tidspunktet i planleggingsfasen. Når du oppretter en prosjektstrukturplan, kan du erstatte roller med bemannede ressurser for prosjektet. Hvis roller erstattes med bemannede ressurser i prosjektstrukturplanen, oppdaterer ressursoppsettet automatisk prosjektgruppeoversikten og -planleggingen.

[![Prosjektgruppeoversikt som inneholder både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for å bestille en ressurs for et prosjekt, for eksempel **Gjenværende kapasitet**, **Full kapasitet**, **Kapasitetsprosent** og **Angi timer**. Disse alternativene for bestilling kan annulleres når som helst hvis ressurstildelinger endres. To typer bestilling støttes:

- **Forpliktende bestilling** – Ressursreserveringen ble godkjent og bekreftet for å arbeide med prosjektet for den angitte varigheten.
- **Ikke-forpliktende bestilling** – Ressursreserveringen ble foreløpig angitt for å arbeide med prosjektet for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

### <a name="create-a-project-team"></a>Opprette et prosjektteam

1. Velg et prosjekt på listesiden **Alle prosjekter**, og velg deretter **Rediger**.
2. I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato for tidsplanen pluss én måned. Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.
3. Velg **Legg til**.
4. I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Overordnet prosjektleder**.
5. Velg **Nødvendige kompetanser**.
6. På siden **Velg egenskaper** er egenskapene som du tidligere har angitt for rollen Overordnet prosjektleder, valgt som standard. Velg **OK**.
7. På siden **Legg til roller i prosjekt** i feltet **Antall ressurser** angir du **1**.
8. I **Ressurs**-feltet vil oppslaget vise alle ressurser som har de nødvendige kompetansene. Velg **Daniel Goldschmidt** og velg deretter **Opprett**.
9. På siden **Prosjekt**, velg **Legg till**.
10. I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Teammedlem**. I feltet **Antall ressurser** angir du **5**.
11. Velg **Opprett**.
12. På siden **Prosjekt**, velg **Oppfyll ressurs**.

## <a name="resource-capacity-synchronization"></a>Synkronisering av ressurskapasitet
Prosessene for ressurssynkronisering sikrer at informasjon for kalenderen og grunnkalenderen slår ned i prosjektressursplanlegging. Hvis kalenderen er endret, vil prosessene foreta de nødvendige oppdateringene i planleggingen av prosjektressurser. Prosessene bidrar også til å forbedre ytelsen, fordi kalenderens ressursinformasjon er synkronisert på forhånd. Derfor opptrer oppdateringer til ressursplanleggingsinformasjon raskere. Vi anbefaler at du planlegger prosessene som en satsvis jobb i stedet for én om gangen. Ellers er det fare for at noen glemmer datoene da informasjonen ble sist synkronisert. Hvis inklusive datoer ikke brukes, kan det oppstå mellomrom under synkronisering av dato.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Synkroniser opprullinger av ressurskapasitet

Synkroniseringsprosessen er utformet for å synkronisere all kalenderinformasjon for ressursen. Denne informasjonen inneholder grunnkalenderinformasjon om eventuelle endringer i prosjektets kapasitetstabell i ressurskalender. Hvis det legges til nye ressurser i prosjektet, synkronisering bidrar til å sikre at det finnes oppdatert kalenderinformasjonen. Denne synkroniseringen kan utføres når som helst.

Vi anbefaler at du bruker et parti. Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.

1. Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullinger av ressuskapasitet**.
2. Sett alternativene i følgende tabell.

    | Alternativ      | beskrivelse |
    |-------------|-------------|
    | Periodekode | Velg valgfritt intervallkoden for hovedboken for å angi start- og sluttdatoer for synkroniseringsprosessen for opprullinger av ressurskapasitet. |
    | Startdato  | Skriv inn startdato for synkroniseringsprosessen for opprullinger av ressurskapasitet. |
    | Sluttdato    | Skriv inn sluttdato for synkroniseringsprosessen for opprullinger av ressurskapasitet. |

[![Synkroniseringsprosess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Definere roller i WBS-maler
Prosjektledere kan definere WBS-maler som kan gjelde når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller ved oppretting av en mal. Bruk følgende fremgangsmåte for å tilordne en rolle til en WBS-mal. 

1. Velg **Prosjektledelse og regnskap** &gt; **Oppsett** &gt; **prosjekter** &gt; **Strukturmaler for arbeidssammenheng**.
2. Velg **Detaljer** for en valgt WBS-mal.
3. Velg en oppgave i listen, og deretter i **Rolle**-feltet velger du en rolle for å tildele til aktiviteten.

### <a name="work-with-a-wbs"></a>Arbeide med en WBS

Du kan opprette en ny WBS, eller du kan kopiere en WBS fra en eksisterende WBS-mal. En prosjektleder kan enkelt håndtere ressursene ved å tilordne roller til nye aktiviteter på WBS-en. Roller kan erstattes enten etter at en ressurs er anskaffet eller etter en bekreftet ressurs for å jobbe på oppgaven, identifiseres. Denne fleksibiliteten gjør det mulig for prosjektledere å utføre følgende oppgaver:

- Identifisere antallet ressurser som kreves for WBS-arbeidspakkene.
- Estimere prosjektkostnader.
- Fastsette et foreløpig budsjett.
- Beregne varigheten til aktiviteten, basert på roller og ressurser.
- Utvikle noen prosjektstyringsplaner, basert på den tilgjengelige prosjektinformasjonen.

Flere alternativer er lagt i WBS for bedre ressursberegning.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressurstilordninger</td>
<td>Vis tildelte ressurser, datoer, antall timer og bestillingstypen for oppgaver på WBS.</td>
</tr>
<tr class="even">
<td>Autogenerer team</td>
<td>Legg automatisk til planlagte ressurser ved hjelp av rollene som er knyttet til en oppgave. Finance and Operations foreslår automatisk planlagte ressurser ved hjelp av en beslutningsanalyse med flere kriterier som er basert på roller. Etter at rollene og innsatsen (timer) er satt til oppgavene i en WBS, og etter at strukturen er frigitt, velger du <strong>Autogenerer team</strong>. Antall planlagte ressurser legges til WBS-en og i kategorien <strong>Prosjekt- og teamplanleggingr</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser til forpliktende eller ikke-forpliktende bestilling, basert på den angitte varigheten. Du kan justere innstillingene for å vise og angi varigheten for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivå ved hjelp av følgende alternativer:
<ul>
<li><strong>Godta</strong> – bekrefte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Avbryt</strong> – avbryte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Tildel automatisk</strong> – en tilgjengelig bemannet ressurs som har en matchende rolle blir automatisk valgt og tilordnet til den valgte oppgaven.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.
2. Velg **Planlegging** &gt; **Aktiviteter** &gt; **Struktur for arbeidssammenheng**.
3. Velg **Ny** for å legge til følgende nivå-en aktiviteter til WBS:

    - Oppstart
    - Planlegging
    - Utfører
    - Overvåking og kontroll
    - Lukk

4. Angi datoene og innsatsen (timer), som vist på den følgende illustrasjonen.

    [![Angi datoene og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Velg oppgavelinjen **Oppstart**, og deretter, i **Rolle**-feltet velger du **Overordnet prosjektleder**.
6. Velg **Publiser**.
7. På samme linje i feltet **Ressurs**, velg **Daniel Goldschmidt** og velg deretter **Aksepter**.
8. Velg oppgavelinjen **Planlegging**, og deretter, i **Rolle**-feltet velger du **Forretningsanalytiker**.
9. Velg **Publiser** og velg deretter **Autogenerer team**.
10. Velg **Ja** i dialogboksen som dukker opp.
11. I **Ressurs**-feltet må du kontrolle at verdien er **Forretningsanalytiker 1**.
12. For **Forretningsanalytiker 1**-ressursen, åpne oppslag, og velg **Lansere ressursoppgaver**. Velg deretter en medarbeider for oppgaven.
13. Velg **Myk tilordning** &gt; **Full kapasitet**.

    > [!NOTE] 
    > Du får ikke en advarsel om at den spesifikke ressursen nå er 2, fordi nummeret på ressursen fortsatt er 1.

14. På siden **Struktur for arbeidsavbrudd**, valider ressurstilordningen på WBS, og velg deretter **Lagre**.

## <a name="resource-fulfillment-for-planned-resources"></a>Oppfyllelse av planlagte ressurser
En prosjektleder kan planlegge nødvendige ressursroller for et prosjekt. Ressursbehandleren vil se disse planlagte ressursene som forespørsler på siden **Ressursoppfyllelse** og kan tildele faktiske ressurser.

1. På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.
2. Velg **Prosjekt** og velg deretter **Rediger**.
3. I kategorien **Prosjektteam og planlegging**, velg **Legg til**.
4. I dialogboksen **Legg til roller** velger du rollen **Programvareutvikler**.
5. Velg **Opprett**, og lukk deretter prosjektsiden.
6. På siden **Ressursoppfyllelse**, velg **Programvareutvikler 1** for **XYZ oppgraderingsprosjekt fase 2**-prosjektet.
7. Velg en medarbeider, og deretter **Tildel**.
8. Kontroller at linjen for **Programvareutvikler 1** er fjernet for prosjektet **XYZ-oppgraderingsfase 2**.
9. I kategorien **Prosjektteam og planlegging** for **XYZ oppgraderingsfase 2**-prosjektet, bekreft at arbeidstageren du valgte i forrige trinn er lagt til som **Programvareutvikler**.

## <a name="requests-for-project-resources"></a>Forespørsler om prosjektressurser
Funksjonaliteten for prosjektressursplanlegging lar kun ressursforvaltere distribuere bemannede ressurser på engasjementer eller prosjekter. For å aktivere denne funksjonaliteten, fullfør følgende oppgaver, eller bekreft at de er fullført:

- Definer nummerserier.
- Definer arbeidsflyter for prosjektstyring og regnskap.
- Aktiver arbeidsflyten for ressursforespørsel.

Etter at de foregående oppgavene er fullført, kan du fullføre følgende oppgaver som du trenger:

- Opprett en ressursforespørsel fra en ikke-forpliktende bemannet ressurs.
- Overvåk ressursforespørsler.
- Oppfyll ressursforespørsler.
- Etterspør en bemannet ressurs fra en WBS.
- Bestill ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.

## <a name="monitor-project-teams"></a>Overvåke prosjektteam
1. På siden **Alle prosjekter**, velg koblingen **Prosjekt-ID** for prosjektet **XYZ opgraderingsfase 2**.
2. I hurtigkategorien **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som er oppført, er riktige.
