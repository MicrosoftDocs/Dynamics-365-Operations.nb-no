---
title: Regulatory Configuration Service (RCS) – Slette et RCS-miljø
description: Denne artikkelen beskriver hvordan en systemadministrator for Regulatory Configuration Service (RCS) kan slette et RCS-miljø og tilknyttede data.
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277248"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – Slette et RCS-miljø

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan en systemadministrator for Regulatory Configuration Service (RCS) kan slette et RCS-miljø og tilknyttede data.

Før du kan fullføre trinnene i denne artikkelen må følgende forutsetninger være på plass:

- Du må ha **Systemadministrator**-rollen tilordnet deg for RCS-miljøet.
- **Systemadministrator**-rollen må ha rollen **RCSDeleteEnvironmentDuty** tilordnet.

## <a name="delete-an-rcs-environment"></a>Slette et RCS-miljø

1. Åpne RCS, og velg arbeidsområdeflisen **Elektronisk rapportering**.
2. Velg **Slett RCS-miljø** i delen **Relaterte koblinger**.

    ![Slette RCS-miljø-kobling i delen Relaterte koblinger.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. I dialogboksen som vises, kan du se gjennom meldingene om omfanget av sletting av miljøet.

    ![Meldinger i dialogboksen Slett RCS-miljø.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > Sletting av et RCS-miljø kan ikke tilbakeføres.
    >
    > Operasjonen sletter det valgte RCS-miljøet og alle relaterte data, inkludert funksjoner og konfigurasjoner som er lagret i det globale repositoriet. Funksjoner og konfigurasjoner som deles med andre organisasjoner, blir ikke delt og slettet hvis de ikke har noen avhengigheter. Funksjoner og konfigurasjoner som har avhengigheter, merkes som avsluttet.

4. I feltet som oppgis, angir du globalt unik identifikator (GUID) for RCS-miljøet for å bekrefte at du vil slette det. Miljøets GUID tas med i slettingsmeldingen.
5. Velg **Slett miljø**.
    
RCS-miljøet og eventuelle tilknyttede data blir nå slettet.

> [!IMPORTANT]
> Etter at du har slettet et RCS-miljø, finnes det ingen måte å gjenopprette dataene på. Et nytt RCS-miljø kan opprettes i et hvilket som helst tilgjengelig RCS-område.
