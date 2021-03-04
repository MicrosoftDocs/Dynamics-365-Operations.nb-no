---
title: Tilpassingsanalyse av planleggingsoptimalisering
description: Dette emnet forklarer hvordan du kontrollerer gjeldende oppsett og data mot funksjonene i planleggingsoptimaliseringsfunksjonaliteten.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 769bd84b4ba23c9de4638df9186381936221414a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434432"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse for tilpassing av planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Du bør analysere resultatet fra analyse for tilpassing av planleggingsoptimalisering som en del av migreringsprosessen. Vær oppmerksom på at planleggingsoptimalisering ikke er lik gjeldende innebygde funksjon for hovedplanlegging. Vi anbefaler at du arbeider med partneren og leser dokumentasjonen for å klargjøre migreringen. 

Analyse for tilpassing av planleggingsoptimalisering lar deg identifisere hvor resultatet kan variere mellom den innebygde hovedplanleggingsmotoren og planleggingsoptimaliseringen. Denne analysen utføres basert på gjeldende oppsett og data. 

Hvis du vil se resultatet for analyse for tilpassing av planleggingsoptimalisering, kan du gå til **Hovedplanlegging** \> **Oppsett** \> **Analyse for tilpassing av planleggingsoptimalisering** og deretter velge **Kjør analyse**. Hvis analysen finner noen uregelmessigheter, vises de på samme side. (Det kan ta noen minutter å kjøre analysen.)

> [!NOTE]
> Hvis det blir funnet uoverensstemmelser, kan du likevel bruke planleggingsoptimalisering. Resultatene av tilpassingsanalysen viser bare steder der planleggingstjenesten ikke respekterer det gjeldende oppsettet. De viser med andre ord steder der noen prosesser kan bli ignorert, eller det er ikke sikkert at de støttes.

## <a name="analysis-results-example-1"></a>Analyseresultater: eksempel 1

- **Funksjon:** produksjon
- **Problem:** Varer med en stykklistenivå som er større enn null: 56
- **Forklaring:** tilpassingsanalysen fant 56 varer som har et oppsett for stykklister for produksjon. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter produksjon, genererer planleggingsoptimalisering bestillingsforslag i stedet for planlagte produksjonsordrer. Den vil også vise en advarsel som viser de berørte varene.

## <a name="analysis-results-example-2"></a>Analyseresultater: eksempel 2

- **Funksjon:** handlinger
- **Problem:** dekningsgrupper med handlingsberegning aktivert: 6
- **Forklaring:** Tilpassingsanalysen fant seks dekningsgrupper der handlingsberegning er aktivert. Fordi den gjeldende versjonen av planleggingsoptimalisering ikke støtter handlinger, blir det ikke generert noen handlinger under hovedplanleggingen.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Oversikt over mulige resultater fra tilpassingsanalysen

