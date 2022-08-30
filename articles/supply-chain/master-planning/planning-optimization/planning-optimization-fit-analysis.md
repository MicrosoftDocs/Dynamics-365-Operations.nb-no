---
title: Analyse for tilpasning av planleggingsoptimalisering
description: Denne artikkelen forklarer hvordan du kontrollerer gjeldende oppsett og data mot funksjonene i planleggingsoptimaliseringsfunksjonaliteten.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 633daba553b1544c2caa788f4cec1da4c1da6960
ms.sourcegitcommit: 7af116c60f3a94671a7a80c04097d70180754930
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9347296"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse for tilpassing av planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Du bør analysere resultatet fra analyse for tilpassing av planleggingsoptimalisering som en del av migreringsprosessen. Vær oppmerksom på at planleggingsoptimalisering ikke er lik gjeldende innebygde funksjon for hovedplanlegging. Det anbefales at du arbeider med partneren og leser dokumentasjonen for å klargjøre migreringen. 

Analyse for tilpassing av planleggingsoptimalisering lar deg identifisere hvor resultatet kan variere mellom den innebygde hovedplanleggingsmotoren og planleggingsoptimaliseringen. Denne analysen utføres basert på gjeldende oppsett og data. 

Hvis du vil se resultatet for analyse for tilpassing av planleggingsoptimalisering, kan du gå til **Hovedplanlegging** \> **Oppsett** \> **Analyse for tilpassing av planleggingsoptimalisering** og deretter velge **Kjør analyse**. Hvis analysen finner noen uregelmessigheter, vises de på samme side. (Det kan ta noen minutter å kjøre analysen.)

> [!NOTE]
>
> - Noen inkonsekvenser kan ikke identifiseres av Analyse for tilpasning av planleggingsoptimalisering. For mer informasjon, se [Forskjeller mellom klassisk hovedplanlegging og planleggingsoptimalisering](planning-optimization-differences-with-built-in.md).
>
> - Hvis det blir funnet uoverensstemmelser, kan du likevel bruke planleggingsoptimalisering. Resultatene av tilpassingsanalysen viser bare steder der planleggingstjenesten ikke respekterer det gjeldende oppsettet. De viser med andre ord steder der noen prosesser kan bli ignorert, eller det er ikke sikkert at de støttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funksjon:** produksjon
- **Problem:** Varer med en stykklistenivå som er større enn null: 56
- **Forklaring:** tilpassingsanalysen fant 56 varer som har et oppsett for stykklister for produksjon. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter produksjon, genererer planleggingsoptimalisering bestillingsforslag i stedet for planlagte produksjonsordrer. Den vil også vise en advarsel som viser de berørte varene.

## <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funksjon:** handlinger
- **Problem:** dekningsgrupper med handlingsberegning aktivert: 6
- **Forklaring:** Tilpassingsanalysen fant seks dekningsgrupper der handlingsberegning er aktivert. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter handlinger, blir det ikke generert noen handlinger under hovedplanleggingen.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Oversikt over mulige resultater fra tilpassingsanalysen

