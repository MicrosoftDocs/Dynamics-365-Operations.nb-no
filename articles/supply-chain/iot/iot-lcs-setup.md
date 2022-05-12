---
title: Installere tillegget for IoT-intelligens i LCS
description: Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).
author: tonyafehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89d2f53a761085949885c987d664654c3423524b
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645084"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Installere tillegget for IoT-intelligens i LCS

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS). Legg merke til at tillegg ikke kan installeres i et demo-/prøvemiljø. Før du kan installere tillegget, må du [opprette Azure-ressursene](iot-azure-setup.md).

Du kan sette opp og konfigurere IoT-intelligens uten å skrive noen kode. Her er de grunnleggende trinnene.

1. [Konfigurer Azure-ressurser](iot-azure-setup.md) – Opprett en IoT Hub, en Redis Cache og en Key Vault som du kan få tilgang til fra Supply Chain Management.
2. [Meldingsskjemaformater for IoT Hub](iot-schema-format.md) – Konfigurer enhetene til å sende meldinger til IoT Hub, og definer JSON-meldingsformatet (JavaScript Object Notation).
3. Aktiver IoT-intelligens-funksjonsflagget i Funksjonsadministrasjon.
4. Installer IoT-intelligens-tillegget i Microsoft Dynamics Lifecycle Services (LCS) – Installer tillegget i LCS, og konfigurer Azure-hemmeligheter (som beskrevet i dette emnet).
5. [Definere metrikk](iot-metrics-setup.md) – Definer mål i Supply Chain Management.
6. [Scenariooppsett](iot-scenario-setup.md) – Sett opp scenariene i Supply Chain Management.

## <a name="set-up-the-lcs-environment"></a>Definere LCS-miljøet

1. Åpne LCS og gå til Microsoft Dynamics 365 Supply Chain Management-miljøet.
2. Bla til delen **Miljøtillegg**.
3. Velg **Installer et nytt tillegg** for å vise listen over tillegg som er aktivert for miljøet.
4. I dialogboksen **Velg et tillegg som skal installeres** velger du **IoT-intelligens**.
5. I dialogboksen **Konfigurer tillegg** angir du detaljene for IoT-huben og Redis-bufferen. Du kan finne de nødvendige verdiene i nøkkelhvelvet du opprettet i [Opprett Azure-ressurser](iot-azure-setup.md).

    + **Leier-ID** – Gå til nøkkelhvelvet i Azure-portalen, og velg deretter **Oversikt** i navigasjonsruten til venstre og kopier verdien **Katalog-ID**. Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.
    + **URI for nøkkelhvelv for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**. Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.
    + **Hemmelig navn for hub-kompatibelt endepunkt for IoT-hendelse** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for hendelseshuben for IoT-huben er lagret. Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.
    + **URI for nøkkelhvelv for Redis-buffer** – Gå til nøkkelhvelvet, og velg deretter **Oversikt** i navigasjonsruten til venstre, og kopier verdien **DNS-navn**. Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.
    + **Hemmelig navn for endepunkt for Redis-buffer** – Gå til nøkkelhvelvet, og deretter velger du **Hemmeligheter** i navigasjonsruten til venstre, og kopierer navnet på hemmeligheten der tilkoblingsstrengen for Redis-bufferen er lagret. Lim inn denne verdien i dialogboksen **Konfigurer tillegg**.

6. Merk av i avmerkingsboksen for å godta vilkårene og betingelsene.
7. Velg **Installer**.
8. Det vises en melding som sier at tillegget ble utløst for installasjon. Velg **OK**.

LCS-installasjonen er nå fullført. Det neste trinnet er å [definere scenarioene](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Avinstallere tillegget

1. I Supply Chain Management [deaktiverer du scenarioene](iot-scenario-setup.md#disable-a-scenario).
2. I LCS går du til detaljene for Supply Chain Management-miljøet.
3. Bla til delen **Miljøtillegg**.
4. Velg **Avinstaller** for tillegget for IoT-intelligens.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]