---
title: Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger
description: Du kan konfigurere systemet slik at det sendes e-postmeldinger til brukere når det oppstår arbeidsflytrelaterte hendelser.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "344599"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Aktiver brukere for mottak av arbeidsflytrelaterte e-postmeldinger

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

