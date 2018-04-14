---
title: Timeregistrering
description: "Tidsregistreringsarbeidere kan angi ulike typer tidsregistreringer, for eksempel stemple inn, stemple ut, registrere indirekte aktiviteter og fraværsregistrering. Dette emnet beskriver registreringer, deres beregning, godkjenning og bruken av arbeidsflyt for å legge til struktur og automatisk godkjenning i prosessen med å godkjenne timeregistreringer."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29040d0c96183898672bc405364ec59707bff53a
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="time-and-attendance-registration"></a>Timeregistrering

[!INCLUDE [banner](../includes/banner.md)]

Tidsregistreringsarbeidere kan angi ulike typer tidsregistreringer, for eksempel stemple inn, stemple ut, registrere indirekte aktiviteter og fraværsregistrering. Dette emnet beskriver registreringer, deres beregning, godkjenning og bruken av arbeidsflyt for å legge til struktur og automatisk godkjenning i prosessen med å godkjenne timeregistreringer. 

<a name="registrations"></a>Registreringer
-------------

I firmaer som bruker Timeregistrering, må ansatte registrere tiden de bruker på arbeid, i tillegg til sin tilstedeværelse. Enkelte firmaer krever kanskje bare at de ansatte registrerer seg når de kommer på arbeidet og når de går hjem. I andre firmaer kan det også være nødvendig for arbeidere å registrere tidsforbruket på de faktiske aktivitetene de utfører i tillegg til pausene de tar. De aktuelle brukerne av Timeregistrering er:
-   Arbeidere, som må bruke timeregistrering med jevne mellomrom, for eksempel daglig, ukentlig eller annenhver uke.
-   Arbeidsledere, ledere og lønnsansvarlige som beregner, godkjenner og overfører arbeiderregistreringer for videre behandling.

| **Obs!**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis du kjører Timeregistrering sammen med produksjonsutførelse, blir alle registreringer på prosjekter, prosjektaktiviteter, indirekte aktiviteter, fraværskoder overtid og fleksitid registrert og brukt til å beregne lønn i begge modulene. |

## <a name="time-registrations-workers"></a>Tidsregistreringsarbeidere
For å kunne bruke Timeregistrering må arbeidere defineres som tidsregistreringsarbeidere i firmaet de arbeider i.

Etter oppsettet kan arbeiderne angi ulike typer registreringer.

-   Stemple inn og ut når de ankommer eller forlater arbeidet.
-   Tids- og vareforbruk på produksjonsjobber.
-   Tid brukt på en maskin på produksjonsgulvet, hvis maskinen er definert som en ressurs.

| **Obs!**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En arbeider kan automatisk tilordnes tidsregistreringer som er gjort på en bestemt maskin på produksjonsgulvet, hvis arbeideren velger å arbeide som assistent for maskinen når han eller hun starter produksjonsjobben. |

-   Tidsregistreringer for prosjekter og prosjektaktiviteter.
-   Registrere prosjektgebyrer og vareforbruk via respektive prosjektgebyrjournaler og prosjektvarejournaler.
-   Planlagt fravær.
-   Fravær når de kommer sent til arbeid eller går tidligere hjem enn planlagt.
-   Arbeidspauser, registreres enten manuelt eller beregnes automatisk av systemet.
-   Indirekte aktiviteter, som er ikke-produktive aktiviteter som en arbeider kan delta i løpet av en arbeidsdag. Eksempler på disse aktivitetene omfatter møter eller rydding av arbeidsområdet.
-   Overtid, som kan registreres som ekstra timer, fleksitid eller overtid.

## <a name="adding-clock-out-registrations"></a>Legge til utstemplingsregistreringer
Hvis en arbeider glemmer å stemple seg ut på slutten av arbeidsdagen, kan den manglende registreringen legges til ved å kjøre en satsvis jobb. Systemet vil sammenligne innstemplingstidspunktet og utstemplingstidspunktet i henhold til profilen knyttet til arbeideren, og automatisk sette inn den manglende utstemplingsregistreringen for å samsvare med profilens sluttidspunkt. Både inn- og utstemplingsregistreringer er viktige for den etterfølgende beregningen og godkjenningen av tidsregistreringer før de kan overføres til lønn.

## <a name="calculating-registrations"></a>Beregne registreringer
Når en registreringsarbeider tilordnes en beregningsgruppe som vanligvis er tilknyttet en bestemt gruppe, skift eller en arbeidsgruppe. Gruppe- eller arbeidslederen validerer vanligvis registreringene som gjøres av arbeiderne, og er derfor også personen som er ansvarlig for å kjøre beregningen for de aktuelle beregningsgruppene daglig. Som en del av beregningsprosessen kan gruppe- eller arbeidslederen:
-   Rette feilregistreringer. For eksempel endre vekslekoder og justere tilbakemelding på produksjonsjobber.
-   Legge til manglende registreringer. For eksempel opprette utstemplingsregistreringer og opprette fraværstransaksjoner.
-   Slette feilregistreringer.

