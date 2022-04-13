---
title: Lagerjournalarbeidsflyten blir aldri fullført, og journalen kan ikke behandles
description: Når du har sendt inn en arbeidsflyt for journalgodkjenning, slutter arbeidsflytbehandlingen å svare, og du kan ikke redigere eller behandle journalene.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488974"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Lagerjournalarbeidsflyten blir aldri fullført, og journalen kan ikke behandles

## <a name="symptoms"></a>Symptomer

Når du har sendt inn en arbeidsflyt for journalgodkjenning, slutter arbeidsflytbehandlingen å svare, og du kan ikke redigere eller behandle journalene.

## <a name="resolution"></a>Løsning

Det er flere årsaker til at arbeidsflytbehandling kanskje ikke fullføres. Se etter følgende problemer:

- Gå til **Lagerstyring &gt; Oppsett &gt; Arbeidsflyter for lagerstyring**, og gå gjennom konfigurasjonen til den berørte arbeidsflyten. Hvis du vil ha mer informasjon, kan du se [Godkjenningsarbeidsflyter for lagerjournal](../../inventory/inventory-journal-workflow.md).
- Arbeidsflyten kan bli utsatt for et unntak eller en feil. Gå gjennom loggen for arbeidselement i den berørte arbeidsflyten for å se om den omfatter en programfeil som avslutter arbeidsflyten.
- Lagerjournalen kan bare oppdateres eller redigeres hvis den er godkjent. Hvis tilbakekalling er aktiv, kan du prøve å tilbakekalle journalen. Kjøring av den satsvise arbeidsflytjobben kan bli avbrutt av flere årsaker. Noen av disse årsakene kan være forårsaket av problemer med arbeidsflytrammeverket.
