---
title: Budsjettplanlegging
description: Formålet med denne øvelsen er å gi en veiledet visning av Microsoft Dynamics 365 Finance-funksjonalitetsoppdateringer i området for budsjettplanlegging. Hensikten med denne øvelsen er å illustrere et eksempel på rask konfigurasjon av budsjettplanleggingsmodulen og vise hvordan budsjettplanlegging kan gjøres ved hjelp av denne konfigurasjonen.
author: panolte
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0420887c35bbb07aaf8cce05a68173ab6c534f92
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595340"
---
# <a name="budget-planning"></a>Budsjettplanlegging

[!include [banner](../includes/banner.md)]

Formålet med denne øvelsen er å gi en veiledet visning av Microsoft Dynamics 365 Finance-funksjonalitetsoppdateringer i området for budsjettplanlegging. Hensikten med denne øvelsen er å illustrere et eksempel på rask konfigurasjon av budsjettplanleggingsmodulen og vise hvordan budsjettplanlegging kan gjøres ved hjelp av denne konfigurasjonen.  Denne laben fokuserer på følgende forretningsprosesser eller -oppgaver:
- Opprette organisasjonshierarki for budsjettplanlegging og konfigurere brukersikkerhet
- Definere budsjettplanscenarioer, budsjettplankolonner, oppsett og Excel-maler
- Opprette og aktivere budsjettetplanleggingsprosess
- Opprette budsjettplandokument ved å dra inn faktiske data fra økonomimodulen
- Bruke tildelinger til å justere budsjettplandokumentdata
- Redigere budsjettplandokumentdata i Excel 

## <a name="prerequisites"></a>Forutsetninger 

I denne opplæringen må du ha tilgang til Microsoft Dynamics 365 Finance-miljøet med Contoso-demonstrasjonsdata og være klargjort som administrator på forekomsten. Ikke bruk nettleseren i privat modus i denne laben. Logg om nødvendig av eventuelle andre kontoer i nettleseren, og logg på med administratorlegitimasjon. Når du logger på, **MÅ** du merke av for La meg være pålogget. Dermed opprettes det en fast informasjonskapsel som Excel-appen trenger. Hvis du logger på programmet ved å bruke en annen nettleser enn IE, blir du bedt om å logge på i Excel-appen. Når du klikker Logg på i Excel-appen, åpnes et popup-vindu for IE, og når du logger på, **MÅ** du merke av for La meg være pålogget. Hvis du klikker Logg på i Excel-programmet og ingenting ser ut til å skje, må du tømme hurtigbufferen for informasjonskapsler i IE.

## <a name="scenario-overview"></a>**Oversikt over scenariet**
Julie jobber som regnskapssjef i Contoso Entertainment Systems i Tyskland (DEMF). Når FY2016 nærmer seg, må hun arbeide med å sette opp firmaets budsjett for kommende år. Budsjettforberedelsen ser slik ut:

1.  Julie bruker fjorårets faktiske data som utgangspunkt for å lage budsjettet.
2.  Basert på fjorårets faktiske data oppretter hun estimater for 12 måneder i det kommende året.
3.  Julie går gjennom budsjettet med økonomidirektøren. Når hun er ferdig, gjør hun nødvendige justeringer for budsjettplanen og fullfører budsjettforberedelsen.

Skjemaet for budsjettplanleggingskonfigurasjon for scenariet ser slik ut:

![Skjema for budsjettplanleggingskonfigurasjon.](./media/screenshot1-300x152.png)

Julie bruker følgende Excel-mal til å forberede budsjettet:

