---
title: Dynamics 365-globaliseringstjenester
description: Dette emnet gir en oversikt over Microsoft Dynamics 365-globaliseringstjenester.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893054"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365-globaliseringstjenester

[!include [banner](../includes/banner.md)]

Følgende globaliseringstjenester kan konfigureres slik at de utvider funksjonene som finnes i enkelte Microsoft Dynamics 365 Online-tjenester:

- **Regulatory Configuration Service (RCS)** støtter konfigurasjonen av ulike typer elektroniske dokumenter og rapporter. RCS er en utvidet versjon av ER-designeren (Elektronisk rapportering) der konfigurasjonsrepositoriet er en frittstående tjeneste. Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Service](rcs-overview.md).
- **Elektronisk fakturering** samler sammen konfigurerbare formater for transformasjoner, digitale signaturer og konfigurerbare integrasjoner for tilkobling med eksterne nettjenester, inkludert sertifisering og svarbehandling. For mer informasjon, se [Elektronisk fakturering](e-invoicing-service-overview.md).
- **Avgiftsberegning** gir utvidet fleksibilitet ved å støtte flere avgifts-ID-er, fastsettelse av mva-koder, avgiftsberegningsdesigneren og en kjøretidsmotor for å overholde komplekse avgiftsbestemmelser over hele verden. Hvis du vil ha mer informasjon, kan du se [Avgiftsberegning](global-tax-calcuation-service-overview.md).

Disse globaliseringstjenestene sørger for direkte integrasjon med følgende Dynamics 365-onlinetjenester.

| Onlinetjeneste | RCS | Elektronisk fakturering | Avgiftsberegning (forhåndsversjon) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Ja | Ja | Ja | 
| Dynamics 365 Supply Chain Management | Ja | Ja | Ja | 
| Dynamics 365 Project Operations | Ja | Ja | Gjelder ikke | 
| Dynamics 365 Commerce | Ja | Gjelder ikke | Gjelder ikke | 

> [!NOTE]
> På grunn av forskjeller i tilgjengeligheten av geografiske Azure-lokasjoner for RCS kan konfigurasjon av denne tjenesten føre til at kundedata overføres utenfor den geografiske lokasjonen som er valgt for den aktuelle Dynamics 365-onlinetjenesten. Hvis du vil ha mer informasjon, kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).