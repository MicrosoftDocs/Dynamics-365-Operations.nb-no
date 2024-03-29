---
title: Innkrevinger i Kunder
description: Informasjon om kundeinnkrevinger administreres i én sentral visning på siden Innkrevinger i Microsoft Dynamics 365 Finance. Ledere for kreditt og innkreving kan bruke denne sentrale visningen til å administrere innkreving. Innkrevingsagenter kan begynne innkrevingsprosessen fra kundelister som genereres ved hjelp av forhåndsdefinerte innkrevingskriterier eller fra kundesiden.
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 00e536241710fc8a75158472688757320abf4247
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067216"
---
# <a name="collections-in-accounts-receivable"></a>Innkrevinger i Kunder

[!include [banner](../includes/banner.md)]

Informasjon om kundeinnkrevinger administreres i én sentral visning på siden Innkrevinger i Microsoft Dynamics 365 Finance. Ledere for kreditt og innkreving kan bruke denne sentrale visningen til å administrere innkreving. Innkrevingsagenter kan begynne innkrevingsprosessen fra kundelister som genereres ved hjelp av forhåndsdefinerte innkrevingskriterier eller fra kundesiden.

Før du begynner å sette opp eller arbeide med samlinger, bør du forstår disse begrepene:
-   Øyeblikksbilder av aldersfordeling for kunder inneholder informasjon på et gitt tidspunkt
-   Innkrevingskundepuljer hjelper med å organisere arbeidet
-   Innkrevingsagenter kan ha sine egne kundepuljer
-   Listesider organiserer innkrevingskunder, aktiviteter og saker
-   All innkrevingsinformasjon for en kunde er på én side, og du kan foreta en handling fra denne siden
-   Frafall, gjenopptagelse eller reversering av renter og gebyrer kan gjøres i ett trinn
-   Oppretting av avskrivningstransaksjoner kan utføres i ett trinn
-   Behandling av betaling uten dekning kan gjøres i ett trinn

Delene nedenfor beskriver hvert begrep.

## <a name="customer-aging-snapshots"></a>Øyeblikksbilder av aldersfordeling for kunde 
Et øyeblikksbilde av aldersfordeling inneholder de beregnede aldersfordelte saldoene for en kunde på ett tidspunkt. Denne informasjonen vises på listesiden Aldersfordelte saldoer og på siden Innkrevinger. Et øyeblikksbilde av aldersfordeling må opprettes før du kan vise informasjon på listesidene for innkreving. 

For hver kunde inneholder et øyeblikksbilde av aldersfordeling et hode for øyeblikksbilde av aldersfordeling og detaljposter som samsvarer med hver aldersfordelingsperiode i definisjonen av aldersfordelingsperioden. 

Hodet for øyeblikksbilde av aldersfordeling inneholder totalbeløp å betale, kredittgrense, følgeseddelbeløp, salgsordrebeløp, antall bestridte transaksjoner og totalbeløp for bestridte transaksjoner for kundekontoen. Alle transaksjoner for kunden inkluderes i beregningen av disse beløpene. Totalbeløpet som forfaller, kredittgrensen, følgeseddelbeløpet og salgsordrebeløpet vises i faktaboksen Kredittinformasjon på siden Innkrevinger. 

For hver aldersfordelingsperiode i definisjonen av aldersfordelingsperiode opprettes en detaljpost for øyeblikksbildet av aldersfordeling. Hver detaljpost for øyeblikksbilde av aldersfordeling inneholder ID-en for aldersfordelingsperioden og totalbeløpet for transaksjoner med datoer i aldersfordelingsperioden. Transaksjoner tilordnes til en aldersfordelingsperiode, for eksempel 30 dager over fristen. Datoen er i forhold til Aldersfordeling per-datoen som angis når du oppretter et øyeblikksbilde av aldersfordeling. Denne informasjonen vises på listesiden Aldersfordelte saldoer og i faktaboksen Aldersfordelte saldoer på siden Innkrevinger.

