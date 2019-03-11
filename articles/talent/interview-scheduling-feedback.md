---
title: Planlegging og tilbakemelding for intervju
description: Dette emnet gir informasjon om planleggings- og tilbakemeldingsaktiviteter for intervju i Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2019
ms.locfileid: "374954"
---
# <a name="interview-scheduling-and-feedback"></a>Planlegging og tilbakemelding for intervju

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Planleggeraktivitet

Planleggeraktiviteten er valgfri og har to komponenter: forespørsel om kandidattilgjengelighet og tidsplan. Med komponenten kandidattilgjengelighet kan du bruke e-post til å spørre om en kandidats tilgjengelighet. Tidsplankomponenten gir mulighet å planlegge intervjuer med kandidaten og ansettelsesteamet.

### <a name="candidate-availability-request"></a>Forespørsel om kandidattilgjengelighet

Hvis du vil sende en e-post til kandidater for å spørre om de er tilgjengelige, velger du feltet **Spør om kandidattilgjengelighet**. Hvis feltet ikke er valgt, vises ikke dette trinnet i ansettelsesprosessen for jobben.

Hvis du vil sende forespørselen om tilgjengelighet, klikker du på **Send forespørsel**, velger de tilgjengelige datoene og en e-postmal, og sender deretter meldingen til kandidaten.

[![Rekrutterervisning i Attract for å sende forespørsel om kandidattilgjengelighet](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Når kandidaten mottar en e-post for å svare på forespørselen, kan de logge på kandidatportalen, velge datoene som samsvarer med deres tilgjengelighet, og klikke på **Send**.

### <a name="schedule"></a>Planlegg
Det finnes flere konfigurasjoner som intervjuplanleggeren kan bruke for å raskt opprette og sende intervjuløkken til intervjuerne og kandidaten.

1. Klikk på **Opprett tidsplan**, og i **Legg til intervjuere**-boksen angir du alle intervjuerne som skal være en del av intervjuløkken.
[![Rekrutterervisning i Attract for å begynne planlegging av en intervjuløkke](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Hvis kandidaten har svart på forespørselen om intervjutilgjengelighet, fylles **Intervjudato**-feltet ut på forhånd med deres valg. Du kan velge en annen dato om nødvendig.
    
    Hvis du velger feltet **Gjør dette til et panelintervju**, flyttes gruppen med intervjuere til venstre til en enkel panelløkke for å opprette intervjuet. Deretter må du definere en bestemt rekkefølge for intervjuene.
    
    Intervjutidsplanen må ordnes slik at den er i best mulig samsvar med deltakernes tilgjengelighet. Hvis det er en intern kandidat, kan du inkludere deres tilgjengelighet som en del av tidsplananbefalingen.
    
    Hvis du vil ha et nettmøte, velger du feltet **Legg til Skype-møter**, og hver intervjuhendelse får en **Skype for Business**-kobling tilgjengelig.

2. Velg intervjuvarigheten for hver intervjuhendelse, og klikk deretter på **OK** for å opprette tidsplanen.

    Hvis **Anbefalinger** er valgt, vises det forslag og intervjurutenettet fylles ut på forhånd. Du vil kunne se gjeldende kalendertilgjengelighet for alle valgte intervjuere. Du vil også kunne vise kandidatens kalender hvis de er interne kandidater.

3. Hvis det ikke finnes noen forslag, i **Intervjuere**-kolonnen klikker du i et tidsrom, angir intervjutittelen, detaljer, og fyller ut stedsdetaljene etter behov. Du kan velge å inkludere **Skype for Business**-koblingen for intervjuet.

4. Hvis du vil ta med flere intervjuere, klikker du på **Legg til intervju**-rutenettkolonnen for å velge én eller flere intervjuere. Du kan bruke alternativet ellipse (...) til å fjerne et intervju fra løkken.
    
5. Hvis intervjuene planlegges i en annen tidssone, velger du nødvendig by/tidssone fra rullegardinlisten øverst til høyre. Rutenettet for intervjuertilgjengelighet oppdateres for å gjenspeile den nye tidssonen. Dette tidssonevalget vil nå også vises i visningen **Intervjusammendrag**, som deles med intervjuerne og kandidaten. 

6. Klikk på **Send til intervjuere** for å sende møteinvitasjonene til intervjuerne som er involvert.

    Når intervjuforespørslene er sendt til intervjuerne, kan de svare direkte fra e-postinvitasjonen de mottar.

    >[!NOTE]
    > For alle 1:1-intervjuer sendes påminnelser til intervjuerne hvert døgn hvis intervjueren ikke har svart (godtatt eller avslått) på intervjuforespørselen.

    > For alle panelintervjuer finnes det ingen automatiske påminnelser for intervjuforespørselen. Hvis du vil utløse en påminnelse manuelt, redigerer du intervjuet og bruker **Oppdater og send**-alternativet for å sende forespørselen tilbake til intervjuerne.

    Intervjuersvar registreres og vises i Attract. Hvis en intervjuer avslår invitasjonen, vil du bli varslet for å gjøre en endring. Hvis du vil vise svaret deres i **Planlegger**-rutenettvisningen, klikker du på bobleikonet.

[![Rekrutterervisning i Attract for en intervjuers svar](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Når intervjutidsplanen er klar til å deles med kandidaten, klikker du på **Send til kandidat**. Du kan velge å vise eller skjule navnene på intervjuere og tidsrom for kandidaten.

8. Velg en postmal og send intervjusammendraget til kandidaten. Kandidaten kan vise denne informasjonen i deres e-post og kandidatportal.
    
>[!NOTE] 
> Kalendertilgjengeligheten for en kandidat vises bare hvis kandidaten er intern. På samme måte kan bare interne kandidater brukes til å forbedre anbefalte intervjutidsplaner. For øyeblikket mottar ikke kandidater (eksterne eller interne) en e-postmøteinvitasjon. De mottar i stedet bare et sammendrag av intervjuene.

## <a name="feedback-activity"></a>Tilbakemeldingsaktivitet

Tilbakemeldingsaktiviteten er valgfri i en jobbmal. I denne aktiviteten kan intervjudeltakere angi anbefalinger eller tilbakemeldinger for en søker. Hvis feltet **Arv tilbakemeldingsdeltakere fra ansettelsesteam** er valgt, angis rekrutterer, ansettelsesansvarlig og intervjuere automatisk i tilbakemeldingsaktiviteten. Organisasjoner kan la intervjuere vise tilbakemeldingen fra andre før de sender sine egen tilbakemelding. Organisasjoner kan også la intervjuerne redigere tilbakemeldingen etter at de har sendt den. Intervjuere blir påminnet om å gi tilbakemelding for intervjuene de nylig har gjennomført, basert på den forhåndsinnstilte konfigurasjonen som del av jobbmalen. Ansettelsesansvarlig eller rekruttereren for jobben kan også velge å minne intervjueren på å gi tilbakemelding, manuelt.

## <a name="interview-activity"></a>Intervjuaktivitet

Intervjuaktiviteten er en valgfri aktivitet med tre komponenter: forespørsel om kandidattilgjengelighet, tidsplan og tilbakemelding. Bruk intervjuaktiviteten i jobbmalen hvis du vil ha hele kandidatens tilgjengelighetsforespørsel, tidsplan og tilbakemelding som en del av prosessen i stedet for å bruke dem hver for seg som en del av ansettelsesprosessen.
