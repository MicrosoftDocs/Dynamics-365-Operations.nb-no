---
title: Prosjektressurser
description: Dette emnet gir informasjon om resourcing for prosjektet.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Prosjektressurser

Dette emnet gir informasjon om resourcing for prosjektet.

En utfordring for prosjektledere og ressursledere i løpet av planleggingsfasen prosjektet er ressursallokering, der de må finne og reservere den riktige ressursen skal arbeide på et prosjekt. I Microsoft Dynamics 365 for operasjoner kan resourcing muligheter for prosjekter du definere roller som skal behandles som midlertidig ressurser som kan reserveres for bestemte forlovelse eller en del av en forlovelse. Denne typen ressurser lar prosjektledere og ressursansvarlige utføre følgende oppgaver:

-   Definer en rolle som har de nødvendige kompetansene til å gjøre det enklere å samsvare med ressurser.
-   Bruk roller for å definere en tidsplan for første engasjement som er basert på reserverte ressurser.
-   Beregne kostnader, og finne et opprinnelig budsjett, basert på tilordnede roller og ressurser for et prosjekt.
-   Bruke roller til å beregne hvor mange reservasjoner for ressursen som kreves for hver engasjement.
-   Beregne hvor mange ressurser som kreves for hele livssyklusen til et prosjekt.
-   Lage en prosjektstrukturplan ved hjelp av de opprinnelige ressurstildelingene.

