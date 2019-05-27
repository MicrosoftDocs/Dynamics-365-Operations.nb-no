---
title: Opprett et nytt produkt
description: Denne oppgaven beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548422"
---
# <a name="create-a-new-product"></a>Opprett et nytt produkt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaven beskriver hvordan du oppretter et nytt delt produkt. Dette utføres vanligvis av en produktdesigner. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.

1. Gå til Behandling av produktinformasjon > Produkter > Produkter.

## <a name="create-a-product"></a>Opprette et produkt
1. Klikk Ny.
2. Skriv inn en verdi i feltet Produktnummer.
    * Hvis det ikke er definert en nummerserie for produktnummeret, må det angis manuelt.  
3. Skriv inn en verdi i feltet Produktnavn.
    * Produktnavnet er som standard søkenavnet. Du kan endre verdien ved behov.  
4. Klikk OK.

## <a name="set-up-dimension-groups"></a>Definere dimensjonsgrupper
1. Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.
2. Angi eller velg en verdi i lagringsdimensjon-feltet.
    * Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir sporet på lageret.  
3. Angi eller velg en verdi i sporingsdimensjon-feltet.
    * Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir håndtert på lageret.  
4. Klikk OK.