## <a name="collections-customer-pools"></a> Innkrevingskundepuljer 
Kundepuljer er spørringer som definerer en gruppe kundeposter som kan vises og administreres for innkrevinger eller aldersfordelingsprosesser. Bruk kundepuljer for å filtrere informasjon på listesiden Aldersfordelte saldoer, Innkrevingsaktiviteter og Innkrevingssaker. Du bruker også kundepuljer til å filtrere kundekontoene som inkluderes når øyeblikksbilder av aldersfordeling opprettes.

## <a name="collections-agents"></a>Innkrevingsagenter
Brukere kan som standard vise all kundeinformasjon på innkrevingslistesidene. Du kan bruke poster for innkrevingsagenter til å bestemme hvilke kundepuljer som er tilgjengelige for å filtrere informasjon på innkrevingslistesidene og på Innkrevinger-siden. 

En innkrevingsagent er en person som arbeider med kunder for å sørge for at betalinger kreves inn i tide. Innkrevingsagenter er arbeidere som er tilordnet til brukere på Brukeroppsett-siden.

## <a name="collections-list-pages"></a> Listesider for innkrevinger 
Følgende listesider hjelper deg med å organisere innkrevingsinformasjon.
-   Aldersfordelte saldoer – Kolonnene på listesiden viser kundesaldoer og aldersfordelte beløp etter aldersfordelingsperiode. Denne informasjonen er lagret i et øyeblikksbilde av aldersfordeling. Aldersfordelingsperiodene bestemmes av den definisjonen av aldersfordelingsperiode som er i bruk. Definisjonen av aldersfordelingsperiode hentes fra kundepuljen, hvis det er angitt en slik for puljespørringen. Hvis puljen ikke har en definisjon for aldersfordelingsperiode, brukes standarddefinisjonen for aldersfordelingsperiode som er angitt på Kundeparametere-siden. Hvis det ikke er angitt en definisjon av standard aldersfordelingsperiode, brukes den første definisjonen av aldersfordelingsperiode som er angitt på siden Definisjoner av aldersfordelingsperiode.
-   Innkrevingsaktiviteter – Kolonnene på listesiden viser aktiviteter som er identifisert som innkrevingsaktiviteter. Disse aktivitetene opprettes ved å bruke Innkrevinger-siden. Bruk aktiviteter til å spore arbeidet du gjør knyttet til innkreving.
-   Innkrevingssaker – Kolonnene på listesiden viser informasjon for saker som har en sakskategori av typen Innkrevinger.

> [!NOTE]
> Et øyeblikksbilde av aldersfordeling må opprettes før du kan vise informasjon på disse listesidene. Informasjonen vises bare for kunder det er blitt opprettet et øyeblikksbilde av aldersfordeling for. Postene som vises på listesiden kan også filtreres på følgende måte:
> <li>Som standard har en Finance and Operations-bruker tilgang til alle kunder som har et øyeblikksbilde av aldersfordeling.</li>
> <li>Hvis det finnes kundepuljer, må en bruker defineres som en innkrevingsagent for å bruke puljer til å filtrere informasjon på innkrevingslistesidene. Informasjon er begrenset til kundene som er med i den valgte kundepuljen.</li>
> <li>Hvis en bruker er konfigurert som innkrevingsagent, er det bare puljene som er valgt for denne innkrevingsagenten, som er tilgjengelige på listesiden. Hvis Tillat agent å vise alle kundepuljer er valgt på siden Innkrevingsagent for innkrevingsagenten, er alle puljer tilgjengelige for denne agenten.</li>


## <a name="collections-page"></a> Innkrevingssiden
Bruk siden Innkrevinger til å vise, administrere og utføre handlinger på innkrevingsinformasjon, aktiviteter og saker for en kunde. 

Den øvre ruten viser saker for den valgte kunden. Den midtre ruten viser transaksjonene for kunden. Den nedre ruten viser aktiviteter for kunden. Du kan opprette innkrevingssaker for å spore innkrevingsinformasjon for én eller flere transaksjoner og aktiviteter. Informasjonen i de øvre og nedre ruten kan filtreres etter sak. 

