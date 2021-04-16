---
title: Kontrollere konfigurasjonen av dobbel skriving i Finance and Operations og Dataverse
description: Dette emnet forklarer hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748855"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kontrollere konfigurasjonen av dobbel skriving i Finance and Operations og Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Det forklarer særlig hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollere at dobbel skriving er konfigurert i en Finance and Operations-app

Hvis du vil finne ut om feilene du ser når du prøver å lagre rader for oppdatering, kommer fra dobbel skriving, må du først kontrollere at dobbel skriving er konfigurert.

+ Hvis du har administratorrettigheter i Finance and Operations-appen, går du til **Arbeidsområder \> Databehandling** og velger **Dobbel skriving**-flisen. Hvis detaljene for de koblede miljøene og listen over tabelltilordninger som kjører, vises, er dobbel skriving konfigurert.

    ![Kontrollere Finance and Operations-apptilkoblingen når du har administratorrettigheter](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheter, får du feilmeldingen *Kan ikke skrive data til enhet \<entity name\>*. I eksemplet i illustrasjonen nedenfor kan du ikke opprette en kunderad i Finance and Operations-appen, fordi dobbel skriving er konfigurert, men referansedataene for kundegruppen og betalingsbetingelsene finnes ikke i Dataverse.

    ![Kontrollere Finance and Operations-apptilkoblingen når du ikke har administratorrettigheter](media/verify_fin_ops_2.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Finance and Operations-apper, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollere at dobbel skriving er konfigurert i Dataverse

Når du oppretter data og ser **Firma**-kolonnen på sider i Dataverse, er dobbel skriving konfigurert.

![Kontrollere Dataverse-tilkoblingen](media/verify_cds.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Dataverse, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Hvis du vil ha informasjon om hvordan du viser feildetaljer hvis det oppstår feil mens du oppretter data i Dataverse, kan du se [Aktivere og vise sporingsloggen for plugin-modul i Dataverse for å vise feildetaljer](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]