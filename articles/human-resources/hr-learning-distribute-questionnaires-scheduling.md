---
title: Distribuere spørreskjemaer ved hjelp av planlegging
description: Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0448a7ebe802a961c8c1296ef57d12ea22e4ec27
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010095"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Distribuere spørreskjemaer ved hjelp av planlegging

Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

## <a name="create-a-questionnaire-schedule"></a>Opprette en spørreskjemaplan

1. Gå til Spørreskjema > Distribuer > Spørreskjemaplaner.

2. Klikk Ny.

3. Skriv inn en verdi i feltet Planlegging.

4. Skriv inn en verdi i feltet Beskrivelse.
    * Sett planen til anonym hvis svarene skal registreres uten navn tilknyttet svaret.  
    * Tillatelse av anonyme resultater må først defineres i parameterne for personal.  

5. I Type-feltet velger du planleggingstypen.  I dette eksemplet bruker vi tilfredshetstypen.

6. Finn og velg ønsket post i listen.

7. Klikk koblingen i den valgte raden i listen.

8. Angi en dato i Dato-feltet.

9. Vis E-post for ansattselvbetjening-delen.

10. Skriv inn en verdi i Emne-feltet.

    * Eksempel: Spørreskjema tilgjengelig  

11. I Tekst-feltet skriver du inn brødteksten i e-postmeldingen. Legg merke til at variabelen kan brukes til å erstatte verdier i systemet.

    * Eksempel: Kjære %P%! Logg på Ansattselvbetjening for å fylle ut spørreskjemaet om ansattes helse.  Contoso  

12. Klikk Lagre.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Bruk oppsettsdetaljene til å velge spørreskjemaet/spørreskjemaene som skal besvares, i tillegg til eventuelle spørringer som skal brukes til å velge respondenter.

1. Klikk Oppsettsdetaljer.

2. Velg en spørring som skal brukes for å søke etter respondenter for spørreskjemaet.

    * Eksempel: Arbeidere  

3. Klikk Vis eller endre spørring for å velge bestemte personer eller endre spørringen for å finne personer som oppfyller bestemte vilkår.

    * Vær oppmerksom på at alle respondenter må også være brukere i systemet.  

4. Merk raden for Person i listen.

5. Angi eller velg en verdi i Kriterier-feltet.

    * Velg Julie Funderburk  

6. Velg Julia Funderburk i listen.

7. Klikk OK.

8. Klikk kategorien Spørreskjemaer.

9. I treet utvider du "the node for the questionnaire type Satisfaction Survey".

10. Merk av for Workforce Health Assessment.

11. Klikk OK.

12. Klikk Planlagt svarøkt.

    * Legg merke til at planlagte svarøkter er opprettet for hver bruker som er valgt/spørres.  

13. Lukk siden.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Start spørreskjemaplanen for å gjøre spørreskjemaet tilgjengelig for respondentene.

1. Klikk Funksjoner.

2. Klikk Start.

3. Klikk OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Send e-post for å varsle svarpersoner om at spørreskjemaet er tilgjengelig.

1. Klikk Funksjoner.

2. Klikk Send e-post.

3. Klikk Avbryt.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Bruk planlagte svarøkter til å følge med på hvem som må fylle ut spørreskjemaet.

1. Klikk Planlagt svarøkt.

    * Slett eventuelle gjenværende planlagte svarøkter når du er klar til å avslutte den planlagte økten.  

2. Klikk Slett.

3. Klikk Ja.

4. Lukk siden.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Avslutt planleggingen når alle respondentene har fullført spørreskjemaet og /eller alle gjenstående planlagte svarøkter er slettet.

1. Klikk Funksjoner.
2. Klikk Avslutt.
3. Klikk OK.

