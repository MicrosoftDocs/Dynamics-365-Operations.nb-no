---
title: Feilsøke hovedplanlegging
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med hovedplanlegging.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809476"
---
# <a name="troubleshoot-master-planning"></a>Feilsøke hovedplanlegging

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med hovedplanlegging.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Stykklistenedbryting er forskjellig for autoriserte produksjonsordrer og for estimerte produksjonsordrer for manuelt opprettet arbeid.

### <a name="issue-description"></a>Problembeskrivelse

Når en produksjonsordre blir autorisert, blir ikke varene nedbrutt når du deler opp stykklisten. Når du oppretter en arbeidsordre manuelt og deretter estimerer produksjonsordren, deles imidlertid varene opp.

### <a name="issue-resolution"></a>Problemløsning

Systemet fungerer som forventet. Nedbrytingen som skjer når produksjonsordren autoriseres, vil peke mot den planlagte ordren, men den viser ikke at den planlagte ordren for øyeblikket er autorisert i dette tilfellet. Hvis imidlertid produksjonsordren er estimert, utløses nedbrytingen fra den frigitte produksjonsordren der det ikke finnes noen planlagt ordre.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Forsinkelsesverdien oppdateres ikke når jeg planlegger en planlagt ordre på nytt.

Hvis du vil oppdatere forsinkelsen for planlagte ordrer, åpner du dialogboksen **Ny planlegging** for den planlagte ordren. I hurtigfanen **Nedbryting** kontrollerer du at alternativet **Utfør nedbryting etter ny planlegging** er satt til *Ja*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Produksjonsplanlegging tar ikke hensyn til sikkerhetsmarginene som er angitt for varedekningen for tilknyttet forsyning.

### <a name="issue-description"></a>Problembeskrivelse

Hovedplanleggingen anser sikkerhetsmarginene. Sikkerhetsmarginer ignoreres imidlertid når planlagte produksjonsordrer planlegges.

### <a name="issue-resolution"></a>Problemløsning

Marger vurderes bare under hovedplanlegging, ikke under manuell planlegging. Marger er utformet for å fungere som en buffer i planleggingsfasen for å gi litt margin for den faktiske prosessen.

Hvis du vil oppnå ønsket resultat, kan du fjerne marginen. Ruten må deretter oppdateres slik at den inneholder ønsket tid (for eksempel køtid). Samtidig skal både hovedplanlegging og manuell planlegging gi samme resultat.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Planlagte ordrer genereres selv om vi har varer på lager og produksjonsordrer allerede finnes for dem.

Det kan hende at du kan løse dette problemet ved å øke verdien **Positive dager** for de relevante gruppene på siden **Dekningsgruppe**. Denne endringen vil føre til at systemet fastslår om lagerbeholdningen kan brukes for behovet. Da vil det ikke bli generert en ny planlagt ordre for varene som er på lager.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Hovedplanleggingen ser ikke ut til å respektere kapasitetsbegrensninger og planlegger mer enn tilgjengelig kapasitet.

### <a name="issue-description"></a>Problembeskrivelse

Når du bruker grovplanlegging der det er begrenset kapasitet, og der ruten angir en blanding av krav for både en ressursgruppe og individuelle ressurser, er det en liten sjanse for overbestilling på grunn av måten algoritmen validerer på kapasitetskonflikter på. Denne overbestillingen kan forekomme når du bruker hjelpeprogrammer til å kjøre hovedplanlegging. Det er mest sannsynlig at det oppstår hvis det finnes mange jobber som har en relativt kort kjøretid.

### <a name="issue-resolution"></a>Problemløsning

Hvis det er viktig at ingen overbestilling forekommer for grovplanlegging, kan du gjøre planleggingsdelen av enkelttrådbasert hovedplanlegging ved å aktivere alternativet **Nøyaktig, begrenset kapasitet for grovplanlegging** på siden **Parametere for hovedplanlegging**. Dette alternativet er ikke tilgjengelig som standard. Du må legge den til siden manuelt ved hjelp av tilpasningsfunksjonene. Når du bruker dette alternativet, vil planleggingen kjøre saktere på grunn av mangelen på parallell behandling.

## <a name="planned-orders-take-a-long-time-to-update"></a>Det tar lang tid å oppdatere planlagte ordrer.

### <a name="issue-description"></a>Problembeskrivelse

Når du oppdaterer behovsantallet eller leveringsdatoen på en planlagt ordre, tar det vanligvis minst 30 sekunder per ordre for å lagre oppdateringen.

### <a name="issue-resolution"></a>Problemløsning

Dette er et kjent problem med den innebygde hovedplanleggingsmotoren. Det skyldes den underliggende automatiske nedbrytingen gjennom stykklistestrukturen under redigeringer. Dette problemet omtales i planleggingsoptimalisering, der en planlegger kan oppdatere og godkjenne de relevante ordrene og, når det er ønskelig, utløse en planleggingskjøring for å oppdatere planlagte ordrer for den underliggende stykklistestrukturen.

Én måte å forbedre ytelsen med den innebygde hovedplanleggingsmotoren på er å gjøre følgende:

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en plan.
1. Utvid hurtigfanen **Horisont i dager**.
1. Angi **Nedbryting** til *Ja*, og sett feltet under denne innstillingen til 0 (null).

> [!NOTE]
> Dette vil begrense perioden for nedbrytinger som utføres for denne hovedplanen, til én enkelt dag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]