---
title: Formalisere forretningsprosesser
description: "Med forretningsprosessfunksjonen kan du opprette en mal for forretningsprosessen for prosesser som må fullføres internt i organisasjonen."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: nb-no
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Formalisere forretningsprosesser
Med forretningsprosessfunksjonen kan du opprette en mal for forretningsprosessen for prosesser som må fullføres internt i organisasjonen. Firmaet kan for eksempel ikke fullføre en personalkontroll hvert år. Du kan opprette en mal for å spore alle oppgavene som består av overvåkingen for å sikre at alle oppgavene som utføres hver gang prosessen er fullført, og hvis det er nødvendig for å sikre at oppgaver utføres i riktig rekkefølge. Maler kan brukes på nytt for regelmessige prosesser, eller kopieres hvis du vil bruke dem som utgangspunkt for å opprette nye.

Når du oppretter en mal, kan en prosess startes og spores i arbeidsområdet Forretningsprosess.  Når du starter en forretningsprosess, blir oppgavene tilordnet til de rette personene og vil inkludere en forfallsdato. Vi beskriver disse komponentene mer detaljert nedenfor.

## <a name="business-process-template"></a>Forretningsprosessmal
En forretningsprosessmal viser en gruppe oppgaver som utgjør en forretningsprosess. Personalledere og -assistenter kan opprette forretningsprosesser som standard.  Men kan imidlertid endres i sikkerhetskonfigurasjonen ved å redigere plikten Vedlikehold generelle forretningsprosesser.

En prosesseier kan defineres for hver prosess.  Prosesseieren vil ha oversikt over alle oppgavene for prosessen, og han/hun kan tildele oppgaver på nytt eller endre forfallsdatoer for fakturaer.  Personaldirektøren kan for eksempel opprette en forretningsprosessmal for gjennomgang av fordeler.  Lederen for kompensasjon og fordeler kan defineres som prosesseieren, slik at han eller hun kan få innsikt i oppgavene som må fullføres som en del av gjennomgangen.  En prosesseier kan ikke opprette eller slette aktive forretningsprosesser eller forretningsmaler for prosessen.

## <a name="task"></a>Oppgave
En forretningsprosess består ofte av flere oppgaver. Noen oppgaver kan fullføres i Dynamics 365 for Talent[?], for eksempel som gjennomgang av interne kurstilbud. I slike tilfeller vil et menyelement velges i feltet Oppgavekobling. Andre oppgaver kan omfatte gjennomgang eller utfylling av skjemaer på et nettsted. Ved å velge URL-adressen i feltet Oppgavekobling, kan webadressen angis. Du kan angi URL-adresser for både eksterne og interne nettsteder i dette feltet. Du kan også opprette oppgaver for oppgaver som du har fullført manuelt, for eksempel å gå gjennom tilgjengeligheten av alle strukturer. I dette tilfellet kreves det ikke en oppgavekobling. Med denne fleksibiliteten kan du spore flere typer oppgaver i en omfattende prosess.

Oppgaver kan tilordnes til en bestemt arbeider eller til en stilling. Lederen for kompensasjon og fordeler vil for eksempel alltid være personen som utfører en evaluering av forsikringspremier.   Når du oppretter denne oppgaven, velger du stillingen for tilordningstypen, og deretter velger du lederen for kompensasjon og fordeler fra listen over stillinger. Når prosessen starter opp, tilordnes oppgaven til arbeideren som har stillingen som leder for kompensasjon og fordeler. Du kan også tilordne en oppgave til en bestemt arbeider ved å velge Arbeider i feltet Tilordningstype, og deretter velger du den aktuelle personen.

