---
title: Budsjettplanlegging
description: "Formålet med denne lab er å gi en veiledende visning av Microsoft Dynamics 365 for operasjoner funksjonalitet oppdateringer i området for budsjettplanlegging. Hensikten med denne øvelsen er å illustrere et eksempel på rask konfigurasjon av budsjettplanleggingsmodulen og vise hvordan budsjettplanlegging kan gjøres ved hjelp av denne konfigurasjonen.  Denne lab fokuserer spesielt på følgende forretningsprosesser eller oppgaver – oppretter organisasjonshierarkiet for budsjett planlegging og konfigurering av brukersikkerhet - definere budsjettplanscenarioer, budsjett plan kolonner, oppsett og Excel - maler for å opprette og aktivere budsjett planlegging prosessen - opprette budsjettplandokument ved å dra inn faktiske data fra Økonomi - ved hjelp av tildelinger til å justere budsjett plan dokumentdata - redigering budsjett plan dokumentdata i Excel"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Budsjettplanlegging

Formålet med denne lab er å gi en veiledende visning av Microsoft Dynamics 365 for operasjoner funksjonalitet oppdateringer i området for budsjettplanlegging. Hensikten med denne øvelsen er å illustrere et eksempel på rask konfigurasjon av budsjettplanleggingsmodulen og vise hvordan budsjettplanlegging kan gjøres ved hjelp av denne konfigurasjonen.  Denne lab fokuserer spesielt på følgende forretningsprosesser eller oppgaver – oppretter organisasjonshierarkiet for budsjett planlegging og konfigurering av brukersikkerhet - definere budsjettplanscenarioer, budsjett plan kolonner, oppsett og Excel - maler for å opprette og aktivere budsjett planlegging prosessen - opprette budsjettplandokument ved å dra inn faktiske data fra Økonomi - ved hjelp av tildelinger til å justere budsjett plan dokumentdata - redigering budsjett plan dokumentdata i Excel 

<a name="prerequisites"></a>Forutsetninger 
------------------

For denne opplæringen må du få tilgang til Dynamics-365 for operasjonsmiljø med Contoso demonstrasjonsdata og klargjøres som en administrator for forekomsten. Ikke bruk i privat modus for Web-leseren for denne lab - logger av fra en annen konto i leseren hvis nødvendig og logge på med Dynamics 365 for operasjoner administratorlegitimasjon. Når du logger inn i Dynamics 365 for operasjoner, du **må** fjerner du merket for "Hold meg pålogget". Dermed opprettes det en fast informasjonskapsel som Excel-appen trenger. Hvis du logger deg på Dynamics-365 for operasjoner som bruker en annen leser enn Internet Explorer, blir deretter du bedt skal logge deg inn i Excel-programmet. Når du klikker Logg på i Excel-appen, åpnes et popup-vindu for Internet Explorer, og når du logger på, **MÅ** du merke av for La meg være pålogget. Hvis du klikker Logg på i Excel-programmet og ingenting ser ut til å skje, må du tømme hurtigbufferen for informasjonskapsler i Internet Explorer.

## <a name="scenario-overview"></a>**Scenario overview**
Julie jobber som regnskapssjef i Contoso Entertainment Systems i Tyskland (DEMF). Når FY2016 nærmer seg, må hun arbeide med å sette opp firmaets budsjett for kommende år. Budsjettforberedelsen ser slik ut:

1.  Julie bruker fjorårets faktiske data som utgangspunkt for å lage budsjettet.
2.  Basert på fjorårets faktiske data oppretter hun estimater for 12 måneder i det kommende året.
3.  Julie går gjennom budsjettet med økonomidirektøren. Når hun er ferdig, gjør hun nødvendige justeringer for budsjettplanen og fullfører budsjettforberedelsen.

Konfigurasjonsskjemaet for scenariet for budsjettplanlegging ser slik ut:

![Screenshot1](./media/screenshot1-300x152.png)

