---
title: Opprette en produktnummerterminologi for forhåndsdefinerte produktvarianter
description: Dette emnet viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5179dd54f22de11dc4c0f54113376f13b2f59c48
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569583"
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