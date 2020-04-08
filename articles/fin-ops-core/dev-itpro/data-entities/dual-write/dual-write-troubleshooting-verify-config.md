---
title: Kontrollere at dobbel skriving er konfigurert i apper i Finance and Operations og Common Data Service
description: Dette emnet forklarer hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172651"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>Kontrollere at dobbel skriving er konfigurert i apper i Finance and Operations og Common Data Service

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Det forklarer særlig hvordan du kan finne ut om dobbel skriving er konfigurert i Finance and Operations-apper og i Common Data Service.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollere at dobbel skriving er konfigurert i en Finance and Operations-app

Hvis du vil finne ut om feilene du ser når du prøver å lagre oppføringer for oppdatering, kommer fra dobbel skriving, må du først kontrollere at dobbel skriving er konfigurert.

+ Hvis du har administratorrettigheter i Finance and Operations-appen, går du til **Arbeidsområder \> Databehandling** og velger **Dobbel skriving**-flisen. Hvis detaljene for de koblede miljøene og listen over enhetstilordninger som kjører, vises, er dobbel skriving konfigurert.

    ![Kontrollere Finance and Operations-apptilkoblingen når du har administratorrettigheter](media/verify_fin_ops_1.png)

+ Hvis du ikke har administratorrettigheter, får du feilmeldingen *Kan ikke skrive data til enhet \<enhetsnavn\>*. I eksemplet i illustrasjonen nedenfor kan du ikke opprette en kundeoppføring i Finance and Operations-appen, fordi dobbel skriving er konfigurert, men referansedataene for kundegruppen og betalingsbetingelsene finnes ikke i Common Data Service.

    ![Kontrollere Finance and Operations-apptilkoblingen når du ikke har administratorrettigheter](media/verify_fin_ops_2.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Finance and Operations-apper, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>Kontrollere at dobbel skriving er konfigurert i Common Data Service

Når du oppretter data og ser **Firma**-feltet på sider i Common Data Service, er dobbel skriving konfigurert.

![Kontrollere Common Data Service-tilkoblingen](media/verify_cds.png)

Hvis du vil ha informasjon om hvordan du løser problemer når du oppretter data i Common Data Service, kan du se [Feilsøke problemer med direkte synkronisering](dual-write-troubleshooting-live-sync.md).

Hvis du vil ha informasjon om hvordan du viser feildetaljer hvis det oppstår feil mens du oppretter data i Common Data Service, kan du se [Aktivere og vise sporingsloggen for plugin-modul i Common Data Service for å vise feildetaljer](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).
