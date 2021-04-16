---
title: Oversikt over MyLeaveRequests
description: MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803639"
---
# <a name="myleaverequests-overview"></a>Oversikt over MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.

## <a name="key"></a>Nøkkel

  | Egenskapsnavn | Datatype |
  |---------------|-----------|
  | dataAreaId    | Streng    |
  | RequestId     | Streng    |
  | LeaveType     | Streng    |
  | LeaveDate     | Dato      |
  
## <a name="properties"></a>Egenskaper

  | Egenskapsnavn     | Datatype | Obligatorisk |
  |-------------------|-----------|----------|
  | dataAreaId        | Streng    | X        |
  | RequestId         | Streng    | X        |
  | LeaveType         | Streng    | X        |
  | LeaveDate         | Dato      | X        |
  | ReasonCodeId      | Streng    |          |
  | PersonnelNumber   | Streng    | X        |
  | RequestDate       | Dato      | X        |
  | Kommentar           | Streng    |          |
  | Status            | Opplisting      | X        |
  | Beløp            | Kommatall      |          |
  | HalfDayDefinition | Opplisting      |          |

## <a name="actions"></a>Handlinger

 | Handlingsnavn                               | Beskrivelse                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [Send](hr-developer-api-myleaverequests-submit.md)   | Sender forespørselen som skal behandles av en arbeidsflyt. |

## <a name="see-also"></a>Se også

- [Sende en permisjonsforespørsel til arbeidsflyt](hr-developer-api-myleaverequests-submit.md)
- [Godkjenning](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]