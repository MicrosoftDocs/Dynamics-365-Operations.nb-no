---
title: Installere tillegget for IoT-intelligens i LCS
description: Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386545"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Installere tillegget for IoT-intelligens i LCS

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS). Før du kan installere tillegget, må du [opprette Azure-ressursene](iot-azure-setup.md).

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

1. I Supply Chain Management [deaktiverer du scenarioene](iot-scenario-setup.md#how-to-disable-a-scenario).
2. I LCS går du til detaljene for Supply Chain Management-miljøet.
3. Bla til delen **Miljøtillegg**.
4. Velg **Avinstaller** for tillegget for IoT-intelligens.
