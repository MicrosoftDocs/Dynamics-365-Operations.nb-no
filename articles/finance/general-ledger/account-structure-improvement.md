---
title: Ytelsesforbedring for kontostrukturaktivering
description: Denne artikkelen forklarer den nye ytelsesforbedringen for aktiveringsprosessen for kontostruktur.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714007"
---
# <a name="account-structure-activation-performance-enhancement"></a>Ytelsesforbedring for kontostrukturaktivering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Ved hjelp av denne ytelsesforbedringen kan du aktivere kontostrukturer raskere ved å kjøre flere transaksjonsoppdateringer samtidig. I tillegg er selve strukturen merket som aktiv etter at den er validert, og transaksjonsbehandling kan fortsette mens eksisterende ikke-posterte transaksjoner oppdateres til den nye strukturen. Siden det kan ta litt tid å oppdatere transaksjoner, kan du spore aktiveringsstatusen ved å velge **Vis aktiveringsstatus** over rutenettet på siden **Kontostrukturer**. Du kan også vise aktiveringsstatusen ved å velge **Vis** i handlingsruten og deretter velge **Aktiveringsstatus** på rullegardinmenyen.

[![Siden Kontostrukturer.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Når du har valgt **Vis aktiveringsstatus**, vises en dialogboks som viser de individuelle oppgavene som kjører som en del av aktiveringsprosessen. For hver oppgave kan du vise statusen samt fullføringsdatoen og -klokkeslettet etter at oppgaven er fullført.

[![Tidslinje for aktivering av kontostruktur.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Tips til aktivering av kontostruktur

Dialogboksen for aktivering av kontostruktur som vises når du velger **Aktiver** for en utkastkontostruktur, har en fanedel som heter **Oppdater ikke-posterte transaksjoner**. Denne delen inneholder et alternativ som heter **Fremtving oppdatering**. Du kan velge dette alternativet for å oppdatere alle ikke-posterte transaksjoner til nåværende struktur. Du bør imidlertid bare bruke dette alternativet når det har oppstått en feil, eller hvis Microsofts kundestøtte har sendt deg beskjed om å bruke det.

Her er noen av faktorene som kan påvirke ytelsen til aktiveringsprosessen:

- et stort antall ikke-posterte journalposter
- et stort antall åpne kildedokumentposter, for eksempel fritekstfakturaer, leverandørfakturaer og tilknyttede dokumenter som bruker kildedokumentrammeverket, og som har åpne regnskapsdistribusjoner
- mengden data i TaxUncommitted
- mengden åpne budsjettdata
- import av journaldata mens aktiveringsoppgaver fremdeles kjører

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
