---
title: Konfigurer Vis eldre partier i lageret på en mobilenhet
description: Dette emnet beskriver hvordan du konfigurerer en mobil enhet til å vise en liste over lokasjoner med partier som er eldre enn den gjeldende plasseringen til en linje i arbeid.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5156b17b9eddc2c3127b6d91fd8cd7d519d240e8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838304"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Konfigurer Vis eldre partier i lageret på en mobilenhet

[!include [banner](../includes/banner.md)]

Den **Vis eldre lagerpartier lageret** konfigurasjon kan du vise en liste over lokasjoner med partier som er eldre enn den gjeldende plasseringen til linjen arbeid. Listen over lokasjoner som skal vises inneholder informasjon om eldre partiene på sted med utløpsdatoen og det fysiske lageret for hver bunke. Du kan velge å velge fra et annet sted, eller for å fortsette plukking fra gjeldende plassering. 
- Velg fra et annet sted - hvis du velger en ny plassering for å velge fra, oppdateres den gjeldende linjen i arbeid hvis du vil bruke den nye plasseringen og fortsetter arbeidet på vanlig måte med den nye plasseringen. For den nye adressen skal være gyldig, må det ha nok tilgjengelig antall for hele fungerer linjen. Hvis behovsantallet ikke er tilgjengelig, oppdateres ikke arbeid linjen, og viser listen. 
- Fortsette plukking fra gjeldende plassering – Hvis du fortsetter med befinner for arbeid, fortsetter antallet for linjen arbeid som skal plukkes fra den opprinnelige plasseringen.

## <a name="where-it-applies"></a>Der det er aktuelt
Vis eldre lageret er konfigurert på mobil enhet, menyelementer og påvirker plukkingen for partiet under elementene.

## <a name="set-up-display-older-batches-within-warehouse"></a>Definere visning eldre bunker i lager
Den **Vis eldre lagerpartier lageret** konfigurasjon er tilgjengelig på mobil enhet menyelementene når den **plukk eldste satsvis** er **varsel**.

- Under **Lagerstyring** > **oppsett** > **mobil enhet** > **mobiltelefon menyelementer**, setter **bruker eksisterende arbeid** til **Ja** for menyelementet, og velg **varsel** i den **plukk eldste satsvis** feltet. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]