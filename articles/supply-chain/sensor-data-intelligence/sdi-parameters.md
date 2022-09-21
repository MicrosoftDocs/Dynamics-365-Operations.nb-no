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
ms.openlocfilehash: 4a6665cc078e54da4ebb7920ec8826352ab7a816
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428438"
---
# <a name="sensor-data-intelligence-parameters"></a>Parametere for sensordataintelligens

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

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
