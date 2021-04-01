---
title: Lån av gjenstander
description: Dette emnet beskriver hvordan du registrerer lån av aktiva i Aktivumbehandling.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d76d8e9b735adc1fa796cff5e0ef7d049d109144
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253452"
---
# <a name="asset-loans"></a>Lån av gjenstander

[!include [banner](../../includes/banner.md)]

 

Hvis firmaet ditt mottar aktiva for reparasjons- eller vedlikeholdsjobber fra enten interne lokasjoner eller kunder, og hvis du midlertidig låner ut aktiva til de aktuelle stedene eller kundene, kan Aktivumbehandling spore lånet av gjenstander.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrere lån av gjenstander på en melding

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlilkeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.
2. Velg vedlikeholdsanmondningen du skal registrere et lån av gjenstander for, og velg deretter **Rediger**.
3. På **Forespørsel**-siden velger du **Send lån av gjenstander**.
4. Velg aktivumet, og angi den forventede returdatoen.
5. Velg **OK**.

> [!NOTE]
> - Du kan bare sende et lån av gjenstander hvis et aktivum av samme type er tilgjengelig.
> - Aktivumet du låner ut, må ha en livssyklustilstand som gjør at det kan brukes som et låneaktivum, for eksempel **InStorage**. Når lånet av gjenstander er registrert, oppdateres aktivumets livssyklustilstand automatisk til for eksempel **OnLoan**.

Hvis du vil vise en liste over alle aktivumene du har lånt ut til andre lokasjoner eller kunder, velger du **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Alle lån av gjenstander**. Hvis det er merket av for **Avsluttet** for et aktivum, er aktivumet registrert som returnert til firmaet.

![Behandle vedlikeholdsforespørsler](media/06-manage-maintenance-requests.png)

På siden **Aktive lån av gjenstander** kan du vise en liste over alle lånegjenstander som ennå ikke er returnert til selskapet.

## <a name="register-loan-assets-as-returned"></a>Registrer lånegjenstander som returnert

1. Velg **Anleggsmiddelbehandling** \> **Felles** \> **Lån av gjenstander** \> **Aktive lån av gjenstander**.
2. Velg lånet av gjenstander du vil registrere som returnert, og velg deretter **Returner lån av gjenstander**.
3. Angi dato og klokkeslett i feltet **Returnert**.
4. Velg **OK**.
5. Oppdater listesiden **Aktive lån av gjenstander**, og legg merke til at lånet av gjenstander ikke lenger vises i listen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]