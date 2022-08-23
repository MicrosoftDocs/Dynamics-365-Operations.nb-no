---
title: Behandling av innkommende elektroniske dokumenter
description: Denne artikkelen gir en oversikt over behandlingen for innkommende elektroniske dokumenter.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277309"
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
