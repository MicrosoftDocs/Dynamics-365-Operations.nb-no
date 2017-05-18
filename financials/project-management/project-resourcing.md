---
title: Prosjektressurser
description: Dette emnet inneholder informasjon om ressursberegning for prosjekter.
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 11755e4ab4b3c1f55da80e57ff96e0b13c84c697
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="project-resourcing"></a>Prosjektressurser

[!include[banner](../includes/banner.md)]


Dette emnet inneholder informasjon om ressursberegning for prosjekter.

En utfordring for prosjektledere og ressursansvarlige i løpet av planleggingsfasen for prosjektet er ressursallokering, der de må finne og reservere den riktige ressursen skal arbeide på et prosjekt. I Microsoft Dynamics 365 for Operations kan ressursfunksjoner for prosjekter la deg definere roller som skal behandles som midlertidige ressurser som kan reserveres for et spesifikt prosjekt eller en del av et prosjekt. Denne typen ressurser lar prosjektledere og ressursansvarlige utføre følgende oppgaver:

-   Definer en rolle som har de nødvendige kompetansene til å gjøre det enklere å samsvare med ressurser.
-   Bruk roller til å definere en innledende prosjekttidsplan som er basert på reserverte ressurser.
-   Beregne kostnader, og finne et opprinnelig budsjett, basert på tilordnede roller og ressurser for et prosjekt.
-   Bruke roller til å beregne hvor mange ressursreservasjoner som kreves for hvert prosjekt.
-   Beregne hvor mange ressurser som kreves for hele livssyklusen til et prosjekt.
-   Lage en prosjektstrukturplan ved hjelp av de opprinnelige ressurstildelingene.

