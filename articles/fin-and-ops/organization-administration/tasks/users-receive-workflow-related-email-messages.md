---
title: Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger
description: Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916398"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser. E-postmeldinger kan for eksempel sendes til brukere når dokumentene er tilordnet til dem for godkjenning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til **Navigasjonsrute > Moduler > Systemadministrasjon > Brukere > Brukere**.
2. Finn og velg ønsket post i listen.
3. Klikk på **Brukeralternativer** i **handlingsruten**.
4. Klikk på kategorien **Arbeidsflyt**. Kontroller at **Varslinger**-delen er utvidet. I delen **Varslinger** kan du angi hvordan du vil at brukeren skal varsles om arbeidsflytrelaterte hendelser.  
5. Velg et alternativ i feltet **Varslingstype for arbeidsflyt for linjeelement**.
    - Gruppert – Varslinger for linjeelementer grupperes i en enkelt e-postmelding.
    - Enkeltvis – En e-postmelding sendes for hvert linjeelement.  
    - Hvis du vil at brukeren skal motta varslinger i klienten, merker du av for **Send varslinger i e-post**.  
6. Klikk **Lagre**.
7. Lukk siden.

