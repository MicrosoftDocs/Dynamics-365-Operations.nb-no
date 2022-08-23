---
title: Konfigurere Azure-ressurser for IoT-intelligens
description: Denne artikkelen forklarer hvordan du oppretter og konfigurerer Microsoft Azure-ressursene du krever for IoT-intelligens.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07c73ba9b7f718efdf2020b334f24d4212573c4a
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228610"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Konfigurere Azure-ressurser for IoT-intelligens

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Denne artikkelen forklarer hvordan du oppretter og konfigurerer Microsoft Azure-ressursene du krever for IoT-intelligens.

## <a name="create-azure-resources"></a>Opprette Azure-ressurser

Følg denne fremgangsmåten for å opprette en IoT-hub, en Redis-buffer og et nøkkelhvelv som Microsoft kan få tilgang til Dynamics 365 Supply Chain Management.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Kontrollerer at ID-en for førstepartsappen for Microsoft Dynamics ERP Microservices er i leieren din

Hvis du vil kontrollere at ID-en for førstepartsappen for Microsoft Dynamics ERP Microservices er i leieren din, gjør du følgende.

1. Logg på Azure-portalen på <https://portal.azure.com>.
2. Gå til **Azure Active Directory**.
3. Gå til **Enterprise-apper**.
4. I feltet **Apptype** velger du **Microsoft-apper**.
5. I søkefeltet angir du **Microsoft Dynamics ERP Microservices**.
6. Kontroller at **Microsoft Dynamics ERP Microservices** er i listen. Andre apper har lignende navn. Kontroller derfor at du finner riktig app. App-ID-en er **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Hvis appen ikke finnes i listen, må du legge den til i leieren din:

    1. På verktøylinjen i Azure-portalen velger du knappen for å åpne Azure Cloud Shell.
    2. Kjør kommandoen **Install-Module AzureAD**. Angi **Y** for å installere modulen.
    3. Kjør kommandoen **Get-InstalledModule -Name "AzureAD"** for å kontrollere at modulen er installert.
    4. Kjør kommandoen **Connect-AzureAD -Confirm** for å kjøre godkjenningen.
    5. Kjør kommandoen **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Du kan nå gjenta trinn 1 til og med 6 for å kontrollere at app-ID-en er i leieren.

### <a name="create-a-key-vault-resource"></a>Opprette en nøkkelhvelvressurs

Hvis du vil opprette en nøkkelhvelvressurs, gjør du følgende.

1. Opprett eller gå til en ressursgruppe i Azure-portalen.
2. Velg **Legg til**.
3. På siden **Ny** i søkefeltet angir du **Nøkkelhvelv**. Velg deretter **Opprett**.
4. På siden **Opprett nøkkelhvelv** i feltet **Navn på nøkkelhvelv** angir du et navn.
5. Gå gjennom standardverdiene, og velg deretter **Se gjennom + Opprett**.
6. Velg **Opprett**.

Nøkkelhvelvet blir opprettet i bakgrunnen.

### <a name="create-an-iot-hub-resource"></a>Opprette en IoT-hubressurs

Hvis du vil opprette en IoT-ressurs, gjør du følgende.

1. Opprett eller gå til en ressursgruppe.
2. Velg **Legg til**.
3. På siden **Ny** i søkefeltet angir du **IoT-hub**. Velg deretter **Opprett**.
4. I feltet **Navn på IoT-hub** angir du et navn.
5. Gå gjennom standardverdiene, og velg deretter **Se gjennom + Opprett**.
6. Velg **Opprett**.

IoT-huben blir opprettet i bakgrunnen.

> [!NOTE]
> Det anbefales at du oppretter bare én IoT-hubressurs per miljø.

### <a name="create-a-redis-cache-resource"></a>Opprette en ressurs for Redis-buffer

Hvis du vil opprette en ressurs for Redis-buffer, gjør du følgende.

1. Opprett eller gå til en ressursgruppe.
2. Velg **Legg til**.
3. På siden **Ny** i søkefeltet angir du **Azure-buffer for Redis**. Velg deretter **Opprett**.
4. I feltet **DNS-navn** angir du et navn.
5. Gå gjennom standardverdiene, og velg deretter **Opprett**.

Redis-bufferen blir opprettet i bakgrunnen.

> [!NOTE]
> Det anbefales at du oppretter bare én Redis-buffer per miljø.

Alle ressursene er nå opprettet.

## <a name="configure-the-azure-resources"></a>Konfigurere Azure-ressursene

### <a name="configure-the-iot-hub"></a>Konfigurere IoT-huben

Hvis du vil konfigurere IOT-huben, gjør du følgende.

1. Velg IoT-hubressursen i ressursene.
2. I navigasjonsruten til venstre velger du **Innebygde endepunkter**.
3. Under **Forbrukergrupper** limer du inn følgende forbrukergrupper. Disse forbrukergruppene samsvarer med de bruksklare scenarioene.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Konfigurere nøkkelhvelvet

Hvis du vil konfigurere nøkkelhvelvet, gjør du følgende.

1. Velg ressursen for nøkkelhvelv i ressursene.
2. Velg **Tilgangspolicyer** i navigasjonsruten til venstre.
3. Velg **Legg til en tilgangspolicy**.
4. På siden **Legg til tilgangspolicy** velger du **Hent** og **Liste** i feltet **Velg tillatelser**.
5. Klikk på i **Velg oppdragsgiver**.
6. I dialogboksen **Oppdragsgiver** søke rdu etter og velger **Microsoft Dynamics ERP Microservices**. Velg deretter **Velg**.
7. Velg **Legg til**.
8. Velg **Lagre**.

Appen har nå tilgang til hemmelighetene i nøkkelhvelvet.

### <a name="save-the-iot-hub-connection-string-secret"></a>Lagre hemmeligheten for tilkoblingsstrengen for IoT-huben

Hvis du vil lagre hemmeligheten for tilkoblingsstrengen for IoT-huben, gjør du følgende.

1. Velg IoT-hubressursen i ressursene.
2. I navigasjonsruten til venstre velger du **Innebygde endepunkter**.
3. Kopier verdien i feltet **Hub-kompatibelt endepunkt for hendelse**.
4. Gå til ressursen for nøkkelhvelv.
5. Velg **Hemmeligheter** i navigasjonsruten til venstre.
6. Velg **Generer/Importer**.
7. Angi et navn i **Navn**-feltet.
8. I feltet **Verdi** limer du inn endepunktverdien du kopierte tidligere.
9. Velg **Opprett**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Lagre hemmeligheten for tilkoblingsstrengen for Redis-bufferen

Hvis du vil lagre hemmeligheten for tilkoblingsstrengen for Redis-bufferen, gjør du følgende.

1. Velg ressursen for Redis-buffer i ressursene.
2. Velg **Tilgangstaster**.
3. Kopier verdien i feltet **Primær tilkoblingsstreng**.
4. Gå til ressursen for nøkkelhvelv.
5. Velg **Hemmeligheter** i navigasjonsruten til venstre.
6. Velg **Generer/Importer**.
7. Angi et navn i **Navn**-feltet.
8. I feltet **Verdi** limer du inn tilkoblingsstrengen du kopierte tidligere.
9. Velg **Opprett**.

> [!NOTE]
> Når du oppdaterer en av tilkoblingsstrengene, må du også oppdatere de hemmelige verdiene.

Du har nå fullført klargjøringen av de obligatoriske Azure-ressursene. Neste trinn er å [installere tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