Julie bruker følgende Excel-mal til å forberede budsjettet:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>Øvelse 1: konfigurasjon
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Oppgave 1: Opprette organisasjonshierarki**
Siden hele budsjetteringsprosessen skjer i økonomiavdelingen, må Julie opprette et svært enkelt organisasjonshierarki som bare består av økonomiavdelingen. 1.1. Gå til organisasjonshierarkier (organisasjonsadministrasjon &gt;organisasjoner &gt;organisasjonshierarkier), og klikk Ny-knappen

![Screenshot3](./media/screenshot3.png) 

1.2. Skriv inn navnet for organisasjonshierarkiet og klikk knappen tilordnes formålet

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Velg Budsjettplanleggingsformålet, klikker du knappen Legg til, og tilordne nylig opprettet organisasjonshierarkiet: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Gjenta trinnet ovenfor for sikkerhetsorganisasjonsformålet. Lukk skjemaet når du er ferdig.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klikk Vis-knappen i skjemaet Organisasjonshierarkier. Klikk Rediger i hierarkidesigneren, og opprett et hierarki ved å klikke Sett inn-knappen.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Velg Økonomiavdeling for budsjetteringshierarkiet. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Når du er ferdig, klikker du knappen Publiser og lukk. Velg 01.01.2015 som ikrafttredelsesdato for publisering av hierarkiet.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>Oppgave 2: konfigurere brukersikkerhet
Budsjettplanlegging bruker spesielle sikkerhetspolicyer for å konfigurere tilgang til data for budsjettplaner. Julie må gi seg selv tilgang til budsjettplaner. 2.1. Bytt til DEMF juridisk enhet kontekst: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Naviger til budsjettering &gt;Setup &gt;budsjettplanlegging &gt;budsjettplanleggingskonfigurasjon. I Parametere-kategorien, angi sikkerhet modell verdien basert på sikkerhet organisasjoner [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Gå til systemadministrasjon &gt;brukere &gt;brukere. Gi brukeren Admin (Julia Funderburk) rollen som budsjettleder. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Velg brukerrolle og klikk Tilordne organisasjoner [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Velg Gi tilgang til bestemte organisasjoner. Velg organisasjonshierarkiet som ble opprettet i det første trinnet. Velg noden Økonomi og klikker Gi med barn-knappen ***viktig!*** *– Pass på at du er i konteksten for DEMF juridisk enhet når du utfører denne oppgaven når organisatoriske sikkerhet brukes per juridisk enhet*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>Oppgave 3: opprette scenarier
3.1. Naviger til budsjettering&gt;Setup &gt;budsjettplanlegging &gt;budsjettplanleggingskonfigurasjon. Legg merke til scenariene vi skal bruke videre i denne laben, på Scenarier-siden: Faktisk, forrige år og Budsjettert. *Obs!  Hvis du vil, kan du opprette nye scenarier for denne øvelsen og bruke dem i stedet.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*notat: Julie ikke er bruker formell godkjenningsprosessen for budsjett forberedelse, vi hopper over arbeidsflyter, faser og arbeidsflytstadier oppsett i denne lab og vil bruke eksisterende oppsett for Auto-godkjenne arbeidsflyt. Se tillegg for konfigurasjon av arbeidsflyt.*

## <a name="task-4-create-budget-plan-columns"></a>Oppgave 4: opprette budsjettplankolonner
Budsjettplankolonner er enten monetære eller antallsbaserte kolonner som kan brukes i oppsett for budsjettplandokument. I vårt eksempel må vi opprette en kolonne for Faktisk, forrige år og 12 kolonner som skal representere hver måned i et budsjettert år. Kolonner kan opprettes ved ganske enkelt å klikke Legg til-knappen og fylle inn verdiene, eller ved hjelp av Dataenhet. Vi skal bruke Dataenhet til å fylle inn verdiene i denne laben. 4.1. I budsjettering&gt;Setup &gt;budsjettplanlegging &gt;budsjett planlegging åpne kolonner på konfigurasjonssiden. Klikk Office-knappen i øvre høyre hjørne i skjemaet, og Velg kolonner (ufiltrert) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Systemet åpner Excel-arbeidsboken som skal brukes til å fylle inn verdiene. Hvis du blir bedt om det, klikker du Aktiver redigering og stole på denne app [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Vi trenger flere kolonner til å fylle ut verdiene. Klikk utforming på den høyre ruten til å legge til kolonner i rutenettet: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Klikk lille blyant-knappen ved siden av PlanColumns for å se tilgjengelige kolonnene du vil legge til rutenettet [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Dobbeltklikk på hvert tilgjengelige felt for å legge dem til i valgte felt, og klikk Oppdater [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Legg til alle kolonnene som skal opprettes, i Excel-tabellen. Bruk Autofyll-funksjonen i Excel til å legge til linjene raskt. Kontroller at linjene blir lagt til som en del av tabellen (når du bruker loddrett Rull, skal du kunne se kolonneoverskriftene øverst i rutenettet) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Gå tilbake til Dynamics 365 for operasjoner og oppdatere siden. Publiserte verdier vises i Dynamics 365 for operasjoner. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Oppgave 5: opprette oppsett og maler for budsjettplandokument
Oppsettet definerer hvordan rutenettlinjer blir seende ut i budsjettplandokumentet når brukere åpner budsjettplandokumentet. Det er også mulig å bytte oppsettet for budsjettplandokument for å se de samme dataene fra ulike vinkler. Nå som hun har kolonner definert for bruk med budsjettplandokumentet vårt, må Julie opprette et oppsett for budsjettplandokument som ligner på Excel-tabellen hun bruker til å lage budsjettdata (se delen Oversikt over scenariet i denne laben) 5.1. I budsjettering&gt;oppsett &gt;budsjettplanlegging &gt;budsjett planlegging åpne oppsett konfigurasjonsside. Opprett et nytt oppsett for oppføringen for månedsbudsjett:

-   Velg dimensjonssettet MA+BU for å ta med hovedkontoer og forretningsenheter i oppsettet.
-   Vis alle budsjettplankolonner som ble opprettet i forrige trinn, i delen Elementer. Gjøre alle redigerbare, unntatt Faktisk, forrige år.
-   Klikk Beskrivelser-knappen for å velge hvilke finansdimensjoner som skal vise beskrivelser i rutenettet.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) basert på budsjettet planlegger Oppsettsdefinisjonen vi kan opprette en Excel-mal som skal brukes som en alternativ måte å redigere budsjettdata. Siden Excel-malen må samsvare med oppsettdefinisjonen for budsjettplan, kan du ikke redigere oppsettet for budsjettplanen etter at du har generert Excel-malen. Derfor må du gjøre denne oppgaven etter at alle oppsettkomponenter er definert. 5.2. For oppsettet som er opprettet i 5.1. Trinn, og klikk mal &gt;Generer. Bekreft advarselen. Klikk mal hvis du vil vise malen, &gt;Vis. *Merk: Pass på at du velger "Lagre som" og velg stedet der malen skal lagres for å redigere den. Hvis brukeren velger "Åpne" i dialogboksen uten å lagre, beholdes ikke endringer som er gjort med filen når filen lukkes.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Valgfritt trinn&gt; endre Excel-malen slik at den ser mer brukervennlig – Legg til total formler, felt, formatering, osv. Lagre endringene og laste opp filen til budsjett plan oppsett ved å klikke Oppsett &gt;laste opp [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>Oppgave 6: opprette en budsjettplanleggingsprosess
Julie må opprette og aktivere en ny budsjettplanleggingsprosess der hele oppsettet ovenfor kombineres, for å begynne å registrere budsjettplaner. Budsjettplanleggingsprosessen definerer hvilke budsjetteringsorganisasjoner, arbeidsflyter, oppsett og maler som skal brukes til å opprette budsjettplaner. 6.1. Naviger til budsjettering &gt;Setup &gt;budsjettplanlegging &gt;budsjett planleggingsprosessen og opprette en ny post.

-   Budsjettplanleggingsprosess – DEMF budgeting FY2016
-   Budsjettsyklus – FY2016
-   Finans – DEMF
-   Standard kontostruktur – Manufacturing P&L
-   Organisasjonshierarki – velg hierarkiet som ble opprettet i begynnelsen av laben
-   Arbeidsflyt for budsjettplanlegging – tilordne automatisk godkjenning av arbeidsflyt for økonomiavdelingen
-   I stadieregler og maler for budsjettplanlegging velger du om det er tillatt å legge til linjer og å endre linjer og hvilket oppsett som skal brukes som standard, for hvert arbeidsflytstadium for budsjettplanlegging.

*Obs!  Du kan opprette flere dokumentoppsett og tilordne dem slik at de er tilgjengelige på arbeidsflytstadiet for budsjettplanlegging, ved å klikke knappen Alternative oppsett.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Velg Handlinger &gt;Aktiver for å aktivere denne budsjettplanleggingsarbeidsflyten [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>Øvelse 2: prosessimulering
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Oppgave 7: generere innledende data for budsjettplan fra Økonomimodul
7.1. Naviger til budsjettering &gt;periodisk &gt;Generer budsjettplan fra økonomimodulen. Fyll ut parameterne for periodisk prosess, og klikk Generer. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Naviger til budsjettering &gt;budsjett planer å finne en budsjettplan som er opprettet av Generer prosess. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7.3. Åpne dokumentdetaljene ved å klikke dokumentnummerhyperkoblingen. Budsjettplanen vises som definert i oppsettet som er opprettet under denne lab [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Oppgave 8: opprette budsjett for gjeldende år basert på fjorårets faktiske data
Tildelingsmetoder kan brukes i budsjettplaner til å kopiere informasjon for budsjettplaner fra ett scenario til et annet, spre dem på tvers av perioder, eller tildele dem til dimensjoner. Vi skal bruke tildelinger til å opprette budsjett for gjeldende år fra fjoråret faktiske data. 8.1. Velg alle linjer i budsjett plan dokumentrutenettet og klikk Tildel budsjett [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Velg tildelingsmetode, Periodenøkkel, kilde- og scenarier og klikk Tildel 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

De faktiske beløpene for forrige år vil bli kopiert til budsjettet for gjeldende år og tildele dem på tvers av perioder med salg kurve Periodenøkkel. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Oppgave 9: justere budsjettplandokument ved hjelp av Excel og gjøre ferdig dokumentet
9.1. Klikk knappen regnearket for å åpne dokumentinnholdet i Excel

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Når Excel-arbeidsboken åpnes, justerer du tallene i budsjettplandokument og klikker Publiser.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Gå tilbake til budsjettplandokument i Dynamics 365 for operasjoner. Klikk arbeidsflyt &gt;sende inn til å automatisk godkjenne dokumentet

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Når arbeidsflyten er fullført, endres budsjettplanstadium for dokumentet til godkjent. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Tillegg
========

### <a name="auto-approve-workflow-configuration"></a>Konfigurasjon av automatisk godkjenning av arbeidsflyt

A. Budsjettering &gt;Setup &gt;budsjettplanlegging &gt;budsjetteringsarbeidsflyter opprette en ny arbeidsflyt ved hjelp av arbeidsflyter for budsjettplanlegging mal:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

Denne arbeidsflyten inneholder bare én oppgave – plan for utarbeidingsstadie overgang budsjett 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Lagre og aktiverer arbeidsflyten. 

B. Naviger til budsjettering &gt;Setup &gt;budsjettplanlegging &gt;budsjettplanleggingskonfigurasjon. I kategorien Opprett 2 stadier – første og sendt i faser 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Naviger til budsjettering &gt;Setup &gt;budsjettplanlegging &gt;budsjettplanleggingskonfigurasjon. I kategorien arbeidsflytstadier knytter arbeidsflyten automatisk – godkjenne opprettet i et trinn med trinnene første og sendt 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


