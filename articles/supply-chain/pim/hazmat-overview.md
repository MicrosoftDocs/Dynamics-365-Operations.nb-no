---
title: Oversikt over farlige materialer
description: Denne artikkelen gir en oversikt over funksjoner som er knyttet til håndtering og dokumentasjon av farlige materialer under produktinformasjonsbehandling og lagerstyring.
author: t-benebo
ms.date: 06/10/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: c2cae4cb65dd163e9fbf1d24cff5a0a040e3ce3a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905812"
---
# <a name="hazardous-materials-overview"></a>Oversikt over farlige materialer

[!include [banner](../includes/banner.md)]

For å overholde samsvar med leverings- og transportforskrifter må organisasjoner som leverer materialer som er klassifisert som farlige varer, inkludere ekstra papirarbeid med forsendelsene. Med funksjonen for farlige materialer kan kundene lagre informasjon som er relatert til frigitte varer. Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen. En organisasjon som leverer farlige varer, må ha sine egne prosesser og prosedyrer for å administrere forsendelsesprosessen. Microsoft Dynamics 365 Supply Chain Management er bare et verktøy som kan hjelpe deg med å generere de nødvendige dokumentene.

Diagrammet nedenfor illustrerer trinnene som trengs for å definere og bruke farlige materialer-funksjonen.

![Oppsett og bruk av farlig materiale-funksjonen.](media/hazmat-overview.png "Oppsett og bruk av farlig materiale-funksjonen")

Farlige materialer-funksjonen er definert i Behandling av produktinformasjon og inneholder dokumenter som kan skrives ut via Lagerstyring. Derfor er disse områdene de to hovedområdene der du ser gjennom, konfigurerer og bruker funksjonaliteten til denne funksjonen:

- **Behandling av produktinformasjon:** – Konfigurer kodene som skal brukes på et utgitt produkt.
- **Lagerstyring** – Arbeid med ekstra forsendelsesdokumenter som skal skrives ut for forsendelser.

> [!IMPORTANT]
> Funksjoner for farlig materiale i Supply Chain Management tilbyr en samling av nyttige produktinformasjonsfelt og relaterte funksjoner som kan hjelpe deg med å registrere og referere til informasjon som er relatert til farlige produkter. Disse funksjonene kan også hjelpe deg med å utforme og skrive ut forsendelsesdokumenter som inneholder noe av den samme informasjonen om eventuelle farlige materialer du leverer. Systemet gjør deg imidlertid ikke automatisk i samsvar med alle gjeldende forskrifter i ditt land / din region. Selv om disse verktøyene er ment å hjelpe deg å samsvare med på vanlige forskrifter, er de verken tilstrekkelig i seg selv eller garanterer at de er det. Organisasjonen din er ansvarlig for å være oppmerksom på alle gjeldende forskrifter og for å gjøre alle nødvendige tiltak for å samsvare med dem.

## <a name="product-information-management"></a>Behandling av produktinformasjon

Behandling av produktinformasjon inneholder et utvalg av oppsettabeller der du kan angi referanseinformasjon for de ulike listene over farlige varer for vei-, luft- og sjøfrakt.

Følgende felles forskrifter ble referert til da denne funksjonaliteten ble utviklet:

- **ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier
- **CFR 49** – Forskrifter i USA for transport av farlig gods
- **IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)
- **IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods

Hvert sett med forskrifter inneholder standardiserte lister over farlige varer og referansekoder. Supply Chain Management inneholder derfor en referansetabell for de felles kodene i disse listene. Hver liste har også noen unike koder som du kan definere.

Hvis du vil ha mer informasjon om hvordan du definerer forskrifter og verdier for farlige materialer, og hvordan du tilordner verdiene til de relevante produktene, kan du se følgende artikler:

- [Definere farlige materialer](hazmat-setup.md)
- [Farlige materialer i produkter, ordrer, forsendelser og laster](hazmat-items.md)

## <a name="warehouse-management"></a>Lagerstyring

Når du klargjør en forsendelse i Lagerstyring, vil du kunne skrive ut flere nye rapporter som bruker informasjonen du har definert i Behandling av produktinformasjon. Hvis du vil ha mer informasjon om tilgjengelige rapporter og hvordan du bruker dem, kan du se [Forespørsler og rapporter om farlige materialer](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]