---
title: Velkomst-e-post sendes ikke når nye kunder opprettes
description: Denne artikkelen gir feilsøkingsveiledning som kan være til hjelp hvis en velkomst-e-postvarsling ikke sendes når en ny kunde opprettes i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219411"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Velkomst-e-post sendes ikke når nye kunder opprettes

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir feilsøkingsveiledning som kan være til hjelp hvis en velkomst-e-postvarsling ikke sendes når en ny kunde opprettes i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Når en ny kunde opprettes i Commerce Headquarters, sendes det ikke en velkomst-e-post til kunden, selv om det er konfigurert en e-postvarsling for e-postvarslingstypen **Kunden er opprettet**.

## <a name="resolution"></a>Oppløsning

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Knytt en e-postvarslingsprofil under Commerce-parametere

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere \> Generelt** i Commerce Headquarters.
2. I rullegardinlisten **E-postvarslingsprofil** velger du e-postvarslingsprofilen som inneholder en tildeling mellom kunden som ble opprettet av en varslingstype, og en e-postmal som ble opprettet av kunden.  

> [!NOTE] 
> Når du aktiverer kundeopprettede varslinger, mottar kunder som opprettes i alle kanaler i den juridiske enheten, en kundeopprettet e-post. Kundeopprettede varslinger kan for øyeblikket ikke begrenses til én enkelt kanal.

Hvis du vil ha mer informasjon, kan du se [Opprette e-postmaler for transaksjonshendelser](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Tilleggsressurser

[Definere en profil for e-postvarsling](../email-notification-profiles.md)