Følgende tabell viser de ulike resultatene som kan vises etter en tilpassingsanalyse. Nummertegn (_\#_) erstattes med et tall som angir antallet poster som har det angitte problemet.

| Funksjon | Oppført problem | Forklaring | Forventet tilgjengelighet |
| --- | --- | --- | --- |
| Handlinger | Dekningsgrupper med handlingsberegning aktivert: _\#_ | Dette funksjonen venter. For øyeblikket blir det ikke generert handlinger under hovedplanlegging når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. Hovedformålet med handlinger er å foreslå endringer i eksisterende ordrer. Evaluer hvis handlinger aktiveres aktivt som en del av forretningsprosessene, eller hvis forsinkelsesinformasjonen som er knyttet til ordrene, er tilstrekkelig. | 2021. oktober |
| Basiskalendere | Kalendere som bruker basiskalender: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres basiskalenderen når planleggingsoptimalisering er aktivert. Evaluer om basiskalenderen er nødvendig for forretningsprosessene, eller om direkte oppsett i kalendere er tilstrekkelig. | 2021. april | 
| Partidisposisjonskoder | Ikke-nettbare partidisposisjonsstandarder: _\#_ | Dette funksjonen venter. Partidisposisjonskoder ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Leveringskapasitet | Standard ordreinnstillinger med leveringsdatokontroll satt til CTP: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres CTP når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | 2021. oktober |
| Kopier statisk til dynamisk plan | Kopi av statisk til dynamisk planen er aktivert for parametere for hovedplanlegging. | Planleggingsoptimalisering kopierer ikke den statiske planen til den dynamiske planen, uavhengig av denne innstillingen. Dette konseptet er generelt mindre relevant på grunn av hastigheten og fullføringsregenereringen som gis av planleggingsoptimaliseringen. Hvis det brukes to eller flere planer, bør hovedplanlegging utløses for hver plan. | 2021. oktober |
| Autorisasjon | Dekningsgrupper med horisont for automatisk autorisering angitt: _\#_ | I versjon 10.0.7 og senere støttes autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen _Automatisk autorisasjon med planleggingsoptimalisering_ er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| Autorisasjon | Dekningsoppføringer for vare med automatisk autorisasjon angitt: _\#_ | I versjon 10.0.7 og senere støttes automatisk autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen _Automatisk autorisasjon med planleggingsoptimalisering_ er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| Autorisasjon | Hovedplaner med automatisk autorisasjon angitt: _\#_ | I versjon 10.0.7 og senere støttes automatisk autorisasjon som en separat satsvis jobb etter at hovedplanleggingen er fullført (forutsatt at funksjonen _Automatisk autorisasjon med planleggingsoptimalisering_ er aktivert i [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Legg merke til at automatisk autorisasjon med planleggingsoptimalisering er basert på ordredatoen (startdato), ikke behovsdatoen (sluttdatoen). Denne virkemåten sikrer at planlagte bestillinger vises i forfallstiden, uten at leveringstiden i autorisasjonshorisonten må tas med. | Støttes |
| FitAnalysisPlanningItems | Planleggingselementer: _\#_ | Dette funksjonen venter. For øyeblikket behandles planleggingselementer som vanlige varer når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Prognose | Dekningsgrupper med "Ta med konserninterne ordrer" aktivert: _\#_ | Dette funksjonen venter. For øyeblikket inkluderer ikke hovedplanlegging nedstrøms planlagt behov når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. Merk at frigitte/autoriserte ordrer fremdeles fungerer med den vanlige konserninterne funksjonaliteten, og vil dekke de fleste scenarier. | 2020. oktober |
| Prognose | Dekningsgrupper med innstillingen "Reduser prognose etter" angir en annen verdi enn "Ordrer": _\#_ | Planleggingsoptimalisering bruker som standard "Reduser prognose etter" for ordrer, uavhengig av denne innstillingen. | November 2020 |
| Prognose | Prognosemodeller med undermodeller: _\#_ | Dette funksjonen venter. For øyeblikket støttes ikke prognoser som bruker undermodeller, når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | 2021. april |
| Prognose | Hovedplaner med "Inkluder forsyningsprognose" aktivert: _\#_ | Dette funksjonen venter. For øyeblikket støttes ikke forsyningsprognoser når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | 2021. oktober |
| Låsningshorisont | Dekningsgrupper med låsningshorisont angitt: _\#_ | Låsingshorisonten brukes ikke ofte, og det er ingen planer om å ta den med for planleggingsoptimalisering. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | I/T |
| Låsningshorisont | Dekningsgrupper for vare med låsningshorisont angitt: _\#_ | Låsingshorisonten brukes ikke ofte, og det er ingen planer om å ta den med for planleggingsoptimalisering. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | I/T |
| Låsningshorisont | Hovedplaner med låsningshorisont angitt: _\#_ | Låsingshorisonten brukes ikke ofte, og det er ingen planer om å ta den med for planleggingsoptimalisering. For øyeblikket ignoreres låsningshorisontoppsettet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | I/T |
| Konserninternt | Hovedplaner inkludert planlagt nedstrømsetterspørsel: _\#_ | Dette funksjonen venter. For øyeblikket inkluderer ikke hovedplanlegging nedstrøms planlagt behov når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. Merk at frigitte/autoriserte ordrer fremdeles fungerer med den vanlige konserninterne funksjonaliteten, og vil dekke de fleste scenarier. | 2020. oktober |
| Kanban | Dekningsoppføringer for vare med Kanban for planlagte ordretype _\#_ | Dette funksjonen venter. For øyeblikket ignoreres varedekningen som er satt til Kanban, når planleggingsoptimalisering er aktivert. Den Kanban-planlagte ordretypen vil opprette en advarsel under hovedplanleggingen, og planlagte bestillinger vil bli opprettet for å dekke det tilknyttede behovet. | 2021. oktober |
| Kanban | Varer med Kanban for standard ordretype: _\#_ | For øyeblikket ignoreres en standard ordretype som er satt til Kanban, når planleggingsoptimalisering er aktivert. Den standard Kanban-ordretypen vil opprette en advarsel under hovedplanleggingen, og planlagte bestillinger vil bli opprettet for å dekke det tilknyttede behovet. | 2021. oktober |
| Livssyklustilstand for produkt   | Statuser for produktlivssyklus ikke aktive for planlegging: _\#_ | Dette er en ventende funksjon. For øyeblikket ignoreres Livssyklustilstand for produkt med Planleggingsoptimalisering aktivert. Du kan justere produktfilteret for plannivå for å unngå å ta med produkter der statusen for produktlivssyklus er deaktivert for planlegging. | November 2020 |
| Produksjon | Stykklistelinjer med avrunding eller flere oppsett: _\#_ | Dette funksjonen venter. Avrunding og flere oppsett ignoreres for øyeblikket på stykklistelinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | 2021. april |
| Produksjon | Stykkliste/formellinjer med formelmåling: _\#_ | Dette funksjonen venter. Formelmåling ignoreres for øyeblikket på stykklistelinjer og formellinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | 2021. oktober |
| Produksjon | Stykklister/formellinjer med vareerstatning (plangrupper): _\#_ | Dette funksjonen venter. Vareerstatning (plangrupper) ignoreres for øyeblikket på stykklistelinjer og formellinjer når planleggingsoptimalisering er aktivert, uavhengig av denne innstillingen. | 2021. oktober |
| Produksjon | Stykkliste/formellinjer med negativt antall: _\#_ | Dette funksjonen venter. Stykkliste- og formellinjer med negativt antall vil bli inkludert med et antall på 0 (null), og det vil bli utstedt en advarsel når planleggingsoptimalisering er aktivert. Oppdater hoveddata for å unngå advarsler. | 2021. oktober |
| Produksjon | Stykkliste/formellinjer med ressursforbruk: _\#_ | Dette funksjonen venter. For tiden ignoreres stykkliste- og formellinjer som har ressursforbruk når planleggingsoptimalisering er aktivert. Når denne funksjonen støttes, blir materialbehovet satt til startdatoen for produksjon. Før denne funksjonen støttes vil det ikke bli generert behov for materialer som er merket med et ressursforbruksflagg. | 2021. april |
| Produksjon | Stykkliste/formellinjer med trinnforbruk: _\#_ | Dette funksjonen venter. For tiden ignoreres trinnforbruk på stykkliste- og formellinjer når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Produksjon | Stykklister med konstant svinn eller variabel svinn definert: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres konstant svinn og variabel svinn som er definert i stykklister, når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Produksjon | Stykklister med utsetting: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres utsettingsoppsett på stykklister når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | 2021. oktober |
| Produksjon | Stykklister uten område: _\#_ | Dette funksjonen venter. Stykklister uten område ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | 2020. oktober |
| Produksjon | Behov med angitt stykkliste eller definerte rutekrav: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres de bestemte stykkliste- eller rutebehovene som er definert i behovet (for eksempel en understykkliste eller underrute i en salgsordre) når planleggingsoptimalisering er aktivert. Standard stykklisten eller -ruten vil bli brukt, uavhengig av denne innstillingen. | 2021. oktober |
| Produksjon | Formelversjoner med ko-/biprodukter: _\#_ | Dette funksjonen venter. Koprodukter og biprodukter som er knyttet til formelversjonen, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Produksjon | Formelversjoner med avkastning: _\#_ | Dette funksjonen venter. Avkastning som er knyttet til formelversjonen, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Produksjon | Planer inkludert sekvensering: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres sekvensiering når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | 2021. oktober |
| Produksjon | Frigitte produksjonsordre som ikke er startet, og der planlagt start er tidligere enn i dag: _\#_ | Dette funksjonen venter. For øyeblikket vil hovedplanleggingen anta at den blir fullført i dag hvis en produksjonsordre blir forsinket. Dette er relevant for frigitte produksjonsordrer der en leveringsdato er i fortiden, men ennå ikke er fullført. | 2021. oktober |
| Produksjon | Ressurser som er planlagt med begrenset kapasitet: _\#_ | Dette funksjonen venter. Ressurser som er planlagt med begrenset kapasitet, ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. Planleggingen utføres basert på standard leveringstid fra produktet. | 2021. april |
| Produksjon | Ruter som brukes i planleggingen: _\#_ | Dette funksjonen venter. Ruter ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. Standard leveringstid fra produktet brukes. | 2021. april |
| Produksjon | Salgslinjereservasjon ved hjelp av nedbryting: _\#_ | Salgslinjereservasjon som bruker nedbryting, støttes ikke når planleggingsoptimalisering er aktivert. | 2021. oktober |
| Produksjon | Planlegging med nedbryting av produksjonsordre: _\#_ | Planlegging som bruker nedbryting av produksjonsordrer, støttes ikke når planleggingsoptimalisering er aktivert. Produksjonsordrer kan planlegges enkeltvis. | 2021. oktober |
| Tilbudsforespørsler | Hovedplaner med tilbudsforespørsler aktivert: _\#_ | Dette funksjonen venter. Tilbudsforespørsler vurderes for øyeblikket ikke som behov når planleggingsoptimalisering aktiveres. De vil ignoreres, uavhengig av denne innstillingen. | 2021. oktober |
| Rekvisisjoner | Hovedplaner med rekvisisjoner aktivert: _\#_ | Dette funksjonen venter. Rekvisisjoner ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | 2021. oktober |
| Sikkerhetsmarginer | Dekningsgrupper med sikkerhetsmargin: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres sikkerhetsmargin når planleggingsoptimalisering er aktivert. Hvis du vil kompensere for denne virkemåten, kan du øke leveringstiden slik at den inkluderer sikkerhetsmarginen. | 2020. oktober |
| Sikkerhetsmarginer | Hovedplaner med sikkerhetsmargin: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres sikkerhetsmargin når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. Hvis du vil kompensere for denne virkemåten, kan du øke leveringstiden slik at den inkluderer sikkerhetsmarginen. | 2020. oktober |
| Fullføring av sikkerhetslager | Varedekningsposter med "Fyll opp minimum" forskjellig fra "Dagens dato + leveringstid": _\#_ | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid*. Denne endringen gjøres for å forberede et forenklet planleggingsoppsett i fremtiden, og for å tilby et gjennomførbart resultat. Hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for den gjeldende lagerbeholdningen, alltid bli forsinket på grunn av leveringstiden. Denne virkemåten kan føre til betydelig støy og uønskede planlagte bestillinger. Den beste fremgangsmåten er å endre innstillingen slik at *Dagens dato + leveringstid* brukes. Oppdater hoveddata for å unngå advarsler. | I/T |
| Salgstilbud | Hovedplaner med salgstilbud aktivert: _\#_ | Dette funksjonen venter. Tilbud ignoreres for øyeblikket når planleggingsoptimalisering er aktivert. De vil ignoreres, uavhengig av denne innstillingen. | 2021. oktober |
| Holdbarhet | Hovedplaner med holdbarhet aktivert: _\#_ | Dette funksjonen venter. For øyeblikket ignoreres holdbarhet når planleggingsoptimalisering aktiveres, uavhengig av denne innstillingen. | 2021. oktober |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over planleggingsoptimalisering](planning-optimization-overview.md)

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Vise planhistorikk og planleggingslogger](plan-history-logs.md)

[Bruke filtre på en plan](plan-filters.md)

[Annullere en planleggingsjobb](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]