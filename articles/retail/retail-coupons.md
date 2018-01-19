---
title: Opprette kuponger for detaljhandelssalg
description: Dette emnet gir en oversikt over detaljhandelskuponger, og forklarer hvordan du foretar oppsettet.
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>Opprette kuponger for detaljhandelssalg

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Oversikt over kuponger

Kuponger er koder og strekkoder som brukes til å legge til detaljhandelrabatter i transaksjoner. Hver kupong kan ha flere koder, og hver kode kan ha egne gyldighetsdatoer. 

Hver kupong er knyttet til en detaljhandelrabatt. Prisgruppene som er tilknyttet rabatten, definerer kundene som kan bruke en kupong eller kanalene der en kupong er gyldig. 

Kuponger er en tilleggsvalidering av detaljhandelrabatter. Kupongen inneholder kupongkoder og strekkoder som er obligatoriske, sammen med tidsrom for kodene. Kupongen tilbyr også valgfrie bruksgrenser og egenskaper som kreves for kunder. Rabatten gir settet med produkter som kupongen er gyldig for. Prisgruppene for rabatten inneholder settet med kunder, kanaler eller kataloger som kupongen er gyldig for.

Hvis du vil opprette en kupong, oppretter du rabatten og kupongen separat. Deretter kobler du dem ved å velge rabatten på kupongsiden i Microsoft Dynamics 365 for Retail. 

> [!NOTE]
> Når en kupong er koblet til en rabatt, blir flere felt på rabattsiden i Microsoft Dynamics 365 for Retail skrivebeskyttet, fordi de styres av kuponginnstillingene. Disse feltene omfatter feltene for status og standard datointervall.

### <a name="limited-use-coupons"></a>Kuponger med begrenset bruk

Du kan konfigurere kuponger som kuponger med begrenset bruk. Bruksgrensen kan defineres per kunde eller kanal, eller som en global begrensning. Denne begrensningen fremtvinges når koden eller strekkoden angis eller skannes i POS eller ved registrering av salgsordre. En kupong registreres som brukt når en ordre er fullført med kupongen som er knyttet til den.

Grensen brukes per kode på en kupong. En engangskupong som har to kupongkoder, kan for eksempel brukes to ganger: én gang for hver kupongkode. Hver kode i en kupong kan uavhengig settes til aktiv.

## <a name="managing-coupons"></a>Behandle kuponger

Du må opprette rabatten og kupongen separat. Deretter kobler du dem ved å velge rabatten på kupongsiden. Når en kupong er koblet til en rabatt, blir flere felt for rabatten skrivebeskyttet, fordi de styres av kuponginnstillingene. Disse feltene omfatter feltene for status og standard datointervall.  

Kuponger er nå en tilleggsvalidering av detaljhandelrabatter. Kupongen inneholder kupongkoder og strekkoder, sammen med datoområder, bruksgrenser og egenskapen som kreves for kunden. Rabatten gir settet med produkter som kupongen er gyldig for. Prisgruppene for rabatten inneholder settet med kunder, kanaler eller kataloger som kupongen er gyldig for.

## <a name="system-setup-for-coupons"></a>Systemkonfigurasjon for kuponger 

Før du kan definere en kupong, må du definere kupongens strekkode og to nummerserier for kupongen. 

1.  På **Masketegn**-siden kan du opprette et nytt masketegn for kupongkoden. Du kan velge alle ubrukte tegn.
2.  På siden **Oppsett for strekkodemaske** oppretter du en ny strekkodemaske. Sett **Type**-feltet til **Kupong**.
3.  På siden **Strekkodeoppsett** oppretter du en ny strekkode som bruker strekkodemasken du nettopp opprettet.
4.  På **Nummerserier**-siden oppretter du to nye nummerserier. Én sekvens er for kupongkode-ID-en, og den andre serien er for kupongnummeret. Kupongkoden-ID-en er den unike identifikatoren for hver kode for en kupong. Kupongnummeret er en unik ID for kupongen. Hver kupong kan ha flere koder og strekkoder som utløser kupongen.

    > [!NOTE]
    > For begge nummerserier må du angi **Område**-feltet til **Firma**. I de fleste tilfeller bør du automatisk generere begge serienumrene.

5.  På siden **Delte parametere for detaljhandel**, i kategorien **Strekkoder**, velger du strekkoden du opprettet tidligere.
6.  På siden **Detaljhandelsparametere**, i kategorien **Nummerserier**, velger du nummerseriene du opprettet for kupongnummeret og kupongkode-IDen.
7.  Du kan åpne **Kuponger**-siden og opprette nye kuponger.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Virkningen av delvis oppdateringer på kuponger

Kupongfunksjonen består av flere forskjellige funksjoner i Dynamics 365 for Retail. Microsoft Dynamics 365 for Detaljhandel Hovedkontor og kanalen kan delvis oppdateres på tvers av komponenter. Det er derfor viktig at du forstår hvordan delvise oppdateringer påvirker kupongfunksjonaliteten i sin helhet.

- **Hovedkontor oppdateres delvis, men Retail og POS oppdateres ikke.** I en Hovedkontor-oppdatering oppdateres kupong- og rabattsidene, og utsalgsprismotoren oppdateres også. Hvis bare én av de to komponentene oppdateres, vil enkelte av sidene i detaljhandel ikke stemme overens med prisberegningsdataene. Derfor kan uventede kontantberegninger eller feil oppstå under rabattberegninger.
- **Hovedkontor oppdateres, men Retail og POS oppdateres ikke (N-1).** Fordi ikke alle detaljhandelbutikker kan oppdateres samtidig, anbefaler vi at du oppdaterer Hovedkontor før du oppdaterer detaljhandelbutikker. I scenarioet med N-1 vil ikke ny funksjonalitet som er knyttet til kuponger, være tilgjengelig i butikker som ennå ikke er oppdatert. Kupongfunksjonen introduserer for eksempel "utelat" linjer. Hvis du bruker utelat linjer i en rabatt, kan de ikke brukes i en butikk for detaljhandel som kjører en tidligere versjon.
- **Hovedkontor oppdateres ikke, men detaljhandelsserver og POS oppdateres (N+1).** Fordi den oppdaterte prismotoren i detaljhandelsserver kan håndtere eldre rabattkoder under prisberegninger, skal ikke oppdateringen ha noen funksjonell innvirkning i dette scenariet.

