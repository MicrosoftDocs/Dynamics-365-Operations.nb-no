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
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434554"
---
# <a name="hazardous-materials"></a>Farlige materialer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Informasjon om farlige materialer settes opp i administrering av produktinformasjon. Denne modulen inneholder også dokumenter som kan skrives ut via lagerstyring.

Når du sender materialer som er klassifisert som farlig gods, må ekstra papirarbeid inkluderes i forsendelsene. Med funksjonaliteten for farlige materialer kan kundene lagre klassifiseringsinformasjon og relatere den til utgitte varer. Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen.

> [!IMPORTANT]
> Funksjoner for farlig materiale i Microsoft Dynamics 365 Supply Chain Management tilbyr en samling av nyttige produktinformasjonsfelt og relaterte funksjoner som kan hjelpe deg med å registrere og referere til informasjon som er relatert til farlige produkter. Disse funksjonene kan også hjelpe deg med å utforme og skrive ut forsendelsesdokumenter som inneholder noe av den samme informasjonen om eventuelle farlige materialer du leverer. Systemet gjør deg imidlertid ikke automatisk i samsvar med alle gjeldende forskrifter i ditt land / din region. Selv om disse verktøyene er ment å hjelpe deg å samsvare med på vanlige forskrifter, er de verken tilstrekkelig i seg selv eller garanterer at de er det. Organisasjonen din er ansvarlig for å være oppmerksom på alle gjeldende forskrifter og for å gjøre alle nødvendige tiltak for å samsvare med dem.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]