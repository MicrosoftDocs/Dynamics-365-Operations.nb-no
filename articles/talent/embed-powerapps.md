---
title: Bygge inn Power Apps-apper i Dynamics 365 Human Resources
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462073"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Bygge inn Power Apps-apper i Dynamics 365 Human Resources

**Avgang**

**Power Apps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.

**Årsak**

Brukergrensesnittutformingen (UI) er endret, og Microsoft Power Apps er nå inkludert i standardtilpasningsmodellen.

**Oppløsning**

Måten Power Apps er innebygget på, er endret. Power Apps legges nå til via tilpasningsmodellen. Du kan legge til Power Apps på nesten alle sider i Microsoft Dynamics 365 Talent.

Hvis du vil ha mer informasjon om hvordan du bygger inn Power Apps i Talent, se [Bygge inn Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Power Apps-kunder som bygget inn apper før endringen, skal ha blitt oppgradert til den nye modellen.

**Power Apps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent. Du kan bruke denne knappen for å sette inn apper.

Her er et eksempel:

1. Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.
2. Velg **Power Apps**-knappen og velg deretter **Legg til en app fra Power Apps**.

    ![Power Apps-knappen](media/png.png)

3. Fyll ut feltene i **Legg til en app fra Power Apps**-dialogboksen.

    ![Legge til en app fra Power Apps-dialogboksen](media/insert-powerapp.png)

Eller følg disse trinnene.

1. I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass denne siden**.

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    Verktøylinjen for tilpassing vises.

2. På verktøylinjen velger du **Legg til en app fra Power Apps**.

    ![Legge til en app fra Power Apps ved hjelp av Tilpasning-verktøylinjen](media/powerapp-bar.png)
