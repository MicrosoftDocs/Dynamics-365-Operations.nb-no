---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734137"
---
# <a name="create-cost-objects"></a>Opprette kostnadsobjekter   

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. 


## <a name="create-new-cost-objects"></a>Opprette nye kostnadsobjekter
1. Gå til **Kostnadsregnskap > Dimensjoner > Dimensjoner for kostnadsobjekt**.
2. Klikk på **Ny**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Angi eller velg en verdi i feltet **Datakobling for dimensjonsmedlemmer**.
5. Skriv inn en verdi i **Beskrivelse**-feltet.
6. Klikk på **Lagre**.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk på **Konfigurer dimensjonsmedlemsleverandør**.
    * Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.  
2. Velg Kostsenter i feltet **Dimensjonsnavn**.
3. Klikk på **OK**.

## <a name="import-cost-centers"></a>Importere kostsentre
1. Klikk på **Importer dimensjonsmedlemmer**.
2. Klikk på **OK**.

## <a name="view-the-imported-cost-centers"></a>Vise de importerte kostsentrene
1. Klikk på **Vis dimensjonsmedlemmer**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
