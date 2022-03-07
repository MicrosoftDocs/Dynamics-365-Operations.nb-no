---
title: Human Resources vises ikke i Microsoft Dynamics 365-apper
description: Dette emnet forklarer hva du kan gjøre hvis Microsoft Dynamics 365 Human Resources ikke er oppført blant Microsoft Dynamics 365-appene.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bdbe6c4065a8266fd30a3b093743ded91524f6a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069686"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources-app vises ikke i Microsoft Dynamics 365-apper


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Problem**

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
