---
title: Angi krysskursen
description: Denne artikkelen gir informasjon om krysskurs i Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889968"
---
# <a name="specify-the-cross-rate"></a>Angi krysskursen

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer formålet med en kryssats, og hvordan du spesifiserer kryssatsen når du utligner en betaling med en faktura. Bruk en kryssats når kriteriene nedenfor gjelder: 
-   Du utligner en betaling med en faktura. 
-   Betalingslinjen og fakturalinjen bruker forskjellige valutaer. 
-   Ingen valuta er regnskapsvalutaen. 

Krysskursen brukes ikke til å beregne valutaomveksling for betalingstransaksjon til betalingsregnskapsvalutaen. Valutakursene fra valutakurstabellene hentes i stedet for å beregne verdien av valutabeløpet for betalingstransaksjonen og valutabeløpet for betalingsregnskapet. 

Regnskapsvalutaen er for eksempel USD, fakturavalutaen er CAD og betalingsvalutaen er EUR. Med kryssatsen kan du angi en valutakurs for å konvertere direkte mellom CAD og EUR, og ikke måtte konvertere gjennom USD. Når du velger en faktura og en hovedbetaling, kan du angi en kryssats for fakturalinjen. Kryssatsen er valutakursen mellom valutaene for disse transaksjonene på utligningsdatoen.

1.  Gå til én av følgende sider:
- **Kunder > Felles > Kunder > Alle kunder** 
- **Leverandører > Felles > Leverandører > Alle leverandører** 
- **Innkjøp og leverandører > Felles > Leverandører > Alle leverandører**
2.  Velg kunden eller leverandøren som du utligner åpne transaksjoner for. 
3.  For en kunde, på **Alle kunder**-listesiden gå til **Samle inn > Utlign åpne transaksjoner**. For en leverandør, på **Alle leverandører**-listesiden gå til **Faktura > Utlign åpne transaksjoner**. 
4.  Velg transaksjonen som er hovedbetalingen, og klikk deretter på **Merk betaling**. Avmerkingsboksen i **Merk**-kolonnen er valgt, og det vises et informasjonsikon i **Primærbetaling**-kolonnen. 
5.  I **Kryssats**-feltet kan du angi valutakursen mellom fakturavalutaen og betalingsvalutaen som gjelder på utligningsdatoen. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