[![Prosjektets livssyklus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Etter hvert som prosjektplanleggingen pågår, kan planlagte ressurser erstattes med bemannede ressurser. Prosjektlederen kan også gå tilbake og oppdatere ressursreservasjoner under ett av prosjektstadiene.

## <a name="set-up-project-resources"></a>Definere prosjektressurser
Du må opprette en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet. Prosjektledere kan utføre ressursutjevning som en del av optimalisering av ressursen, under installasjonen av kalenderen. Basert på tidspunktet i kalenderen, kan begrensninger plasseres på ressurser. Du kan opprette en kalender på siden **Kalendere**. 

Når du definerer en arbeider som en prosjektressurs, kan du velge blant arbeidere som arbeider i firmaet du vil konfigurere ressurser for, eller du kan velge arbeidere fra andre firmaer i organisasjonen. Dette er konserninterne ressurser. Fremgangsmåtene nedenfor beskriver hvordan du definerer en arbeider som en ressurs i firmaet og hvordan du definerer en konsernintern prosjektressurs.

### <a name="set-up-a-worker-as-a-project-resource"></a>Definere en arbeider som en prosjektressurs

1.  I **Arbeidere**-listen på siden **Arbeidere**, velger du arbeideren som du legger til som en prosjektressurs, og åpner arbeiderposten.
2.  I handlingsruten klikker du på **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.
3.  Velg en kalender, og lukk deretter siden.

Du kan også angi standardprosjekter for en ressurs som en type førtilordning. Førtildelinger kan brukes når ressursansvarlig eller prosjektleder vet hvilke prosjekter som ressursen vil arbeide med på forhånd. Førtildelinger kan også være basert på forespørsel fra en prosjektsponsor eller kunde. Hvis du vil førtilordne et prosjekt, på siden **Tilordne prosjekter** i kategorien **Prosjekter** i lsietn **Gjenværende prosjekter**, velger du det aktuelle prosjektet.

### <a name="set-up-an-intercompany-resource"></a>Definere en konsernintern ressurs

Når du definerer en arbeider som en konsernintern ressurs, må du fullføre oppsettet i utlånsfirmaet og lånefirmaet. 

**I utlånsfirmaet:**

1.  I Dynamics 365 for Operations kontrollerer du at utlånsfirmaet er valgt, og deretter fullfører du fremgangsmåten ovenfor, "Definere en arbeider som en prosjektressurs".
2.  Gå til **Finans** &gt; **Posteringsoppsett** &gt; **Konserninternt regnskap**. Klikk på **Ny**.
3.  I feltet **ID for juridisk enhet** velger du utlånsfirmaet. Fyll ut de gjenværende feltene etter behov, og klikk deretter på **Lagre**.
4.  Gå til **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser** &gt; **Overføringspris**.** **
5.  I skjemaet **Overføringspris** klikker du på **Ny**, og i feltet **Juridisk enhet som låner** velger du det riktige firmaet.
6.  Hvis du bare vil låne til lånefirmaet ressursen du opprettet i begynnelsen av denne delen, i **Ressurs**-feltet, velger du navnet på ressursen du opprettet. Hvis du vil gjøre alle ressurser i firmaet tilgjengelig for låneselskapet, lar du **Ressurs**-feltet være tomt.
7.  Gå til **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Parametere for prosjektstyring og regnskap**, og i kategorien **Konsernintern** setter du feltet **Aktiver konsernintern ressursplanlegging og timeregistreringer** til **Ja**.

**I lånefirmaet:**

1.  Gå til **Prosjektstyring og regnskap** &gt; **Prosjektressurser** &gt; **Ressursliste**.
2.  I søkefilteret angir du navnet på ressursen som du opprettet i forrige fremgangsmåte for utlånsfirmaet, for å kontrollere at navnet er inkludert i ressurslisten for lånefirmaet.

## <a name="manage-resource-competencies"></a>Administrere ressurskompetanser
Ressurskompetanser er en viktig del av ressursbehandling. Kompetanser kan brukes som et utgangspunkt til å fastsette ressurser som har den riktige balansen mellom ferdigheter, utdanning, sertifisering og prosjekterfaring. Du bør definere denne informasjonen for hver ressurs og oppdatere den med jevne mellomrom. På denne måten kan du maksimere muligheter når bestemte ressurskompetanser sammenlignes under ressurstildeling i prosjektet. [![Eksempler på ferdigheter, sertifiseringer, utdanning og prosjekterfaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Fremgangsmåtene nedenfor forklarer hvordan du setter opp noen av kompetansetypene for en ressurs. 

Hvis du vil definere kompetanse for en arbeider, kan du bruke **Arbeidere**-listesiden i Personale eller **Ressurser**-listesiden i Prosjektstyring og regnskap. For følgende fremgangsmåter brukes **Arbeidere**-listesiden i Personale.

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
1.  Klikk på **Prosjektstyring og regnskap** &gt; **Arbeidsområder** &gt; **Prosjektstyring**.
2.  Klikk **Nytt prosjekt**, og angi deretter følgende verdier:
    -   **Prosjekttype:** – Tid og materialer
    -   **Prosjektnavn:** – XYZ-oppgraderingsfase 2
    -   **Prosjektgruppe:** – TM\_WIP
    -   **Prosjektkontrakt-ID:** – 00000002
3.  Klikk **Opprett prosjekt**.

### <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1.  Klikk på **Personale** &gt; **Arbeidere** &gt; **Arbeidere**.
2.  I **Arbeidere**-listen velger du posten for arbeideren som du allerede har installert kompetanser for, og åpne arbeiderposten.
3.  I handlingsruten i kategorien **Prosjekt** i **Oppsett**-gruppen klikker du **Tilordne prosjekter**.
4.  På siden **Prosjekttilordninger for ressursvalidering** klikker du kategorien **Prosjekter**.
5.  Under **Legg til prosjektet for valgte prosjekter** filtrerer du etter prosjektet XYZ-oppgraderingsfase 2
6.  I ruten **Gjenværende prosjekter** velger du et prosjekt og klikker deretter pilen for å legge det til i ruten **Valgte prosjekter**.
7.  Lukk siden.

Hvis du trenger det, kan du også tilordne kategorier for en ressurs. Kategoritypen er enten kostnad eller inntekt. Dette bestemmes av organisasjonen. Hvis det finnes ingen tilordnede kategorier for ressursen, slår Dynamics 365 for Operations opp standardkategorien på timeprisene for kostnader og inntekter.

### <a name="set-up-project-resource-and-role-characteristics"></a>Definere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektetressursfunksjonaliteten til å opprette roller som kreves for prosjektet. Roller kan brukes når bekreftede ressurser fremdeles er ukjent under reservering av ressurser. Roller kan reserveres midlertidig som planlagte ressurser, slik at du kan fortsette prosjektetplanleggingsfasene. 

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble ansatt for å fullføre et tid og materialer-prosjekt som har et godkjent prosjektdokument. Den underordnede prosjektlederen fullfører fremdeles omfanget av prosjektet. Ressursbehandleren identifiserer de bestemte ressursene som skal reserveres, for å arbeide med det nye prosjektet. Én av rollene som prosjektsponsoren har forespurt, er overordnet prosjektleder, på grunn av kritiske arten av prosjektet. Ressursbehandleren må få den nye ressursen og definere rollen i systemet, i tilfelle den underordnede prosjektlederen krever ressursinformasjonen under planleggingen av prosjektet. 

Følgende fremgangsmåte viser hvordan ressursbehandleren kan definere rollen som overordnet prosjektleder og tilknytte ressursegenskaper til den. Rollen kan senere brukes til å søke etter ressurser som samsvarer med de nødvendige ressurskompetansene.

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Ressurser** &gt; **Oppsettsroller**.
2.  Klikk **Ny**, og angi deretter følgende verdier:
    -   **Rolle-ID:** – Overordnet prosjektleder
    -   **Beskrivelse:** – Overordnet prosjektleder
3.  Klikk **Opprett**.
4.  Velg rollen **Overordnet prosjektleder**, og klikk deretter **Konfigurer kjennetegn**.
5.  I feltet **Egenskapstype** velger du **Ferdighet**.
6.  I feløtet **Tilgjengelige egenskaper** angir du ferdigheten du søker etter.
7.  I feltet **Egenskapstype** velger du **Sertifikat**.
8.  I feltet **Tilgjengelige egenskaper** angir du sertifikattypen du skal søke etter.
9.  Klikk **OK**, og lukk siden.

### <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Felles** &gt; **Prosjekter** &gt; **Alle prosjekter**, og åpne prosjektet **XYZ-oppgraderingsfase 2**.
2.  I kategorien **Prosjektteam og planlegging** klikker du **Legg til**.
3.  I **Rolle**-feltet velger du **Teammedlem**.
4.  Klikk **Bestill fra kalender**.
5.  På siden **Ressurstilgjengelighet** klikker du **Visningsinnstillinger**.
6.  På siden **Juster visningsinnstillinger** angir du følgende verdier:
    -   **Format for visning av datoområde:** – Dag
    -   **Vis tilgjengelighetsbeskrivelser:** – Ja
    -   **Vis gjenstående kapasitet:** – Ja
7.  Velg en ressurs i listen over ressurser.
8.  Klikk på **Forpliktende bestilling** &gt; **Full kapasitet**.
9.  Lukk siden.

### <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe prosjekt- eller ressursledere kan du drille ytterligere ned på ressursene som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig anskaffet ressurs. Eksempel: Da Daniel ble ansatt, hadde han erfaring og ferdigheter til å fylle rollen som forretningsanalytiker. Ressursbehandleren tilordnet denne rollen som Daniels standardrolle. Derfor la ressursbehandleren Daniel til i et utvalg av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter. 

Under ressursreservering kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter. De kan bruke denne informasjonen som én av betingelsene når de utfører analyse av beslutninger med flere kriterier under ressursoppfyllelse. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har bestemte ferdigheter, utdanning og erfaring for et bestemt prosjekt. 

**Scenario:** Et godkjent prosjekt er startet, og rollen Overordnet prosjektstyrer ble reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen. Ressurslederen har nå anskaffet seg en ressurs for å oppfylle rollen Overordnet prosjektleder.

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Prosjektressurser** &gt; **Ressursliste**.
2.  I **Ressurs**-listen velger du **Daniel Goldschmidt**.
3.  Klikk på **Prosjektressurs** &gt; **Vedlikehold** &gt; **Ressursrolle**.
4.  Klikk **Ny**, og angi deretter følgende verdier:
    -   **Gjelder fra:** – (Gjeldende dato)
    -   **Utløper:** – Aldri
    -   **Rolle:** – Overordnet prosjektleder
5.  Klikk **Lagre**, og lukk deretter siden.
6.  I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og **PMP**-sertifikatet.

## <a name="set-up-role-based-pricing"></a>Definere rollebasert prising
Alle kostnader, salg, og overføringspriser kan defineres for roller.

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser** &gt; **Salgspris (time)**.
2.  Klikk på **Ny**.
3.  Angi en gyldighetsdato.
4.  Velg en rolle i **Rolle**-kolonnen.
5.  I **Prising**-kolonnen, angi en pris for den valgte ressursrollen.

## <a name="form-a-project-team"></a>Danne et prosjektteam
Hvis du vil bruke rollene som tidligere ble angitt i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Du kan tilordne flere roller for et prosjekt, og Dynamics 365 for Operations merker automatisk disse rollene under reservering for å unngå forvirring. Hvis for eksempel prosjektlederen krever tre programmerere, vil tre programmererroller som har programmerer 1, programmerer 2 og programmerer 3 som etiketter, bli generert automatisk. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter ved søking etter en ressurs. Du kan legge flere egenskaper etter behov for å spesifisere søket ytterligere. 

Visningsinnstillinger kan også tilpasses for å få en bedre oversikt over tilgjengelige ressurser. Det finnes alternativer for å vise tilgjengelighet for hver time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenværende kapasitet i ressurser. Dette alternativet er nyttig for tidsadministrasjon når du gjør beregninger tilgjengelig tid for aktiviteter eller tilgjengelige ressurser. 

Prosjektlederen kan velge en rolle på siden, og hvis det finnes en tilgjengelig ressurs som passer til behovet, velge å reservere en ressurs til å fylle rollen. Legg merke til at ressursene ikke trenger å reserveres på dette tidspunktet i løpet av planleggingsstadiet. Når du oppretter en prosjektstrukturplan, kan du erstatte roller med bemannede ressurser for prosjektet. Hvis roller erstattes med bemannede ressurser i prosjektstrukturplanen, oppdaterer ressursoppsettet automatisk prosjektgruppeoversikten og -planleggingen. 

[![Prosjektgruppeoversikt som inneholder både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for å bestille en ressurs for et prosjekt, for eksempel **Gjenværende kapasitet**, **Full kapasitet**, **Kapasitetsprosent** og **Angi timer**. Disse alternativene for bestilling kan annulleres når som helst hvis ressurstildelinger endres. To typer bestilling støttes:

-   **Forpliktende bestilling** – Ressursreserveringen ble godkjent og bekreftet for å arbeide med prosjektet for den angitte varigheten.
-   **Ikke-forpliktende bestilling** – Ressursreserveringen ble foreløpig angitt for å arbeide med prosjektet for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

### <a name="create-a-project-team"></a>Opprette et prosjektteam

1.  På listesiden **Alle prosjekter** velger du et prosjekt og klikker deretter **Rediger**.
2.  I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato for tidsplanen pluss én måned. Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.
3.  Klikk **Legg til**.
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

**Synkroniser opprullinger av ressurskapasitet**

Synkroniseringsprosessen er utformet for å synkronisere all kalenderinformasjon for ressursen. Denne informasjonen omfatter grunnleggende kalenderinformasjon om endringer i prosjektets kapasitetstabell for ressurskalenderen. Hvis det legges til nye ressurser i prosjektet, synkronisering bidrar til å sikre at det finnes oppdatert kalenderinformasjonen. Denne synkroniseringen kan utføres når som helst. 

Vi anbefaler at du bruker et parti. Alternativene er tilgjengelige i reservasjoner av synkroniseringskapasitet.

-   Klikk på **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetsynkronisering** &gt; **Synkroniser opprullinger av ressurskapasitet**.

| Alternativ | beskrivelse                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synkroniser alle ressursdata med kalenderen og grunnleggende kalenderinformasjon, og erstatt all informasjon i prosjektets ressurskapasitetskalender.                                                  |
| Antall     | Synkroniser ressursdata basert på datointervallkoden og de angitte start- og sluttdatoene. Dette alternativet fjerner ikke eksisterende data og oppdaterer informasjon bare for nylige ressurser. |

[![Synkroniseringsprosess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Definere roller i WBS-maler
Prosjektledere kan definere WBS-maler som kan gjelde når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller ved oppretting av en mal. Bruk følgende fremgangsmåte for å tilordne en rolle til en WBS-mal.** ** 

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Prosjekter** &gt; **Maler for arbeidsnedbrytningsstruktur**.
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
<td>Legg automatisk til planlagte ressurser ved hjelp av rollene som er knyttet til en oppgave. Dynamics 365 for Operations foreslår automatisk planlagte ressurser ved hjelp av en beslutningsanaluyse med flere kriterier som er basert på roller. Etter roller og innsats (timer) er definert for aktivitetene i en WBs, og strukturen er frigitt, klikker du <strong>Autogenerer team</strong>. Antall planlagte ressurser legges til WBS-en og i kategorien <strong>Prosjekt- og teamplanleggingr</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser til forpliktende eller ikke-forpliktende bestilling, basert på den angitte varigheten. Du kan justere innstillingene for å vise og angi varigheten for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivå ved hjelp av følgende alternativer:
<ul>
<li><strong>Godta</strong> – bekrefte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Avbryt</strong> – avbryte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Tilordne automatisk</strong> – Dette alternativet velger en tilgjengelig bemannet ressurs med en samsvarende rolle som den valgte oppgaven.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Prosjekter** &gt; **Alle prosjekter**.
2.  I listen velger du prosjektet **XYZ-oppgraderingsfase 2**.
3.  Klikk på **Plan** &gt; **Aktiviteter** &gt; **Arbeidsnedbrytningsstruktur**.
4.  Klikk **ny** for å legge til følgende aktiviteter på nivå én i WBS-en:
    -   Oppstart
    -   Planlegging
    -   Utfører
    -   Overvåking og kontroll
    -   Lukk

5.  Angi datoer og innsats (timer), som vist i følgende skjermbilde.[![Angi datoer og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Klikk på **Tilordne uforpliktende** &gt; **Full kapasitet**.
17. Klikk **Lagre**, og lukk siden. 

> [!NOTE] 
> Du mottar ikke en advarsel om at den angitte ressursen nå er 2, på grunn av antallet ressurser som gjenstår på 1.
18. På siden **Arbeidsnedbrytningsstruktur** validerer du ressurstildelingen på WBS-en og klikker deretter **Lagre**.

## <a name="resource-fulfillment-for-planned-resources"></a>Oppfyllelse av planlagte ressurser
En prosjektleder kan planlegge nødvendige ressursroller for et prosjekt. Ressursbehandleren vil se disse planlagte ressursene som forespørsler på siden **Ressursoppfyllelse** og kan tildele faktiske ressurser.

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Prosjekter** &gt; **Alle prosjekter**.
2.  I listen velger du prosjektet **XYZ-oppgraderingsfase 2**.
3.  Klikk **Prosjekt**.
4.  Klikk **Rediger**.
5.  I kategorien **Prosjektteam og planlegging** klikker du på **Legg til**.
6.  I dialogboksen **Legg til roller** velger du rollen **Programvareutvikler**.
7.  Klikk **Opprett**.
8.  Lukk prosjektsiden.
9.  Klikk på **Prosjektstyring og regnskap** &gt; **Prosjektressurser** &gt; **Ressursoppfyllelse**.
10. Velg **Programvareutvikler 1** for prosjektet **XYZ-oppgraderingsfase 2**.
11. Velg en arbeider, og klikk deretter **Tilordne**.
12. Kontroller at linjen for **Programvareutvikler 1** er fjernet for prosjektet **XYZ-oppgraderingsfase 2**.
13. I kategorien **Prosjektteam og planlegging** for prosjektet **XYZ-oppgraderingsfase 2** må du kontrollere at arbeideren du valgte i trinn 11, er lagt til som **Programvareutvikler**.

## <a name="requests-for-project-resources"></a>Forespørsler om prosjektressurser
Planleggingsfunksjonen for prosjektressurs støtter bare at ressursansvarlige distribuerer bemannede ressurser på engasjementer eller prosjekter. Hvis du vil aktivere denne funksjonaliteten, fullfører du oppgavene nedenfor eller kontrollerer at de er fullført.

-   Definer nummerserier.
-   Definer arbeidsflyter for prosjektstyring og regnskap.
-   Aktiver arbeidsflyt for ressursforespørsel.

Når du har bekreftet eller fullførte oppgavene ovenfor, kan du fullføre oppgavene nedenfor etter behov.

-   Opprett en ressursforespørsel fra en ikke-forpliktende bemannet ressurs.
-   Overvåk ressursforespørsler.
-   Oppfyll ressursforespørsler.
-   Be om en bemannet ressurs fra WBS.
-   Bestill ressurser til et prosjekt uten en forespørsel om en bemannet ressurs.

## <a name="monitor-project-teams"></a>Overvåke prosjektteam
1.  Klikk på **Prosjektstyring og regnskap** &gt; **Prosjekter** &gt; **Alle prosjekter**.
2.  I listen over prosjekter klikker du koblingen **Prosjekt-ID** for prosjektet **XYZ-oppgraderingsfase 2**.
3.  I hurtigkategorien **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som er oppført, er riktige.





