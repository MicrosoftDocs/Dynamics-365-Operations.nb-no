---
title: Opprette forhåndsdefinerte produktvarianter
description: Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "349820"
---
# <a name="create-predefined-product-variants"></a>Opprette forhåndsdefinerte produktvarianter

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner. Demonstrasjonsfirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-product-master"></a>Opprette en produktstandard
1. Gå til Behandling av produktinformasjon > Produkter > Produktstandarder.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Produktnummer.
    * Det er bare obligatorisk å angi et produktnummer manuelt hvis ingen nummerserie er definert for produktnummerfeltet. Hopp med andre ord over dette trinnet hvis nummerserien er definert for feltet.  
4. Skriv inn en verdi i feltet Produktnavn.
5. Angi eller velg en verdi i Feltet Produktdimensjonsgruppe.
    * Velg produktdimensjonsgruppen SizeCol (størrelse og farge).  
6. Klikk OK.

## <a name="add-product-dimensions"></a>Legge til produktdimensjoner
1. Klikk Produktdimensjoner.
    * Dette eksemplet viser hvordan du manuelt angir produktdimensjoner. Du kan også velge en størrelse, farge eller stilgruppe som inkluderer produktdimensjonsverdiene du vil bruke.  
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Angi eller velg en verdi i Størrelse-feltet.
5. Skriv inn en verdi i Navn-feltet.
6. Klikk Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i Størrelse-feltet.
9. Skriv inn en verdi i Navn-feltet.
10. Klikk kategorien Farger.
11. Klikk Ny.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i feltet Farge.
14. Skriv inn en verdi i Navn-feltet.
15. Klikk Ny.
16. Merk den valgte raden i listen.
17. Angi eller velg en verdi i feltet Farge.
18. Skriv inn en verdi i Navn-feltet.
19. Klikk Lagre.
20. Lukk siden.

## <a name="generate-product-variants"></a>Generere produktvarianter
1. Klikk Størrelser for produktvarianter.
2. Klikk Variantforslag.
3. Klikk Velg alt.
    * I dette eksemplet velges alle mulige varianter. Hvis bare et delsett av de mulige produktdimensjonskombinasjoner skal brukes for å opprette varianter, kan du velge de enkelte postene.  
4. Klikk Opprett.
    * Du kan generere beskrivelser for alle varianter basert på kombinasjonen av produktdimensjonsverdier. Beskrivelser er valgfritt.  
5. Klikk Lagre.

