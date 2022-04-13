---
title: Utvidelse av planleggingsoptimalisering
description: Dette emnet beskriver utvidingsscenarier som støttes i planleggingsoptimalisering.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: d7e39c9ecd1dc1a101e219764e8f4457bb06ff7a
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468895"
---
# <a name="planning-optimization-extensibility"></a>Utvidelse av planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver utvidingsscenarier som er relatert til hovedplanlegging og støttes i planleggingsoptimalisering. Disse funksjonene er tilgjengelige fra versjon 10.0.13 i Microsoft Dynamics 365 Supply Chain Management.

## <a name="custom-processing-when-master-planning-is-completed"></a>Egendefinert behandling når hovedplanleggingen er fullført

I det vanligste utvidbarhetsscenariet i Planleggingsoptimalisering utføres egendefinert behandling etter at planen er oppdatert. Du kan for eksempel legge til en kolonne i tabellen for planlagte ordrer (`ReqPO`), eller du vil kanskje hente statistisk informasjon fra den genererte planen. Det viktigste utvidbarhetspunktet som aktiverer disse scenariene er `jobCompletedSuccessfully`-metoden i `MpsMasterPlanningEvents`-klassen.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Her er et eksempel på en utvidelse som angir et egendefinert `CstmOrderPriority`-felt i den planlagte bestillingen.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Når du legger til egendefinert logikk, må du vurdere følgende begrensninger og anbefalte fremgangsmåter:

- Metoden `jobCompletedSuccessfully` kalles utenfor transaksjonsområdet. Derfor er planen allerede synlig for brukeren når den egendefinerte logikken begynner å kjøre. Hvis tilpasningen setter inn flere felt i planlagte ordrer, er det viktig at du gir brukerne beskjed om at verdiene til disse feltene til slutt vil være konsekvent (det kan med andre ord være utdaterte rett etter at en planleggingsjobb er fullført).
- En annen hovedplanleggingsjobb kan starte når `jobCompletedSuccessfully`-metoden kalles. Den nye jobben kan påvirke hele planen eller deler av planen. Den nye jobben kan oppdatere eller slette de samme planlagte ordrene eller behovstransaksjonene som ble opprettet eller oppdatert som en del av planleggingsjobben som ble behandlet i `jobCompletedSuccessfully`. Oppdateringskonfliktsunntak må behandles når denne hendelsen utvides.
- Unngå å bruke enkelt transaksjonsområde når du utvider denne metoden. En enkelt hovedplanleggingskjøring kan produsere millioner av behovstransaksjoner og hundretusener av planlagte bestillinger. Hvis alle disse transaksjonene og de planlagte ordrene behandles i samme transaksjonsområde, vil det oppstå mange SQL-låser og blokkere andre planleggingsprosesser. Hvis transaksjonen finnes i lang tid, vil også "spøkelsesposter" bli opprettet i SQL-databasen. Innlegging av poster vil ha en negativ innvirkning på alle prosesser i systemet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]