---
title: Oppgaveopptaker og hjelp for salgssted
description: Dette emnet beskriver hvordan du bruker oppgaveopptaker i moderne salgssted for detaljhandel og skysalgssted.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: 41
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 007a7e8a34f3f5a2d0d18eb3955822a8fd8bdd0a
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Oppgaveopptaker og hjelp for salgssted
<a id="task-recorder-and-help-for-pos" class="xliff"></a>

Dette emnet beskriver hvordan du bruker oppgaveopptaker i moderne salgssted for detaljhandel og skysalgssted.

Oversikt
<a id="overview" class="xliff"></a>
--------

Oppgaveopptaker i moderne salgssted for detaljhandel og skysalgssted er en ny løsning som ble bygd med fokus på høy hastighet. Den gir et fleksibelt Application Program Interface (API) for fleksibilitet og sømløs integrasjon med forbrukere av forretningsprosessregistreringer. I tillegg er Oppgaveopptak-integrasjon med verktøyet Forretningsprosessmodelerer (BPM) på Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) implementert. Derfor kan brukere fortsette å produsere rike forretningsprosessdiagrammer fra opptak for å analysere og utforme programmene.

## Arkitektur
<a id="architecture" class="xliff"></a>
Oppgaveopptaker kan registrere brukerhandlinger i klienten med nøyaktig gjengivelse. Hver kontroll er utstyrt for å varsle Oppgaveopptaker om utførelsen av en handling. Kontrollen varsler Oppgaveopptaker om at en hendelse oppstod og sender all relevant informasjon om den aktuelle brukerhandlingen i sanntid. Ved hjelp av denne informasjonen kan Oppgaveregistrering registrere typen brukerhandling (for eksempel en knapp klikkes, verdiregistrering eller navigasjon) og eventuelle data som er knyttet til handlingen (for eksempel inndataverdien og typen, skjemakontekst eller postkontekst). Oppgaveopptaker behandler informasjonen detaljert nok til å sikre at en avspilling av opptaket kan utføre de registrerte handlingene nøyaktig slik brukeren har utført dem. (Avspillingsfunksjonen er ennå ikke implementert i Moderne salgssted for detaljhandel eller Skybasert salgssted.)

## Grunnleggende konfigurasjon
<a id="basic-configuration" class="xliff"></a>
Følg disse trinnene for å aktivere oppgaveopptak på salgssted.

1.  Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.
2.  Klikk kassen for å aktivere oppgaveopptak.
3.  I kategorien **Register** i hurtigfanen **Generelt** angir du alternativet **Aktiver oppgaveregistrering** til **Ja**.
4.  Klikk **Lagre**.
5.  Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
6.  Velg jobben **Kasser (1090)**, og klikk deretter **Kjør nå**.

## Opprett et opptak
<a id="create-a-recording" class="xliff"></a>
Følg denne fremgangsmåten for å opprette en ny registrering ved hjelp av oppgaveopptaker.

