---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543777"
---
# <a name="create-cost-objects"></a>Opprette kostnadsobjekter   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.


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

