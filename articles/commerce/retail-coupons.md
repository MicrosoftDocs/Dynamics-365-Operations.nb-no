---
title: Definere kuponger for detaljhandelssalg
description: Dette emnet gir en oversikt over kuponger, og forklarer hvordan du foretar oppsettet.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: bc79970528e23397b756fa15a715fba834edcc06e4522c6c35b64aede4976300
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745314"
---
# <a name="set-up-coupons-for-retail-sales"></a>Definere kuponger for detaljhandelssalg

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Oversikt over kuponger

Kuponger er koder og strekkoder som brukes til å legge til rabatter i transaksjoner. Hver kupong kan ha flere koder, og hver kode kan ha egne gyldighetsdatoer.

Hver kupong er knyttet til én rabatt. Prisgruppene som er tilknyttet rabatten, definerer kundene som kan bruke en kupong eller kanalene der en kupong er gyldig.

Kuponger er en tilleggsvalidering av rabatter. Kupongen inneholder kupongkoder og strekkoder som er obligatoriske, sammen med tidsrom for kodene. Kupongen tilbyr også valgfrie bruksgrenser og egenskaper som kreves for kunder. Rabatten gir settet med produkter som kupongen er gyldig for. Prisgruppene for rabatten inneholder settet med kunder, kanaler eller kataloger som kupongen er gyldig for.

Hvis du vil opprette en kupong, oppretter du rabatten og kupongen separat. Deretter kobler du dem ved å velge rabatten på kupongsiden i Commerce.

> [!NOTE]
> Når en kupong er koblet til en rabatt, blir flere felt på rabattsiden i Commerce skrivebeskyttet, fordi de styres av kuponginnstillingene. Disse feltene omfatter feltene for status og standard datointervall.
> 
> Når du bruker kupongen i telefonsenterkanalen, må du velge **Omberegn**-knappen **(Selg-fanen > Beregn > Omberegn)** for at rabatten som er knyttet til kupongen, skal bli brukt. Dette tilleggstrinnet blir fjernet i en fremtidig versjon.

### <a name="limited-use-coupons"></a>Kuponger med begrenset bruk

Du kan konfigurere kuponger som kuponger med begrenset bruk. Bruksgrensen kan defineres per kunde eller kanal, eller som en global begrensning. Denne begrensningen fremtvinges når koden eller strekkoden angis eller skannes i POS eller ved registrering av salgsordre.

Grensen brukes per kode på en kupong. En engangskupong som har to kupongkoder, kan for eksempel brukes to ganger: én gang for hver kupongkode. Hver kode i en kupong kan uavhengig settes til aktiv.

Kupongene kan brukes i alle salgskanaler, men kuponger med begrensninger kan bare brukes for telefonsenterordrer der **Ordrefullføring**-innstillingen er aktivert for telefonsenteret. Hvis denne innstillingen ikke er aktivert, kan bare ubegrensede kuponger brukes i telefonsenterordre.

> [!NOTE]
> Når grensen for bruk av en kupongkode er nådd, endrer *ikke* systemet automatisk statusen for kupongkoden til "Brukes". Denne kupongkoden har imidlertid nådd bruksgrensen, og kan ikke brukes. Hvis statusen for en kupongkode er manuelt satt til annet enn **Aktiv**, kan ikke denne kupongkoden som ikke kan brukes i noen kanaler.  

## <a name="managing-coupons"></a>Behandle kuponger

Du må opprette rabatten og kupongen separat. Deretter kobler du dem ved å velge rabatten på kupongsiden. Når en kupong er koblet til en rabatt, blir flere felt for rabatten skrivebeskyttet, fordi de styres av kuponginnstillingene. Disse feltene omfatter feltene for status og standard datointervall.

Kuponger er nå en tilleggsvalidering av rabatter. Kupongen inneholder kupongkoder og strekkoder, sammen med datoområder, bruksgrenser og egenskapen som kreves for kunden. Rabatten gir settet med produkter som kupongen er gyldig for. Prisgruppene for rabatten inneholder settet med kunder, kanaler eller kataloger som kupongen er gyldig for.

## <a name="system-setup-for-coupons"></a>Systemkonfigurasjon for kuponger

Før du kan definere en kupong, må du definere kupongens strekkode og to nummerserier for kupongen.

1. På **Masketegn**-siden kan du opprette et nytt masketegn for kupongkoden. Du kan velge alle ubrukte tegn.
2. På siden **Oppsett for strekkodemaske** oppretter du en ny strekkodemaske. Sett **Type**-feltet til **Kupong**.
3. På siden **Strekkodeoppsett** oppretter du en ny strekkode som bruker strekkodemasken du nettopp opprettet.
4. På **Nummerserier**-siden oppretter du to nye nummerserier. Én sekvens er for kupongkode-ID-en, og den andre serien er for kupongnummeret. Kupongkoden-ID-en er den unike identifikatoren for hver kode for en kupong. Kupongnummeret er en unik ID for kupongen. Hver kupong kan ha flere koder og strekkoder som utløser kupongen.

    > [!NOTE]
    > For begge nummerserier må du angi **Område**-feltet til **Firma**. I de fleste tilfeller bør du automatisk generere begge serienumrene.

5. På siden **Handelsparametere**, i kategorien **Strekkoder**, velger du strekkoden du opprettet tidligere.
6. På siden **Delte handelsparametere**, i kategorien **Nummerserier**, velger du nummerseriene du opprettet for kupongnummeret og kupongkode-IDen.
7. Du kan åpne **Kuponger**-siden og opprette nye kuponger.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Virkningen av delvis oppdateringer på kuponger

Kupongfunksjonen består av flere forskjellige funksjoner. Commerce Headquarters (HQ) og kanalen kan delvis oppdateres på tvers av komponenter. Det er derfor viktig at du forstår hvordan delvise oppdateringer påvirker kupongfunksjonaliteten i sin helhet.

- **Hovedkontor oppdateres delvis, men Commerce Scale Unit og POS oppdateres ikke.** I en Hovedkontor-oppdatering oppdateres kupong- og rabattsidene, og utsalgsprismotoren oppdateres også. Hvis bare én av de to komponentene oppdateres, vil enkelte av sidene i Commerce ikke stemme overens med prisberegningsdataene. Derfor kan uventede kontantberegninger eller feil oppstå under rabattberegninger.
- **Hovedkontor oppdateres, men Commerce Scale Unit og POS oppdateres ikke (N-1).** Fordi ikke alle butikker kan oppdateres samtidig, anbefaler vi at du oppdaterer Hovedkontor før du oppdaterer butikker. I scenarioet med N-1 vil ikke ny funksjonalitet som er knyttet til kuponger, være tilgjengelig i butikker som ennå ikke er oppdatert. Kupongfunksjonen introduserer for eksempel "utelat" linjer. Hvis du utelater linjer i en rabatt, kan de ikke brukes i en butikk som kjører en tidligere versjon.
- **Hovedkontor oppdateres ikke, men Commerce Scale Unit og POS oppdateres (N+1).** Fordi den oppdaterte prismotoren i Commerce Scale Unit kan håndtere eldre rabattkoder under prisberegninger, skal ikke oppdateringen ha noen funksjonell innvirkning i dette scenariet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