Følgende tabell viser de ulike resultatene som kan vises etter en tilpassingsanalyse. Nummertegn (*\#*) erstattes med et tall som angir antallet poster som har det angitte problemet.

> [!IMPORTANT]
> For funksjoner som ennå ikke støttes, gir følgende tabell forventet tilgjengelighetsinformasjon som estimeres basert på nåværende kart. Disse estimatene kan endres uten forvarsel.

| Funksjon | Oppført problem | Forklaring | Forventet tilgjengelighet |
| --- | --- | --- | --- |
| Handlinger | Dekningsgrupper med handlingsberegning aktivert: *\#* | Dette funksjonen støttes nå. | Støttes |
| Basiskalendere | Kalendere som bruker basiskalender: *\#* | Dette funksjonen støttes nå. | Støttes | 
| Partidisposisjonskoder | Ikke-nettbare partidisposisjonsstandarder: *\#* | Dette funksjonen venter. Partidisposisjonskoder ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 |
| Leveringskapasitet | Standard ordreinnstillinger med leveringsdatokontroll satt til CTP: *\#* | I Supply Chain Management 10.0.28 og nyere gjør en prosess kalt for *CTP for planleggingsoptimalisering* bekreftede datoer for forsendelse og mottak tilgjengelig etter at den dynamiske planen er kjørt. For eldre versjoner av Supply Chain Management ignoreres den eldre CTP-innstillingen når planleggingsoptimalisering er aktivert. | Støttes |
| Kopier statisk til dynamisk plan | Kopi av statisk til dynamisk planen er aktivert for parametere for hovedplanlegging. | Planleggingsoptimalisering kopierer ikke den statiske planen til den dynamiske planen, uavhengig av denne innstillingen. Dette konseptet er generelt mindre relevant på grunn av hastigheten og fullføringsregenereringen som gis av planleggingsoptimaliseringen. Hvis det brukes to eller flere planer, bør hovedplanlegging utløses for hver plan. | Ikke tilgjengelig |
| Autorisasjon | Dekningsgrupper med automatisk autorisasjonshorisont angitt: *\#* | I versjon 10.0.7 og senere støttes autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen *Automatisk autorisasjon med planleggingsoptimalisering* er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| Autorisasjon | Dekningsoppføringer for vare med automatisk autorisasjon angitt: *\#* | I versjon 10.0.7 og senere støttes automatisk autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen *Automatisk autorisasjon med planleggingsoptimalisering* er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| Autorisasjon | Hovedplaner med automatisk autorisasjon angitt: *\#* | I versjon 10.0.7 og senere støttes automatisk autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen *Automatisk autorisasjon med planleggingsoptimalisering* er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| FitAnalysisPlanningItems | Planleggingselementer: *\#* | Dette funksjonen venter. For øyeblikket behandles planleggingselementer som vanlige varer når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 eller senere |
| Prognose | Dekningsgrupper med "Ta med konserninterne ordrer" aktivert: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Konsernintern planlegging](Intercompany-planning.md). | Støttes |
| Prognose | Dekningsgrupper med innstillingen "Reduser prognose etter" angir en annen verdi enn "Ordrer": *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging med behovsprognoser](demand-forecast.md). | Støttes |
| Prognose | Prognosemodeller med undermodeller: *\#* |  Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging med behovsprognoser](demand-forecast.md). | Støttes |
| Prognose | Hovedplaner med "Inkluder forsyningsprognose" aktivert: *\#* | Dette funksjonen venter. For øyeblikket støttes ikke forsyningsprognoser når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 eller senere |
| Låsningshorisont | Dekningsgrupper med låsningshorisont angitt: *\#* | Dette funksjonen venter. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Låsningshorisont | Dekningsgrupper for vare med låsningshorisont angitt: *\#* | Dette funksjonen venter. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Låsningshorisont | Hovedplaner med låsningshorisont angitt: *\#* | Dette funksjonen venter. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Konserninternt | Hovedplaner inkludert planlagt nedstrømsetterspørsel: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Konsernintern planlegging](Intercompany-planning.md). | Støttes |
| Kanban | Dekningsoppføringer for vare med Kanban for planlagte ordretype *\#* | Dette funksjonen venter. For øyeblikket ignoreres varedekningen som er satt til Kanban, når planleggingsoptimalisering er aktivert. Den Kanban-planlagte ordretypen vil opprette en advarsel under hovedplanleggingen, og planlagte bestillinger vil bli opprettet for å dekke det tilknyttede behovet. | Fremtidig bølge |
| Kanban | Varer med Kanban for standard ordretype: *\#* | For øyeblikket ignoreres en standard ordretype som er satt til Kanban, når planleggingsoptimalisering er aktivert. Den standard Kanban-ordretypen vil opprette en advarsel under hovedplanleggingen, og planlagte bestillinger vil bli opprettet for å dekke det tilknyttede behovet. | Fremtidig bølge |
| Livssyklustilstand for produkt | Livssyklustilstander for produkt ikke aktive for planlegging: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Ekskludereprodukter som har bestemte livssyklustilstander for produkt](product-lifecycle-state.md). | Støttes |
| Produksjon | Stykklistelinjer med avrunding eller flere oppsett: *\#* | Dette funksjonen venter. Avrunding og flere oppsett ignoreres for øyeblikket på stykklistelinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | Fremtidig bølge|
| Produksjon | Stykkliste/formellinjer med formelmåling: *\#* | Dette funksjonen venter. Formelmåling ignoreres for øyeblikket på stykklistelinjer og formellinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykklister/formellinjer med vareerstatning (plangrupper): *\#* | Dette funksjonen venter. Vareerstatning (plangrupper) ignoreres for øyeblikket på stykklistelinjer og formellinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykkliste/formellinjer med negativt antall: *\#* | Dette funksjonen venter. Stykkliste- og formellinjer med negativt antall vil bli inkludert med et antall på 0 (null), og det vil bli utstedt en advarsel når planleggingsoptimalisering er aktivert. Oppdater hoveddata for å unngå advarsler. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykkliste/formellinjer med ressursforbruk: *\#* | Dette funksjonen venter. For tiden ignoreres stykkliste- og formellinjer som har ressursforbruk når planleggingsoptimalisering er aktivert. Når denne funksjonen støttes, blir materialbehovet satt til startdatoen for produksjon. Før denne funksjonen støttes vil det ikke bli generert behov for materialer som er merket med et ressursforbruksflagg. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykkliste/formellinjer med trinnforbruk: *\#* | Dette funksjonen venter. For tiden ignoreres trinnforbruk på stykkliste- og formellinjer når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykklister med konstant svinn eller variabel svinn definert: *\#* | Dette funksjonen venter. For øyeblikket ignoreres konstant svinn og variabel svinn som er definert i stykklister, når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 |
| Produksjon | Stykklister med utsetting: *\#* | Dette funksjonen støttes nå. | Støttes |
| Produksjon | Stykklister uten område: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Produksjonsplanlegging](production-planning.md). | Støttes |
| Produksjon | Behov med angitt stykkliste eller definerte rutekrav: *\#* | Dette funksjonen venter. For øyeblikket ignoreres de bestemte stykkliste- eller rutebehovene som er definert i behovet (for eksempel en understykkliste eller underrute i en salgsordre) når planleggingsoptimalisering er aktivert. Standard stykklisten eller -ruten vil bli brukt, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Produksjon | Formelversjoner med ko-/biprodukter: *\#* | Dette funksjonen venter. Koprodukter og biprodukter som er knyttet til formelversjonen, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 |
| Produksjon | Formelversjoner med avkastning: *\#* | Dette funksjonen venter. Avkastning som er knyttet til formelversjonen, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | lanseringsbølge 2 i 2022 |
| Produksjon | Planer inkludert sekvensering: *\#* | Dette funksjonen venter. For øyeblikket ignoreres sekvensiering når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Produksjon | Frigitte produksjonsordre som ikke er startet, og der planlagt start er tidligere enn i dag: *\#* | Dette funksjonen venter. For øyeblikket vil hovedplanleggingen anta at den blir fullført i dag hvis en produksjonsordre blir forsinket. Dette er relevant for frigitte produksjonsordrer der en leveringsdato er i fortiden, men ennå ikke er fullført. | Fremtidig bølge |
| Produksjon | Ressurser som er planlagt med begrenset kapasitet: *\#* | Dette funksjonen venter. Ressurser som er planlagt med begrenset kapasitet, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. Planleggingen utføres basert på standard leveringstid fra produktet. | lanseringsbølge 2 i 2022 |
| Produksjon | Ruter som brukes i planleggingen: *\#* | Dette funksjonen støttes. | Støttes |
| Produksjon | Salgslinjereservasjon ved hjelp av nedbryting: *\#* | Salgslinjereservasjon som bruker nedbryting, støttes ikke når planleggingsoptimalisering er aktivert. | Fremtidig bølge |
| Produksjon | Planlegging med nedbryting av produksjonsordre: *\#* | Planlegging som bruker nedbryting av produksjonsordrer, støttes ikke når planleggingsoptimalisering er aktivert. Produksjonsordrer kan planlegges enkeltvis. | Fremtidig bølge |
| Tilbudsforespørsler | Hovedplaner med tilbudsforespørsler aktivert: *\#* | Dette funksjonen venter. Tilbudsforespørsler vurderes for øyeblikket ikke som behov når planleggingsoptimalisering aktiveres. De vil ignoreres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 |
| Rekvisisjoner | Hovedplaner med rekvisisjoner aktivert: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Innkjøpsrekvisisjoner](purchase-requisitions.md). | Støttes |
| Sikkerhetsmarginer | Dekningsgrupper med sikkerhetsmargin: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Sikkerhetsmarginer](safety-margins.md). | Støttes |
| Sikkerhetsmarginer | Hovedplaner med sikkerhetsmargin: *\#* | Dette funksjonen støttes nå. Hvis du vil ha mer informasjon, kan du se [Sikkerhetsmarginer](safety-margins.md). |  Støttes |
| Fullføring av sikkerhetslager | Varedekningsposter med "Fyll opp minimum" forskjellig fra "Dagens dato + leveringstid": *\#* | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid*. Denne endringen gjøres for å forberede et forenklet planleggingsoppsett i fremtiden, og for å tilby et gjennomførbart resultat. Hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for den gjeldende lagerbeholdningen, alltid bli forsinket på grunn av leveringstiden. Denne virkemåten kan føre til betydelig støy og uønskede planlagte bestillinger. Den beste fremgangsmåten er å endre innstillingen slik at *Dagens dato + leveringstid* brukes. Oppdater hoveddata for å unngå advarsler. | I/T |
| Salgstilbud | Hovedplaner med salgstilbud aktivert: *\#* | Dette funksjonen venter. Tilbud ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | lanseringsbølge 2 i 2022 eller senere |
| Holdbarhet | Hovedplaner med holdbarhet aktivert: *\#* | Dette funksjonen venter. For øyeblikket ignoreres holdbarhet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | Støttes |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Forskjeller mellom klassisk hovedplanlegging og planleggingsoptimalisering](planning-optimization-differences-with-built-in.md)

[Parametere som ikke brukes av planleggingsoptimalisering](not-used-parameters.md)

[Vis planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
