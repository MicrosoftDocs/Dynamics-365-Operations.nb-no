---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976121"
---
# <a name="create-cost-objects"></a>Opprette kostnadsobjekter   

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. 


## <a name="create-new-cost-objects"></a>Opprette nye kostnadsobjekter
1. Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Lagre.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk Konfigurer dimensjonsmedlemsleverandør.
    * Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.  
2. Velg Kostsenter i feltet Dimensjonsnavn.
3. Klikk OK.

## <a name="import-cost-centers"></a>Importere kostsentre
1. Klikk Importer dimensjonsmedlemmer.
2. Klikk OK.

## <a name="view-the-imported-cost-centers"></a>Vise de importerte kostsentrene
1. Klikk Vis dimensjonsmedlemmer.

