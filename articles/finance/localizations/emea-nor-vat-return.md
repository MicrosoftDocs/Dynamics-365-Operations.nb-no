---
title: Mva-retur med direkte innsending til Altinn
description: Dette emnet gir informasjon om mva-returer med direkte innsending til Altinn-funksjonen, som kan brukes til å sende mva-returer i Norge.
author: liza-golub
ms.author: elgolu
ms.date: 11/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.search.validFrom: 2022-11-15
ms.openlocfilehash: 8df6374aacd9e204d7b9df423d66122b8c0638bc
ms.sourcegitcommit: a11e8f4e764ff0bb210875401ae0671bc6412bde
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7866805"
---
# <a name="vat-return-with-direct-submission-to-altinn"></a>Mva-retur med direkte innsending til Altinn

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om funksjonen for **mva-retur med direkte innsending til Altinn**-funksjonen i Microsoft Dynamics 365 Finance. Denne funksjonen kan brukes til å sende inn mva-returer i Norge.

I Skatteinfo nr. 11/2020 innførte Skattemyndighetene et krav til mva-returrapportering som omfatter direkte digital innsending fra regnskapssystemer til Altinn-skatteportalen. Denne digitale innsendingsprosessen erstatter den manuelle prosessen for innsending av mva-returer for periodene 1. januar 2022. Hvis du vil ha mer informasjon om mva-returer med direkte innsending til Altinn, kan du se [Mva-meldingen](https://skatteetaten.github.io/mva-meldingen/english/).

Funksjonen for **Mva-retur med direkte innsending til Altinn** i Finance støtter arkivering av mva-retur for [flere mva-registreringer](emea-multiple-vat-registration-numbers.md) og for firmaer som rapporterer som en [mva-gruppe](emea-nor-vat-return-setup.md#vat-group) i den samme systemdatabasen.

Hvis du vil ha mer informasjon om hvordan du klargjør en mva-retur med direkte innsending til Altinn, kan du se følgende emner:

- [Registrere et integreringspunkt i webportalen for ID-porten](emea-nor-vat-return-integration-point.md)
- [Klargjøre miljøet for samarbeid med nettjenestene ID-porten og Altinn](emea-nor-vat-return-setup.md)
- [Kontrolliste for oppsett av elektroniske meldinger for mva-returer med direkte innsending til Altinn](emea-nor-vat-return-checklist.md)
- [Autorisere Finance-miljøet for samhandling med nettjenestene ID-porten og Altinn](emea-nor-vat-return-authorization.md)
- [Sende en mva-retur til webtjeneste Altinn](emea-nor-vat-return-submission.md)

## <a name="privacy-notice"></a>Personvernerklæring

Når du aktiverer Finance til å samhandle med Skattemyndighetenes API for mva-programvare, vil både kundeinnhold og personlige data deles med skattemyndighetene som del av innsendingen av mva-deklareringen. Denne informasjonen kan inneholde navnet på personen som sendte inn mva-deklareringen. Hvis du vil vite mer om hvilke typer informasjon som inkluderes i innsendingen, kan du se skattemyndighetenes [krav](https://go.microsoft.com/fwlink/?linkid=2178205). En systemadministrator kan deaktivere samhandlingen med Skattemyndighetenes webtjeneste i Finance ved å gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger**.

Personvernet er viktig for oss. Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.