Forfallsdatoer for oppgave avhenger av måldatoen som er angitt i begynnelsen av prosessen. Noen oppgaver må fullføres innen måldatoen, og noen kan fullføres etter måldatoen.  Når du definerer en oppgave, angir du en forfallsdato som står i forhold til måldatoen i feltet Forfallsdato samsvarer ikke med måldato. La oss si at lederen for kompensasjon og fordeler for eksempel må utføre en evaluering av forsikringsbonuser 10 dager før personalkontrollen er fullført. Den opprettede oppgaven vil ha en forfallsdato i forhold til måldatoen på -10. Hvis prosessen starter 13 mai., har oppgaven dermed forfall 3. mai. Merk: Forfallsdato kan også endres etter at prosessen er startet.

Kompliserte oppgaver kan kreve flere trinn, eller krever at enkeltpersonen utfører oppgavene for å formidle tilleggsinformasjon. Du kan legge til instruksjoner for oppgaven, og du kan også inkludere formatering av rik tekst for instruksjonene. Instruksjonene kan gir ytterligere informasjon om hvordan du fullfører oppgaven til personen som er tilordnet til å fullføre den.

Starte en prosess. En prosess kan startes i en forretningsprosessmal ved å velge Start prosess.  Når en prosess er startet, opprettes det oppgaver for de valgte arbeiderne og/eller stillingene som er definert i oppgavene som er inkludert i forretningsprosessmalen. En forfallsdato blir også tilordnet til hver oppgave ved å legge til eller trekke fra forskyvningsdagene fra måldatoen (se opplysninger om forskyvningsdager i oppgavedelen). Du kan vise aktive forretningsprosesser i arbeidsområdet Forretningsprosesser. 

## <a name="employee-self-service"></a>Ansattselvbetjening
Når en oppgave er tilordnet til en ansatt, vises den ansattes tildelte oppgaver på siden Ansattselvbetjening. Ansatte som har tilordnet en forretningsprosessoppgave, kan vise oppgaven, dens beskrivelse, instruksjoner for å fullføre, og navnet på kontaktpersonen. I tillegg kan vedkommende åpne den tilknyttede Dynamics365-siden eller -nettsiden fra sin egen Ansattselvbetjening-side. Oppgaver kan være merket som Pågår, Avbrutt eller Fullført.

## <a name="business-process-workspace"></a>Arbeidsområdet Forretningsprosess
Personaleksperter kan vise de aktive forretningsprosessene fra arbeidsområdet Forretningsprosess. Arbeidsområdet viser alle aktive prosesser og oppgavene som er knyttet til hver av dem. Den omfattende oppgavelisten kan filtreres etter forfallsdato. Siden viser også forfalte oppgaver og oppgaver som er spesifikt tilordnet til personaleksperter. Statusen for alle oppgaver kan også oppdateres, og om nødvendig kan oppgaver tilordnes på nytt slik at den generelle forretningsprosessen har fremdrift.

## <a name="my-business-processes-workspace"></a>Arbeidsområdet Mine forretningsprosesser
Prosesseiere kan vise de aktive forretningsprosessene som er tilordnet til dem fra arbeidsområdet Min forretningsprosess. Arbeidsområdet viser alle aktive prosesser og tilknyttede oppgaver som den brukeren eier.  Den omfattende oppgavelisten kan filtreres etter forfallsdato. Siden inneholder også oppgaver som er spesifikt tilordnet til prosesseieren. Prosesseieren kan også oppdatere statusen for alle oppgaver, i tillegg til å tilordne oppgaver på nytt.

## <a name="navigating-business-processes"></a>Flytte rundt i forretningsprosesser
1.   Hvis du vil legge til forretningsprosessmalen, går du til Forretningsprosesser, koblinger – Administrasjon for forretningsprosesser.
 - a.   Ny vil opprette en ny mal.
 - b.   Kopier fra mal vil kopiere den valgte malen til en ny mal.
 - c.   Start prosessen vil starte den valgte forretningsprosessen, tilordne oppgaver og beregne forfallsdatoer.  
2.  Hvis du vil vise aktive prosesser og tilknyttede oppgaver, går du til arbeidsområdet Forretningsprosesser.

