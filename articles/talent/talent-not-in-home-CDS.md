---
title: Talent vises ikke blant appene i Microsoft Dynamics 365 (Common Data Service 1.0)
description: Dette emnet forklarer hva du gjør hvis kunden ikke kan du se appen Microsoft Dynamics 365 Talent blant Microsoft Dynamics 365-appene.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772994"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent vises ikke blant appene i Microsoft Dynamics 365 (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**Avgang**

Kunden kan ikke se Microsoft Dynamics 365 Talent-appen blant Microsoft Dynamics 365-apper.

**Oppløsning**

Brukeren må legges til Miljøskaper-rollen for miljøet i Microsoft Power Apps.

1. Admin-brukeren som har en Power Apps Plan 2-lisens, må åpne [Power Apps-administrasjonsportalen](https://preview.admin.powerapps.com/).
2. Velg **Miljøer**, og velg riktig miljø for Talent.
3. I fanen **Sikkerhet** i fanen **Miljøroller** velger du **Miljøskaper**.

    ![Fanen Miljøroller](media/environment-roles.png)

4. I fanen **Brukere** legger du til brukeren eller organisasjonen.

    ![Fanen Brukere](media/environment-maker.png)

5. Velg **Lagre**.
6. Brukeren må nå logge på [Microsoft Dynamics 365](https://home.dynamics.com/).
7. Velg **Synkroniser** for å oppdatere brukerappene.

    ![Synkroniser-knappen](media/get-more.png)

    Når synkroniseringen er fullført, vises Talent på startsiden.
