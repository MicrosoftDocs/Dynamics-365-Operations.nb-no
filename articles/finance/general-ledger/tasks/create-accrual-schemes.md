---
title: Opprette avsetningsplaner
description: Dette emnet forklarer hvordan du oppretter en avsetningsplan.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446473"
---
# <a name="create-accrual-schemes"></a>Opprette avsetningsplaner

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en avsetningsplan. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppsett > Avsetningsplaner**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Avsetningsidentifikasjon**.
4. Skriv inn en verdi i feltet **Beskrivelse av avsetningsplan**.
5. Angi de ønskede verdiene i feltet **Debet**. Hovedkontoen definert vil erstatte debet hovedkontoen i journalbilagslinjen, og den brukes også for tilbakeføring av henvisning basert på finansavsetningstransaksjoner.  
6. Angi de ønskede verdiene i feltet **Kredit**. Hovedkontoen definert vil erstatte kredit hovedkontoen i journalbilagslinjen, og den brukes også for tilbakeføring av henvisning basert på finansavsetningstransaksjoner.  
7. I **Bilag**-feltet velger du hvordan bilaget bestemmes når transaksjonene posteres.
8. Skriv inn en verdi for å beskrive transaksjonene som posteres i **Beskrivelse**-feltet.
9. Velg hvor ofte transaksjoner skal skje i **Periodefrekvens**-feltet.
10. Angi et nummer i feltet **Antall forekomster etter periode**.
11. Velg når transaksjonene skal posteres, for eksempel **per måned**, i feltet **Poster transaksjoner**.

