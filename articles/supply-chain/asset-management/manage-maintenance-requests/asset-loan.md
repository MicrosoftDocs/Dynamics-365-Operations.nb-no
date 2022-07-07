---
title: Objektlån
description: Denne artikkelen beskriver hvordan du registrerer lån av aktiva i Aktivumbehandling.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectLoanSend, EntAssetObjectLoanListPage, EntAssetObjectLoanReturn, EntAssetObjectLoanInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f70b29ef69b80160f108e6f53edda12b86c2c9db
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015761"
---
# <a name="asset-loans"></a>Objektlån

[!include [banner](../../includes/banner.md)]

 

Hvis firmaet ditt mottar aktiva for reparasjons- eller vedlikeholdsjobber fra enten interne lokasjoner eller kunder, og hvis du midlertidig låner ut aktiva til de aktuelle stedene eller kundene, kan Aktivastyring spore objektlånene.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Registrere lån av gjenstander på en melding

1. Velg **Aktivastyring** \> **Meldinger** \> **Alle meldinger** eller **Aktive meldinger**.
2. Velg vedlikeholdsanmondningen du skal registrere et obektlån for, og velg deretter **Rediger**.
3. På **Forespørsel**-siden velger du **Send utlånsobjekt**.
4. Velg aktivumet, og angi den forventede returdatoen.
5. Velg **OK**.

> [!NOTE]
> - Du kan bare sende et utlånsobjekt hvis et aktivum av samme type er tilgjengelig.
> - Aktivumet du låner ut, må ha en livssyklustilstand som gjør at det kan brukes som et utlånsobjekt, for eksempel **InStorage**. Når objektlånet er registrert, oppdateres aktivumets livssyklustilstand automatisk til for eksempel **OnLoan**.

Hvis du vil vise en liste over alle aktivumene du har lånt ut til andre lokasjoner eller kunder, velger du **Aktivastyring** \> **Objektlån** \> **Alle objektlån**. Hvis det er merket av for **Avsluttet** for et aktivum, er aktivumet registrert som returnert til firmaet.

![Behandle meldinger.](media/06-manage-maintenance-requests.png)

På siden **Aktive objektlån** kan du vise en liste over alle utlånsobjekter som ennå ikke er returnert til selskapet.

## <a name="register-loan-assets-as-returned"></a>Registrer utlånsobjekter som returnert

1. Velg **Aktivastyring** \> **Objektlån** \> **Aktive objektlån**.
2. Velg lånet av gjenstander du vil registrere som returnert, og velg deretter **Returner objektlån**.
3. Angi dato og klokkeslett i feltet **Returnert**.
4. Velg **OK**.
5. Oppdater listesiden **Aktive objektlån**, og legg merke til at objektlånet ikke lenger vises i listen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]