---
title: Oversikt over MyLeaveRequests
description: MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 90698ddcc8fcf0eb975dffed0bdad11e6b277c90
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984702"
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