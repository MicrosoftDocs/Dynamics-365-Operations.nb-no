---
title: Definere veksler
description: "Dette emnet beskriver fremgangsmåten for hvordan du konfigurerer veksler."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Definere veksler

Dette emnet beskriver fremgangsmåten for hvordan du konfigurerer veksler.

En veksel er en skriftlig eller elektronisk ordre fra en kunde som angir at en annen part, vanligvis en bank, skal betale et angitt beløp til selskapet. Når du bruker en veksel som betaling for en salgsordrefaktura eller fritekstfaktura, krediterer du kundekontoen. Denne kreditten sikres av vekselen, til kunden betaler vekselen til banken. Vanligvis vil du utligne fakturaen med vekselen på forfallsdatoen. Når du mottar varsel fra banken om at vekselen er innløst, kan du lukke den. Du kan tegne en vekselen gjennom banken på et av følgende tidspunkt:

-   På forfallsdatoen. Denne metoden kalles remitter for inkasso.
-   Før forfallsdatoen, vanligvis på rabattdatoen som er angitt i betalingsbetingelsene som er definert for kunden. Når du posterer transaksjonen, posteres rabattbeløpet til en utgiftskonto. Det resterende beløpet er gjeld til deg til banken mottar betaling fra kunden. Denne metoden kalles remitter for diskonto.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Definere posteringsprofiler for veksler
Bruk av **kundeposteringsprofilene** siden for å definere posteringsprofiler som kan brukes med veksler, protestere veksler, remisser for inkasso og remisser for diskonto. I den **Samlekonto**, velger du samlekontoen du vil postere vekselbeløp til. Denne kontoen debiteres eller krediteres, avhengig av hvilken type vekseltransaksjon:
-   For veksler debiteres denne kontoen når en veksel posteres, og krediteres når en remisse for diskonto eller en remisse for inkasso posteres.
-   For protestert veksel debiteres denne kontoen når en protestert  veksel posteres.
-   For remisser for inkasso debiteres denne kontoen når en remisse for inkasso posteres.
-   For remisser for diskonto debiteres denne kontoen når en remisse for diskonto posteres.

I den **Utligningskonto**, velger du kontantkontoen du vil postere vekselbeløp til. Denne kontoen debiteres når en veksel utlignes. I den **mva-forskuddsbetalinger**, velger du samlekontoen du vil postere mva-beløp til når veksler brukes for forskuddsbetalinger. I den **konto for rabattavsetning**, velger du kontoen du vil bokføre rabattbeløp for remisser for diskonto til. Denne kontoen krediteres når en remisse for diskonto posteres.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Definere kundeparametere for veksler
På den **Kundeparametere** siden, standard posteringsprofiler for veksler som er angitt på den **finans og merverdiavgift** i kategorien. Nummerserier er definert på den **nummerserier** i kategorien.
Definere journalnavn for veksler
------------------------------------------

På den **navn på journaler for** side, Opprett minst fem journalnavn for bruk for veksler. Her er journaltypene:
-   **Trekk veksel** – Opprett et journalnavn for Draw vekseljournal.
-   **Protester veksel** – Opprett et journalnavn for protestert vekseljournal.
-   **Kundens tilbaketrekking av veksel** – Opprett et journalnavn for tilbaketrekking av vekseljournalen.
-   **Kunde: bankremisse** – Opprett et journalnavn for remitteringsjournalen.
-   **Kunde: avregn veksel** – Opprett et journalnavn for leverandøravregning vekseljournal.

På siden journal bilag for hver Vekseljournal angir informasjon om vekselen på den **veksel** i kategorien. Når journallinjene vekselen er postert, kan du vise dem på den **veksel journal forespørsel** siden og **Vekselstatistikk** siden.
Definere betalingsmåter for veksler
-----------------------------------------------

På den **betalingsmåter for** -siden Definer minst én betalingsmåte for veksler. Hvis du gjør forretninger med flere banker, må du definere en betalingsmåte som tilsvarer remitteringsformat som krever at hver enkelt bank for veksler.
Definere betalingsgebyrer for veksler
-----------------------------------------

Et betalingsgebyr et er gebyr som er tilknyttet prosessen med å samle inn betaling fra kunder. Flere oppsett av Kundebetalingsgebyr linjer kan være tilknyttet hvert betalingsgebyr. Du kan bruke linjer til å styre hvordan standardbeløp for betalingsgebyr skal beregnes. Du kan for eksempel opprette konfigurasjonslinjer for betalingsmåter, betalingsspesifikasjoner, valutaer og tidsperioder. Du kan også opprette konfigurasjonslinjer for en prosent eller et beløp basert på dagsintervaller. Du kan for eksempel definere en renteprosenten som er basert på hvor lenge betalingen har forfalt. Hvis banken krever ulike gebyrer for ulike remissetyper, som **samling** eller **rabatt**, opprette en egen betalingsgebyr linje for hver remitteringstype.
Definere remitteringsgebyrer for bankremissefiler
------------------------------------------------

På den **bankkonti** siden, kan du definere remitteringsgebyrer som belaster banken for hver remitteringsfil som genereres. Remitteringsgebyrene posteres når remitteringen er bekreftet og de realiserte gebyrbeløpene er kjent. Remitteringsgebyrene skiller seg fra betalingsgebyrer, som samles fra kunder og knyttet til journallinjene.
Definere dokumentoppsett for veksler
---------------------------------------------

På den **bankkonti** klikker du **satt opp**, og angi oppsettet for dokumentet som kreves for hver bankkonto som du vil generere utskrevne veksler dokumenter.
Definere kunder for veksler
--------------------------------------

På den **kunder** side, for hver kunde som har avtalt å betale ved hjelp av en veksel, kan du definere en standard betalingsmåte for veksler på den **Betalingsstandarder** i kategorien.