Siden den registrerte tiden må samsvare med arbeiderens tidsprofil før beregning av registreringer, må du overstyre arbeidstidsprofilen for en arbeider som har et unntak for sin standard arbeidstid i profilen. I tilfeller der arbeiderprofilen er dagskift, og arbeideren har sagt seg villig til å ta et nattskift uten overtidsbetaling, må gruppe- eller arbeidslederen overstyre standard arbeiderprofil for å beregne arbeidstiden til standard nattsats og ikke som overtid. Beregningen vises også en feil hvis det mangler en fraværsregistrering. Den må legges til før beregningen kan fullføres.

## <a name="approving-registrations"></a>Godkjenne registreringer
På samme måte som du tilordner en beregningsgruppe til en tidsregistreringsarbeider, må du også tilordne en godkjenningsgruppe. Gruppen er vanligvis spesifikk for et skift, et arbeidslag eller en arbeidsgruppe. Du må godkjenne tidsregistreringene som ble beregnet på riktig måte – dette betyr at utfører en beregning uten feil – før lønnsposter kan genereres som senere kan overføres til et lønningssystem. Lønnsadministratoren utfører vanligvis godkjenning av registreringer, og før godkjenningen kan han:
-   Overstyre lønnsavtaler for individuelle ansatte.
-   Legge til manuelle bonuser.
-   Legge inn tilleggsinformasjon om fraværsregistreringer.

| **Obs!**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis det er beregnet overtid for bestemte ansatte, kan overtiden tilordnes bestemte jobber i løpet av dagen. Dette er relevant hvis jobbkostnadene beregnes på grunnlag av den ansattes lønn. |

## <a name="approving-registrations-using-workflow"></a>Godkjenne registreringer ved hjelp av arbeidsflyt
Du kan definere en godkjenningsprosess for arbeidsflyt som automatisk godkjenner registreringer som samsvarer med arbeidsflytregler, slik at bare avvik skal behandles manuelt. Hvis arbeidsflytgodkjenning er aktivert, sender gruppe- eller arbeidslederen de beregnede registreringene for godkjenning. Arbeidsflytprosessen oppretter de aktuelle godkjenningene og oppgavene, og tilordner dem til de aktuelle brukerne og rollene som er identifisert i arbeidsflyten. Det finnes to arbeidsflytgodkjenninger for timeregistrering.

| Arbeidsflyt                                  | Formål                                                                                                   | Registreringstype                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Totalt antall timeregistreringsdager            | Arbeidsflyten validerer registreringer mot for eksempel det forventede antallet timer for dagen. |                                                                                                                                                                                                                                                       |
| Journalregistrering for timeregistrering. | Arbeidsflyten validerer hver registreringstype for datoen for registreringen.                           | Timeregistrering • innstempling • utstempling • fravær • pause • vekslekode • prosjekt • prosjektaktivitet • indirekte aktivitet produksjonsjobber • kø før • oppsett • prosess • overlapping • transport • kø etter • start assistanse • stopp assistanse |



## <a name="transferring-approved-registrations"></a>Overføre godkjente registreringer
Når registreringer er godkjent, kan de overføres til den periodiske lønnsjobben. En overført registrering blir postert til en aktivitet eller en jobb som den er knyttet til, for eksempel en produksjonsordre eller et prosjekt. Lønnstransaksjoner genereres for hver arbeider basert på registreringene.  

## <a name="reversing-transferred-registrations"></a>Tilbakeføre overførte registreringer
Du kan gjøre oppgaven med å tilbakeføre transaksjoner – tilbakestille dem – til lønnsperiodens lønnsoverføring kjøres. Dette betyr at lønnsdata er overført til en ekstern fil. Når de er tilbakeført, trekkes alle registreringer tilbake, og alle transaksjoner som er postert på produksjonsordrer eller prosjekter, blir motregnet og gjort nøytral.

| **Obs!**                                                 |
|----------------------------------------------------------|
| Den eksterne filen kan importeres til et lønningssystem. |

## <a name="registrations-in-electronic-timecards"></a>Registreringer i elektroniske tidskort
Ansatte med prosjektoppgaver som ikke krever umiddelbar tilbakemelding, som er tilfellet med produksjonsjobber, men som arbeider med prosjektaktiviteter, kan med fordel bruke det elektroniske tidskortet. Elektroniske tidskort gir fleksibilitet til å angi registreringer når som helst og best tilpasset firmaets tidsplan – daglig, ukentlig eller når en arbeider er tilbake på kontoret etter å ha vært borte. Hvis du vil bruke elektroniske tidskort eller disse arbeiderne, må du angi Bruk tidskort i arbeiderdetaljene. Elektroniske tidskort gjør at arbeideren kan registrere:

-   Dato
-   Registreringstype
-   Jobbreferanse, for eksempel prosjekt, indirekte aktivitet eller produksjonsordre
-   Jobbidentifikasjon
-   Tidsforbruk
-   Prosjektgebyrer
-   Prosjektvarer