1.  Start moderne salgssted for detaljhandel og skysalgssted, og logg på.
2.  På **Innstillinger**-siden, i delen **Oppgaveopptaker**, klikker du **Åpne Oppgaveregistrering**. Ruten **Oppgaveopptaker** vises. Du kan klikke **Lukk**-knappen (**X**) i øvre høyre hjørne for å lukke ruten **Oppgaveopptaker** før du begynner et nytt opptak. For å åpne ruten igjen gjentar du trinn 2.
[![Rute for oppgaveopptaker](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Skriv inn et navn på og en beskrivelse av opptaket, og klikk deretter **Start**. Opptaksøkten begynner når du klikker **Start**.

**Merk:** Hvis du klikker **Lukk**-knappen (**X**) i øvre høyre hjørne når et opptak pågår, lukkes ruten **Oppgaveopptak**, men opptaksøkten avsluttes ikke. For å åpne ruten for oppgaveopptaker på nytt kan du klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen. 

[![Spørsmålstegn](./media/help.jpg)](./media/help.jpg)

4.  Når du har klikket **Start**, går oppgaveopptak inn i opptaksmodus. Ruten for **oppgaveopptak** viser informasjon og kontroller som er knyttet til opptaksprosessen.
5.  Utfør handlingene du vil utføre i grensesnittet for moderne salgssted for detaljhandel og skysalgssted.
6.  Klikk **Stopp** for å avslutte opptaksøkten.

## Nedlastingsalternativer
<a id="download-options" class="xliff"></a>
Når du har avsluttet opptaksøkten, vises flere alternativer, slik at du kan laste ned opptaket. 
[![Nedlastingsalternativer](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### Lagre på denne PC-en
<a id="save-to-this-pc" class="xliff"></a>

Du kan bruke opptakspakken til å spille av en oppgaveveiledning, vedlikeholde opptaket eller redigere merknader i opptaket. (Denne funksjonen er ennå ikke implementert i Moderne salgssted for detaljhandel eller Skybasert salgssted.)

### Eksporter som Word-dokument
<a id="export-as-word-document" class="xliff"></a>

Du kan lagre opptaket som et Microsoft Word-dokument. Dokumentet inneholder trinnene du har tatt opp samt skjermbilder som er tatt.

### Lagre som utvikleropptak
<a id="save-as-developer-recording" class="xliff"></a>

Rå opptaksfilen er nyttig for utviklerscenarioer, for eksempel generering av testkode. (Denne funksjonen er ikke implementert ennå.)

## Opptakskontroller
<a id="recording-controls" class="xliff"></a>
### [![Opptakskontroller](./media/controls.jpg)](./media/controls.jpg)
<a id="recording-controlsmediacontrolsjpgmediacontrolsjpg" class="xliff"></a>

### Stopp
<a id="stop" class="xliff"></a>

Klikk **Stopp** for å avslutte opptaksøkten. Vær oppmerksom på at du ikke kan starte en økt på nytt når du har avsluttet den. Derfor må du sørge for at opptaket er fullført før det avsluttes.

### Stans midlertidig
<a id="pause" class="xliff"></a>

Klikk **Stans midlertidig** for å stanse opptaksøkten midlertidig og fortsette med operasjonen. Trinnene du utfører når du har klikket **Stans midlertidig**, tas ikke opp.

### Fortsett
<a id="continue" class="xliff"></a>

For å gjenoppta opptaksøkten når du har stanset midlertid, klikker du **Fortsett**.

### Ta skjermbilder
<a id="capture-screenshots" class="xliff"></a>

Oppgaveopptaker kan ta skjermbilder av brukergrensesnittet for Moderne salgssted for detaljhandel mens du tar opp en forretningsprosess. Oppgaveopptak bruker skjermbildene hvis du laster ned opptaket som et Word-dokument. Hvis du vil aktivere opptaksfunksjonen for skjermbilde, kan du angi **Ta skjermbilder** til **Ja**. 

#### Merk
<a id="note" class="xliff"></a>
> Funksjonen for å ta skjermbilder støttes ikke i skysalgssted.

### Start oppgave og avslutt oppgave
<a id="start-task-and-end-task" class="xliff"></a>

Du kan angi begynnelsen og slutten av et sett med grupperte trinn ved hjelp av knappene **Start oppgave** og **Avslutt** **oppgave**. Klikk **Start oppgave** for å legge til et "Start oppgave"-trinn, og utfør deretter trinnene som skal tas med i gruppen. Når du er ferdig med å utføre trinnene for gruppen, klikker du **Avslutt oppgave**. Oppgavene hjelper deg med å organisere dine prosedyrer. Oppgaver kan nestes i andre oppgaver. På denne måten kan du organisere svært lange og kompliserte forretningsprosesser bedre.

## Å legge til merknader
<a id="adding-annotations" class="xliff"></a>
En merknad er tilleggstekst du legger til et trinn i en registrering. Du kan for eksempel bruke merknader til å gi brukeren mer kontekst eller instruksjoner. Du kan legge til merknader før eller etter et trinn. Du kan legge til en merknad til et hvilket som helst trinn ved å klikke knappen **Rediger** (blyantsymbol) til høyre for trinnet. 

[![Rediger-knappen for et trinn](./media/annotate.jpg)](./media/annotate.jpg)

### Tekster og merknader
<a id="texts-and-notes" class="xliff"></a>

Du kan bruke feltene **Tekster** og **Merknader** til å legge til tekst som skal knyttes til et trinn i en oppgaveveiledning.
[![Tekst og merknader-felt](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### Tekst
<a id="text" class="xliff"></a>

Teksten du skriver inn i **Tekst**-feltet, vises *over* trinnteksten i oppgaveveiledningen. Denne plasseringen er egnet for tekst som du vil at brukeren leser før han eller hun fullfører trinnet.

#### Notater
<a id="notes" class="xliff"></a>

Teksten du skriver inn i **Merknader**-feltet, vises *under* trinnteksten i oppgaveveiledningen. Hvis brukeren skal lese merknadsteksten, må han/hun utvide trinnteksten i popup-vinduet. Denne plasseringen er egnet for valgfritt lesemateriale eller annen informasjon som kan være nyttig for brukeren, men som brukeren ikke trenger for å fullføre handlingen.

## Hjelp i moderne salgssted for detaljhandel og skysalgssted
<a id="help-in-retail-modern-pos-and-cloud-pos" class="xliff"></a>
Hvis du vil vise dine egne oppgaveopptak i Hjelp-ruten i moderne salgssted for detaljhandel og skysalgssted, slik at de kan vises som tekst, må du lagre oppgaveopptakene i ditt eget Forretningsprosessmodeler-bibliotek og deretter oppdatere hjelpesystemparameterne slik at de peker mot Forretningsprosessmodeler-biblioteket ditt. Hvis du vil ha mer informasjon, kan du se [Connecting the help system](/dynamics365/unified-operations/dev-itpro/get-started/help-connect). Hjelp for moderne salgssted for detaljhandel og skysalgssted søker i LCS i sanntid. Den søker gjennom alle BPM-biblioteker som er valgt i hjelpesystemparametere for Microsoft Dynamics 365 for Retail, og viser de relevante resultatene. Du kan åpne **Hjelp**-menyen ved å klikke **Hjelp**-knappen (spørsmålstegn) øverst på skjermen og deretter skrive inn prosessnavnet ditt i søkeboksen og klikke på søkeknappen. 

[![Hjelp-knappen](./media/help.jpg)](./media/help.jpg) 

Når du klikker en oppgaveveiledning i søkeresultatene, kan du se trinnene som et hjelpeemne eller eksportere trinnene til et Word-dokument. 
#### Merk
<a id="note" class="xliff"></a>
> Hjelp i moderne salgssted for detaljhandel Cloud POS henter ikke frem oppgaveveiledninger i henhold til hvilket skjema du bruker eller hva du holder på med. Du må skrive inn prosessnavnet i søkeboksen, og deretter klikke **Søk**.


