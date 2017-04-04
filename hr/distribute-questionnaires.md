---
title: "Distribuere og fylle ut et spørreskjema"
description: "Dette emnet forklarer hvordan fordele spørreskjemaer som du utformer, slik at de er tilgjengelige for personen eller gruppen av personer som fullfører dem.."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Distribuere og fylle ut et spørreskjema

Dette emnet forklarer hvordan fordele spørreskjemaer som du utformer, slik at de er tilgjengelige for personen eller gruppen av personer som fullfører dem.. 

Et spørreskjema kan distribueres på flere ulike måter:

-   Merk spørreskjemaet som aktivt. Spørreskjemaet blir dermed tilgjengelig for alle ansatte, med mindre en spørreskjemagruppe er konfigurert slik at tilgangen til den er begrenset.
-   Tilordne rettigheter til en spørreskjemagruppe. Spørreskjemaet blir dermed tilgjengelig for alle medlemmer av den valgte gruppen.
-   Opprett planlagte svarøkter. Spørreskjemaet blir dermed tilgjengelig bare for en bestemt person.
-   Opprett en tidsplan. Spørreskjemaet kan dermed bli tilgjengelig for flere personer.

## <a name="marking-a-questionnaire-as-active"></a>Merke et spørreskjemaet som aktivt
Ved å angi den **aktive** feltet til **Ja** på den **spørreskjemaer** siden du gjøre spørreskjemaet tilgjengelig for alle ansatte til å fullføre. Svarpersoner kan fylle ut spørreskjemaet flere ganger. Denne funksjonen er nyttig hvis du vil samle inn kontinuerlig tilbakemelding i løpet av året. Du kan for eksempel lage et spørreskjema som ansatte bruker til å gi tilbakemelding om lunsjtjenesten i kaféen.

## <a name="questionnaire-groups"></a>Spørreskjemagrupper
Du kan definere spørreskjemagrupper og deretter inkludere respondenter som et spørreskjema skal distribueres til. 

Du kan opprette spørreskjemagrupper fra følgende sider:

-   **Spørreskjemagrupper **– Bare personer i en spørreskjemagruppe kan fylle ut et valgt spørreskjema. La oss si at den planlagte målgruppen for eksempel er leverandører, så du oppretter en spørreskjemagruppe som er spesifikk for disse respondentene.
-   **Medlemmer av spørreskjemagruppe** – Du kan legge til personer i spørreskjemagruppene.

Slik tilordner du en spørreskjema-gruppe til et spørreskjema på den **spørreskjemaer** klikker du **brukerrettigheter**. Når spørreskjemaet er lagret som aktiv, kan medlemmer av spørreskjemagruppen fylle ut spørreskjemaet. Denne funksjonen er nyttig hvis du vil teste et spørreskjema i en utvalgt gruppe av personer før du ruller i en større gruppe, eller hvis du vil utforme et spørreskjema til en bestemt målgruppe.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Planlagte svarøkter i et spørreskjema
Planlagte svarøkter er spørreskjemaer du har utformet og valgt respondentene for. 

**Obs! ** Før du kan definere planlagte svarøkter, må du utforme et spørreskjema. 

Du kan opprette en planlagt svarøkt for én ansatt på siden **Planlagt svarøkt**. Listen på siden viser alle planlagte spørreskjemaer. 

Planlagte svarøkter brukes også på siden **Spørreskjemaplaner**, der du kan planlegge spørreskjemaer for flere personer:

-   Ansatte
-   Kursdeltakere
-   Organisasjonsenheter

Hver person kan svare på spørreskjemaet bare én gang.

## <a name="scheduling-a-questionnaire"></a>Planlegge et spørreskjema
Du kan velge om du vil planlegge et spørreskjema for flere respondenter.

### <a name="planning-types"></a>Planleggingstyper

Planleggingstyper er nødvendige hvis du vil planlegge planlagte svarøkter for flere respondenter. Planleggingstyper brukes til å klassifisere spørreskjemaplaner. Du kan for eksempel planlegge spørreskjemaer for følgende formål:

-   Evaluering
-   Undersøkelse
-   Testing

Du kan angi planleggingstyper for en spørreskjemaplan på siden **Spørreskjemaplaner**.

### <a name="reference-types-for-questionnaire"></a>Referansetyper for spørreskjema

Du kan bruke referansetyper til å angi kriterier for respondentene du kanskje velger når du planlegger et spørreskjema. 

