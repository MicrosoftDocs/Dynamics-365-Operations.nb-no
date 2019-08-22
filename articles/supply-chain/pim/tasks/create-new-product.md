---
title: Opprette et nytt produkt
description: Dette emnet beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844807"
---
# <a name="create-a-new-product"></a>Opprette et nytt produkt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet beskriver hvordan du oppretter et nytt delt produkt. Dette utføres vanligvis av en produktdesigner. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.


## <a name="create-a-product"></a>Opprette et produkt
1. I navigasjonsruten går du til **Moduler > Behandling av produktinformasjon > Produkter > Produkter**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Produktnummer**. Hvis det ikke er definert en nummerserie for produktnummeret, må det angis manuelt.  
4. Skriv inn en verdi i feltet **Produktnavn**. Produktnavnet er som standard søkenavnet. Du kan endre verdien ved behov.  
5. Velg **OK**.

## <a name="set-up-dimension-groups"></a>Definere dimensjonsgrupper
1. Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.
2. Angi eller velg en verdi i **Lagringsdimensjonsgruppe**-feltet. Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir sporet på lageret.  
3. Angi eller velg en verdi i **Sporingsdimensjonsgruppe**-feltet. Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir håndtert på lageret.  
4. Velg **OK**.

