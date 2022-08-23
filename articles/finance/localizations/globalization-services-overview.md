---
title: Dynamics 365-globaliseringstjenester
description: Denne artikkelen gir en oversikt over Microsoft Dynamics 365-globaliseringstjenester.
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278240"
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
| Dynamics 365 Project Operations | Ja | Ja | Gjelder ikke her | 
| Dynamics 365 Commerce | Ja | Gjelder ikke her | Gjelder ikke | 

> [!NOTE]
> På grunn av forskjeller i tilgjengeligheten av geografiske Azure-lokasjoner for RCS kan konfigurasjon av denne tjenesten føre til at kundedata overføres utenfor den geografiske lokasjonen som er valgt for den aktuelle Dynamics 365-onlinetjenesten. Hvis du vil ha mer informasjon, kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).
