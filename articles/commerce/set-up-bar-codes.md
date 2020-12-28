---
title: Definere strekkoder
description: Denne artikkelen beskriver hvordan du bruker strekkoder i Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0785f499a3e106e36b803ae61a9acbdbb072ce17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414741"
---
# <a name="set-up-bar-codes"></a>Definere strekkoder

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker strekkoder i Dynamics 365 Commerce.

Du kan bruke strekkoder til å kjøpe og selge produkter, spore produktvarianter og sette opp kunder og ansatte. Du kan også bruke strekkoder til å utstede og godkjenne kuponger, gavekort, og kreditnotaer. Du kan definere produkter slik at de har standard strekkoder eller egendefinerte, interne strekkoder. Produkter kan ha flere enn én strekkode. For eksempel kan et produkt ha flere strekkoder hvis det kommer fra ulike produsenter, eller hvis det har varianter som er basert på størrelse, stil eller farge. Strekkoder kan inneholde vekt eller pris for produktet. Strekkodemasker er maler som brukes til å opprette strekkoder.

> [!NOTE]
> Hvis du tilordner en unik strekkode til hver variantkombinasjon kan du skanne strekkoden i kassen og la programmet bestemme hvilken variant av produktet som selges. Du kan også samle inn og vise statistikk om salg etter variant. Hver størrelses-, farge- og stilgruppe kan tilordnes et unikt nummer som identifiserer denne gruppen i strekkoden. Commerce bruker strekkodemasken til å generere strekkoder automatisk for hver variantkombinasjon. Denne funksjonaliteten kan være nyttig hvis det finnes mange størrelser, farger og stiler, fordi antall kombinasjoner øker betraktelig med hver tilføyde variantkode. Hvis denne funksjonaliteten ikke brukes, må strekkodene tilordnes manuelt til hver kombinasjon som representerer en produktvariant.

Du kan også opprette strekkoder manuelt eller automatisk. For å opprette strekkoder kan du fullføre følgende oppgaver i rekkefølgen de er oppført.

1. [Definere tegn for strekkodemaske](set-up-bar-code-masks.md).
2. [Definere strekkodemasker](set-up-bar-code-masks.md).
3. Konfigurere strekkodeoppsett.
4. [Opprette strekkoder for produkter](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Definere strekkodemasker](set-up-bar-code-masks.md)
