---
title: Registrere leier i utenlandsk valuta
description: Dette emnet forklarer hvordan leieavtaler i andre valutaer enn regnskaps- eller rapporteringsvalutaen skal registreres.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 92177d4f808bfec88dabe9277c3d584ed02e401e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446590"
---
# <a name="record-leases-in-foreign-currencies"></a>Registrere leier i utenlandsk valuta

[!include [banner](../includes/banner.md)]

Aktivaleiekontoer for leieavtaler i andre valutaer enn regnskapsvalutaen eller rapporteringsvalutaen, fastsettes på siden **Finansoppsett**. Alle leieavtaler skal angis i transaksjonsvalutaen. De bør med andre ord angis i valutaen som er angitt i leiekontrakten. Dette emnet forklarer hvordan leieavtaler i andre valutaer enn regnskaps- eller rapporteringsvalutaen skal registreres.

Hvis du angir en leieavtale i en utenlandsk valuta, avskrives bruksrettseiendelen i både regnskapsvalutaen og rapporteringsvalutaen. Disse valutaene er konfigurert på **Finansoppsett**-siden. Denne virkemåten brukes også i Anleggsmidler. Når du oppretter en leieavtale i en utenlandsk valuta, velger du transaksjonsvalutaen i **Valuta**-feltet.

Valutakursen for regnskapsvalutaen er standardverdien i feltet **Valutakurs for regnskapsvaluta**. Valutakursen for rapporteringsvalutaen er standardverdien i feltet **Valutakurs for rapporteringsvaluta**. Disse valutakursene var gjeldende på startdatoen for leieavtalen. Feltene **Valutakurs for regnskapsvaluta** og **Valutakurs for rapporteringsvaluta** finnes i hurtigfanen for **finans- og rapporteringskursopplysninger** på siden **Leiedetaljer**.

1. Merk av for **Fast kurs** for å overstyre valutakursen som ble angitt automatisk, og angi deretter den nye kursen.
2. I de andre feltene angir du informasjonen som kreves for leieavtalen, og deretter velger du **Opprett tidsplaner**.
3. På siden **Leiedetaljer** velger du **Tablåer**.
4. På siden **Leietablå** i kategorien for **finans- og rapporteringskursopplysninger** kontrollerer du verdiene i feltene for **første bruksrettseiendel for regnskapsvaluta** og **første bruksrettseiendel for rapporteringsvaluta**. Hvert av disse feltene viser den oversatte bruksrettseiendelssaldoen i tilhørende valuta. Disse feltene oppdateres hver gang du endrer finansiell informasjon. Velg **Opprett tidsplaner** før du bekrefter betalingsplanen.

    Journaloppføringen for opprinnelig føring registrerer bruksrettseiendelen som bruker valutakursene som er oppført på leieavtalen. Journaloppføringen inneholder også verdiene fra feltene for **første bruksrettseiendel for regnskapsvaluta** og **første bruksrettseiendel for rapporteringsvaluta**.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Etterfølgende målinger for leieavtaler i utenlandsk valuta

Avskrivningsplanen viser de forventede avskrivningsutgiftsbeløpene i rapporteringsvalutaen, regnskapsvalutaen og transaksjonsvalutaen.

Hvis du vil vise bruksrettseiendelsaldoene og avskrivningsbeløpene enten i rapporteringsvalutaen eller regnskapsvalutaen, åpner du siden **Avskrivningsplan for aktiva** og merker av for **Vis regnskapsvalutabeløp** eller **Vis rapporteringsvalutabeløp**.

Når du oppretter journaloppføringene for avskrivningskostnad mot en leieavtale som er pålydende i en utenlandsk valuta, bruker posten valutakursene som er oppført i leieavtalen. Den bruker også verdiene fra feltene for **første bruksrettseiendel for regnskapsvaluta** og **første bruksrettseiendel for rapporteringsvaluta**.

Den endelige avskrivningskostnaden kan beregnes ved å bruke en litt annerledes valutakurs, slik at bruksrettseiendelen avskrives helt i både regnskapsvalutaen og rapporteringsvalutaen.

Hvis leieavtalen er reklassifisert som **Utsatt leie**, fjerner systemet automatisk valutakursene for regnskaps- og rapporteringsvalutaene hvis de allerede er definert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]