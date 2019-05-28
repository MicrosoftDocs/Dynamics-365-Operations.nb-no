---
title: Administrere oppdateringer av standardkostnader
description: 'Oppdateringer av standard kostdata kan behandles på to ulike måter: enversjonsmåten eller toversjonsmåten.'
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e72d4e90ac83787ed7c58d91c2102696acfac68
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553513"
---
# <a name="manage-standard-cost-updates"></a>Administrere oppdateringer av standardkostnader

[!include [banner](../includes/banner.md)]

Oppdateringer av standard kostdata kan behandles på to ulike måter: enversjonsmåten eller toversjonsmåten. 

Enversjonsmåten bruker én etterkalkuleringsversjon som inneholder alle kostnadsposter. Disse postene inneholder de opprinnelige kostnadene og alle kostnadsoppdateringer.

Toversjonsmåten bruker én versjon som inneholder poster for de opprinnelige kostnadene, og en ny versjon som inneholder poster for alle kostnadsoppdateringer. En viktig fordel med toversjonsmåten er den klare avmerkingen og sporingen av kostoppdateringer i en egen kostnadsberegningsversjon, uten at den opprinnelige kostnadsberegningsversjonen påvirkes. Toversjonsmåten kan brukes til å identifisere flere inkrementelle oppdateringer, hvor hver inkrementelle oppdatering har en egen etterkalkuleringsversjon som inneholder de inkrementelle kostprispostene. 

**Eksempel** 

Følgende eksempel viser hvordan enversjons- og toversjonsmåten kan brukes til å oppdatere standardkostnader i et produksjonsmiljø. For eksempel oppdateringer som gjenspeiler nye varer eller korrigeringer av feil. Anta at én enkelt etterkalkuleringsversjon representerer standardkostnadene for inneværende år. Identifikatoren for denne versjonen er 2016-STD. Versjon 2016-STD inneholder gjeldende aktive kostnader for alle varer. Den inneholder i tillegg alle rutingrelaterte kostpriskategorier og beregningsformler for indirekte kostnader som var kjent ved starten av 2016. 2016-STD er den opprinnelige etterkalkuleringsversjonen.

-   **Enversjons tilnærming til oppdateringer av kostprisdata** − I enversjonsmåten inneholder den opprinnelige etterkalkuleringsversjonen 2016-STD alle kostprisposter. Kostnadsoppdateringer registreres i 2016-STD og settes til statusen "Venter". De uavsluttede kostprisene kan legges inn manuelt for nye innkjøpte varer, eller de kan beregnes for en produsert vare for å gjenspeile korrigeringer. Når enversjonsmåten brukes, krever ikke stykklisteberegningene noe tilbakefallsdatakilde, fordi alle aktive kostpriser finnes i kostnadsberegningsversjonen. Nå de uavsluttede kostprisene blir aktivert, vil den opprinnelige etterkalkuleringsversjonen 2016-STD igjen inneholde alle gjeldende aktive kostpriser.
-   **Toversjons tilnærming til oppdateringer av kostprisdata** − Toversjonsmåten krever en ekstra etterkalkuleringsversjon som bare inneholder kostnadsoppdateringene. Identifikatoren for denne versjonen er 2016-STD-ENDRINGER. Kostnadsoppdateringer registreres i 2016-STD-CHANGES og settes til statusen "Venter". Med toversjonsmåten krever stykklisteberegninger av uavsluttede kostpriser for produserte varer tilbakefallsdatakilde. Dette skyldes at den ekstra etterkalkuleringsversjonen 2016-STD-ENDRINGER inneholder bare et delsett av kostnadsdata. Tilbakefallsprinsippet kan uttrykkes som de aktive kostprisene eller som etterkalkuleringsversjonen 2016-STD, fordi begge identifiserer kilden til kostnadsdataene når de ikke er inkludert i 2016-STD-ENDRINGER. Når de uavsluttede kostprisene blir aktivert, vil etterkalkuleringsversjonen 2016-STD-ENDRINGER inneholde gjeldende aktive kostpriser som gjenspeiler oppdateringene, mens den opprinnelige etterkalkuleringsversjonen 2016-STD vil være urørt. Når toversjonsmåten brukes, må det defineres sperrepolicyer for den opprinnelige kostnadsberegningsversjonen for å hindre oppdateringer. Det må defineres nøyaktig de samme blokkeringspolicyene for den andre kostnadsberegningsversjonen, med unntak av den angitte fra-datoen og den selektive bruken av sperrepolicyer for å tillate oppdateringer. Den angitte fra-datoen må oppdateres med hvert sett med endringer for å gjenspeile den planlagte aktiveringsdatoen.

Dette eksemplet brukte en ekstra kostnadsberegningsversjon til å håndtere oppdateringer gjennom hele 2016. Det er også mulig å bruke flere ekstra kostnadsberegningsversjoner, for eksempel en egen versjon for hvert sett med oppdateringer. Når mer enn én ekstra etterkalkulering brukes, må tilbakefallsprinsippet uttrykkes som de aktive kostprisene fordi de aktive kostprisene er spredt over flere etterkalkuleringsversjoner.





