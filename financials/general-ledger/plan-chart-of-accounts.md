---
title: Planlegge kontoplanen
description: "Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4c57c4fe8cc66228062f7b64c88efe255657d016
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="plan-your-chart-of-accounts"></a>Planlegge kontoplanen

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.

Hvis du vil spore og vedlikeholde økonomisk informasjon i en organisasjon, kan du definere en kontoplan. En kontoplan er en samling kontoer som definerer et økonomisk rammeverk. Hvis du vil spore transaksjonene videre i disse kontoene, kan du legge til segmenter, som kalles finansdimensjoner. En utgiftskonto kan for eksempel omfatte finansdimensjoner kalt Avdeling, Kostsenter og Formål. Brukerdefinerte regler, som kalles kontostrukturer og avanserte regler, fastsetter hvordan finansdimensjonene er knyttet til hovedkontoene og andre finansdimensjoner, og også hvordan transaksjoner registreres. 

Kontoplanen er en strukturert liste over den juridiske enhetens finanskontoer. Listen brukes til å utarbeide økonomiske rapporter til myndigheter og eiere. Kontoene grupperes i kontotyper og aggregeres deretter ytterligere i større, overordnede kategorier. På det øverste nivået grupperes kontoene som henholdsvis inntekter og kostnader (driftskontoer) og aktiva og gjeld (balansekontoer). 

En kontoplan kan deles og brukes av alle juridiske enheter i en organisasjon. Kontoplanen som brukes av en juridisk enhet, er definert på **Finans**-siden. 

Her er noen av faktorene du må vurdere når du planlegger strukturen til kontoplanen for organisasjonen:

-   Rapporteringskravene i landet/området der organisasjonen holder til
-   Rapporteringskravene til den juridiske enheten
-   Graden av detaljer som kreves, både for den eksterne organisasjonen og organisasjonen din

Definer kontoplanen på **Kontoplan**-siden. Hovedkontoer kan opprettes fra **Kontoplan**-siden eller **Hovedkontoer**-siden. Hovedkontoene kan ikke bruke spesialtegn som brukes som skilletegn for kontoplan. Hvis du har et spesialtegn som er det samme som skilletegnet for kontoplan, kan dette føre til ustabilitet, eller det kan bli nødvendig å alltid bruke oppslag eller undermenyen når du angir kombinasjoner av konto og dimensjon. 

Det er lurt å koble hovedkontoene til hovedkontokategorier, slik at du kan dra nytte av standard økonomiske rapporter uten å måtte gjøre endringer. Derfor går det raskere og enklere å utforme og vedlikeholde rapporter. 

Bruk siden **Konfigurer kontostrukturer** til å opprette kontostrukturer. Kontostrukturer brukes til å definere gyldige kombinasjoner. Kombinasjonene, sammen med hovedkontoer, utgjør en kontoplan. 

**Overstyringer for juridisk enhet** 

Ikke alle hovedkontoer er gyldige for alle juridiske enheter, og noen er kanskje bare relevante i en bestemt tidsperiode. I denne situasjonen kan delen Overstyringer for juridisk enhet brukes til å identifisere hvilke firmaer hovedkontoen skal suspenderes for, hvem som er eier, og tidsperioden dimensjonen er aktiv. Overstyringene på det delte nivået kan ikke være mer begrensende enn overstyringer på nivået for juridisk enhet.

Hvis du vil ha mer informasjon, kan du se [Finansdimensjoner](financial-dimensions.md).




