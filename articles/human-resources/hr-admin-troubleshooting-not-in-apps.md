---
title: Human Resources vises ikke i Microsoft Dynamics 365-apper
description: Denne artikkelen forklarer hva du gjør hvis kunden ikke kan du se appen Microsoft Dynamics 365 Human Resources blant Microsoft Dynamics 365-appene.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 292db7e430bf0f2171f2b0a482ad70250774caec
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346352"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources vises ikke i Microsoft Dynamics 365-apper

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Avgang**

Kunden kan ikke se Dynamics 365 Human Resources blant Microsoft Dynamics 365-apper.

**Oppløsning**

Brukeren må legges til Miljøskaper-rollen for miljøet i Microsoft Power Apps.

1. Admin-brukeren som har en Power Apps Plan 2-lisens, må åpne [Power Apps-administrasjonsportalen](https://preview.admin.powerapps.com/).

2. Velg **Miljøer**, og velg riktig miljø for Human Resources.

3. I fanen **Sikkerhet** i fanen **Miljøroller** velger du **Miljøskaper**.

    ![Fanen Miljøroller.](media/environment-roles.png)

4. I fanen **Brukere** legger du til brukeren eller organisasjonen.

    ![Fanen Brukere.](media/environment-maker.png)

5. Velg **Lagre**.

6. Brukeren må nå logge på [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Velg **Synkroniser** for å oppdatere brukerappene.

    ![Synkroniser-knappen.](media/get-more.png)

    Når synkroniseringen er fullført, vises Human Resources på startsiden.


[!INCLUDE[footer-include](../includes/footer-banner.md)]