---
title: Generere en begrenset plan
description: Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e36396ce12ec51d9c093fbf7c72051f7501d84900ec62d6f3ebd8f36296636e3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744112"
---
# <a name="generate-a-constrained-plan"></a>Generere en begrenset plan

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger. Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt. 

Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produksjonsplanleggeren.


## <a name="set-up-a-constrained-plan"></a>Definere en begrenset plan
1. Velg arbeidsområdet **Hovedplanlegging** på startsiden.
2. Velg **Hovedplaner** i listen over koblinger helt til høyre på siden i arbeidsområdet.
3. Finn og velg ønsket post i listen. Eksempel: **Statisk plan**  
4. Velg **Ja** i **Begrenset kapasitet**-feltet.
5. I feltet **Horisont for begrenset kapasitet** angir du `30`.
6. Utvid delen **Horisonter i dager**.
7. Velg **Ja** i **Kapasitet**-feltet.
8. Angi et tall i feltet **Kapasitetsplanleggingshorisont (dager)**. Eksempel: `60`  
9. Velg **Ja** i feltet **Beregnede forsinkelser**.
10. Angi et tall i feltet **Beregn forsinkelseshorisont (dager)**. Eksempel: `60` 
11. Utvid delen **Beregnede forsinkelser**.
12. Velg **Ja** i alle felt kalt **Legg til den beregnede forsinkelsen i behovsdatoen**.
13. Lukk siden.

## <a name="create-a-constrained-plan"></a>Opprette en begrenset plan
1. Velg **Kjør**.
2. I **Hovedplan**-feltet angir eller velger du planen du har definert betingelser for.  
3. Velg **OK**.
4. Velg **Planlagte ordrer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]