---
title: Beregne linjenettobeløp på nytt når du importerer salgsordrer, tilbud og returer
description: Denne artikkelen beskriver om og hvordan systemet omberegner nettobeløp på linjer når salgsordrer, tilbud og returer importeres. Det forklarer også hvordan du kan kontrollere virkemåten i ulike versjoner av Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 08b30044a93e46c9c83848b60d69c595bc774570
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335563"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-quotations-and-returns"></a>Beregne linjenettobeløp på nytt når du importerer salgsordrer, tilbud og returer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver om og hvordan systemet omberegner nettobeløp på linjer når salgsordrer, tilbud og returer importeres. Det forklarer også hvordan du kan kontrollere virkemåten i ulike versjoner av Microsoft Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Hvordan oppdateringer til nettolinjebeløp beregnes ved import

Supply Chain Management-versjon 10.0.23 innført i [feilretting 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Denne feilrettingen endret betingelsene som **Nettobeløp**-feltet på en linje kan oppdateres eller beregnes på nytt under oppdateringer til eksisterende salgsordrer, returer og tilbud importeres. I versjon 10.0.29 kan du erstatte dette selskapet ved å slå på funksjonen *Beregn linjenettobeløp ved import*. Denne funksjonen har en lignende effekt, men gir en global innstilling som gjør det mulig å gå tilbake til den gamle virkemåten hvis du må det. Selv om den nye virkemåten gjør at systemet arbeider på en mer fornuftig måte, kan det føre til uventede resultater i bestemte scenarioer der alle følgende betingelser er oppfylt:

- Data som oppdaterer eksisterende poster, importeres via *Salgsordrelinjer V2*, *Salgstilbudslinjer V2* eller enheten for *returordrelinjer* ved hjelp av OData (Open Data Protocol), inkludert situasjoner der du bruker skrive- eller import-/eksport via Excel og noen integreringer fra tredjeparter.
- [Policyer for forretningsavtaleevaluering](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) som er på plass, etablerer en endringspolicy som begrenser oppdateringer i **Nettobeløp**-feltet på salgsordrelinjer, salgstilbudslinjer eller returordrelinjer.
- De importerte dataene omfatter endringer i **Nettobeløp**-feltet på linjer, eller endringer (for eksempel enhetspris, antall eller rabatt) som fører til at verdien i **Nettobeløp**-feltet på linjer omberegnes for en eller flere eksisterende linjeposter.

I disse bestemte scenarioene er virkningen av evalueringspolicyen for forretningsavtale å sette en begrensning på oppdateringene i **Nettobeløp**-feltet på linjen. Denne begrensningen kalles *endringspolicy*. På grunn av denne policyen, blir du bedt om å bekrefte om du vil gjøre endringen når du bruker brukergrensesnittet til å redigere eller omberegne feltet. Når du importerer en post, må imidlertid systemet gjøre et valg for deg. Før versjon 10.0.23 lot systemet alltid nettobeløpet stå uendret, med mindre nettobeløpet for den innkommende linjen er 0 (null). I nyere versjoner vil imidlertid systemet alltid oppdatere eller omberegne nettobeløpet etter behov, med mindre det er uttrykkelig instruert om ikke å gjøre det. Selv om den nye virkemåten er mer logisk, kan det forårsake problemer for deg hvis du allerede kjører prosesser eller integreringer som antar den eldre virkemåten. Denne artikkelen beskriver hvordan du går tilbake til den gamle virkemåten hvis du må det.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Kontroller beregninger av nettobeløp for linjer i versjon 10.0.29 og nyere

Supply Chain Management, versjon 10.0.29 innførte en funksjon kalt *Beregn linjenettobeløp ved import*. Denne funksjonen legger til et alternativ som kalles **Beregn linjenettobeløp**, til siden **Kundeparametere**. Med dette alternativet kan du velge mellom den nye og den gamle virkemåten for beregning av nettobeløp på importlinje.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Slå funksjonen Beregn linjenettobeløp ved import på eller av

Når du oppdaterer til versjon 10.0.29, aktiveres funksjonen *Beregn linjenettobeløp ved import* som standard, og det nye alternativet **Beregn linjenettobeløp** settes i utgangspunktet til *Ja*. *Ja*-innstillingen tilsvarer den nye standardvirkemåten. Den samsvarer med systemvirkemåten når funksjonen er slått av, bortsett fra hvis det gjelder funksjonaliteten til [CalculateLineAmount-parameteren](#CalculateLineAmount), som beskrevet senere i denne artikkelen. Innstillingen *Nei* samsvarer med systemvirkemåten før versjon 10.0.23, og angis vanligvis for å støtte eldre integreringsscenarioer.

Administratorer kan slå på funksjonen *Beregn linjenettobeløp ved import* ved hjelp av [arbeidsområdet for funksjonsadministrasjon](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Angi alternativet Beregn linjenettobeløp ved import

Når funksjonen *Beregn linjenettobeløp ved import* er aktivert, kan du angi alternativet **Beregn linjenettobeløp** ved å følge disse trinnene.

1. Gå til **Kunder \> Oppsett \> Kundeparametere**.
1. På fanen **Priser** på hurtigfanen **Beregning av linjenettobeløp gjennom integrering** angir du alternativet **Beregn linjenettobeløp** til en av følgende verdier:

    - *Ja* – Systemet vil alltid omberegne og oppdatere linjebeløpene ved behov. (Derfor vil den ignorere evalueringspolicyen for forretningsavtale.)
    - *Nei* – Hvis det eksisterende eller innkommende nettobeløpet for en linje er 0 (null), beregnes verdien for denne linjen på nytt basert på andre verdier (som enhetspris, antall og rabatt). Hvis det eksisterende eller innkommende nettobeløpet er forskjellig fra 0 (null), og det er angitt en endringspolicy i **Nettobeløp**-feltet på linjen, vil feltet ikke omberegnes eller oppdateres, selv om innkommende endringer i linjepris, antall eller rabatt vil innebærer at linjetotalen bør omberegnes. Denne virkemåten samsvarer med versjon 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Hvordan funksjonen Beregn linjenettobeløp ved import påvirker parameteren CalculateLineAmount

Når funksjonen *Beregn linjenettobeløp ved import* er aktivert, har ikke verdien for `CalculateLineAmount`-parameteren for `SalesLine`- og `SalesQuotationLine`-tabellene noen virkning. I stedet blir virkemåten globalt kontrollert av alternativet **Beregn linjenettobeløp** som er beskrevet i forrige del. Når funksjonen er aktivert, må du derfor ikke ha noen avhengighet til `CalculateLineAmount`-verdien.

Når funksjonen *Beregn linjenettobeløp ved import* er slått av, fungerer `CalculateLineAmount`-parameteren for `SalesLine`- og `SalesQuotationLine`-tabellene slik den gjør i Supply Chain Management versjon 10.0.23 til og med 10.0.28, som beskrevet i neste del.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontroller beregninger av linjenettobeløp i versjon 10.0.28 og tidligere

Da [feilretting 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) ble lansert i versjon 10.0.23, ble det mulig å velge hvordan hver relevante dataenhet skal lagre når et linjenettobeløp ble redigert eller måtte omberegnes på grunn av andre endringer (for eksempel en oppdatert varepris). Du kan styre denne virkemåten ved å angi den nye `CalculateLineAmount`-parameteren for hver linje til en av følgende verdier i den importerte filen:

- **`CalculateLineAmount` = *1*** – Feltet **Nettobeløp** på linjen omberegnes alltid og oppdateres, uansett om det er angitt en endringspolicy for feltet, og uavhengig av verdien til nettobeløpet for den innkommende eller den eksisterende linjen.
- **`CalculateLineAmount` = *0*** – Hvis det eksisterende eller innkommende nettobeløpet for en linje er 0 (null), beregnes verdien for denne linjen på nytt basert på andre verdier (som enhetspris, antall og rabatt). Hvis det eksisterende eller innkommende nettobeløpet er forskjellig fra 0 (null), og det er angitt en endringspolicy i **Nettobeløp**-feltet på linjen, omberegnes eller oppdateres ikke feltet.  

Systemvirkemåten avhenger av din versjon av Supply Chain Management:

- I versjon 10.0.22 og tidligere fungerer systemet alltid som om `CalculateLineAmount` er satt til *0*, og det er ingen måte å gjøre få den til å opptre som om `CalculateLineAmount` er satt til *1*.
- I versjon 10.0.23 til 10.0.28 fungerer systemet som om `CalculateLineAmount` er satt til *1* for alle linjer der det ikke er uttrykkelig angitt til *0* i importfilen.
