---
title: Opprette sjekker som har tom status
description: Dette emnet beskriver hvordan du oppretter en tom sjekk for en bankkonto på Sjekker-siden.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 94d3a4ac8a3906e48f5a6053c031001c111549ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254041"
---
# <a name="create-checks-that-have-blank-status"></a>Opprette sjekker som har tom status

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter tomme sjekker. Du kan for eksempel opprette en tom sjekk for å registrere en sjekk som er skadet, og som ikke kan brukes til betaling.

På **Sjekker**-siden utfører du vedlikeholdsoppgaver for sjekker. Du kan for eksempel opprette nye sjekknumre og slette sjekker. Du kan også opprette sjekker som har statusen **Tom**. Når tomme sjekker er opprettet, kan de ikke slettes eller brukes på nytt i systemet.

> [!NOTE]
> Denne funksjonen er tilgjengelig på **Sjekker**-siden bare hvis du aktiverer funksjonen **Opprett sjekker med tom status på Sjekker-siden** på siden **Funksjonsbehandling**. Hvis funksjonen ikke er aktivert, kan sjekker som har statusen **Tom**, bare opprettes fra dialogboksen **Betaling med sjekk** under betalingsgenereringsprosessen i Leverandører.

Hvis du vil åpne **Sjekker**-siden, går du til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**, og deretter velger du **Sjekker** i gruppen **Beslektet informasjon** i fanen **Administrer betalinger** i handlingsruten. Alternativt kan du gå til **Kontant- og bankbehandling \> Forespørsler og rapporter \> Sjekker**.

Hvis du vil opprette sjekker som har statusen **Tom**, velger du **Opprett tomme sjekker** i handlingsruten. Mens systemet oppretter tomme sjekker, er den tilknyttede bankkontoen midlertidig deaktivert. Denne virkemåten reduserer risikoen for at betalinger blir generert samtidig som tomme sjekker opprettes. Når behandlingen er fullført, aktiveres den tilknyttede bankkontoen på nytt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]