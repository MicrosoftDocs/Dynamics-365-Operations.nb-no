---
title: Farlige materialer
description: Dette emnet inneholder informasjon om dokumenter om farlige materialer samt informasjon som er lagret i miljøet.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208473"
---
# <a name="hazardous-materials"></a>Farlige materialer

[!include [banner](../includes/banner.md)]

Informasjon om farlige materialer settes opp i administrering av produktinformasjon. Denne modulen inneholder også dokumenter som kan skrives ut via lagerstyring.

Når du sender materialer som er klassifisert som farlig gods, må ekstra papirarbeid inkluderes i forsendelsene. Med funksjonaliteten for farlige materialer kan kundene lagre klassifiseringsinformasjon og relatere den til utgitte varer. Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen.

> [!IMPORTANT]
> For å forenkle administrering av forsendelser av farlig gods lar Microsoft Dynamics 365 Supply Chain Management deg sette opp ytterligere referanseinformasjon relatert til produkter. Du kan også sette opp ytterligere forsendelsesdokumenter. Systemet er imidlertid ikke automatisk i samsvar med forskriftene i ditt land / din region. Det er i stedet et verktøy som kan hjelpe deg med det samlede programmet.

Før du kan bruke denne funksjonaliteten, kreves følgende konfigurasjon:

- **Administrering av produktinformasjon:** Sett opp koder som kan brukes på utgitte produkter.
- **Lagerstyring:** Bruk ytterligere forsendelsesdokumenter til å skrive ut forsendelsesinformasjon.

## <a name="product-information-management"></a>Behandling av produktinformasjon

I Administrering av produktinformasjon er det et utvalg av oppsettstabeller der du kan legge til referanseinformasjon oppgitt i lister over farlig gods for vei-, luft- og sjøfrakt.

Her er noen av forskriftene som det ofte henvises til:

- **ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier
- **CFR 49** – Forskrifter i USA for transport av farlig gods
- **IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)
- **IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods

Hver av disse forskriftene har en liste over farlig gods som inkluderer referansekoder. Listene for hver transporttype kombineres på delte internasjonale klassifiseringer. Supply Chain Management inneholder en referansetabell for de delte kodene i disse listene. Hver liste har også noen unike koder som kan defineres.

Hvis du vil begynne å konfigurere denne informasjonen, oppretter du en forskrift som du kan bruke til å konfigurere de opprinnelige parameterne.

## <a name="warehouse-management"></a>Lagerstyring

Når en forsendelse er klargjort, kan flere nye rapporter skrives ut. Disse rapportene bruker informasjonen du definerer i Administrering av produktinformasjon.
