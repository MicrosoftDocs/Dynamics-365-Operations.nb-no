---
title: Tilbakeføring av ferdigmeldinger oppretter en uventet åpen transaksjon
description: Tilbakeføring av ferdigmeldte varer som har merking, oppretter en åpen transaksjon der det tilbakeførte antallet har de samme lagerdimensjonene som den tilbakeførte transaksjonen.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714216"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Tilbakeføring av ferdigmeldinger oppretter en uventet åpen transaksjon

KB-nummer: 4612469

## <a name="symptoms"></a>Symptomer

Hvis du tilbakefører ferdigmeldte varer som har merking, oppretter systemet en åpen transaksjon der det tilbakeførte antallet har de samme lagerdimensjonene som den tilbakeførte transaksjonen.

## <a name="resolution"></a>Oppløsning

Når du tilbakefører en ferdigmeldingsoperasjon, initialiseres lagerdimensjonen fra produksjonsjournalen. Derfor hentes partinummeret. På grunn av merking vil salgsordretransaksjonene arve partinummeret.

Dimensjonen kan tilbakestilles når ferdigmeldingen posteres.
