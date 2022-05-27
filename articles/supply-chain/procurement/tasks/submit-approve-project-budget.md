---
title: Arbeidflyten Opprette og sende et prosjektbudsjett
description: Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.
author: GalynaFedorova
ms.date: 11/22/2021
ms.topic: article
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e554fb578371f52f665ef348d6fa81fd27196a9e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671036"
---
# <a name="create-and-submit-a-project-budget-workflow"></a>Arbeidflyten Opprette og sende et prosjektbudsjett

[!include [banner](../../includes/banner.md)]

Når du oppretter et prosjektbudsjett, kan du angi estimerte inntekter og kostnader for prosjektet, og bruke verdiene til å kontrollere de faktiske prosjekttransaksjonene. Prosjektbudsjettering krever at alle opprinnelige budsjetter og endringer sendes til en projektarbeidsflyt for godkjenning. Arbeidsflyten gir deg bedre kontroll over budsjetteringen og oppretter en endringshistorikkpost. Når du har [opprettet et proskelt](/dynamicsax-2012/appuser-itpro/create-a-project), bruker du denne prosedyren til å opprette og sende inn budsjettet.

1. Gå til **Moduler** > **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**.
1. Velg prosjektet fra prosjektlisten.
1. Velg kategorien **Plan** på prosjektets detaljside.
1. Velg **Prosjektbudsjett** under **Budsjett**-gruppe.
1. På **Generelt**-hurtigfanen angir du informasjonen nedenfor:
   - Skriv inn en verdi i **Beskrivelse**-boksen.
   - Velg alternativ for **Opprinnelig budsjett**.
   - Velg alternativ for **Gjenstående budsjett**.
1. Utvid hurtigfanen **Kostnader**, og velg **Ny**. Deretter kan du utføre følgende innstillinger:
   - Velg et alternativ for **Transaksjonstype**.
   - Velg en passende **Kategori**.
   - Angi en verdi i **Opprinnelig budsjett**.
1. Utvid hurtigfanen **Omsetning**, og velg **Ny**. Deretter kan du utføre følgende innstillinger:
   - Velg et alternativ for **Transaksjonstype**.
   - Velg en **Kategori**.
   - Angi en verdi for **Opprinnelig budsjett**.
1. Velg **Lagre**.
1. Velg **Arbeidsflyt \> Send inn**.
1. På siden **Se gjennom arbeidsflyt for opprinnelig budsjett - Send inn** angir du en **Kommentar**, og velger **Send inn**.
