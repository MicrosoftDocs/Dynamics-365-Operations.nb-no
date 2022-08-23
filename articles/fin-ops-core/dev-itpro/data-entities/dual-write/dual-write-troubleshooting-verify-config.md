---
title: Bekreft konfigurasjon av dobbel skriving i økonomi- og driftsapper og Dataverse
description: Denne artikkelen forklarer hvordan du kan finne ut om dobbel skriving er konfigurert i økonomi- og driftsapper og i Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289398"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Bekreft konfigurasjon av dobbel skriving i økonomi- og driftsapper og Dataverse

[!include [banner](../../includes/banner.md)]





Denne artikkelen inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Det forklarer særlig hvordan du kan finne ut om dobbel skriving er konfigurert i økonomi- og driftsapper og i Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Bekreft at dobbel skriving er konfigurert i en økonomi- og driftsapp

Hvis du vil finne ut om feilene du ser når du prøver å lagre rader for oppdatering, kommer fra dobbel skriving, må du først kontrollere at dobbel skriving er konfigurert.

+ Hvis du har administratorrettigheter i økonomi- og driftsappen, går du til **Arbeidsområder \> Databehandling** og velger **Dobbel skriving**-flisen. Hvis detaljene for de koblede miljøene og listen over tabelltilordninger som kjører, vises, er dobbel skriving konfigurert.

    ![Kontroller økonomi- og driftsapptilkoblingen når du har administratorrettigheter.](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheter, får du feilmeldingen *Kan ikke skrive data til enhet \<entity name\>*. I eksemplet i illustrasjonen nedenfor kan du ikke opprette en kunderad i økonomi- og driftsappen, fordi dobbel skriving er konfigurert, men referansedataene for kundegruppen og betalingsbetingelsene finnes ikke i Dataverse.

    ![Kontroller økonomi- og driftsapptilkoblingen når du ikke har administratorrettigheter.](media/verify_fin_ops_2.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i økonomi- og driftsapper, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollere at dobbel skriving er konfigurert i Dataverse

Når du oppretter data og ser **Firma**-kolonnen på sider i Dataverse, er dobbel skriving konfigurert.

![Kontrollere Dataverse-tilkoblingen.](media/verify_cds.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Dataverse, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Hvis du vil ha informasjon om hvordan du viser feildetaljer hvis det oppstår feil mens du oppretter data i Dataverse, kan du se [Aktivere og vise sporingsloggen for plugin-modul i Dataverse for å vise feildetaljer](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
