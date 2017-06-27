---
title: Fakturakontroll og konserninterne bestillinger
description: "Den juridiske enheten for innkjøp som er involvert i en konsernintern handelstransaksjon kan være konfigurert til å bruke leverandørfakturasamsvar. I så fall må posteringskravene for både konsernintern handel og leverandørfakturasamsvar være oppfylt før konserninterne leverandørfakturaer kan posteres."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 07c101b886d33fa5fc9e8129230ca270f48c5217
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Fakturakontroll og konserninterne bestillinger

[!include[banner](../includes/banner.md)]


Den juridiske enheten for innkjøp som er involvert i en konsernintern handelstransaksjon kan være konfigurert til å bruke leverandørfakturasamsvar. I så fall må posteringskravene for både konsernintern handel og leverandørfakturasamsvar være oppfylt før konserninterne leverandørfakturaer kan posteres.

Eksemplene i dette emnet bruker følgende oppsett for konsernintern handel:
-   Fabrikam Innkjøp er den juridiske enheten for innkjøp.
-   Fabrikam Salg er den juridiske enheten salg.
-   Kunde 4020 finnes hos Fabrikam Salg.
-   Leverandør 3024 finnes hos Fabrikam Innkjøp.
-   Konsernintern informasjon er angitt i Fabrikam Innkjøp for leverandør 3024. Fabrikam Salg er angitt som kunden, og kunde 4020 er angitt som kundekontoen som tilsvarer den juridiske enheten i Fabrikam Innkjøp.
-   Konsernintern informasjon er angitt i Fabrikam Salg for kunde 4020. Fabrikam Kjøp er angitt som leverandør, og leverandør 3024 er angitt som leverandørkontoen som tilsvarer den juridiske enheten i Fabrikam Salg.

I disse eksemplene brukes følgende oppsett for fakturasamsvar for leverandører for Fabrikam Innkjøp:
-   På siden Leverandørparametere velges alternativet Aktiver validering av fakturakontroll.
-   På Leverandørparametere-siden settes feltet Poster faktura med avvik til Krev godkjenning.
-   Pristoleranseprosenten for den juridiske enheten er 2 prosent.

## <a name="example-price-matching-and-intercompany-trade"></a> Eksempel: Prissamsvar og konsernintern handel
Nettobeløpene for konsernintern leverandørfaktura og konsernintern kundefaktura må være lik. Dette kravet overstyrer alle fakturakontrollgodkjenninger eller pristoleranseprosenter som gjelder. Du følger eksempelvis disse trinnene.
1.  Opprett salgsordren SO888 for kunde 4020 i Fabrikam Innkjøp. Den konserninterne bestillingen ICPO222 opprettes automatisk i Fabrikam Innkjøp for leverandør 3024, og salgsordren ICSO888 opprettes automatisk i Fabrikam Salg.
2.  Registrerer at varene er mottatt, i Fabrikam Salg, og poster en følgeseddel. Status for ICSO888 endres til Levert. Status for ICPO222 endres til Mottatt.
3.  Utfør en fakturaoppdatering for ICSO888 i Fabrikam Salg. Enhetsprisen er 0,45, og 100 varer oppdateres.
4.  Opprett en faktura for ICPO222 i Fabrikam Innkjøp. Du endrer nettoprisen fra 45,00 til 54,00 ved et uhell. Et ikon vises for å angi at prisen overskrider den tillatte pristoleransen på 2 prosent.
5.  På Fakturakontroll-detaljsiden velger du alternativet for å godkjenne postering med samsvarende avvik. På siden Leverandørfaktura klikk OK. Hvis leverandørfakturaen ikke var en konsernintern leverandørfaktura, er postering fullført. Fordi du arbeider med en konsernintern leverandørfaktura, er imidlertid postering mislykket. For konsernintern handel må fakturatotaler i den konserninterne salgsordren være lik fakturatotaler i den tilsvarende konserninterne bestillingen. Du må korrigere nettoprisen på fakturaen ved å endre nettoprisen tilbake til standardbeløpet 45,00 for å løse dette problemet.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Eksempel: Antallssamsvar med konsernintern handel
Antallene på den konserninterne bestillingen og den konserninterne salgsordren må være like. Dette kravet overstyrer alle fakturakontrollgodkjenninger som gjelder. I dette eksemplet brukes følgende tillegg til oppsettet for konsernintern handel:
-   I Fabrikam Innkjøp er handlingspolicy for bestilling for leverandør 3024 satt opp til å automatisk postere både den opprinnelige kundefakturaen og den konserninterne leverandørfakturaen.

I dette eksemplet brukes følgende tilleggoppsett for leverandørfakturakontroll for Fabrikam Innkjøp:
-   På siden Varemodellgrupper for modellgruppen som brukes av vare B-R14, er alternativet Mottar krav valgt.
-   Beholdningen av vare B-R14 er 0 (null).

Du følger eksempelvis disse trinnene.
1.  Opprett salgsordren SO999 for kunde 4020 i Fabrikam Innkjøp. Ordren inneholder ett linjeelement: 100 batterier (vare B-R14) til en enhetspris på 1,00 per stykk. Den konserninterne bestillingen ICPO333 opprettes automatisk i Fabrikam Innkjøp for leverandør 3024, og salgsordren ICSO999 opprettes automatisk i Fabrikam Salg.
2.  Utfør en fakturaoppdatering for ICSO999 i Fabrikam Salg. Posteringen er ikke vellykket, fordi varen ikke finnes på lager og er ennå ikke mottatt. Derfor kan ikke den finansielle informasjonen oppdateres.
3.  Registrer at varene er mottatt, og posterer en følgeseddel for ICSO999 i Fabrikam Salg. En produktkvittering for ICPO333 posteres automatisk i Fabrikam Innkjøp. Det mottatte antallet av vare B-R14 i Fabrikam Innkjøp endres til 100.
4.  Utfør en fakturaoppdatering for ICSO999 i Fabrikam Salg. Posteringen er vellykket i begge de juridiske enhetene. Det innkjøpte antallet av vare B-R14 i Fabrikam Innkjøp endres til 100. 






