---
title: Angi krysskurs
description: Dette emnet gir informasjon om krysskurs i Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "320242"
---
# <a name="specify-the-cross-rate"></a>Angi krysskurs

[!include [banner](../includes/banner.md)]

Dette emnet forklarer formålet med en kryssats, og hvordan du spesifiserer kryssatsen når du utligner en betaling med en faktura. Bruk en kryssats når alle kriteriene nedenfor gjelder: 
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
