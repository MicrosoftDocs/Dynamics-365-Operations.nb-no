--- 
title: Opprette et produktnummer for konfigurerte produktvarianter
description: "Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 8a9bf8241a0dc66f34715513d2d201569b810582
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a>Opprette et produktnummer for konfigurerte produktvarianter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard. Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktstandarden D0004. Denne oppgaven vil vanligvis bli utført av en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktterminologi.
3. Klikk Ny.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Legg til.
7. Klikk Produktstandardnummer.
8. Klikk Legg til.
9. Klikk Tekstkonstant.
10. Merk den valgte raden i listen.
11. Skriv inn en verdi i Tekst-feltet.
12. Klikk Legg til.
13. Klikk Konfigurasjon.
14. Lukk siden.

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a>Tilordne produktnummerterminologien til en produktstandard
1. Klikk Produktstandarder.
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger.
5. Velg Ja i feltet Bruk nomenklatur.
6. Angi eller velg en verdi i feltet Produktvariantnummerterminologi.
7. Lukk siden.
8. Lukk siden.

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a>Opprette terminologi for en komponent i en produktkonfigurasjonsmodell
1. Klikk Produktkonfigurasjonsmodeller.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger.
5. Velg Ja i feltet Bruk konfigurasjonsnomenklatur.
6. Klikk Legg til.
7. Klikk Attributtverdi.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet Attributt.
10. Klikk Legg til.
11. Klikk Tekstkonstant.
12. Merk den valgte raden i listen.
13. Skriv inn en verdi i Tekst-feltet.
14. Klikk Legg til.
15. Klikk Attributtverdi.
16. Merk den valgte raden i listen.
17. Angi eller velg en verdi i feltet Attributt.
18. Klikk Legg til.
19. Klikk Tekstkonstant.
20. Merk den valgte raden i listen.
21. Skriv inn en verdi i Tekst-feltet.
22. Klikk Legg til.
23. Klikk Attributtverdi.
24. Merk den valgte raden i listen.
25. Angi eller velg en verdi i feltet Attributt.
26. Klikk Legg til.
27. Klikk Tekstkonstant.
28. Merk den valgte raden i listen.
29. Skriv inn en verdi i Tekst-feltet.
30. Klikk Legg til.
31. Klikk Attributtverdi.
32. Merk den valgte raden i listen.
33. Angi eller velg en verdi i feltet Attributt.
34. Klikk Legg til.
35. Klikk Tekstkonstant.
36. Merk den valgte raden i listen.
37. Skriv inn en verdi i Tekst-feltet.
38. Klikk Legg til.
39. Klikk Nummerserieverdi.
40. Merk den valgte raden i listen.
41. Angi eller velg en verdi i Nummerserieverdi-feltet.
42. Lukk siden.
43. Lukk siden.
44. Lukk siden.

