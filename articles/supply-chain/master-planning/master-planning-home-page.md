---
title: Startside for hovedplanlegging
description: "Med hovedplanlegging kan selskaper bestemme og balansere fremtidige behov for råvarer og kapasitet for å oppfylle målene til firmaet."
author: YuyuScheller
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 18ed011fa1c1aa35b4a401d51bffc6af19395577
ms.openlocfilehash: 030579ac73d6333ac4ed55433b9679a58247c088
ms.contentlocale: nb-no
ms.lasthandoff: 02/13/2018

---

# <a name="master-planning-home-page"></a>Startside for hovedplanlegging

[!include [banner](../includes/banner.md)]

Det mest sentrale i hovedplanlegging er at selskaper kan bestemme og balansere fremtidige behov for råvarer og kapasitet for å oppfylle målene til firmaet. Hovedplanlegging vurderer følgende: 

-  Hvilke råmaterialer og kapasiteter er tilgjengelige? 
-  Hvilke råmaterialer og kapasiteter kreves for å fullføre produksjonen? For eksempel hva må produseres, kjøpes inn, overføres, eller settes til side som sikkerhetslager før du kan fullføre produksjonen.

Hovedplanlegging bruker informasjonen til å beregne behovene og generere planlagte ordrer.

De tre hovedplanleggingsprosessene er:

-  **Hovedplanlegging** - Hovedplanen beregner nettobehov. Den er basert på faktiske gjeldende ordrer og gjør det mulig for selskapet å kontrollere etterfylling av lagre på kort sikt, på daglig basis. En annen term som beskriver det, er *nettobehovsplan*. Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging](master-plans.md). 

-  **Prognoseplanlegging** - Prognoseplanen beregner bruttobehov. Det er basert på fremtidige overslag (eller prognoser), og gjør det mulig for selskaper å utføre langsiktig planlegging av materialer og kapasitet. Hvis du vil ha mer informasjon, kan du se [Prognoseplanlegging](introduction-demand-forecasting.md). 

-  **Konsernintern hovedplanlegging** - Den konserninterne hovedplanen beregner nettobehov på tvers av juridiske enheter. Den kobler behov og forsyning mellom firmaer, ikke bare for kortsiktig fast behov og forsyning, men også for langsiktig og planlagt (som ikke har autorisasjon) behov og forsyning. Hvis du vil ha mer informasjon, se [Konsernintern hovedplanlegging](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (e-læring) (krever CustomerSource-konto). 

Firmaer kan endre resultatet av planen. De kan kjøre regenererende, nettoendring eller begge deler. Regenererende planer oppdaterer alle behovene, mens nettoendringsplaner bare oppdatere planen for varer med nye behov som har kommet inn etter den siste planleggingskjøringen.

Hovedplanleggingsplaner omfatter vanligvis kort sikt, som kan være alt fra én uke til seks måneder. Hovedplanleggingsmodulen bestemmer behovet for forsyning (materialer) og kapasitet (ressurser) som skal dekke gjeldende etterspørsel (nettobehov). I de fleste firmaer er dette utvidet til å inkludere lengste samlede leveringstid blant produktene som skal mottas.

## <a name="learning-map"></a>Opplæringskart

De følgende opplæringskart viser de store konseptene og oppgavene som utgjør rammen for hovedplanleggingsmodulen. Klikk koblingene i [Hurtigkoblinger](#quick-links)-delen for å lære hvordan du bruker modulen.

[![Opplæringskart for hovedplanlegging](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Hurtigkoblinger

|      |   |
|------|---|
|        [Hovedplaner](master-plans.md)       |     [Generere en begrenset plan](./tasks/constrained-plan.md)  |
| [Opprette en materialplan for koprodukter](./tasks/create-material-plan-co-products.md)   |  [Hovedplanlegging og multisite-funksjonalitet](master-plan-multisite-functionality.md)  |
| [Opprette en konsernintern plan](./tasks/create-intercompany-plan.md) | [Oversikt over behovsprognose](introduction-demand-forecasting.md)  | 
|[Reduksjonsnøkler](reduction-keys.md)| [Grunnleggende om hovedplanlegging](https://mbspartner.microsoft.com/AX/CourseOverview/1275) (e-læring) (krever CustomerSource-konto)     |
|  [Hovedplanlegging for prosessproduksjon](https://mbspartner.microsoft.com/D365E/CourseOverview/1514) (e-læring) (krever CustomerSource-konto) | [Konsernintern hovedplanlegging](https://mbspartner.microsoft.com/AX/CourseOverview/1276) (e-læring) (krever CustomerSource-konto)|
                                  
## <a name="additional-resources"></a>Tilleggsressurser

### <a name="roadmaps"></a>Veikart
Gå til [Veikart for Microsoft Dynamics 365](https://roadmap.dynamics.com/) for å se hvilke nye funksjoner som har blitt utgitt og hvilke nye funksjoner som er under utvikling.

### <a name="blogs"></a>Blogger
Du kan finne meninger, nyheter og annen informasjon om hovedplanlegging og andre løsninger, i [Dynamics AX Manufacturing R&D-teambloggen](https://blogs.msdn.microsoft.com/axmfg) og [Forsyningskjedeadministrasjon i Dynamics AX R&D-teambloggen](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Oppgaveveiledninger
Mer hjelp er tilgjengelig som oppgaveveiledninger i Finance and Operations. For å få tilgang til oppgaveveiledninger klikker du på **Hjelp**-knappen på en side.

### <a name="webinars"></a>Webinarer
[Bruke Azure Machine Learning for behovsprognose](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Registreringer for teknisk konferanse
-  [Utvide funksjonaliteten for behovsprognose](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
-  [Hovedplanlegging – tips og triks for feilsøkingsytelse](https://youtu.be/7v8BPmEs9Dg)
-  [Hjelp! MRP er treg!](https://youtu.be/RLXybx20B5o)




