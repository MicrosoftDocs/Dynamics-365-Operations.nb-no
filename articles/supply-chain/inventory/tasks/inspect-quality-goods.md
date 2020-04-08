---
title: Kontrollere varekvaliteten
description: Dette emnet forklarer hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75fbfbb7b993b528e96d247dafa2bdfe20837987
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145623"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrollere varekvaliteten

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du behandler en kvalitetsordre. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Før du starter denne eksempelprosedyren, må du bekrefte bestillingen "000016" og postere en produktkvittering. Dermed opprettes automatisk en kvalitetsordre. Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.


## <a name="select-a-quality-order"></a>Velge en kvalitetsordre
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer**.
2. Velg kvalitetsordren som ble opprettet før du startet denne prosedyren.  

## <a name="record-test-results"></a>Registere testresultater
1. Velg **Resultater**.
2. Velg **Rediger**.
3. Angi et tall i **Resultatantall**-feltet.
4. Velg det ønskede oppslaget på rullegardinmenyen i **Resultat**-feltet.  
- I dette eksemplet er resultatet basert på et forhåndsdefinert resultat. Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.  
5. Velg **Lagre**.
6. Lukk siden.

## <a name="validate-the-quality-order"></a>Valider kvalitetsordren
1. Velg **Valider**.
2. I feltet **Validert av** velger du brukeren som utfører inspeksjonen, fra rullegardinmenyen.  
3. Klikk **Velg**.
4. Velg **OK**.
5. Lukk siden.

