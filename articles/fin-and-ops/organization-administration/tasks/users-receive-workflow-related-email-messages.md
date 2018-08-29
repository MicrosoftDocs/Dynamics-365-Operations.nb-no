--- 
title: "Konfigurere systemet for å sende arbeidsflytrelatert e-post til brukere"
description: "Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a>Konfigurere systemet for å sende arbeidsflytrelatert e-post til brukere

[!include [task guide banner](../../includes/task-guide-banner.md)]

Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser. E-postmeldinger kan for eksempel sendes til brukere når dokumentene er tilordnet til dem for godkjenning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.

1. Gå til Systemadministrasjon > Brukere > Brukere.
2. Finn og velg ønsket post i listen.
3. Klikk Brukeralternativer.
4. Klikk Arbeidsflyt-kategorien.
    * Kontroller at delen Varslinger er utvidet.     I delen Varslinger kan du angi hvordan du vil at brukeren skal varsles om arbeidsflytrelaterte hendelser.  
5. Velg et alternativ i feltet Varslingstype for arbeidsflyt for linjeelement.
    * Gruppert – Varslinger for linjeelementer grupperes i en enkelt e-postmelding.    Enkeltvis – En e-postmelding sendes for hvert linjeelement.  
    * Hvis du vil at brukeren skal motta varslinger i klienten, merker du av for Send varslinger i e-post.  
6. Klikk Lagre.
7. Lukk siden.


