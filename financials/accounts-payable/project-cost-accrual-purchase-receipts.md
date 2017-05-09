---
title: "Påløpte prosjektkostnader på kjøpsmottak"
description: "Dette emnet beskriver hvordan påløpte prosjektkostnader fra kjøpsmottak kan spores i Microsoft Dynamics 365 for Operations."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 27a0a71095dce46c0119b32a92f8c4dce0f42e43
ms.lasthandoff: 03/31/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Påløpte prosjektkostnader på kjøpsmottak

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan påløpte prosjektkostnader fra kjøpsmottak kan spores i Microsoft Dynamics 365 for Operations. 

Fakturaer for et prosjekt ankommer ofte etter at varene og tjenestene er levert, noe som kan ha betydelig innvirkning på prosjektets nøkkelytelsesindikatorer (KPI-er). Det er viktig å kunne spore disse transaksjonene i både økonomisk rapporter og prosjektrapporter.

Eksemplet nedenfor illustrerer dette. 

Contoso Consulting har startet et nytt skydistribusjonsprosjekt. Det opprettes en bestilling for å kjøpe en datamaskin for prosjektet. Datamaskinen vil koste USD 1 500, og installeringstjenester vil koste USD 150. Leverandøren har levert og installert datamaskinen, men fakturaen har ennå ikke ankommet Contoso Consulting. Prosjektlederen vil gjerne se de påløpte prosjektkostnadene på USD 1 650 før fakturaen leveres. Denne kostnaden skal også gjenspeiles i selskapets regnskapsoppgjør ved månedsslutt. 

De påløpte kostnadene må være registrert på finansnivå og prosjektnivå for rapporteringsformål. Den økonomiske oppdatering av produktmottaket kan spores i Dynamics 365 for Operations for vare- og innkjøpskategoriene. 

For varer går du til siden **Leverandørparametere** og velger alternativet **Poster mottakssedler til finans**.
[![Avsetninger1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

For innkjøpskategorier går du til siden **Kategoripolicyregel**, velger **Innkjøpspolicyer** og velger deretter **Avsett innkjøpsutgift ved mottak** for hver innkjøpskategori.
[![Avsetninger2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Kontoene **Innkjøpsutgift, ikke-fakturert** og **Innkjøp, avsetning** i **Posteringsoppsett** vil bli brukt ved postering av bilag som er knyttet til mottaksseddelen.
[![Avsetninger3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

La oss bruke det samme scenariet og se hvordan postering av en mottaksseddel vil ha innvirkning på finans- og prosjektinformasjon. 

**Trinn 1:** Opprett og bekreft en ny bestilling for prosjektet for å registrere innkjøp av en datamaskin til USD 1 500 og installasjonstjenester til USD 150.
[![Avsetninger4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Når bestillingen er bekreftet, blir det opprettet transaksjoner for den igangsatte kostnaden for prosjektet. 
[![Avsetninger5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Transaksjonene for den igangsatte kostnaden vil feltet **Transaksjonsopprinnelse** satt til **Bestilling**. Oppretting og bekreftelse av en bestilling oppretter ikke transaksjoner for et prosjekt. 

**Trinn 2:** Varer og tjenester blir levert, og en mottaksseddel registreres. 

Postering av en mottaksseddel vil generere og postere et bilag i Finans. Bilaget vil debitere kontoen Innkjøpsutgift, ikke-fakturert og kreditere kontoen Innkjøpsavsetning. 
[![Avsetninger6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Postering av en mottaksseddel bruker posteringsoppsettet for innkjøpskategorier og produkter, og ikke posteringsoppsettet for prosjektkategorier. Oppsettet må justeres for å gjenspeile riktig økonomiske innvirkningen av Innkjøpsavsetning. 

Det er mulig å tilordne innkjøpskategorier til prosjektkategorier på siden **Innkjøpskategori**.
[![Avsetninger7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Trinn 3:** Opprett et leverandørfakturautkast. 

I Dynamics 365 for Operations vil ikke postering av en produktkvittering påvirke prosjektinformasjonen. For å omgå dette kan du generere et leverandørfakturautkast direkte etter postering av mottaksseddelen. Gå til siden **Bestilling** &gt; kategorien **Faktura** &gt; **Generer** &gt; **Faktura**. Dette oppretter et ventende fakturadokumentet som oppdaterer prosjektinformasjonen. 

Oppretting av et leverandørfakturautkast genererer ventende prosjekttransaksjoner. 
[![Avsetninger8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

På siden **Igangsatt kost** vil poster som ble opprettet i trinn 1, bli lukket, og nye poster vil bli opprettet for å gjenspeile igansatt kost som kommer fra den ventende leverandørfakturaen. Feltet **Transaksjonsopprinnelse** for den igangsatte kostnaden vil bli satt til **Leverandørfaktura**.
[![Avsetninger9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Leverandørfakturaen forblir i en ventetilstand til den faktiske leverandørfakturaen ankommer.




