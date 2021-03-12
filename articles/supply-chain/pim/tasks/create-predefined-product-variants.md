---
title: Opprette forhåndsdefinerte produktvarianter
description: Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d07a090dbd41eb17e8d604887435bbb8b07e8d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966936"
---
# <a name="create-predefined-product-variants"></a>Opprette forhåndsdefinerte produktvarianter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner. Demonstrasjonsfirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-product-master"></a>Opprette en produktstandard
1. Gå til Behandling av produktinformasjon > Produkter > Produktstandarder.
2. Klikk på Ny.
3. Skriv inn en verdi i feltet Produktnummer.
    * Det er bare obligatorisk å angi et produktnummer manuelt hvis ingen nummerserie er definert for produktnummerfeltet. Hopp med andre ord over dette trinnet hvis nummerserien er definert for feltet.  
4. Skriv inn en verdi i feltet Produktnavn.
5. Angi eller velg en verdi i Feltet Produktdimensjonsgruppe.
    * Velg produktdimensjonsgruppen SizeCol (størrelse og farge).  
6. Klikk på OK.

## <a name="add-product-dimensions"></a>Legge til produktdimensjoner
1. Klikk på Produktdimensjoner.
    * Dette eksemplet viser hvordan du manuelt angir produktdimensjoner. Du kan også velge en størrelse, farge eller stilgruppe som inkluderer produktdimensjonsverdiene du vil bruke.  
2. Klikk på Ny.
3. Merk den valgte raden i listen.
4. Angi eller velg en verdi i Størrelse-feltet.
5. Skriv inn en verdi i Navn-feltet.
6. Klikk på Ny.
7. Merk den valgte raden i listen.
8. Angi eller velg en verdi i Størrelse-feltet.
9. Skriv inn en verdi i Navn-feltet.
10. Klikk på fanen Farger.
11. Klikk på Ny.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i feltet Farge.
14. Skriv inn en verdi i Navn-feltet.
15. Klikk på Ny.
16. Merk den valgte raden i listen.
17. Angi eller velg en verdi i feltet Farge.
18. Skriv inn en verdi i Navn-feltet.
19. Klikk på Lagre.
20. Lukk siden.

## <a name="generate-product-variants"></a>Generere produktvarianter
1. Klikk på Størrelser for produktvarianter.
2. Klikk på Variantforslag.
3. Klikk på Velg alt.
    * I dette eksemplet velges alle mulige varianter. Hvis bare et delsett av de mulige produktdimensjonskombinasjoner skal brukes for å opprette varianter, kan du velge de enkelte postene.  
4. Klikk på Opprett.
    * Du kan generere beskrivelser for alle varianter basert på kombinasjonen av produktdimensjonsverdier. Beskrivelser er valgfritt.  
5. Klikk på Lagre.