Bruk **Referansetyper**-siden til å definere referansetyper for et spørreskjema. Hver referansetype tilsvarer en tabell i Microsoft Dynamics 365 for operasjoner. Når du oppretter spørreskjemaplaner, kan du angi enkeltposter i tabellen eller et utvalg av poster som spørreskjemaet skal knyttes til. 

Hvis du for eksempel velger Kurs-tabellen, kan du bestemme det bestemte kurset spørreskjemaet skal være for. Når du definerer en referanse til Kurs-tabellen, blir enkelte felt og knapper på **Kurs**-siden tilgjengelige.

### <a name="questionnaire-schedules"></a>Spørreskjemaplaner

Du kan bruke spørreskjemaplaner til å generere flere planlagte svarøkter for en gruppe av brukere, basert på en referansetype. Opprette en plan på det **spørreskjemaplaner** siden. Velg plantypen til å kategorisere tidsplanen, og også velge hvilken type som skal brukes til å spørre systemet for bestemte brukere. Hvis du angir referansetypen i kurs-tabellen, kan du for eksempel velge et bestemt kurs i den **referanse** feltet. 

Klikk **Oppsettsdetaljer** for å velge spørreskjemaet og andre kriterier. For eksempel angi at instruktøren navn som et kriterium Hvis spørreskjemaet er en evaluering av instruktøren. Når du er ferdig med å skrive inn setup detaljene, vil systemet genererer planlagte svarøkter for brukerne som er inkludert i spørringen. 

Klikk **Planlagte svarøkter** for å vise svarøkter for tidsplanen. Du kan deretter manuelt opprette flere planlagte svarøkter eller slette planlagte svarøkter som ikke er besvart. 

Klikk **funksjoner**&gt;**Start** å gjøre spørreskjemaet tilgjengelig for brukerne i relaterte planlagte svarøkter. Klikk **Svar** for å vise de fullførte svarene på spørreskjemaet. Du kan eventuelt kopiere innstillingene for spørreskjemaplan, planlagte svarøkter og svar på en ny spørreskjemaplan.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Varsle respondenter om spørreskjemaer som er tilgjengelige for dem
Når du distribuerer et spørreskjema, må du varsle respondentene om at spørreskjemaet er tilgjengelige for dem. 

**Merk:** respondentene må være brukere i Microsoft Dynamics 365 for operasjoner for å fylle ut et spørreskjema.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Varsle respondenter om en planlagt svarøkt

Hvis du bruker en planlagt svarøkt, må du varsle personen direkte, for eksempel via telefon eller e-post.

### <a name="notifying-respondents-about-a-scheduling"></a>Varsle respondenter om en planlegging

Bruk siden **Spørreskjemaplaner** til å klargjøre og sende e-post til alle respondenter som er tilordnet spørreskjemaet. Skriv inn e-postteksten i fanen **E-post for ansattselvbetjening**. Når planen er startet, klikker du **funksjoner**&gt;**Send e-post** til å generere og sende e-postmeldingen til deltakerne. Svarpersoner kan deretter logge deg på webområdet og fylle ut spørreskjemaet. 

**Obs! ** Før du kan bruke e-postfunksjonaliteten, må IT-administratoren angi e-postinnstillingene på siden **E-postparametere**.

## <a name="ending-a-scheduled-questionnaire"></a>Avslutte et planlagt spørreskjema
Du kan avslutte et planlagt spørreskjema når alle respondentene har fullført sin svarøkt. Når et planlagt spørreskjema er avsluttet, kan du ikke kopiere innstillingene til en ny plan. 

**Obs! ** If én eller flere respondenter ikke har fylt ut spørreskjemaet, men du likevel vil avslutte planleggingen, må du først slette disse respondentene fra listen, på siden **Planlagt svarøkt**. Du kan deretter avslutte tidsplanen.

## <a name="completing-questionnaires"></a>Fylle ut spørreskjemaer
Når du har utformet og distribuert et spørreskjema, kan spørreskjemaet fylles ut av valgte respondenter. Du kan fylle ut spørreskjemaene som er tilgjengelige for deg fra to steder:

-   I navigasjonsruten klikker du **spørreskjemaer**&gt;**fordel**&gt;**fylle ut et spørreskjema**.
-   I Ansattselvbetjening klikker du **Spørreskjemaer som skal fullføres**.

Spørreskjemaer kan gjøres tilgjengelige for bestemte brukere eller brukergrupper eller alle brukere i et nettverk.

<a name="see-also"></a>Se også
--------

[Utforme spørreskjemaer](design-questionnaires.md)

[Bruke spørreskjemaer](questionnaires.md)

[Vise og evaluere resultatene for spørreskjemaer](evaluate-questionnaire-results.md)


