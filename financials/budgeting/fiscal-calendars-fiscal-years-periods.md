---
title: "Regnskapskalendere, regnskapsår og perioder"
description: "Denne artikkelen omhandler økonomisk kalendere, regnskapsår og perioder og hvordan du bruker dem for juridiske enheter, aktiva og budsjettering."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 22a08b1b9e819f5c683d278f37bf3404e757d200
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Regnskapskalendere, regnskapsår og perioder

[!include[banner](../includes/banner.md)]


Denne artikkelen omhandler økonomisk kalendere, regnskapsår og perioder og hvordan du bruker dem for juridiske enheter, aktiva og budsjettering.

Økonomiske kalendere gir et rammeverk for den økonomiske aktiviteten i en organisasjon. Hver regnskapskalender inneholder ett eller flere regnskapsår, og hvert regnskapsår inneholder flere perioder. Økonomiske kalendere kan følge kalenderåret fra 1. januar til 31. desember, eller den kan være basert på datoer du velger. Noen organisasjoner velger for eksempel en økonomisk kalender som starter 1. juli ett år og slutter 30. juni det påfølgende året. 

Det er ingen grense for hvor mange økonomiske kalendere du kan opprette, og ingen grense for hvor mange regnskapsår som kan opprettes for en økonomisk kalender. Hver regnskapskalender er uavhengig av organisasjonen, og kan brukes av flere juridiske enheter i organisasjonen. En organisasjon har for eksempel åtte avdelinger, og hver avdeling er en separat juridisk enhet. Fem av dem deler samme økonomiske kalender, og tre bruker ulike økonomiske kalendere. Du kan opprette én regnskapskalender for de fem juridiske enhetene som deler samme regnskapskalender, og deretter opprette forskjellige regnskapskalendere for de andre juridiske enhetene.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Opprette økonomiske kalendere, regnskapsår og regnskapsperioder
Du kan opprette og slette regnskapskalendere, regnskapsår og perioder på Regnskapskalendere-siden. Du kan også dele opp eksisterende perioder og opprette avslutningsperioder som kan brukes til å avslutte et regnskapsår. 

En avslutningsperiode brukes til å skille økonomimodultransaksjoner som genereres når et regnskapsår avsluttes. Når avslutningstransaksjonene er i en regnskapsperiode, er det enklere å opprette regnskapsoppgjør som enten inkluderer eller ekskluderer ulike typer avslutningsoppføringer. Hvis et regnskapsår er delt opp i tolv regnskapsperioder, er avslutningsperioden vanligvis den trettende perioden. En avslutningsperiode kan imidlertid opprettes fra enhver periode med statusen Åpen. 

Når du oppretter en avslutningsperiode, velger du en periode som har statusen Åpen og har datoene du vil bruke. Den nye avslutningsperioden kopierer start- og sluttdatoene fra den eksisterende perioden. Den opprinnelige perioden finnes fortsatt. La oss si at du velger Periode 12, som er siste periode i regnskapsåret, og som har datoene fra 1. august til og med 31. august. Du skriver inn et navn for avslutningsperioden, for eksempel Slutt. Etter at du har opprettet den nye avslutningsperioden, har du nå den opprinnelige perioden og avslutningsperioden. Begge har datoer som begynner 1. august og slutter 31. august.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Velge regnskapskalendere for finans, anleggsmidler og budsjettsykluser
Økonomiske kalendere brukes til avskrivning av anleggsmidler, økonomiske transaksjoner og budsjettsykluser. Når du oppretter en økonomisk kalender, kan du bruke den til flere formål. Du kan velge en økonomisk kalender for en verdimodell eller et avskrivningstablå for å gjøre den om til en anleggsmiddelkalender. Du kan velge en økonomisk kalender for en finans for å gjøre den om til en finanskalender. Du kan også velge en økonomisk kalender for en budsjettsyklus for å gjøre den om til en budsjettkalender. Du kan bruke samme regnskapskalender for alle disse.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Velge en regnskapskalender for den juridiske enheten

Velg den økonomiske kalenderen du vil bruke for finans for den juridiske enheten i Finans-skjemaet. Du må velge en regnskapskalender på siden Finans for hver juridiske enhet. Når du har valgt en regnskapskalender, kan du definere periodestatuser og -tillatelser på siden Finanskalender for alle periodene som er en del av et regnskapsår.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Velge en økonomisk kalender for anleggsmidler

Du kan velge en økonomisk kalender for en verdimodell eller et avskrivningstablå, og denne økonomiske kalenderen brukes av anleggsmidlene som bruker den valgte verdimodellen eller det valgte avskrivningstablået. Du kan velge en hvilken som helst regnskapskapender som er definert på siden Regnskapskalendere.

### <a name="define-budget-cycle-time-spans"></a>Definere tidsrom for budsjettsyklus

Budsjettsykluser er tidsrommet et budsjett brukes i. Budsjettsykluser kan inkludere en del av et regnskapsår eller flere regnskapsår, for eksempel en toårig eller treårig budsjettsyklus. Tidsrommet for budsjettsyklus definerer antall perioder som er inkludert i budsjettsyklusen. For å angi tidsrom for budsjettsyklus bruk siden Tidsrom for budsjettsyklus.

## <a name="maintain-periods-for-your-organization"></a>Vedlikeholde perioder for organisasjonen
Du kan bruke Finanskalender-siden til å vise detaljene for regnskapskalenderen, regnskapsåret og periodene som brukes i organisasjonen. Du kan også endre statusen for periodene og velge hvilke brukere som kan postere regnskapstransaksjoner til perioder. I begynnelsen av en ny periode vil du for eksempel kanskje at en gruppe brukere skal fullføre posteringene av finanstransaksjoner i den forrige perioden, mens andre grupper bare arbeider i den nye perioden.






