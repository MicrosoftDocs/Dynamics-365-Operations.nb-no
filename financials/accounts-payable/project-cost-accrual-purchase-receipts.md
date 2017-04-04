---
title: "Project kostnadsbelastning på kjøpsmottak"
description: "Dette emnet beskriver hvordan påløpte kostnader for prosjekt fra innkjøp mottak kan spores i Microsoft Dynamics 365 for operasjoner."
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

# <a name="project-cost-accrual-on-purchase-receipts"></a>Project kostnadsbelastning på kjøpsmottak

Dette emnet beskriver hvordan påløpte kostnader for prosjekt fra innkjøp mottak kan spores i Microsoft Dynamics 365 for operasjoner. 

Fakturaer for et prosjekt kommer ofte senere enn varene og tjenestene er levert, som kan ha betydelig innvirkning på prosjekt viktige ytelsesindikatorer (KPIer). Det er viktig å kunne spore disse transaksjonene i både økonomisk og project-rapporter.

Følgende eksempelscenario illustrerer dette. 

Konsulenttjenester for Contoso har startet et nytt prosjekt for sky-distribusjon. Det opprettes en bestilling for å kjøpe en datamaskin for prosjektet. Datamaskinen vil koste $1500 og installeringstjenester vil koste $150. Leverandøren har levert og installert på datamaskinen, men fakturaen har nådd ikke Contoso konsulenttjenester. Prosjektlederen vil se prosjektet kostnadsbelastning for $1650 før fakturaen er levert. Denne kostnaden skal også gjenspeiles i selskapets måned slutten regnskapsoppgjør. 

Påløpne kostnader må være registrert på økonomiske nivå og prosjektnivå for rapportering. Økonomisk oppdatering av produkt-mottaket kan spores i Dynamics 365 for operasjoner, for kategoriene element og innkjøp. 

For varer, på den **leverandørparametere** velger du **postere produktkvitteringer til finans** alternativet.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

For innkjøpskategorier på den **Kategoripolicyregelen** velger **kjøp** policyer, og velg **Avsett innkjøpsutgift ved mottak** for hver innkjøpskategori.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Den **kjøpe utgift ikke-fakturert** og **kjøp belastning** kontoer i **Posteringsoppsett** vil bli brukt ved postering av bilag som er knyttet til produktkvitteringen.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Ved hjelp av denne samme scenario, la oss se hvordan postering av en produkt-tilgang vil ha innvirkning på finans- og prosjektinformasjon. 

**Trinn 1:** opprette og bekrefte en ny bestilling for prosjektet til å registrere innkjøp av en datamaskin for installasjon av $1500 og tjenester for $150.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Når bestillingen er bekreftet, blir det opprettet transaksjoner for den igangsatte kostnaden for prosjektet. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Transaksjonene for den igangsatte kostnaden vil ha den **transaksjonsopprinnelse** -feltet satt til **bestillingen**. Opprette og bekrefter en bestilling opprettes ikke transaksjoner for et prosjekt. 

**Trinn 2:** levert varer og tjenester, og en produkt-bekreftelse er registrert. 

Postering av en produkt-tilgang vil generere og postere et bilag i Finans. Bilaget debet kjøp utgifter, ikke-fakturert konto og kreditere inngående Avsetningskonto. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Postering av en produktkvittering bruker posteringsoppsettet for innkjøpskategorier og produkter, og ikke posteringsoppsettet for project-kategorier. Dette installasjonsprogrammet må justeres for å gjenspeile riktig økonomiske virkningen av Påløpte innkjøp. 

Det er mulig å tilordne innkjøpskategorier til prosjektkategorier på den **innkjøpskategori** siden.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**Trinn 3:** opprette en leverandørfaktura for utkast. 

I Dynamics 365 for operasjoner påvirker postering av en produktkvittering ikke project-informasjon. For å unngå dette, kan du generere en leverandørfaktura utkast direkte etter bokføring av mottaket. Gå til den **bestillingen** siden &gt;**kategorien faktura**&gt;**generere**&gt;**faktura**. Dette oppretter en ventende fakturadokumentet som oppdaterer prosjektinformasjon. 

Opprette en leverandørfaktura utkast genererer ventende prosjekttransaksjoner. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

I den **utført kostnaden** siden postene som er opprettet i trinn 1, vil bli lukket og nye oppføringer vil bli opprettet for å gjenspeile kostnader engasjement kommer fra den ventende leverandørfakturaen. Den **transaksjonsopprinnelse** -feltet for den igangsatte kostnaden vil bli satt til **leverandørfakturaen**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Leverandørfakturaen, forblir i en ventetilstand til faktiske leverandørfakturaen kommer.


