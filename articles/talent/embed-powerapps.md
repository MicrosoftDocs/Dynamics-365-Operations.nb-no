---
title: Bygge inn PowerApps-apper i Core HR
description: "Dette emnet forklarer hvordan du løser problemet der PowerApps-menyelementet er fjernet fra systemadministrasjonsmodulen."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a>Bygge inn PowerApps-apper i Core HR

[!include [banner](includes/banner.md)]

**Utstede**

**PowerApps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.

**Årsak**

Brukergrensesnittutformingen (UI) er endret, og Microsoft PowerApps er nå inkludert i standardtilpasningsmodellen.

**Oppløsning**

Måten PowerApps-programmer er innebygget på, er endret. PowerApps-programmer legges nå til via tilpasningsmodellen. Du kan legge til PowerApps-programmer på nesten alle sider i Microsoft Dynamics 365 for Talent.

Hvis du vil ha mer informasjon om hvordan du bygger inn PowerApps-apper i Talent, kan du se  [Bygge inn PowerApps-apper](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

PowerApps-kunder som bygde inn apper før endringen, skal ha blitt oppgradert til den nye modellen.

**PowerApps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent. Du kan bruke denne knappen for å sette inn en PowerApps-app.

Her er et eksempel:

1. Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.
2. Velg **PowerApps**, og velg deretter **Sett inn en PowerApp**.

    ![PowerApps-knappen](media/png.png)

3. Fyll ut feltene i dialogboksen **Sett inn en PowerApp**.

    ![Sette inn en PowerApp-dialogboks](media/insert-powerapp.png)

Eller følg disse trinnene.

1. I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass dette skjemaet**.

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    Verktøylinjen for tilpassing vises.

2. På verktøylinjen velger du **Sett inn \> PowerApp**.

    ![Sette inn et PowerApps-program ved hjelp av verktøylinjen for tilpasning](media/powerapp-bar.png)
