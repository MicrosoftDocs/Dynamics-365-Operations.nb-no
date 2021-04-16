---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820015"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a>Opprette en produktnummerterminologi for konfigurerte produktvarianter

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard. Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktstandarden D0004. Denne oppgaven vil vanligvis bli utført av en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi
1. Klikk på Definisjon av produktvariantmodell.
2. Klikk på Produktterminologi.
3. Klikk på Ny.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk på Legg til.
7. Klikk på Produktstandardnummer.
8. Klikk på Legg til.
9. Klikk på Tekstkonstant.
10. Merk den valgte raden i listen.
11. Skriv inn en verdi i Tekst-feltet.
12. Klikk på Legg til.
13. Klikk på Konfigurasjon.
14. Lukk siden.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tilordne produktnummerterminologien til en produktstandard
1. Klikk på Produktstandarder.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.
3. Klikk på koblingen i den valgte raden i listen.
4. Klikk på Rediger.
5. Velg Ja i feltet Bruk nomenklatur.
6. Angi eller velg en verdi i feltet Produktvariantnummerterminologi.
7. Lukk siden.
8. Lukk siden.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Opprette terminologi for en komponent i en produktkonfigurasjonsmodell
1. Klikk på Produktkonfigurasjonsmodeller.
2. Finn og velg ønsket post i listen.
3. Klikk på koblingen i den valgte raden i listen.
4. Klikk på Rediger.
5. Velg Ja i feltet Bruk konfigurasjonsnomenklatur.
6. Klikk på Legg til.
7. Klikk på Attributtverdi.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet Attributt.
10. Klikk på Legg til.
11. Klikk på Tekstkonstant.
12. Merk den valgte raden i listen.
13. Skriv inn en verdi i Tekst-feltet.
14. Klikk på Legg til.
15. Klikk på Attributtverdi.
16. Merk den valgte raden i listen.
17. Angi eller velg en verdi i feltet Attributt.
18. Klikk på Legg til.
19. Klikk på Tekstkonstant.
20. Merk den valgte raden i listen.
21. Skriv inn en verdi i Tekst-feltet.
22. Klikk på Legg til.
23. Klikk på Attributtverdi.
24. Merk den valgte raden i listen.
25. Angi eller velg en verdi i feltet Attributt.
26. Klikk på Legg til.
27. Klikk på Tekstkonstant.
28. Merk den valgte raden i listen.
29. Skriv inn en verdi i Tekst-feltet.
30. Klikk på Legg til.
31. Klikk på Attributtverdi.
32. Merk den valgte raden i listen.
33. Angi eller velg en verdi i feltet Attributt.
34. Klikk på Legg til.
35. Klikk på Tekstkonstant.
36. Merk den valgte raden i listen.
37. Skriv inn en verdi i Tekst-feltet.
38. Klikk på Legg til.
39. Klikk på Nummerserieverdi.
40. Merk den valgte raden i listen.
41. Angi eller velg en verdi i Nummerserieverdi-feltet.
42. Lukk siden.
43. Lukk siden.
44. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]