---
title: Installere tillegget for IoT-intelligens i LCS
description: Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c4727f4341104b77838c103fcf378a5971f8ba176f18c2d32d619ecd6614b1ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736825"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Installere tillegget for IoT-intelligens i LCS

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du installerer tillegget for IoT-intelligens i Microsoft Dynamics Lifecycle Services (LCS). Legg merke til at tillegg ikke kan installeres i et demo-/prøvemiljø. Før du kan installere tillegget, må du [opprette Azure-ressursene](iot-azure-setup.md).

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