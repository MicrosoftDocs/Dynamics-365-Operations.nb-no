---
title: Opprette en produktkonfigurasjonsmodell
description: Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bdbf9a0708a8e5ae15516ffd603fa0e01595dc8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147808"
---
# <a name="create-a-product-configuration-model"></a>Opprette en produktkonfigurasjonsmodell

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-product-model"></a>Opprette en produktmodell
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktkonfigurasjonsmodeller.
3. Klikk Ny.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Velg et alternativ i feltet Problemløserstrategi.
    * Problemløserstrategien bestemmer hvordan restriksjonene i en restriksjonsbasert produktkonfigurasjonsmodell skal behandles. Dette valget kan ha innvirkning på ytelsen til produktkonfigurasjonsmodellen.  
7. Skriv inn en verdi i Navn-feltet.
    * Rotkomponenten representerer produktkonfigurasjonsmodellen, men den kan også brukes i andre produktmodeller.  
8. Klikk OK.
9. Velg et alternativ i feltet Bruk konfigurasjoner på nytt.
    * Hvis parameteren Bruk konfigurasjoner på nytt er satt til Ja, kontrollerer systemet for identiske konfigurasjoner etter hver konfigurasjonsøkt og bruker dem på nytt hvis det blir funnet et nøyaktig samsvar.  

## <a name="add-attributes"></a>Legg til attributter
1. Utvid delen Attributter.
2. Klikk Legg til.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Problemløsernavn.
    * Problemløsernavnet brukes i problemløseren for begrensning for produktkonfiguratoren. Det må ikke inneholde mellomrom eller spesialtegn med unntak av _ (understrekingstegn).  
6. Skriv inn en verdi i feltet Beskrivelse.
    * Den beskrivende teksten vises for konfigurasjonsbrukeren, og kan derfor fungere som hjelp til å velge riktig attributtverdi.  
7. Angi eller velg en verdi i Attributtype-feltet.
    * Attributtypen bestemmer hvilke verdier som er tilgjengelige for attributtet.  
8. Merk av for Ta med i gjenbruk.
    * Dette alternativet er bare tilgjengelig når alternativet Bruk konfigurasjoner på nytt er valgt. Når du inkluderer attributtet i avmerkingsboksen for gjenbruk, betyr det at attributtet vurderes når systemet søker etter et nøyaktig samsvar.  

## <a name="add-subcomponents"></a>Legge til delkomponenter
1. Utvid delen Underkomponenter.
2. Klikk Legg til.
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Problemløsernavn.
6. Skriv inn en verdi i feltet Beskrivelse.
7. Angi eller velg en verdi i feltet Komponent.
    * Hver underkomponent må referere til en komponentdefinisjon. Denne utformingen støtter gjenbrukbare komponenter og sikrer at når en komponent er definert, så kan den brukes i mange produktmodeller.  
8. Klikk Lagre.
9. Klikk Detaljer om stykklistelinje.
    * I skjemaet Detaljer om stykklistelinje kan brukeren velge de nødvendige egenskapene for delkomponenten. Hver egenskap kan gis en fast verdi eller tilordnes til et attributt. Tilordning til et attributt fører til at egenskapen Stykklistelinje får ulike verdier avhengig av konfigurasjonsvalget.  
10. Angi eller velg en verdi i Varenummer-feltet.
    * Hver underkomponent representerer en konfigurerbar produktstandard med teknologi for restriksjonsbasert konfigurasjon. Referansen utføres via varenummeret.  
11. Merk av for Sett.
12. Velg Ja i feltet Beregning.
    * Når du angir beregningsalternativet, sikrer du at produktet vil bli inkludert når du kjører en kostberegning for produktet.  
13. Klikk kategorien Oppsett.
14. Merk av for Sett.
15. Angi et tall i feltet Antall.
    * Antall-feltet bestemmer hvor mye av dette produktet som skal forbrukes i det konfigurerte produktet.  
16. Merk av for Sett.
17. Angi et tall i feltet Per serie.
18. Klikk OK.

