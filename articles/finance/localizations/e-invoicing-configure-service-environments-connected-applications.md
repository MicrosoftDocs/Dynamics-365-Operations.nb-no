---
title: Konfigurere tjenestemiljøer og tilkoblede programmer
description: Dette emnet inneholder informasjon om hvordan du konfigurerer tjenestemiljøene og tilkoblede programmer.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371615"
---
# <a name="configure-service-environments-and-connected-applications"></a>Konfigurere tjenestemiljøer og tilkoblede programmer

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om hvordan du konfigurerer tjenestemiljøene og tilkoblede programmer. Denne prosessen består av tre trinn. Trinn 1 er obligatorisk, og trinn 2 og 3 er valgfrie.

## <a name="step-1-create-a-service-environment"></a>Trinn 1: Opprett et tjenestemiljø

Når du oppretter tjenestemiljøet, definerer du listen over brukere som kan rulle ut globaliseringsfunksjoner til det. For noen av scenarioene kan du valgfritt definere listen over eksterne programmer som kan kommunisere med tjenesten for elektronisk fakturering. Konfigurer nummerserier hvis du vil bruke dem i scenarioene.

Se [Tjenestemiljøer](e-invoicing-service-environments.md) for å fullføre dette trinnet.

## <a name="step-2-add-certificates-and-secrets"></a>Trinn 2: Legg til sertifikater og hemmeligheter

Legg til en referanse til Microsoft Azure-nøkkelhvelvet og -hemmeligheter for å bruke dem i scenarioene. Dette trinnet er obligatorisk hvis handlingene i datasamlebåndene for behandling bruker sertifikater og hemmeligheter til digital signering eller kommunikasjon med eksterne nettjenester.

Du kan fullføre dette trinnet ved å se [Kundesertifikater og -hemmeligheter](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Trinn 3: Konfigurer tilkoblede programmer

For å kunne konfigurere kommunikasjon mellom Dynamics 365 Finance- eller Dynamics 365 Supply Chain Management-programmer og elektronisk fakturering må du først konfigurere Finance eller Supply Chain Management for å konstruere oppkallet til tjenesten for elektronisk fakturering og klargjøre forretningsdata i en enhetlig struktur som kan transformeres til det elektroniske formatet som kreves. Programmene må også behandle svar fra tjenesten på riktig måte. Du kan fullføre denne konfigurasjonen direkte i Finance- eller Supply Chain Management-miljøet, eller du kan fullføre den i Regulatory Configuration Service (RCS). Hvis du fullfører konfigurasjonen i RCS, kan du deretter distribuere den til Finance- eller Supply Chain Management-miljøet. I dette trinnet registrerer du det tilkoblede programmet for parameterdistribusjon.

Se [Tilkoblede programmer](e-invoicing-connected-applications.md) for å fullføre dette trinnet.
