---
title: Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter
description: Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920663"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse. Denne oppgaven vil vanligvis bli utført av en produktdesigner.


## <a name="create-a-product-number-nomenclature"></a>Opprette produktnummerterminologi

1. Gå til **Behandling av produktinformasjon \> Oppsett \> Produktterminologi**.
1. Velg **Ny**.
1. I **Navn**-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel `ColorSize`.
1. Skriv inn en verdi i **Beskrivelse**-feltet.
1. Velg **Legg til**.
1. Velg **Produktstandardnummer**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Farge**.
1. Velg **Legg til**.
1. Velg **Tekstkonstant**.
1. Skriv inn en verdi i **Tekst**-feltet.
1. Velg **Legg til**.
1. Velg **Størrelse**.
1. Lukk siden.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Tilordne terminologien til en produktstandard

1. Velg **Produktdimensjonsgrupper**.
2. Velg **produktdimensjonsgruppen SizeCol**.
3. Velg **Rediger**.
4. Velg **Ja** i feltet **Bruk nomenklatur**.
5. Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.
6. Lukk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]