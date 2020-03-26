---
title: Nøkkelbegreper for innkrevingsbehandling
description: Emnene definerer nøkkelbegreper for innkrevingsadministrasjon.
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8bee320beb411a5ee0829a0e3170de0c7f293172
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124237"
---
# <a name="collections-management-key-concepts"></a>Nøkkelbegreper for innkrevingsbehandling

[!include [banner](../includes/banner.md)]

Før du begynner å sette opp eller arbeide med samlinger, bør du forstår disse begrepene:

- Øyeblikksbilder av aldersfordeling for kunder inneholder informasjon på et bestemt tidspunkt.
- Innkrevingskundepuljer hjelper med å organisere arbeidet.
- Innkrevingsagenter kan ha sine egne kundepuljer.
- Listesider organiserer innkrevingskunder, aktiviteter og saker.
- All innkrevingsinformasjon for en kunde er på én side, og du kan foreta en handling fra denne siden.
- Renter og gebyrer kan frafalles, gjenopptas eller reverseres i ett trinn.
- Avskrivningstransaksjoner kan opprettes i ett trinn.
- Betaling uten dekning kan behandles i ett trinn.

Dette emnet beskriver hvert begrep.

## <a name="customer-aging-snapshots"></a>Øyeblikksbilder av aldersfordeling for kunde 

Et øyeblikksbilde av aldersfordeling inneholder de beregnede aldersfordelte saldoene for en kunde på ett bestemt tidspunkt. Denne informasjonen vises på listesiden **Aldersfordelte saldoer** og siden **Innkrevinger**. Et øyeblikksbilde av aldersfordeling må opprettes før du kan vise informasjon på listesidene for innkreving (**Aldersfordelte saldoer**, **Innkrevingsaktiviteter** og **Innkrevingssaker**).

For hver kunde har et øyeblikksbilde av aldersfordeling et hode for øyeblikksbilde av aldersfordeling og detaljposter som samsvarer med hver aldersfordelingsperiode i definisjonen av aldersfordelingsperioden.

Hodet for øyeblikksbilde av aldersfordeling inneholder totalbeløpet som forfaller, kredittgrense, følgeseddelbeløp, salgsordrebeløp, antall bestridte transaksjoner og totalbeløp for bestridte transaksjoner for kundekontoen. Alle transaksjoner for kunden inkluderes i beregningen av disse beløpene. Totalbeløpet som forfaller, kredittgrensen, følgeseddelbeløpet og salgsordrebeløpet vises i faktaboksen **Kredittinformasjon** på siden **Innkrevinger**.

For hver aldersfordelingsperiode i definisjonen av aldersfordelingsperiode opprettes en detaljpost i øyeblikksbildet av aldersfordeling. Hver detaljpost inneholder ID-en for aldersfordelingsperioden og totalbeløpet for transaksjoner som har datoer i aldersfordelingsperioden. Transaksjoner tilordnes til en aldersfordelingsperiode, for eksempel 30 dager over fristen. Datoen er i forhold til **Aldersfordeling per**-datoverdien som du angir når du oppretter et øyeblikksbilde av aldersfordeling. Denne informasjonen vises på listesiden **Aldersfordelte saldoer** og i faktaboksen **Aldersfordelte saldoer** på siden **Innkrevinger**.

## <a name="collections-customer-pools"></a> Innkrevingskundepuljer 

Kundepuljer er spørringer som definerer en gruppe kundeposter. Du kan bruke disse grupperte postene til å vise informasjon for kundekontoene som er inkludert, og til å behandle innkrevinger eller aldersfordelingsprosesser for dem. Du kan bruke kundepuljer for å filtrere informasjon på listesidene for innkrevinger. Du kan også bruke dem til å filtrere kundekontoene som inkluderes når øyeblikksbilder av aldersfordeling opprettes.

## <a name="collections-agents"></a>Innkrevingsagenter