Faktabokser viser informasjon om aldersfordelte saldoer og kredittgrense for den valgte kunden. Denne informasjonen er lagret i øyeblikksbildet av aldersfordeling. Om nødvendig kan du oppdatere øyeblikksbildet av aldersfordeling med gjeldende informasjon. 

Handlingsruten inneholder knapper som viser tilknyttet informasjon for den valgte kunden, saken, transaksjonen eller aktiviteten. Du kan også utføre vanlige handlinger, for eksempel endre purrestatusen for en transaksjon, sende e-postkorrespondanse gjennom integrasjon med e-postleverandøren, refundere kunder, behandle betalinger uten dekning og avskrive saldoer som ikke kan inndrives.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Frafalle, gjenoppta eller reversere renter og gebyrer 
Du kan frafalle, gjenoppta eller reversere hele rentenotaer eller gebyrer og transaksjonsrente som er en del av rentenotaer. Du kan gjøre dette fra kategorien Innkreving i handlingsruten på listesiden Alle kunder ved å klikke Rentenota, Transaksjonsrente eller Gebyr. 

Disse justeringene påvirker bare rentenotaer og rente og gebyrer som de inkluderer. Bruk fremgangsmåten i delen Opprette avskrivningstransaksjoner i ett trinn for å skrive av alle tilleggene som en kunde skylder.

For mer informasjon, se [Opprette en rentekode med et område](tasks/create-interest-code-range.md) og [Behandle rente](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Opprette avskrivningstransaksjoner
Du kan skrive av misligholdt gjeld ved å klikke Avskriv i innkrevingsskjemaet og på listesiden Aldersfordelte saldoer, Kunder og Åpne kundefakturaer. 

Når du avskriver transaksjoner for en kunde, merkes alle transaksjoner for kunden automatisk for utligning. Beløpet som avskrives, avhenger av nettobeløpet for de merkede transaksjonene. Avskrivningstransaksjonen opprettes i en økonomijournal og kan inneholde opptil tre typer journallinjer.

-   Den første typen journallinje inneholder avskrivningsposten for kunden. Hvis de merkede transaksjonene inneholder flere kombinasjoner av valutakode, dimensjon og posteringsprofil, opprettes en egen journallinje for hver kombinasjon.
-   Den andre typen journallinje inneholder avskrivningsposten for økonomimodulen. Hvis de merkede transaksjonene inneholder flere kombinasjoner av valutakode, dimensjon og posteringsprofil, opprettes en egen journallinje for hver kombinasjon.
-   Den tredje typen journallinje inneholder informasjon om økonomimodulens avskrivning for merverdiavgift. Denne journallinjen opprettes bare hvis Separat merverdiavgift er valgt på siden Kundeparametere. Hvis de merkede transaksjonene inneholder flere kombinasjoner av betalingskonto for merverdiavgift, dimensjon og mva-kode, opprettes en egen journallinje for hver kombinasjon.

Avskrivningstransaksjonen opprettes i transaksjonsvalutaen.

For mer informasjon, se [Opprette en avskrivningsjournal for en kunde](tasks/create-write-off-journal-customer.md).

## <a name="process-not-sufficient-funds-nsf-payments"></a>Behandle betalinger uten dekning  

Du kan behandle betalinger uten dekning ved å klikke Betaling uten dekning på Innkrevinger-siden. Når du klikker denne knappen, blir betalingen avbrutt. Hvis det forekommer et gebyr for betalingen uten dekning for kunden, blir det opprettet en tilleggstransaksjon i en betalingsjournal. Gebyrbeløpet er basert på innstillingene for de automatiske tilleggene. De automatiske tilleggene som gjelder for betalinger uten dekning, angis av gebyrgruppen som er valgt på Bankkontoer-siden for den aktuelle bankkontoen.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

