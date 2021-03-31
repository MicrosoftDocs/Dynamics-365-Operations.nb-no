---
title: Opprette et nytt produkt
description: Dette emnet beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90fdd0a3cbe90c7d3752c4ca2de1c2665968dc35
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218543"
---
# <a name="create-a-new-product"></a>Opprette et nytt produkt

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]