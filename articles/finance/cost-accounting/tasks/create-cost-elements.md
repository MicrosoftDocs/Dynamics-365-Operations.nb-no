---
title: 'Opprette kostnadselementer  '
description: Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5458227138c704ab08295d885e8c3a6b4500b1f4
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565888"
---
# <a name="create-cost-elements"></a>Opprette kostnadselementer   

[!include [banner](../../includes/banner.md)]

Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap. Denne fremgangsmåten viser hvordan du oppretter kostnadselementer ved å importere -hovedkontoer via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-new-cost-elements"></a>Opprette nye kostnadselementer
1. Gå til Kostnadsregnskap > Dimensjoner > Kostnadselementdimensjoner.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Lagre.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk Konfigurer dimensjonsmedlemsleverandør.
2. Skriv inn eller velg en verdi Kontoplan-feltet.
    * Velg Delt for å bruke den delte kontoplanen.  
3. Klikk Ny.
4. Merk den valgte raden i listen.
    * Du kan bruke filtre på kontoer som oppfyller kriteriene dine.  
5. Angi eller velg en verdi i feltet Fra hovedkonto.
6. Angi eller velg en verdi i feltet Til hovedkonto.
7. Klikk OK.

## <a name="import-main-accounts"></a>Importer hovedkontoer
1. Klikk Importer dimensjonsmedlemmer.
    * Hovedkontoer blir importert til kostnadsregnskap og brukt som kostnadselementer.  
2. Klikk OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Vise de importerte kontoene som kostnadselementer
1. Klikk Vis dimensjonsmedlemmer.
    * Vis de importerte finanskontoene som kostnadselementer i bedriften som kostnader kan flyte til.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]