---
title: Lån av gjenstander
description: Dette emnet beskriver hvordan du registrerer lån av aktiva i Aktivumbehandling.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8680241b1300aceda3280893982a1eff3d2e09e0
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847488"
---
# <a name="asset-loans"></a>Lån av gjenstander

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Hvis firmaet ditt mottar aktiva for reparasjons- eller vedlikeholdsjobber fra enten interne lokasjoner eller kunder, og hvis du midlertidig låner ut aktiva til de aktuelle stedene eller kundene, kan Aktivumbehandling spore lånet av gjenstander.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrere lån av gjenstander på en vedlikeholdsanmodning

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlilkeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.
2. Velg vedlikeholdsanmondningen du skal registrere et lån av gjenstander for, og velg deretter **Rediger**.
3. På **Forespørsel**-siden velger du **Send lån av gjenstander**.
4. Velg aktivumet, og angi den forventede returdatoen.
5. Velg **OK**.

> [!NOTE]
> - Du kan bare sende et lån av gjenstander hvis et aktivum av samme type er tilgjengelig.
> - Aktivumet du låner ut, må ha en livsløpstilstand som gjør at det kan brukes som et låneaktivum, for eksempel **InStorage**. Når lånet av gjenstander er registrert, oppdateres aktivumets livsløpstilstand automatisk til for eksempel **OnLoan**.

Hvis du vil vise en liste over alle aktivumene du har lånt ut til andre lokasjoner eller kunder, velger du **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Alle lån av gjenstander**. Hvis det er merket av for **Avsluttet** for et aktivum, er aktivumet registrert som returnert til firmaet.

![Figur 1](media/06-manage-maintenance-requests.png)

På siden **Aktive lån av gjenstander** kan du vise en liste over alle lånegjenstander som ennå ikke er returnert til selskapet.

## <a name="register-loan-assets-as-returned"></a>Registrer lånegjenstander som returnert

1. Velg **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Aktive lån av gjenstander**.
2. Velg lånet av gjenstander du vil registrere som returnert, og velg deretter **Returner lån av gjenstander**.
3. Angi dato og klokkeslett i feltet **Returnert**.
4. Velg **OK**.
5. Oppdater listesiden **Aktive lån av gjenstander**, og legg merke til at lånet av gjenstander ikke lenger vises i listen.