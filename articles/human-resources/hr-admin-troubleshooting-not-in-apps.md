---
title: Human Resources vises ikke i Microsoft Dynamics 365-apper
description: Denne artikkelen forklarer hva du kan gjøre hvis Microsoft Dynamics 365 Human Resources ikke er oppført blant Microsoft Dynamics 365-appene.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d520ac06bcc0990714929c0fdd622516eda5f30
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872246"
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
