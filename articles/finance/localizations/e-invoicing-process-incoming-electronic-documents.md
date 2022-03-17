---
title: Behandling av innkommende elektroniske dokumenter
description: Dette emnet gir en oversikt over behandlingen for innkommende elektroniske dokumenter.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9701367e1ba1f9dbd1e53deb863c10af4213a359
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371604"
---
# <a name="processing-of-incoming-electronic-documents"></a>Behandling av innkommende elektroniske dokumenter

[!include [banner](../includes/banner.md)]

Innkommende elektroniske dokumenter, for eksempel elektroniske leverandørfakturaer, kan importeres og behandles på to måter:

- Filer hentes fra eksterne kanaler og sendes direkte til det tilkoblede programmet. Der gjennomgår de ytterligere transformasjon og importeres deretter til databasen.
- Filer gjennomgår forhåndsbehandling i tjenesten for elektronisk fakturering og sendes deretter til det tilkoblede programmet.

Elektronisk fakturering støtter to kanaler for innkommende dokumenter: e-post og Microsoft SharePoint-mapper.

Det finnes to oppsettyper som brukes til å angi om dokumenter skal gjennomgå forhåndsbehandling eller i stedet sendes direkte til det tilkoblede programmet:

- **Datakanal** – Systemet sender dokumentet direkte til det tilkoblede programmet.
- **Datakanal med datasamlebånd for behandling** – Du kan konfigurere flere handlinger som skal kjøres før dokumentet sendes til det tilkoblede programmet.

Hvis du vil ha informasjon om hvordan du konfigurerer scenarioene for behandling av innkommende elektroniske dokumenter for de ulike kanalene, kan du se [Konfigurer en e-postkanal](e-invoicing-configure-email.md) og [Konfigurer en SharePoint-kanal](e-invoicing-configure-sharepoint-channel.md).