Brukere kan som standard vise all kundeinformasjon på innkrevingslistesidene. Poster for innkrevingsagenter lar deg bestemme hvilke kundepuljer som kan brukes for å filtrere informasjon på innkrevingslistesidene og **Innkrevinger**-siden.

Innkrevingsagenter arbeider med kunder for å sørge for at betalinger kreves inn i tide. De er arbeidere som er tilordnet til brukere på **Brukeroppsett**-siden.

## <a name="collections-list-pages"></a> Listesider for innkrevinger 

Følgende listesider hjelper deg med å organisere innkrevingsinformasjon:

- **Aldersfordelte saldoer** – Kolonnene på denne listesiden viser kundesaldoer og aldersfordelte beløp etter aldersfordelingsperiode. Denne informasjonen er lagret i et øyeblikksbilde av aldersfordeling. Aldersfordelingsperiodene bestemmes av den definisjonen av aldersfordelingsperiode som er i bruk. Definisjonen av aldersfordelingsperiode hentes fra kundepuljen, hvis det er angitt en kundepulje for puljespørringen. Hvis puljen ikke har en definisjon for aldersfordelingsperiode, brukes standarddefinisjonen for aldersfordelingsperiode som er angitt på **Kundeparametere**-siden. Hvis det ikke er angitt en definisjon av standard aldersfordelingsperiode, brukes den første definisjonen av aldersfordelingsperiode som er angitt på siden **Definisjoner av aldersfordelingsperiode**.
- **Innkrevingsaktiviteter** – Kolonnene på denne listesiden viser aktiviteter som er identifisert som innkrevingsaktiviteter. Disse aktivitetene opprettes på **Innkrevinger**-siden. Du bruker aktiviteter til å spore arbeidet knyttet til innkreving som du gjør.
- **Innkrevingssaker** – Kolonnene på denne listesiden viser informasjon for saker som tilhører en sakskategori som har sakstypen **Innkrevinger**.

### <a name="aging-snapshots"></a>Øyeblikksbilder av aldersfordeling

Et øyeblikksbilde av aldersfordeling må opprettes før du kan vise informasjon på listesidene for innkreving. Informasjonen vises bare for kunder det er blitt opprettet et øyeblikksbilde av aldersfordeling for. Postene som vises på listesiden, kan filtreres ytterligere, som beskrevet her:

- Som standard har brukere tilgang til alle kunder som har et øyeblikksbilde av aldersfordeling.
- Hvis det finnes kundepuljer, må en bruker defineres som en innkrevingsagent for å bruke puljer til å filtrere informasjon på innkrevingslistesidene. Informasjon er begrenset til kundene som er med i den valgte kundepuljen.
- Hvis en bruker er konfigurert som innkrevingsagent, er det bare puljene som er valgt for denne innkrevingsagenten, som er tilgjengelige på innkrevingslistesidene. Hvis alternativet **Tillat agent å vise alle kundepuljer** er valgt på siden **Innkrevingsagent** for innkrevingsagenten, er alle puljer tilgjengelige for denne agenten.

## <a name="collections-page"></a> Innkrevingssiden

Du kan bruke siden **Innkrevinger** til å vise, administrere og utføre handlinger på innkrevingsinformasjon, aktiviteter og saker for en kunde.

Den øvre delen av siden viser saker for den valgte kunden, den midterste delen viser transaksjoner for kunden, og den nedre delen viser aktiviteter for kunden. Du kan opprette innkrevingssaker for å spore innkrevingsinformasjon for én eller flere transaksjoner og aktiviteter. Informasjonen i den øvre og nedre delen kan filtreres etter sak.

Faktabokser viser informasjon om aldersfordelte saldoer og kredittgrense for den valgte kunden. Denne informasjonen er lagret i øyeblikksbildet av aldersfordeling. Om nødvendig kan du oppdatere øyeblikksbildet av aldersfordeling med gjeldende informasjon.

