---
title: Bygge inn Power Apps-apper i Dynamics 365 – Core HR
description: Dette emnet beskriver hvordan du løser problemet der Microsoft Power Apps-menyelementet er fjernet fra systemadministrasjonsmodulen.
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830215"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Bygge inn Power Apps-apper i Dynamics 365 – Core HR

[!include [banner](includes/banner.md)]

**Avgang**

**Power Apps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.

**Årsak**

Brukergrensesnittutformingen (UI) er endret, og Microsoft Power Apps er nå inkludert i standardtilpasningsmodellen.

**Oppløsning**

Måten Power Apps er innebygget på, er endret. Power Apps legges nå til via tilpasningsmodellen. Du kan legge til Power Apps på nesten alle sider i Microsoft Dynamics 365 Talent.

Hvis du vil ha mer informasjon om hvordan du bygger inn Power Apps i Talent, se [Bygge inn Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Power Apps-kunder som bygget inn apper før endringen, skal ha blitt oppgradert til den nye modellen.

**Power Apps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent. Du kan bruke denne knappen for å sette inn Power Apps.

Her er et eksempel:

1. Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.
2. Velg **Power Apps**, og velg deretter **Sett inn en PowerApp**.

    ![Power Apps-knappen](media/png.png)

3. Fyll ut feltene i dialogboksen **Sett inn en PowerApp**.

    ![Sette inn en PowerApp-dialogboks](media/insert-powerapp.png)

Eller følg disse trinnene.

1. I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass dette skjemaet**.

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    Verktøylinjen for tilpassing vises.

2. På verktøylinjen velger du **Sett inn \> PowerApp**.

    ![Sette inn en Power Apps-app ved hjelp av verktøylinjen for tilpasning](media/powerapp-bar.png)
