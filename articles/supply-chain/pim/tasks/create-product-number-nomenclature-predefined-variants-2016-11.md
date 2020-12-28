---
title: Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter
description: Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434404"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse. Denne oppgaven vil vanligvis bli utført av en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi
1. Velg **Definisjon av produktvariantmodell**.
2. Velg **Produktnummerterminologi**.
3. Velg **Ny**.
4. I **Navn**-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel `ColorSize`.
5. Skriv inn en verdi i **Beskrivelse**-feltet.
6. Velg **Legg til**.
7. Velg **Produktstandardnummer**.
8. Velg **Legg til**.
9. Velg **Tekstkonstant**.
10. Skriv inn en verdi i **Tekst**-feltet.
11. Velg **Legg til**.
12. Velg **Farge**.
13. Velg **Legg til**.
14. Velg **Tekstkonstant**.
15. Skriv inn en verdi i **Tekst**-feltet.
16. Velg **Legg til**.
17. Velg **Størrelse**.
18. Lukk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tilordne terminologien til en produktstandard
1. Velg **Produktdimensjonsgrupper**.
2. Velg **produktdimensjonsgruppen SizeCol**.
3. Velg **Rediger**.
4. Velg **Ja** i feltet **Bruk nomenklatur**.
5. Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.
6. Lukk siden.

