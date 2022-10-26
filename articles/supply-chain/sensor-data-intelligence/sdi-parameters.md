---
title: Parametere for sensordataintelligens
description: Denne artikkelen inneholder informasjon om konfigurasjonsinnstillinger som er tilgjengelige på siden Parametere for sensordataintelligens.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689380"
---
# <a name="sensor-data-intelligence-parameters"></a>Parametere for sensordataintelligens

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Siden **Parametere for sensordataintelligens** har noen innstillinger som du kan bruke til å konfigurere funksjonen. Disse innstillingene omfatter Azure-tilkoblingsparametere og en parameter for levetiden til varslingsmeldinger som sendes til brukere som svar på sensormålinger.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Les og endre tilkoblingsdetaljer for Azure IoT-løsningen

Vanligvis konfigurerer du Azure IoT-løsningen og kobler den til Microsoft Dynamics 365 Supply Chain Management fra siden **Distribuer og koble til Azure-ressurser**, som veileder deg gjennom begge prosedyrene. (Hvis du vil ha mer informasjon, kan du se [Distribuer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md).) Du kan også vise og redigere tilkoblingsdetaljene når som helst i Supply Chain Management ved å følge disse trinnene.

1. Gå til **Systemadministrasjon \> Oppsett \> Sensordataintelligens \> Parametere for sensordataintelligens**.
1. På **Tidsserier**-fanen, i feltet **Tilkoblingsstreng for metrisk lagring av Redis**, angir du verdien for **Primær tilkoblingsstreng (StackExchange.Redis)** for Azure IoT-løsningen du vil koble til. Hvis du vil ha mer informasjon om hvordan du finner denne verdien, kan du se [Distribuer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md).
1. På **Integrasjoner**-fanen, i feltet **Azure AD-appklient-ID**, angir du **Klient-ID**-verdien for Azure IoT-løsningen du vil koble til. Hvis du vil ha mer informasjon om hvordan du finner denne verdien, kan du se [Distribuer en IoT-løsning på Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Angi levetiden for varslingsmeldinger

Hver gang sensordataintelligens oppdager en situasjon som krever brukerens oppmerksomhet, sendes det en varsling til den aktuelle brukeren. For å hindre at disse meldingene hoper seg opp i systemet, bør du angi at de skal utløpe etter et par dager.

1. Gå til **Systemadministrasjon \> Oppsett \> Sensordataintelligens \> Parametere for sensordataintelligens**.
1. På **Varslinger**-fanen, i feltet **Varslingsdager til aktiv**, angir du hvor mange dager en varsling skal beholdes. Etter at den angitte tidsperioden er over, blir varslingen slettet.
