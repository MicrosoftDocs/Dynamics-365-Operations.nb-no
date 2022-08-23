---
title: Støtte for flere mva-registreringsnumre i Norges mva-retur
description: Denne artikkelen beskriver hvordan du støtter flere mva-registreringsnumre i en mva-retur i Norge.
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: atrukawk
ms.search.validFrom: 2021-22-12
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 2db400f87f7c62cb213d2f2bfe6c3f380d348441
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272113"
---
# <a name="support-for-multiple-vat-registration-numbers-in-the-vat-return-of-norway"></a>Støtte for flere mva-registreringsnumre i Norges mva-retur

[!include [banner](../includes/banner.md)]

I Skatteinfo nr. 11/2020 innførte Skattemyndighetene et krav til mva-returrapportering som omfatter direkte digital innsending fra regnskapssystemer til Altinn-skatteportalen. Denne digitale innsendingsprosessen erstatter den manuelle prosessen for innsending av mva-returer for periodene 1. januar 2022. Hvis du vil ha mer informasjon om mva-returer med direkte innsending til Altinn, kan du se [Mva-meldingen](https://skatteetaten.github.io/mva-meldingen/english/). Hvis du vil ha mer informasjon om hvordan du definerer og bruker funksjonen **Mva-retur med direkte innsending til Altinn** i Microsoft Dynamics 365 Finance, kan du se [Mva-retur med direkte innsending til Altinn](emea-nor-vat-return.md).

Hvis du vil rapportere en mva-retur for Norge fra en juridisk enhet som har primæradresse utenfor Norge, anbefaler vi at du bruker [Avgiftsberegning](global-tax-calcuation-service-overview.md)-tjenesten, og at du aktiverer funksjonen [Støtte for flere mva-registreringsnumre](emea-multiple-vat-registration-numbers.md) i arbeidsområdet **Funksjonsbehandling**. I tillegg må du kontrollere at du definerer et mva-registreringsnummer i tilleggsfeltet for **Avgiftsregistreringsnummer** i produksjonsbehandlingen **NO mva-retur** i oppsettet for Elektroniske meldinger. Dette nummeret brukes til å sende mva-returen til norske skattemyndigheter. Hvis du vil ha mer informasjon om hvordan du angir et mva-registreringsnummer, kan du se [Angi mva-registreringsnummeret til firmaet som rapporterer en mva-retur](emea-nor-vat-return-setup.md#vat-registration-number).