[![Excel-mal.](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>Øvelse 1: konfigurasjon

### <a name="task-1-create-organizational-hierarchy"></a>**Oppgave 1: opprette et organisasjonshierarki**
Siden hele budsjetteringsprosessen skjer i økonomiavdelingen, må Julie opprette et svært enkelt organisasjonshierarki som bare består av økonomiavdelingen. 

1.1. Naviger til organisasjonshierarkier (Organisasjonsstyring &gt; Organisasjoner &gt; Organisasjonshierarkier), og klikk Ny-knappen.

![Organisasjonshierarkier.](./media/screenshot3.png) 

1.2. Skriv inn navnet på organisasjonshierarkiet, og klikk knappen Tilordne formål i Navn-boksen.

1.3. Velg budsjettplanleggingsformålet, klikk Legg til, og tilordne det nylig opprettede organisasjonshierarkiet. 

[![Tilordne formål.](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Gjenta trinnet ovenfor for sikkerhetsorganisasjonsformålet. Lukk skjemaet når du er ferdig.

1.5. Klikk Vis-knappen i skjemaet Organisasjonshierarkier. Klikk Rediger i hierarkidesigneren, og opprett et hierarki ved å klikke Sett inn-knappen.

[![Sett inn.](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Velg Økonomiavdeling for budsjetteringshierarkiet. 

[![Finans.](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Når du er ferdig, klikker du knappen Publiser og lukk. Velg 01.01.2015 som ikrafttredelsesdato for publisering av hierarkiet.

[![Gyldighetsdato.](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>Oppgave 2: konfigurere brukersikkerhet
Budsjettplanlegging bruker spesielle sikkerhetspolicyer for å konfigurere tilgang til data for budsjettplaner. Julie må gi seg selv tilgang til budsjettplaner. 

2.1. Bytt til konteksten med den juridiske enheten. 


2.2. Gå til Budsjettering &gt; Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. I Parametere-fanen setter du Sikkerhetsmodell-verdien til Basert på sikkerhetsorganisasjoner. 

[![Parametere.](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Gå til Systemadministrasjon &gt; Brukere &gt; Brukere. Gi brukeren Admin (Julia Funderburk) rollen som budsjettleder. 

[![Budsjettbehandling.](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Velg brukerrolle, og klikk Tilordne organisasjoner. 

[![Tilordne organisasjoner.](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Velg Gi tilgang til bestemte organisasjoner. Velg organisasjonshierarkiet som ble opprettet i det første trinnet. Velg Finans-noden, og klikk Gi tilgang til underordnede. 

***Viktig!** _ _Sørg for at du er i konteksten med den juridiske enheten DEMF når du utfører denne oppgaven, siden organisasjonssikkerhet brukes per juridiske enhet* 

### <a name="task-3-create-scenarios"></a>Oppgave 3: opprette scenarier
3.1. Gå til Budsjettering&gt;Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. Legg merke til scenariene vi skal bruke videre i denne laben, på Scenarier-siden: Faktisk, forrige år og Budsjettert. 

*Obs! Hvis du vil, kan du opprette nye scenarier for denne øvelsen og bruke dem i stedet.* 

[![Nye scenarier.](./media/screenshot15.png)](./media/screenshot15.png) 

*Obs! Siden Julie ikke bruker formell godkjenningsprosess i budsjettforberedelsen, hopper vi over oppsett av arbeidsflyter, stadier og oppsett av arbeidsflytstadier i denne laben og bruker eksisterende oppsett for automatisk godkjenning av arbeidsflyt. Se i tillegget hvis du vil ha informasjon om denne arbeidsflytkonfigurasjonen.*

### <a name="task-4-create-budget-plan-columns"></a>Oppgave 4: opprette budsjettplankolonner
Budsjettplankolonner er enten monetære eller antallsbaserte kolonner som kan brukes i oppsett for budsjettplandokument. I vårt eksempel må vi opprette en kolonne for Faktisk, forrige år og 12 kolonner som skal representere hver måned i et budsjettert år. Kolonner kan opprettes ved ganske enkelt å klikke Legg til-knappen og fylle inn verdiene, eller ved hjelp av Dataenhet. Vi skal bruke Dataenhet til å fylle inn verdiene i denne laben. 

4.1. Åpne Kolonner-siden i Budsjettering&gt;Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. Klikk Office-knappen i øvre høyre hjørne i skjemaet, og velg Kolonner (ufiltrerte). 

[![Ufiltrerte kolonner.](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Systemet åpner en Excel-arbeidsbok som skal brukes til å fylle inn verdiene. Hvis du får spørsmål, klikker du Aktiver redigering og alternativet for å klarere denne appen. 

4.3. Vi trenger flere kolonner til å fylle ut verdiene. Klikk Utforming i ruten til høyre for å legge til kolonner i rutenettet. 

[![Utforming.](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klikk blyantknappen ved siden av PlanColumns for å se de tilgjengelige kolonnene som skal legges til i rutenettet. 

[![Rediger.](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Dobbeltklikk hvert tilgjengelige felt for å legge dem til i Valgte felt, og klikk Oppdater. 

4.6. Legg til alle kolonnene som skal opprettes, i Excel-tabellen. Bruk Autofyll-funksjonen i Excel til å legge til linjene raskt. Kontroller at linjene legges til som en del av tabellen (når du bruker loddrett rulling, skal du kunne se kolonneoverskrifter øverst i rutenettet). 

4.7. Gå tilbake til programmet, og oppdater siden. Publiserte verdier vises. 

[![Forny.](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>Oppgave 5: opprette oppsett og maler for budsjettplandokument
Oppsettet definerer hvordan rutenettlinjer blir seende ut i budsjettplandokumentet når brukere åpner budsjettplandokumentet. Det er også mulig å bytte oppsettet for budsjettplandokument for å se de samme dataene fra ulike vinkler. Nå som hun har kolonner definert for bruk med budsjettplandokumentet vårt, må Julie opprette et oppsett for budsjettplandokument som ligner på Excel-tabellen hun bruker til å lage budsjettdata (se delen Oversikt over scenariet i denne laben) 

5.1. Åpne Oppsett-siden i Budsjettering&gt;Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. Opprett et nytt oppsett for oppføringen for månedsbudsjett:

-   Velg dimensjonssettet MA+BU for å ta med hovedkontoer og forretningsenheter i oppsettet.
-   Vis alle budsjettplankolonner som ble opprettet i forrige trinn, i delen Elementer. Gjøre alle redigerbare, unntatt Faktisk, forrige år.
-   Klikk Beskrivelser-knappen for å velge hvilke finansdimensjoner som skal vise beskrivelser i rutenettet.

[![Beskrivelser.](./media/screenshot24.png)](./media/screenshot24.png) 

Basert på oppsettdefinisjonen for budsjettplan kan vi opprette en Excel-mal som skal brukes som en alternativ måte å redigere budsjettdata på. Siden Excel-malen må samsvare med oppsettdefinisjonen for budsjettplan, kan du ikke redigere oppsettet for budsjettplanen etter at du har generert Excel-malen. Derfor må du gjøre denne oppgaven etter at alle oppsettkomponenter er definert. 

5.2. For oppsettet som er opprettet i trinn 5.1. , klikker du knappen Mal &gt; Generer. Bekreft advarselen. Klikk Mal &gt; Vis for å vise malen. 

*Obs! Pass på at du velger Lagre som, og velg hvor malen skal lagres, slik at du kan redigere den. Hvis brukeren velger Åpne i dialogboksen uten å lagre, beholdes ikke endringene i filen når filen lukkes.* 
[![Malvisning.](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valgfritt trinn&gt; Endre Excel-malen slik at den ser mer brukervennlig ut. Legg til totalformler, overskriftsfelt, formatering og så videre. Lagre endringene, og last opp filen til budsjettplanoppsettet ved å klikke Oppsett &gt; Last opp. 


### <a name="task-6-create-a-budget-planning-process"></a>Oppgave 6: opprette en budsjettplanleggingsprosess
Julie må opprette og aktivere en ny budsjettplanleggingsprosess der hele oppsettet ovenfor kombineres, for å begynne å registrere budsjettplaner. Budsjettplanleggingsprosessen definerer hvilke budsjetteringsorganisasjoner, arbeidsflyter, oppsett og maler som skal brukes til å opprette budsjettplaner. 

6.1. Gå til Budsjettering &gt; Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingsprosess, og opprett en ny post.

-   Budsjettplanleggingsprosess – DEMF budgeting FY2016
-   Budsjettsyklus – FY2016
-   Finans – DEMF
-   Standard kontostruktur – Manufacturing P&L
-   Organisasjonshierarki – velg hierarkiet som ble opprettet i begynnelsen av laben
-   Arbeidsflyt for budsjettplanlegging – tilordne automatisk godkjenning av arbeidsflyt for økonomiavdelingen
-   I stadieregler og maler for budsjettplanlegging velger du om det er tillatt å legge til linjer og å endre linjer og hvilket oppsett som skal brukes som standard, for hvert arbeidsflytstadium for budsjettplanlegging.

*Obs! Du kan opprette flere dokumentoppsett og tilordne dem slik at de er tilgjengelige på arbeidsflytstadiet for budsjettplanlegging, ved å klikke knappen Alternative oppsett.* 

[![Alternative oppsett.](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Velg Handlinger &gt; Aktiver for å aktivere denne arbeidsflyten for budsjettplanlegging. 

[![Aktiver.](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>Øvelse 2: prosessimulering

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>Oppgave 7: generere innledende data for budsjettplan fra Økonomimodul
7.1. Gå til Budsjettering &gt; Periodisk &gt; Generer budsjettplan fra økonomimodul. Fyll ut parameterne for periodisk prosess, og klikk Generer. 

7.2. Gå til Budsjettering &gt; Budsjettplaner for å finne en budsjettplan som er opprettet av genereringsprosessen. 

[![Budsjettplan.](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Åpne dokumentdetaljene ved å klikke dokumentnummerhyperkoblingen. Budsjettplan vises som definert i oppsettet som ble opprettet i denne laben. 

[![Visning av budsjettplan.](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>Oppgave 8: opprette budsjett for gjeldende år basert på fjorårets faktiske data
Tildelingsmetoder kan brukes i budsjettplaner til å kopiere informasjon for budsjettplaner fra ett scenario til et annet, spre dem på tvers av perioder, eller tildele dem til dimensjoner. Vi skal bruke tildelinger til å opprette budsjett for gjeldende år fra fjoråret faktiske data. 

8.1. Velg alle linjene i rutenettet for budsjettplandokument, og klikk knappen for å tildele budsjett. 

[![Alle linjer.](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Velg tildelingsmetode, periodenøkkel, kilde- og målscenarier, og klikk Tildel. 

[![Tildel.](./media/screenshot33.png)](./media/screenshot33.png)

Systemet kopierer fjorårets faktiske beløp til budsjettet for gjeldende år, og fordeler dem på tvers av periodene ved hjelp av periodenøkkelen for salgskurve. 

[![Salgskurve.](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>Oppgave 9: justere budsjettplandokument ved hjelp av Excel og gjøre ferdig dokumentet
9.1. Klikk knappen for regnearket for å åpne dokumentinnholdet i Excel.

9.2. Når Excel-arbeidsboken åpnes, justerer du tallene i budsjettplandokument og klikker Publiser.

9.3. Gå tilbake til budsjettplandokumentet. Klikk Arbeidsflyt &gt; Send inn for å godkjenne dokumentet automatisk.

[![Godkjenn automatisk.](./media/screenshot37.png)](./media/screenshot37.png) 

Når arbeidsflyten er fullført, endres stadiet for budsjettplandokument til godkjent. [![Godkjent.](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Tillegg

### <a name="auto-approve-workflow-configuration"></a>Konfigurasjon av automatisk godkjenning av arbeidsflyt

A. Budsjettering &gt; Oppsett &gt; Budsjettplanlegging &gt; Budsjetteringsarbeidsflyter. Opprett en ny arbeidsflyt med malen Arbeidsflyter for budsjettplanlegging:

[![Opprette en ny arbeidsflyt.](./media/screenshot39.png)](./media/screenshot39.png)

Denne arbeidsflyten inneholder bare én oppgave – Faseovergang for budsjettplan. 

[![Faseovergang for budsjettplan.](./media/screenshot40.png)](./media/screenshot40.png) 

Lagre og aktiver arbeidsflyten. 

B. Gå til Budsjettering &gt; Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. Opprett to stadier i Stadier-fanen – Innledende og Sendt. 

[![Opprinnelig og sendt.](./media/screenshot41.png)](./media/screenshot41.png)

C. Gå til Budsjettering &gt; Oppsett &gt; Budsjettplanlegging &gt; Budsjettplanleggingskonfigurasjon. I Arbeidsflytstadier-fanen knytter du arbeidsflyten for automatisk godkjenning som ble opprettet i trinn A, til stadiene Innledende og Sendt.

[![Budsjettering og budsjettplanlegging.](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
