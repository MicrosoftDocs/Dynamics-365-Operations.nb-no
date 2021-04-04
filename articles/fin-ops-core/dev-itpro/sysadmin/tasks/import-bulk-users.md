---
title: Importere brukere fra Azure Active Directory
description: Denne fremgangsmåten kan brukes av systemansvarlige til å manuelt importere utvalgte brukere eller importere et stort antall brukere fra Azure Active Directory.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571011"
---
# <a name="import-users-from-azure-active-directory"></a>Importere brukere fra Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Importere utvalgte brukere

Denne fremgangsmåten kan brukes av systemansvarlige til å importere utvalgte brukere fra Azure Active Directory (Azure AD).

1. Brukeren vil bli importert til det gjeldende øktfirmaet som standardfirma. Endre gjeldende firma hvis det er aktuelt, før du importerer brukere.
2. Gå til **Systemadministrasjon > Brukere > Brukere**.
3. Klikk **Importer brukere**.
4. Velg brukerne som skal importeres, og velg **Importer brukere**.

Når importen er fullført, må det tilordnes roller til brukerne.

## <a name="import-users-in-bulk"></a>Masseimportere brukere

Denne fremgangsmåten kan brukes av systemansvarlige til å importere et stort antall brukere fra Azure Active Directory.
Vær oppmerksom på at det ikke er mulig å velge brukere når du bruker alternativet for satsvis import.

## <a name="run-the-import-as-a-batch-job"></a>Kjøre importen som en satsvis jobb
1. Brukeren vil bli importert til det gjeldende øktfirmaet som standardfirma. Endre gjeldende firma hvis det er aktuelt, før du importerer brukere.
2. Gå til **Systemadministrasjon > Brukere > Brukere**.
3. Klikk **Satsvis import**.
4. Vis delen **Kjør i bakgrunnen**.
4. Velg **Ja** i feltet **Satsvis behandling**.
6. Angi eller velg en verdi i feltet **Satsvis gruppe**. Dette er et valgfritt trinn.  
7. Velg **Ja** i feltet **Privat**. Dette er et valgfritt trinn.  
8. Velg **Ja** i feltet **Kritisk jobb**. Dette er et valgfritt trinn.  
9. Velg et alternativ i feltet **Overvåkingskategori**.
10. Klikk på **OK**.

Når importen er fullført, må det tilordnes roller til brukerne.

## <a name="run-in-a-sandbox-environment"></a>Kjøre i et sandkassemiljø
1. Velg **Satsvis import**.
2. Velg **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]