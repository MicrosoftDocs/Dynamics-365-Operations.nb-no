---
title: Opprette konfigurasjonsleverandører og merke dem som aktive
description: Dette emnet forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER) i Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dfbcf70493a43320e17d4d2734fe6343d43eaf3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850333"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Opprette konfigurasjonsleverandører og merke dem som aktive

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER) i Dynamics 365 for Finance and Operations. Hver ER-konfigurasjon refererer til leverandøren som forfatteren av konfigurasjonen. I dette eksemplet skal du opprette en konfigurasjonsleverandør for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjonsleverandører deles mellom alle firmaer.

## <a name="create-a-provider"></a>Opprette en leverandør
1. Gå til **navigasjonsruten** i øvre venstre hjørne, og velg **Organisasjonsstyring**.
2. Gå til **Arbeidsområder > Elektronisk rapportering**.
3. Gå til **Relaterte koblinger > Konfigurasjonsleverandører**.
4. Velg **Ny**.
    - En leverandørpost har et unikt navn og URL-adresse. Gå gjennom innholdet på denne siden, og hopp over denne fremgangsmåten hvis en post for Litware, Inc. (https://www.litware.com) allerede finnes.  
5. I Navn-feltet skriver du inn `Litware, Inc.`.
6. Skriv inn `https://www.litware.com` i feltet Internett-adresse.
7. Velg **Lagre**.
8. Lukk siden.

## <a name="select-as-an-active-provider"></a>Velg som en aktiv leverandør
1. Velg levandøren Litware, Inc. provider.
2. Velg **Angi som aktiv**.

