---
title: Opprette konfigurasjonsleverandører og merke dem som aktive
description: Denne artikkelen forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267821"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Opprette konfigurasjonsleverandører og merke dem som aktive

[!include [banner](../../includes/banner.md)]

Denne artikkelen forklarer hvordan en bruker som er tilordnet til rollen Systemansvarlig eller Utvikler av elektronisk rapportering, kan opprette en konfigurasjonsleverandør for elektronisk rapportering (ER). Hver ER-konfigurasjon refererer til leverandøren som forfatteren av konfigurasjonen. I dette eksemplet skal du opprette en konfigurasjonsleverandør for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma ettersom ER-konfigurasjonsleverandører deles mellom alle firmaer.

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

![Arbeidsområdesiden Elektronisk rapportering.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
