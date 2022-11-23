---
title: 'Opprette kostnadselementer  '
description: Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779696"
---
# <a name="create-cost-elements"></a>Opprette kostnadselementer   

[!include [banner](../../includes/banner.md)]

Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap. Denne fremgangsmåten viser hvordan du oppretter kostnadselementer ved å importere -hovedkontoer via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-new-cost-elements"></a>Opprette nye kostnadselementer
1. Gå til **Kostnadsregnskap > Dimensjoner > Kostnadselementdimensjoner**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Angi eller velg en verdi i feltet **Datakobling for dimensjonsmedlemmer**.
5. Skriv inn en verdi i **Beskrivelse**-feltet.
6. Klikk på **Lagre**.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk på **Konfigurer dimensjonsmedlemsleverandør**.
2. Skriv inn eller velg en verdi **Kontoplan**-feltet.
    * Velg **Delt** for å bruke den delte kontoplanen.  
3. Klikk på **Ny**.
4. Merk den valgte raden i listen.
    * Du kan bruke filtre på kontoer som oppfyller kriteriene dine.  
5. Angi eller velg en verdi i feltet **Fra hovedkonto**.
6. Angi eller velg en verdi i feltet **Til hovedkonto**.
7. Klikk på **OK**.

## <a name="import-main-accounts"></a>Importer hovedkontoer
1. Klikk på **Importer dimensjonsmedlemmer**.
    * Hovedkontoer blir importert til kostnadsregnskap og brukt som kostnadselementer.  
2. Klikk på **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Vise de importerte kontoene som kostnadselementer
1. Klikk på **Vis dimensjonsmedlemmer**.
    * Vis de importerte finanskontoene som kostnadselementer i bedriften som kostnader kan flyte til.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
