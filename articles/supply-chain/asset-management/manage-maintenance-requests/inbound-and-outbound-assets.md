---
title: Innkommende og utgående aktiva
description: Dette emnet forklarer hvordan du registrerer innkommende og utgående aktiva i Aktivabehandling.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c77aa0dc10844fbe07afa0b8d2a6f3578a246ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253355"
---
# <a name="inbound-and-outbound-assets"></a>Innkommende og utgående aktiva

[!include [banner](../../includes/banner.md)]

 

Hvis firmaet har reparasjonsjobber eller vedlikeholdsjobber på aktiva som mottas fra andre lokasjoner eller kunder, kan Aktivastyring spore både innkommende aktiva som er på vei til firmaet og utgående aktiva som returneres.

> [!NOTE]
> Hvis du vil bruke inngående og utgående livssyklustilstander til å administrere aktiva som kommer inn og blir returnert, må du definere livssyklustilstander for vedlikeholdsforespørsler og livssyklusmodeller for å støtte disse handlingene. Hvis du vil ha mer informasjon, kan du se [Meldinger](../setup-for-maintenance-requests/requests.md).

Oppsettet av Aktivastyring bestemmer om du kan arbeide med inngående og utgående aktiva.

## <a name="register-assets-as-inbound"></a>Registrer aktiva som inngående

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.
2. Velg vedlikeholdsforespørselen.
3. Velg **Oppdater tilstand for vedlikeholdsforespørsel**.
4. Velg **Inngående** (eller en annen livssyklustilstand som du har opprettet for innkommende aktiva), og velg deretter **OK**.

![Registrer aktiva som inngående](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Registrer innkommende aktiva som mottatt

1. Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Innkommende aktiva**.
2. Velg aktivumet eller vedlikeholdsforespørselen.
3. Velg **Motta aktiva**.
4. Angi dato og klokkeslett i feltet **Mottatt**. Velg deretter **OK**. Posten fjernes fra listesiden **Innkommede aktiva**.

![Registrer innkommende aktiva som mottatt](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Registrer aktiva som utgående

Når du har fullført vedlikeholds- eller reparasjonsjobben, kan du registrere aktivumet som returnert.

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.
2. Velg vedlikeholdsforespørselen.
3. Velg **Oppdater tilstand for vedlikeholdsforespørsel**.
4. Velg **Utgående** (eller en annen livssyklustilstand som du har opprettet for utgående aktiva), og velg deretter **OK**.

## <a name="register-outbound-assets-as-delivered"></a>Registrer utgående aktiva som levert

1. Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Utgående aktiva**.
2. Velg aktivumet eller vedlikeholdsforespørselen.
3. Velg **Lever aktiva**.
4. Angi dato og klokkeslett i feltet **Levert**. Velg deretter **OK**. Posten fjernes fra listesiden **Utgående aktiva**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]