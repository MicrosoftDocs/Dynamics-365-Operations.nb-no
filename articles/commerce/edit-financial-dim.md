---
title: Redigere finansdimensjoner for detaljhandelstransaksjoner
description: Dette emnet beskriver hvordan du redigerer finansdimensjoner for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019913"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Redigere finansdimensjoner for detaljhandelstransaksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du redigerer finansdimensjoner for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Redigere finansdimensjoner

Følg denne fremgangsmåten for å redigere finansdimensjoner for detaljhandelstransaksjoner i Commerce Headquarters.

1. Åpne siden **Konfigurasjon av finansdimensjoner for programintegrering**.
1. Velg den aktive posten **Integrering av standarddimensjoner**.
1. I hurtigfanen **Finansdimensjoner** sørger du for at alle dimensjonene du vil redigere i Excel-regnearket, finnes i listen **Valgt**. Hvis du vil ha mer informasjon, kan du se [Dataenheter](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Last ned og åpne Excel-filen fra siden **Utdrag**, siden **Detaljhandelstransaksjoner** eller flisen **Transaksjonsvalideringsfeil** i arbeidsområdet **Finans for handelsbutikk**.
1. Hvis du vil endre finansdimensjonen for transaksjonen, velger du **Utforming**, og deretter velger du blyantsymbolet ved siden av raden **Transaksjon (kan overvåkes)**.
1. Finn og merk av i feltet **FinancialDimensionDisplayValue**, velg en celle i hodedelen av Excel-regnearket, og velg deretter **Legg til etikett**.
1. Merk en celle under cellen du merket i det forrige trinnet, velg **Legg til verdi**, og velg deretter **Oppdater**. Finansdimensjonene legges til i Excel-regnearket, og de kan deretter redigeres og publiseres.
1. Hvis du vil endre dimensjonene på transaksjonslinjene, velger du **Salgstransaksjoner (kan overvåkes)**, velger blyantsymbolet, og gjentar deretter trinn 6 og 7.
1. Hvis du vil endre dimensjonene på betalingslinjene, velger du **Betalingstransaksjoner (kan overvåkes)**, velger blyantsymbolet, og gjentar deretter trinn 6 og 7.

## <a name="additional-resources"></a>Tilleggsressurser

[Redigere og overvåke hentesalgs- og kassastyringstransaksjoner](edit-cash-trans.md)

[Rediger og overvåk nettordretransaksjoner og asynkrone kundeordretransaksjoner](edit-order-trans.md)

[Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](create-excel-edit.md)

[Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]