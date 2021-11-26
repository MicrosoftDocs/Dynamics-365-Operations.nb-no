---
title: Distribuere spørreskjemaer ved hjelp av planlegging
description: Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2336cafe7e2c914c2592c91c888b1e0ae1bc608
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728682"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Distribuere spørreskjemaer ved hjelp av planlegging

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med planlegging av spørreskjema kan du planlegge og distribuere spørreskjemaer til flere respondenter. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

## <a name="create-a-questionnaire-schedule"></a>Opprette en spørreskjemaplan

1. Gå til **Spørreskjema** > **Distribuer** > **Spørreskjemaplaner**.

2. Klikk på **Ny**.

3. Skriv inn en verdi i feltet **Planlegging**.

4. Skriv inn en verdi i **Beskrivelse**-feltet.
    * Sett planen til **Anonym** hvis svarene skal registreres uten navn tilknyttet svaret.  
    * Tillatelse av anonyme resultater må først defineres i parameterne for personal.  

5. I **Type**-feltet velger du planleggingstypen.  I dette eksemplet bruker vi **tilfredshetstypen**.

6. Finn og velg ønsket post i listen.

7. Klikk koblingen i den valgte raden i listen.

8. Angi en dato i **Dato**-feltet.

9. Vis delen **E-post for ansattselvbetjening**.

10. Skriv inn en verdi i **Emne**-feltet.

    * Eksempel: Spørreskjema tilgjengelig  

11. I **Tekst**-feltet skriver du inn brødteksten i e-postmeldingen. Legg merke til at variabelen kan brukes til å erstatte verdier i systemet.

    * Eksempel: Kjære %P% Logg på Ansattselvbetjening for å fylle ut spørreskjemaet om ansattes helse.  Contoso  

12. Klikk på **Lagre**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Bruk oppsettsdetaljene til å velge spørreskjemaet/spørreskjemaene som skal besvares, i tillegg til eventuelle spørringer som skal brukes til å velge respondenter.

1. Klikk på **Oppsettsdetaljer**.

2. Velg en spørring som skal brukes for å søke etter respondenter for spørreskjemaet.

    * Eksempel: Arbeidere  

3. Klikk på **Vis eller endre spørring** for å velge bestemte personer eller endre spørringen for å finne personer som oppfyller bestemte vilkår.

    * Vær oppmerksom på at alle respondenter må også være brukere i systemet.  

4. Merk raden for Person i listen.

5. Angi eller velg en verdi i **Kriterier**-feltet.

    * Velg Julie Funderburk  

6. Velg Julia Funderburk i listen.

7. Klikk på **OK**.

8. Klikk på **Spørreskjemaer**-fanen.

9. I treet utvider du noden for spørreskjematypen **Undersøkelse om tilfredshet**.

10. Merk av for Workforce Health Assessment.

11. Klikk på **OK**.

12. Klikk på **Planlagt svarøkt**.

    * Legg merke til at **planlagte svarøkter** er opprettet for hver bruker som er valgt/spørres.  

13. Lukk siden.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Start spørreskjemaplanen for å gjøre spørreskjemaet tilgjengelig for respondentene.

1. Klikk **Funksjoner**.

2. Klikk på **Start**.

3. Klikk på **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Send e-post for å varsle svarpersoner om at spørreskjemaet er tilgjengelig.

1. Klikk **Funksjoner**.

2. Klikk på **Send e-post**.

3. Klikk på **Avbryt**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Bruk planlagte svarøkter til å følge med på hvem som må fylle ut spørreskjemaet.

1. Klikk på **Planlagt svarøkt**.

    * Slett eventuelle gjenværende planlagte svarøkter når du er klar til å avslutte den planlagte økten.  

2. Klikk på **Slett**.

3. Klikk på **Ja**.

4. Lukk siden.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Avslutt planleggingen når alle respondentene har fullført spørreskjemaet og /eller alle gjenstående planlagte svarøkter er slettet.

1. Klikk **Funksjoner**.
2. Klikk på **Avslutt**.
3. Klikk på **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
