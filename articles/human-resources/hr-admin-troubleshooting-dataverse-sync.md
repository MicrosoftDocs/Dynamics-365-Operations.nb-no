---
title: Tilbakestille Dataverse synkronisering
description: Dette emnet beskriver hvordan du feilsøker poster som ikke synkroniseres riktig mellom Microsoft Dynamics 365 Human Resources og fellesløsningen for forvaltning av menneskelig kapital (MCM) i Microsoft Dataverse.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d88f538fbf22313feaca6771b7cb1757a3c3fbad
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559670"
---
# <a name="reset-dataverse-synchronization"></a>Tilbakestille Dataverse synkronisering

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problem

Poster synkroniseres ikke mellom Microsoft Dynamics 365 Human Resources og enhetene i fellesløsningen for forvaltning av menneskelig kapital i Microsoft Dataverse. Hvis du vil ha mer informasjon om synkronisering, kan du gå til [Konfigurer Dataverse-integrering](hr-admin-integration-common-data-service.md). Feil synkronisering kan oppstå når de satsvise jobbene **nytt forsøk påDataverse-integrering** eller **manglende forespørselssynkronisering for Dataverse- integrering** blir låst i en **Utfører**-tilstand.

## <a name="resolution"></a>Oppløsning

Når de satsvise jobbene **nytt forsøk påDataverse-integrering** eller **manglende forespørselssynkronisering for Dataverse-integrering** blir låst i en **Utfører** eller **Avbryter**-tilstand, kan du tilbake statusen. Dette kan gjøres ved å avbryte den satsvise jobben ved å følge retningslinjene i [Tilbakestille satsvise jobber som står fast](hr-admin-troubleshooting-batch-execution.md). Når du har avbrutt den satsvise jobben, kan du tilbakestille den satsvise jobben ved å angi den til **Venter**-status. Den satsvise jobben vil deretter kjøres i løpet av neste planlagte kjøretid.

1. Hvis du ikke allerede har gjort det, aktiverer du funksjonen **Forbedret partiavbrudd** i **Funksjonsbehandling**.
   1. Gå til siden **Funksjonsbehandling** (**Systemadministrasjon** > **Sammendrag** > **Funksjonsbehandling**).
   2. Velg **Alle**-fanen.
   3. Velg kolonnen **Funksjonsnavn** og filtrer etter **Forbedret partiavbrudd**.
   4. Velg **Aktiver**-handlingen hvis den ikke allerede er aktivert.

2. Slå av Dataverse-integreringen.
   1. Gå til **Microsoft Dataverse-integrering**-siden (**Systemadministrasjon**, gå til **Koblinger** > **Integreringer** > **Dataverse konfigurasjon**).
   2. Sett **Aktiver Dataverse-integrering** til **Nei**.

3. Avbryt den satsvise jobben for **nytt forsøk på Dataverse-integrering**.
   1. Gå til siden **Satsvise jobber** (**Systemadministrasjon**, gå til **Koblinger** > **Satsvise jobber** > **Satvise jobber**).
   2. Filtrer **Jobbbeskrivelse**-kolonnen etter **Integrering**.
   3. Velg den satsvise jobben for **nytt forsøk på Dataverse-integrering**.
   4. Velg **Satsvis jobb** på handlingsbåndet, **Tving avbrudd**, og velg deretter **Ja** for å bekrefte.

   > [!NOTE]
   > Avhengig av når integreringen først ble aktivert, kan den satsvise jobben ha beskrivelsen **nytt forsøk på Common Data Service-integrering**. Velg denne satsvise jobben hvis den er oppført, i stedet for den satsvise jobben **nytt forsøk på Dataverse-integrering**.

4. Slett alle satvise jobber for Dataverse-integrering.
   1. På siden **Satsvise jobber** velger du de satsvise jobbene **manglende forespørselssynkronisering for Dataverse-integrering**, **nytt forsøk på Dataverse-integrering** og **innledende synkronisering av Dataverse-integrering**.
   2. På handlingsbåndet velger du handlingen **Endre status**. 
   3. Velg **Trekk tilbake**, og velg **OK**.
   4. Velg **Slett**-handlingen på handlingsbåndet, og velg deretter **Ja** for å bekrefte handlingen.

5. Slå på de satsvise jobbene for Dataverse-integrering.
   1. Gå til siden for **Microsoft Dataverse-integrering** (**Systemadministrasjon** > **Koblinger** > **Integrasjon** > **Dataverse konfigurasjon**).
   2. Sett **Aktiver Dataverse-integrering** til **Ja**.

6. Gå til siden **Satsvise jobber**, og bekreft at de satvise jobbene **nytt forsøk på Dataverse-integrering** og **manglende forespørselssynkronisering for Dataverse-integrering** er opprettet.

Når de satsvise jobbene er opprettet på nytt, kan du nå overvåke den satsvise jobben **nytt forsøk på Dataverse-integrering** for å se hvor lenge det tar å utføre jobben. Du kan deretter kontrollere om postene synkroniseres riktig med HCM Common-løsningen i Microsoft Dataverse.

## <a name="see-also"></a>Se også

[Konfigurere Dataverse-integrering](hr-admin-integration-common-data-service.md)<br>
[Tilbakestille satsvise jobber som står fast](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
