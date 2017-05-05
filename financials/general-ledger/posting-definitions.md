---
title: Posteringsdefinisjoner
description: "Denne artikkelen inneholder informasjon om posteringsdefinisjoner og hvordan du definerer og kobler dem. Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 357ae498e84ef27e46142c7dcc0f90ecb0ee9f1c
ms.lasthandoff: 03/31/2017


---

# <a name="posting-definitions"></a>Posteringsdefinisjoner

Denne artikkelen inneholder informasjon om posteringsdefinisjoner og hvordan du definerer og kobler dem. Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer.

Når det gjelder støttede posteringstyper og dokumenter, kan du bruke posteringsdefinisjoner i stedet for posteringsprofiler til å klassifisere hovedkontoer og finansdimensjoner i regnskapsoppføringer. Du kan vise de støttede dokumentene og posteringstypene på siden **Definisjoner for transaksjonspostering**. 

Hvis du vil begynne å bruke posteringsdefinisjoner, velger du alternativet **Bruk posteringsdefinisjoner** på **Økonomiparametere**-siden. Selv når du bruker posteringsdefinisjoner, må du definere posteringsprofiler for de opprinnelige oppføringene og posteringstyper og dokumenter som ikke støttes. 

Du må bruke posteringsdefinisjoner for å kunne aktivere disposisjonsregnskap for bestillinger og forhåndsdisposisjonsregnskap for innkjøpsrekvisisjoner.

## <a name="defining-posting-definitions"></a>Definere posteringsdefinisjoner
Bruk **Posteringsdefinisjoner**-siden for å angi treffvilkårene og definere oppføringene som skal genereres når det oppstår et treff. Treffvilkårene evalueres for de opprinnelige oppføringene som regnskapsdistribusjoner. 

På **Posteringsdefinisjoner**-siden kan du også tilordne prioritetsnumre til oppføringslinjer for å kontrollere rekkefølgen linjene evalueres i. Linjene som har det laveste prioritetsnummeret, evalueres først. Et eksempel er at alle linjer som har prioriteten 1, blir evaluert, og deretter linjer som har prioriteten 2 og så videre. Når et treff blir funnet, ignoreres de andre treffvilkårene. I tillegg er det bare kriteriene i gruppen som samsvarer med den opprinnelige transaksjonen, som oppretter genererte oppføringer. 

Du kan validere posteringsdefinisjonene ved å bruke veiviseren **Test posteringsdefinisjon**. Når du har definert en opprinnelig eksempeloppføring for en posteringsdefinisjon, ser du de genererte oppføringene. 

Du kan bruke posteringsdefinisjonsversjoner med gyldighetsdatoer. Du kan for eksempel opprette en fremtidig versjon av en posteringsdefinisjon for å postere til en annen finanskonto i et nytt regnskapsår. 

Bruk siden **Definisjoner for transaksjonspostering** til å tilordne posteringsdefinisjoner til transaksjonstyper.

## <a name="linking-posting-definitions"></a>Koble posteringsdefinisjoner
Du kan koble fra én posteringsdefinisjon til en annen når du oppretter posteringsdefinisjoner. Kriteriene for definisjonen du koblet til, vurderes deretter i tillegg til kriteriene for den gjeldende posteringsdefinisjonen. Denne funksjonen er tidsbesparende fordi du ikke trenger å angi kriterier på nytt i hurtigfanen **Oppføringer** på **Posteringsdefinisjoner**-siden for den gjeldende posteringsdefinisjonen hvis du allerede har angitt disse linjene for en annen definisjon. 

Ta med koblinger du kanskje kommer til å bruke, i diagrammer eller tabeller. Du kan unngå konflikter med gjeldende posteringsdefinisjon ved å sikre at linjene i enhver posteringsdefinisjon du kobler til, er unik. 

Følgende begrensninger gjelder når du oppretter koblinger i posteringsdefinisjoner:

-   En gitt posteringsdefinisjon kan enten kobles til en annen posteringsdefinisjon eller kobles til fra en annen posteringsdefinisjon, men ikke begge. En posteringsdefinisjon kan imidlertid koble til flere posteringsdefinisjoner.
-   Du kan bare definere koblinger blant posteringsdefinisjoner som er i samme modul.
-   Du kan tilordne en posteringsdefinisjon til en hvilken som helst transaksjonstype, men transaksjonstypen må være i samme modul som posteringsdefinisjonen. Bruk siden **Definisjoner for transaksjonspostering** for å se hvilken modul en transaksjonstype er i.


Hvis du vil ha mer informasjon, kan du se [Eksempler på posteringsdefinisjoner](/general-ledger/example-posting-definitions.md). 
