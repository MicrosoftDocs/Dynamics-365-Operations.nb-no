---
title: Annuller serviceordrer
description: Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved å kjøre en periodisk jobb.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a253a9c9ae4d7c34403db9bb5f3d63bc77e11101
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259680"
---
# <a name="cancel-service-orders"></a>Annuller serviceordrer   

[!include [banner](../includes/banner.md)]


Du kan annullere en serviceordre eller serviceordrelinje fra selve serviceordren, eller du kan annullere flere serviceordrer ved å kjøre en periodisk jobb.


> [!NOTE]
> <P>Serviceordrer kan ikke annulleres hvis stadiet serviceordren er i, ikke tillater annullering, hvis serviceordren har varebehov, eller hvis seviceordren allerede er postert.</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>Annullere en serviceordre fra Serviceordrer-skjemaet

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**. Velg serviceordren, og klikk deretter på **Annuller ordre** i handlingsruten.

## <a name="cancel-a-service-order-line"></a>Annullere en serviceordrelinje

1.  Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**. Dobbeltklikk på serviceordren som inneholder linjen du vil annullere.

2.  Velg serviceordrelinjen du vil annullere, og klikk deretter **Avbryt ordrelinje** for å endre statusen for linjen til **Avbrutt**.


> [!TIP]
> <P>For å tilbakeføre annullering av en serviceordrelinje og endre statusen tilbake til <STRONG>Opprettet</STRONG>, klikk på <STRONG>Opphev annullering</STRONG>.</P>


## <a name="cancel-multiple-service-orders"></a>Annullere flere serviceordrer

1.  Klikk på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Annuller serviceordrer**.

2.  Klikk på **Velg**-knappen.

3.  I **Forespørsel**-skjemaet i **Vilkår**-kolonnen velger du serviceordrene du vil annullere.

4.  Klikk på **OK** for å lukke **Forespørsel**-skjemaet.

5.  Merk av for **Vis infologg** for å generere en informasjonslogg som viser de annullerte serviceordrene.

6.  Merk av for **Opphev annullering** hvis du vil tilbakeføre en serviceordres **Avbrutt**-status.

7.  Klikk på **OK**.

De valgte serviceordrene blir enten annullert, eller de får sin fremdriftsstatus **Avbrutt** tilbakeført til **Pågår**.


> [!NOTE]
> <P>Hvis du merker av for <STRONG>Opphev annullering</STRONG>, blir serviceordrer med fremdriftsstatusen <STRONG>Avbrutt</STRONG> tilbakeført, og serviceordrer med fremdriftsstatusen <STRONG>Pågår</STRONG> blir ikke annullert.</P>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]