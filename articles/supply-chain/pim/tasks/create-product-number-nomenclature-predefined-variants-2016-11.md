--- 
title: "Opprette et produktnummer for forhåndsdefinerte produktvarianter"
description: "Denne veiledningen viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f14ee57564ad70bb7f28cd9274fc97d07974ec32
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Opprette et produktnummer for forhåndsdefinerte produktvarianter

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse. Denne oppgaven vil vanligvis bli utført av en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi
1. Klikk Definisjon av produktvariantmodell.
2. Klikk Produktterminologi.
3. Klikk Ny.
4. I Navn-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel ColorSize.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Legg til.
7. Klikk Produktstandardnummer.
8. Klikk Legg til.
9. Klikk Tekstkonstant.
10. Skriv inn en verdi i Tekst-feltet.
11. Klikk Legg til.
12. Klikk Farge.
13. Klikk Legg til.
14. Klikk Tekstkonstant.
15. Skriv inn en verdi i Tekst-feltet.
16. Klikk Legg til.
17. Klikk Størrelse.
18. Lukk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tilordne terminologien til en produktstandard
1. Klikk Produktdimensjonsgrupper.
2. Velg produktdimensjonsgruppen SizeCol.
3. Klikk Rediger.
4. Velg Ja i feltet Bruk nomenklatur.
5. Angi eller velg en verdi i feltet Produktvariantnummerterminologi.
6. Lukk siden.