Handlingsruten inneholder knapper som lar deg vise tilknyttet informasjon for den valgte kunden, saken, transaksjonen eller aktiviteten. Du kan også utføre vanlige handlinger, for eksempel endre purrestatusen for en transaksjon, sende e-post gjennom integrasjon med e-postleverandøren, refundere kunder, behandle betalinger uten dekning og avskrive saldoer som ikke kan inndrives.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Frafalle, gjenoppta eller reversere renter og gebyrer

Du kan frafalle, gjenoppta eller reversere hele rentenotaer eller gebyrene og transaksjonsrenten som er en del av rentenotaer. I kategorien **Innkreving** i handlingsruten på listesiden **Alle kunder** velger du **Rentenota**, **Transaksjonsrente** eller **Gebyr**.

Disse justeringene påvirker bare rentenotaer og rente og gebyrer som de inkluderer. Hvis du vil ha informasjon om hvordan du avskriver alle gebyrer som en kunde skylder, kan du se delen [Opprette avskrivningstransaksjoner](#creating-write-off-transactions) i dette emnet.

For mer informasjon, se Opprette en rentekode med et område og Behandle rente.

## <a name="creating-write-off-transactions"></a>Opprette avskrivningstransaksjoner

Du kan avskrive misligholdt gjeld ved å velge **Avskriv** på **Innkrevinger**-siden og innkrevingslistesidene.

Når du avskriver transaksjoner for en kunde, merkes alle transaksjoner for denne kunden automatisk for utligning. Beløpet som avskrives, avhenger av nettobeløpet for de merkede transaksjonene. Avskrivningstransaksjonen opprettes i en økonomijournal og kan inneholde opptil tre typer journallinjer:

- Den første typen journallinje inneholder avskrivningsposten for kunden. Hvis de merkede transaksjonene inneholder flere kombinasjoner av valutakoder, dimensjoner og posteringsprofiler, opprettes en egen journallinje for hver kombinasjon.
- Den andre typen journallinje inneholder avskrivningsposten for økonomimodulen. Hvis de merkede transaksjonene inneholder flere kombinasjoner av valutakoder, dimensjoner og posteringsprofiler, opprettes en egen journallinje for hver kombinasjon.
- Den tredje typen journallinje inneholder informasjon om økonomimodulens avskrivning for merverdiavgift. Denne journallinjen opprettes bare hvis alternativet **Separat merverdiavgift** er valgt på siden **Kundeparametere**. Hvis de merkede transaksjonene inneholder flere kombinasjoner av betalingskontoer for merverdiavgift, dimensjoner og mva-koder, opprettes en egen journallinje for hver kombinasjon. Avskrivningstransaksjonen opprettes i transaksjonsvalutaen. For mer informasjon, se Opprette en avskrivningsjournal for en kunde.

## <a name="process-nsf-payments"></a>Behandle betalinger uten dekning

Du kan behandle betalinger uten dekning ved å velge **Betaling uten dekning** på **Innkrevinger**-siden. Når du velger denne knappen, blir betalingen avbrutt. Hvis det forekommer et gebyr for betalingen uten dekning for kunden, blir det opprettet en tilleggstransaksjon i en betalingsjournal. Beløpet for gebyret er basert på innstillingene for de automatiske tilleggene. De automatiske tilleggene som gjelder for betalinger uten dekning, angis av gebyrgruppen som er valgt på **Bankkontoer**-siden for den aktuelle bankkontoen.

## <a name="additional-resources"></a>Tilleggsressurser

[Oppsett av parametere for kundekredittbehandling](./cm-credit-mgmt-setup.md)

[Informasjon om oppsett av kundekredittbehandling](./cm-setup-information.md)

[Legge til kredittbehandlingsinformasjon for en kunde](./cm-add-credit-mgmt-information-customer.md)

[Kundekredittgrupper](./cm-customer-credit-groups.md)

[Kundekredittgrensejusteringer](./cm-credit-limit-adjustments.md)

[Kredittsperrer for salgsordrer](./cm-sales-order-credit-holds.md)

[Periodiske oppgaver for kundekredittbehandling](./cm-periodic-tasks.md)