[![Prosjektets levetid](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Planlagte ressurser kan erstattes med bemannet ressurser som project planlegger overskudd. Prosjektlederen kan også gå tilbake og Oppdater resourcing reservasjoner under noen av prosjektstadiene.

## <a name="set-up-project-resources"></a>Definere prosjektressurser
Du må opprette en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressurser som er reservert for prosjektet. Prosjektledere kan utføre ressursutjevning som en del av optimalisering av ressursen, under installasjonen av kalenderen. Basert på tidspunktet i kalenderen, kan begrensninger plasseres på ressurser. Du kan opprette en kalender på den **kalendere** siden. 

Når du setter opp en arbeider som en ressurs, kan du velge blant ansatte som arbeider i firmaet du vil konfigurere ressurser, eller du kan velge arbeidere fra andre firmaer i organisasjonen. Dette er en konsernintern ressurser. Følgende fremgangsmåter forklarer hvordan du setter opp en arbeider som en ressurs i selskapet og hvordan du setter opp en konsernintern project-ressurs.

### <a name="set-up-a-worker-as-a-project-resource"></a>Definere en arbeider som en prosjektressurs

1.  På den **arbeidere** side i den **arbeidere** velger arbeideren som du legger til som en ressurs, og åpne oppføringen arbeider.
2.  I handlingsruten, klikker du **prosjektet**&gt;**Setup**&gt;**Prosjektoppsett**.
3.  Velg en kalender, og deretter lukke siden.

Du kan også angi standardprosjekter for en ressurs som en type førtilordning. Førtildelinger kan brukes når ressursansvarlig eller prosjektleder vet hvilke prosjekter som ressursen vil arbeide med på forhånd. Førtildelinger kan også være basert på forespørsel fra en prosjektsponsor eller kunde. Hvis du vil førtilordne et prosjekt, på siden **Tilordne prosjekter** i kategorien **Prosjekter** i lsietn **Gjenværende prosjekter**, velger du det aktuelle prosjektet.

### <a name="set-up-an-intercompany-resource"></a>Konfigurere en konsernintern ressurs

Når du setter opp en arbeider som en konsernintern ressurs, må du fullføre oppsettet i lån firma og låner. 

**I lån selskapet:**

1.  I Dynamics 365 for operasjoner, må du kontrollere at lån selskapet er valgt, og fullfør deretter fremgangsmåten ovenfor, "Angi en arbeider som en ressurs".
2.  Gå til ** finans **&gt; ** Posteringsoppsett **&gt;**konserninternt regnskap**. Click **New**.
3.  I den ** ID for juridisk enhet ** velger lån selskapet. Fyll ut de gjenstående feltene etter behov, og klikk deretter **lagre**.
4.  Gå til ** prosjekt prosjektstyring og regnskap **&gt; ** installasjonsprogrammet **&gt;**priser ** &gt;**Overføringsprisen**.** **
5.  På den ** Overføringsprisen ** klikker **ny**, og i den ** juridisk enhet som låner ** velger det riktige firmaet.
6.  Hvis du vil låne bare firmaet låner ressursen du opprettet i begynnelsen av denne delen i den **ressurs**, velger du navnet på ressursen som du opprettet. Hvis du vil gjøre alle ressurser i selskapet tilgjengelig for lån selskapet, lar du ** ressurs ** feltet være tomt.
7.  Gå til ** prosjekt prosjektstyring og regnskap **&gt; ** installasjonsprogrammet **&gt;**Project management og regnskap parametere**, og på den ** konserninterne ** kategorien den ** Aktiver konsernintern ressursplanlegging og timeregistreringer ** feltet til **Ja**.

**I låner selskapet:**

1.  Gå til **prosjekt prosjektstyring og regnskap**&gt;**ressurser i Project**&gt;**i listen over ressurser**.
2.  Angi navnet på ressursen som du opprettet i forrige fremgangsmåte for lån firmaet til å kontrollere at navnet er inkludert i ressurslisten for lån selskapet i søkefilteret.

## <a name="manage-resource-competencies"></a>Administrere ressurskompetanser
Ressurskompetanser er en viktig del av ressursbehandling. Kompetanser kan brukes som et utgangspunkt til å fastsette ressurser som har den riktige balansen mellom ferdigheter, utdanning, sertifisering og prosjekterfaring. Du bør definere denne informasjonen for hver ressurs og oppdatere den med jevne mellomrom. På denne måten kan du maksimere muligheter når bestemte ressurskompetanser sammenlignes under ressurstildeling i prosjektet. [![Eksempler på ferdigheter, sertifiseringer, utdanning og prosjekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Fremgangsmåtene nedenfor forklarer hvordan du setter opp noen av kompetansetypene for en ressurs. 

Hvis du vil definere kompetanse for en arbeider, kan du bruke **Arbeidere**-listesiden i Personale eller **Ressurser**-listesiden i Prosjektstyring og regnskap. For følgende fremgangsmåter, den **arbeidere** listesiden i menneskelige ressurser brukes.

### <a name="set-up-competencies-certificates"></a>Angi kompetanser: Sertifikater

1.  På **Arbeidere**-listesiden velger du linjen for arbeideren som du legger til sertifikatinformasjon for.
2.  I handlingsruten i kategorien **Arbeider** i **Kompetanser**-gruppen klikker du **Sertifikater**.
3.  Klikk **Ny**.
4.  I feltet **Attesttype** velger du **PMP**.
5.  I **Startdato**-feltet velger du **10/1/2015**.
6.  Klikk **Lagre**, og lukk deretter siden.

### <a name="set-up-competencies-skills"></a>Definer kompetanser: Ferdigheter

1.  På **Arbeidere**-listesiden må du kontrollere at det fortsatt er merket av for arbeideren som du brukte i forrige fremgangsmåte. I handlingsruten i kategorien **Arbeider** i **Kompetanser**-gruppen klikker du deretter **Ferdigheter**.
2.  Klikk **Ny**.
3.  I **Ferdighet**-feltet velger du **Prosjektstyring**.
4.  I **Nivå**-feltet velger du **5 Ekspert**.
5.  I **Nivådato**-feltet velger du **1-/14/2014**.
6.  I feltet **År med erfaring** angir du **10**.
7.  Klikk **Lagre**, og lukk deretter siden.

## <a name="create-a-new-project"></a>Opprett nytt prosjekt
1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**arbeidsområder**&gt;**Project management**.
2.  Klikk **Nytt prosjekt**, og angi deretter følgende verdier:
    -   **Prosjekttype** – etter regning
    -   **Prosjektnavn** -XYZ oppgradere fase 2
    -   **Prosjektgruppen** -TM\_via
    -   **Kontrakt-ID i Project** -00000002
3.  Klikk **Opprett prosjekt**.

### <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1.  Klikk **Personale**&gt;**arbeidere**&gt;**arbeidere**.
2.  I **Arbeidere**-listen velger du posten for arbeideren som du allerede har installert kompetanser for, og åpne arbeiderposten.
3.  I handlingsruten i kategorien **Prosjekt** i **Oppsett**-gruppen klikker du **Tilordne prosjekter**.
4.  På siden **Prosjekttilordninger for ressursvalidering** klikker du kategorien **Prosjekter**.
5.  I den **legge til prosjektet i valgte prosjekter**, filter på prosjekt, XYZ oppgradere fase 2
6.  I ruten **Gjenværende prosjekter** velger du et prosjekt og klikker deretter pilen for å legge det til i ruten **Valgte prosjekter**.
7.  Lukk siden.

Hvis du trenger det, kan du også tilordne kategorier for en ressurs. Kategoritypen er enten kostnad eller inntekt. Dette bestemmes av organisasjonen. Hvis det finnes ingen tilordnede kategorier for ressursen, slår Dynamics 365 for operasjoner opp standardkategori på time prisene for kostnader og inntekter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Definere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektetressursfunksjonaliteten til å opprette roller som kreves for prosjektet. Rollene kan brukes når bekreftede ressurser er fortsatt ukjent når du reserverer ressurser. Roller kan reserveres midlertidig som planlagt ressurser, slik at du kan fortsette prosjektet planlegging faser. 

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble ansatt for å fullføre et tid og materialer-prosjekt som har et godkjent prosjektdokument. Den underordnede prosjektlederen fullfører fremdeles omfanget av prosjektet. Ressursbehandleren identifiserer for øyeblikket bestemte ressurser som skal reserveres for å arbeide på det nye prosjektet. Én av rollene på prosjektsponsor forespurt, på grunn av kritiske natur av prosjektet, er Senior prosjektleder. Ressursbehandling må hente den nye ressursen, og definere rollen i systemet i tilfelle Senior prosjektleder krever ressursinformasjon under prosjektplanlegging av. 

Følgende trinn viser hvordan ressursbehandleren kan definere rollen som Senior prosjekt leder og tilknytte ressurs egenskapene til den. Rollen kan senere brukes til å søke etter ressurser som samsvarer med de nødvendige ressurskompetansene.

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**Setup**&gt;**ressurser**&gt;**oppsett roller**.
2.  Klikk **Ny**, og angi deretter følgende verdier:
    -   **Rolle-ID** -Senior prosjektleder
    -   **Beskrivelse** -Senior prosjektleder
3.  Klikk **Opprett**.
4.  Velg rollen **Overordnet prosjektleder**, og klikk deretter **Konfigurer kjennetegn**.
5.  I feltet **Egenskapstype** velger du **Ferdighet**.
6.  I feløtet **Tilgjengelige egenskaper** angir du ferdigheten du søker etter.
7.  I feltet **Egenskapstype** velger du **Sertifikat**.
8.  I feltet **Tilgjengelige egenskaper** angir du sertifikattypen du skal søke etter.
9.  Klikk **OK**, og lukk siden.

### <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**vanlige**&gt;**prosjekter**&gt;**alle prosjekter**, og åpne den **XYZ oppgradere fase 2** prosjektet.
2.  I kategorien **Prosjektteam og planlegging** klikker du **Legg til**.
3.  I **Rolle**-feltet velger du **Teammedlem**.
4.  Klikk **Bestill fra kalender**.
5.  På siden **Ressurstilgjengelighet** klikker du **Visningsinnstillinger**.
6.  På siden **Juster visningsinnstillinger** angir du følgende verdier:
    -   **Format for visning av dato spekter** - dag
    -   **Vis tilgjengelighet beskrivelse** - Ja
    -   **Vis gjenværende kapasitet** - Ja
7.  Velg en ressurs i listen over ressurser.
8.  Klikk **forpliktende**&gt;**Full kapasitet**.
9.  Lukk siden.

### <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe ledere for prosjektet eller ressursen, kan du gå ned ytterligere ressurser som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig anskaffet ressurs. For eksempel når Daniel ble ansatt, hadde han erfaring og ferdigheter til å fylle rollen som Business analyst. Ressursbehandling tilordnet denne rollen som Daniels standardrolle. Derfor legges ressursbehandleren Daniel til et utvalg av business analytikere som er tilgjengelige for å arbeide på prosjekter. 

Prosjektledere kan filtrere rolle ressursene som er tilgjengelige for å arbeide med prosjekter under reservasjon av ressurser. De kan bruke denne informasjonen som én av betingelsene når de utfører analyse av beslutninger med flere kriterier under ressursoppfyllelse. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har bestemte ferdigheter, utdanning og erfaring for et bestemt prosjekt. 

**Scenario:** et godkjent prosjekt har startet, og Senior project manager rollen er reservert som en planlagt ressurs i løpet av planleggingsfasen prosjektet. Ressurslederen har nå anskaffet seg en ressurs for å oppfylle rollen Overordnet prosjektleder.

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**ressurser i Project**&gt;**i listen over ressurser**.
2.  I **Ressurs**-listen velger du **Daniel Goldschmidt**.
3.  Klikk **Project-ressurs**&gt;**Behold**&gt;**Ressursrollen**.
4.  Klikk **Ny**, og angi deretter følgende verdier:
    -   **Effektiv** - (gjeldende dato)
    -   **Utløp** - aldri
    -   **Rollen** -Senior prosjektleder
5.  Klikk **Lagre**, og lukk deretter siden.
6.  I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og **PMP**-sertifikatet.

## <a name="set-up-role-based-pricing"></a>Definere rollebasert prising
Alle kostnader, salg, og overføringspriser kan defineres for roller.

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**Setup**&gt;**priser**&gt;**Salgspris (time)**.
2.  Click **New**.
3.  Angi en gyldighetsdato.
4.  Velg en rolle i **Rolle**-kolonnen.
5.  I **Prising**-kolonnen, angi en pris for den valgte ressursrollen.

## <a name="form-a-project-team"></a>En prosjektgruppe for skjema
Hvis du vil bruke rollene som tidligere ble angitt i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Flere roller som kan tilordnes for et prosjekt, og Dynamics 365 for operasjoner merker automatisk disse rollene under reservering for å unngå forvirring. For eksempel hvis prosjektlederen krever tre programvare ingeniører, tre Software engineer roller som har programvare tekniker 1, genereres 2 utvikling av programvare og programvare utvikling 3 som etikettene automatisk. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter ved søking etter en ressurs. Du kan legge flere egenskaper etter behov for å spesifisere søket ytterligere. 

Visningsinnstillinger kan også tilpasses for å få en bedre oversikt over tilgjengelige ressurser. Det finnes alternativer for å vise tilgjengelighet for hver time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenværende kapasitet i ressurser. Dette alternativet er nyttig for tidsadministrasjon når du gjør beregninger tilgjengelig tid for aktiviteter eller tilgjengelige ressurser. 

Prosjektlederen kan velge en rolle på siden og deretter, hvis det finnes en tilgjengelig ressurs som passer behovet, velge for å reservere en ressurs for å fylle rollen. Vær oppmerksom på at ressursene ikke har reserveres nå løpet av planleggingsstadiet. Når du oppretter en Prosjektstrukturplan, kan du erstatte roller med bemannet ressursene for prosjektet. Hvis rollene er erstattet med bemannet ressurser i WBS, oppdaterer ressurs oppsettet automatisk prosjektgruppen oppføring og planlegging. 

[![Prosjektgruppen liste som inneholder både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for å bestille en ressurs for et prosjekt, for eksempel **Gjenværende kapasitet**, **Full kapasitet**, **Kapasitetsprosent** og **Angi timer**. Disse alternativene for bestilling kan annulleres når som helst hvis ressurstildelinger endres. To typer bestilling støttes:

-   **Forpliktende** – reservasjonen ressursen ble godkjent og bekreftet til å arbeide på kontaktpunktet for den angitte varigheten.
-   **Myk bok** – reservasjoner for ressursen foreløpig ble satt til å arbeide på kontaktpunktet for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

### <a name="create-a-project-team"></a>Opprette et prosjektteam

1.  På listesiden **Alle prosjekter** velger du et prosjekt og klikker deretter **Rediger**.
2.  På den **prosjekt team og planlegging** -kategorien i den **planlagt sluttdato** angir startdatoen for estimat pluss én måned. Hvis for eksempel, startdato tidsplanen er 24. juni 2017 (24/06/2017), angi **24/07/2017**.
3.  Click **Add**.
4.  I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Overordnet prosjektleder**.
5.  Klikk **Obligatoriske kompetanser**.
6.  På siden **Velg egenskaper**er egenskapene som du tidligere har angitt for rollen Overordnet prosjektleder, valgt som standard. Klikk **OK**.
7.  På siden **Legg til roller i prosjekt** i feltet **Antall ressurser** angir du **1**.
8.  I **Ressurs**-feltet vil oppslaget vise alle ressurser som har de nødvendige kompetansene. Velg **Daniel Goldschmidt**, og klikk deretter **Opprett**.
9.  På **Prosjekt**-siden klikker du **Legg til**.
10. I ruten **Legg til roller i prosjektet** i **Rolle**-feltet velger du **Teammedlem**. I feltet **Antall ressurser** angir du **5**.
11. Klikk **Opprett**.
12. På **Prosjekter**-siden klikker du **Fyll opp ressurs**.

## <a name="resource-capacity-synchronization"></a>Synkronisering av ressurskapasitet
Prosessene for synkronisering av ressurser kan garantere at kalenderen og basisinformasjonen fordeles til prosjektetets ressursplanlegging. Hvis kalenderen er endret, vil prosessene foreta de nødvendige oppdateringene i planleggingen av prosjektressurser. Prosessene forbedrer også ytelsen, fordi ressursinformasjon for kalenderen synkroniseres på forhånd, slik at oppdateringer til ressursens planleggingsinformasjon utføres raskere. Vi anbefaler at du planlegger prosessene som en satsvis jobb i stedet for én om gangen. Ellers er det fare for at noen glemmer datoene da informasjonen ble sist synkronisert. Hvis inklusive datoer ikke brukes, kan det oppstå mellomrom under synkronisering av dato.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Synkroniseringsprosessen er utformet for å synkronisere all kalenderinformasjon for ressursen. Denne informasjonen omfatter grunnleggende kalenderinformasjon om endringer i prosjektets kapasitetstabell for ressurskalenderen. Hvis det legges til nye ressurser i prosjektet, sikrer synkronisering at kalenderinformasjonen oppdatert er tilgjengelig. Denne synkroniseringen kan utføres når som helst. 

Vi anbefaler at du bruker et parti. Alternativene er tilgjengelige i reservasjoner av synkroniseringskapasitet.

-   Klikk **prosjekt prosjektstyring og regnskap**&gt;**periodisk**&gt;**kapasitet synkronisering**&gt;**synkronisere ressurser kapasitet fremhevinger**.

| Alternativ | beskrivelse                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synkroniser alle ressursdata med kalenderen og grunnleggende kalenderinformasjon, og erstatt all informasjon i prosjektets ressurskapasitetskalender.                                                  |
| Antall     | Synkroniser ressursdata basert på datointervallkoden og de angitte start- og sluttdatoene. Dette alternativet fjerner ikke eksisterende data og oppdaterer informasjon bare for nylige ressurser. |

[![Synkroniseringsprosessen](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Definere roller i WBS-maler
Prosjektledere kan definere WBS-maler som kan gjelde når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller når de oppretter en mal. Bruk følgende prosedyre til å tilordne en rolle til en WBS-template.* * **

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**Setup**&gt;**prosjekter**&gt;**maler for arbeidsnedbrytningsstruktur**.
2.  Klikk **Detaljer** for en valgt WBS-mal.
3.  Velg en oppgave i listen, og deretter i **Rolle**-feltet velger du en rolle for å tildele til aktiviteten.

### <a name="work-with-a-wbs"></a>Arbeide med en WBS

Du kan opprette en ny WBS, eller du kan kopiere en WBS fra en eksisterende WBS-mal. En prosjektleder kan enkelt håndtere ressursene ved å tilordne roller til nye aktiviteter på WBS-en. Roller kan erstattes etter at en ressurs er anskaffet, eller når en bekreftet ressurs for arbeid på aktiviteten er angitt. Denne fleksibiliteten gjør det mulig for prosjektledere å utføre følgende oppgaver:

-   Identifisere antallet ressurser som kreves for WBS-arbeidspakkene.
-   Estimere prosjektkostnader.
-   Fastsette et foreløpig budsjett.
-   Beregne varigheten til aktiviteten, basert på roller og ressurser.
-   Utvikle noen prosjektstyringsplaner, basert på den tilgjengelige prosjektinformasjonen.

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
<td>Legg automatisk til planlagte ressurser ved hjelp av rollene som er knyttet til en oppgave. Dynamics 365 for operasjoner foreslår automatisk planlagte ressurser ved hjelp av flere kriterier beslutning-analysen som er basert på roller. Etter roller og innsats (timer) er definert for aktivitetene i en WBs, og strukturen er frigitt, klikker du <strong>Autogenerer team</strong>. Antall planlagte ressurser legges til WBS-en og i kategorien <strong>Prosjekt- og teamplanleggingr</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser til forpliktende eller ikke-forpliktende bestilling, basert på den angitte varigheten. Du kan justere innstillingene for å vise og angi varigheten for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivå ved hjelp av følgende alternativer:
<ul>
<li><strong>Godta</strong> – bekrefte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Avbryt</strong> – avbryte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Tilordne automatisk</strong> – dette alternativet velger en tilgjengelig ressurs som er bemannet med en samsvarende rolle til den merkede aktiviteten.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**prosjekter**&gt;**alle prosjekter**.
2.  I listen velger du prosjektet **XYZ-oppgraderingsfase 2**.
3.  Klikk **planlegger**&gt;**aktiviteter**&gt;**prosjektstrukturplan**.
4.  Klikk **ny** for å legge til følgende aktiviteter på nivå én i WBS-en:
    -   Oppstart
    -   Planlegging
    -   Utfører
    -   Overvåking og kontroll
    -   Lukk

5.  Angi datoer og innsats (timer), som vist i følgende skjermbilde. [![Når du angir datoer og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Velg oppgavelinjen **Oppstart**, og deretter, i **Rolle**-feltet velger du **Overordnet prosjektleder**.
7.  Klikk **Publiser**.
8.  På samme linje, i **Ressurs**-feltet velger du **Daniel Goldschmidt**.
9.  Klikk **Godta**.
10. Velg oppgavelinjen **Planlegging**, og deretter, i **Rolle**-feltet velger du **Forretningsanalytiker**.
11. Klikk **Publiser**, og klikk deretter **Autogenerer team**.
12. Klikk **Ja** i dialogboksen som vises.
13. I **Ressurs**-feltet må du kontrolle at verdien er **Forretningsanalytiker 1**.
14. For ressursen **Forretningsanalytiker 1** åpner du oppslaget og klikker **Start ressurstilordningsskjema**.
15. Velg en arbeider for oppgaven.
16. Klikk **myke tilordne**&gt;**Full kapasitet**.
17. Klikk **Lagre**, og lukk siden. 

> [!NOTE] 
> Du mottar ikke en advarsel om at den angitte ressursen er 2, fordi antall ressurser forblir på 1.
18. På siden **Arbeidsnedbrytningsstruktur** validerer du ressurstildelingen på WBS-en og klikker deretter **Lagre**.

## <a name="resource-fulfillment-for-planned-resources"></a>Oppfyllelse av planlagte ressurser
En prosjektleder kan planlegge nødvendige ressursroller for et prosjekt. Ressursbehandleren vil se disse planlagte ressursene som forespørsler på siden **Ressursoppfyllelse** og kan tildele faktiske ressurser.

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**prosjekter**&gt;**alle prosjekter**.
2.  I listen velger du prosjektet **XYZ-oppgraderingsfase 2**.
3.  Klikk **Prosjekt**.
4.  Klikk **Rediger**.
5.  På den **prosjekt team og planlegging av** i kategorien ** ** klikker **Legg til**.
6.  I dialogboksen **Legg til roller** velger du rollen **Programvareutvikler**.
7.  Klikk **Opprett**.
8.  Lukk prosjektsiden.
9.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**ressurser i Project**&gt;**ressurs oppfyllelse**.
10. Velg **Programvareutvikler 1** for prosjektet **XYZ-oppgraderingsfase 2**.
11. Velg en arbeider, og klikk deretter **Tilordne**.
12. Kontroller at linjen for **Programvareutvikler 1** er fjernet for prosjektet **XYZ-oppgraderingsfase 2**.
13. I kategorien **Prosjektteam og planlegging** for prosjektet **XYZ-oppgraderingsfase 2** må du kontrollere at arbeideren du valgte i trinn 11, er lagt til som **Programvareutvikler**.

## <a name="requests-for-project-resources"></a>Forespørsler om project-ressurser
Planleggingsfunksjonen for project-ressurs støtter bare ressursledere å levere bemannet ressurser på å få eller prosjekter. Hvis du vil aktivere denne funksjonaliteten, fullføre oppgavene nedenfor, eller Kontroller at de er fullført.

-   Definer nummerserier.
-   Definer prosjektstyring og regnskap arbeidsflyter.
-   Aktivere arbeidsflyt ressurs.

Når du har bekreftet eller fullførte aktiviteter ovenfor, kan du fullføre følgende oppgaver etter behov.

-   Opprette en ressursforespørsel fra en ikke-forpliktende bemannet ressurs.
-   Overvåke forespørsler som ressursen.
-   Oppfylle forespørsler for ressursen.
-   Be om en bemannet ressurs fra WBS.
-   Reservere ressurser til et prosjekt uten en forespørsel om en bemannet ressurs.

## <a name="monitor-project-teams"></a>Prosjektgrupper skjerm
1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**prosjekter**&gt;**alle prosjekter**.
2.  I listen over prosjekter klikker du koblingen **Prosjekt-ID** for prosjektet **XYZ-oppgraderingsfase 2**.
3.  I hurtigkategorien **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som er oppført, er riktige.



