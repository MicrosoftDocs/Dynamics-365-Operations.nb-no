---
title: Opprette og tilordne avanserte regelstrukturer
description: Dette emnet forklarer hvordan du oppretter og tilordner en avansert regelstruktur til en kontostruktur.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb18b96d6d7db84262f8fcfadb15afa80e2fa3d8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145129"
---
# <a name="create-and-assign-advanced-rule-structures"></a>Opprette og tilordne avanserte regelstrukturer

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter og tilordner en avansert regelstruktur til en kontostruktur. Denne veiledningen bruker USMF demo firmaet.

## <a name="create-an-advanced-rule-structure"></a>Opprett en avansert regelstruktur
1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Avanserte regelstrukturer**.
2. Velg **Ny** for å åpne nedtrekksdialogen.
3. I feltet **Avansert regelstruktur** skriver du inn et navn som beskriver strukturen for regelen.
4. Velg **OK**.
5. Velg **Legg til segment**.
6. Velg en finansdimensjon i listen over segmenter. For eksempel **Butikk**.  
7. Velg **Legg til segment**.
8. Velg **Aktiver**.

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a>Bruke en avansert regelstruktur for en kontostruktur
1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Kontoplan > Strukturer > Konfigurer kontostrukturer**.
2. I listen, Finn og Merk kontostrukturen du vil bruke den avanserte regelen for.
3. Velg **Rediger**. Du kan også velge **Avanserte regler**, og du blir bedt om å plassere kontostrukturen i **utkastmodus**.  
4. Velg **Avanserte regler**.
5. Velg **Ny** for å åpne nedtrekksdialogen.
6. Skriv inn en verdi i feltet **Avansert regel**.
7. Skriv inn en verdi i **Navn**-feltet.
8. Velg **Opprett**.
9. Velg **Legg til nye kriterier**.
10. Velg hovedkontoen eller en finansdimensjon i feltet **Hvor**.
11. Velg et alternativ, for eksempel **er mellom** og **inkluderer** i **Operator**-feltet.
12. Skriv inn en verdi i **Verdi**-feltet.
13. Skriv inn en verdi i feltet **via**.
14. Velg **Legg til** for å åpne nedtrekksdialogen.
15. I listen finner du den avanserte regelstrukturen du vil bruke når kriteriene du angav er oppfylt.
16. Velg **Legg til**.
17. Lukk siden.
18. Velg **Aktiver**.

