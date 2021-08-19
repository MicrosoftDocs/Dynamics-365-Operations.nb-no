---
title: Sammenligning av skyfunksjoner og lokale funksjoner
description: Emnet viser hvilke funksjoner som støttes i skyen og lokalt.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 68082ad0ae264b76a852d8d12412af8c4ad917703441c41e67743d1b499a8d73
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736228"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Sammenligning av skyfunksjoner og lokale funksjoner

[!include [banner](../includes/banner.md)]

Dette emnet viser en sammenligning av funksjoner som er tilgjengelige i skyen, sammenlignet med følgende programmer:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Informasjon om [funksjonene for utvikling og administrasjon](cloud-prem-comparison.md#development-and-administration-features) er også inkludert.

Tabellene nedenfor viser programområdene. Søttte for sky og lokalt er oppført for funksjonen som helhet. Der spesifikke funksjoner er forskjellige fra det totale området, er funksjonene oppført på en egen linje i funksjonskolonnen.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Areal**             | **Funksjon**                | **Sky** | **Lokalt** |
|---------------------|-----------------------------|-----------|-----------------|
| Overholdelse og sertifiseringer        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1-sertifisering                                                                | Ja       | Nei              |
| Databehandling og integrering      |                                                                                           | Ja       | Ja             |
|                                      | Eksporter data til ditt eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport av inkrementelle oppdateringer til en dataenhet                                 | Ja       | Ja             |
|                                      | Dataintegreringer                                                                         | Ja       | Ja             |
| Dokumentstyring                  |                                                                                           | Ja       | Ja             |
| Økonomistyring                 |                                                                                           | Ja       | Ja             |
| Hjelp                                 |                                                                                           | Ja       | Antall              |
| Personale                      |                                                                                           | Ja       | Ja             |
| Intelligens                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronisk rapportering (ER)                                                                 | Ja       | Ja             |
|                                      | ER: Integrering med LCS                                                                  | Ja       | Nei              |
|                                      | ER: Integrering med SharePoint                                                           | Ja       | Nei              |
|                                      | ER: Integrasjon med Regulatory Configuration Services (RCS)                              | Ja       | Nei              |
|                                      | ER: Bruker lokalt filsystem som lagring for ER-konfigurasjoner som er tilgjengelige via ER-repositorier | Nei        | Ja             |
|                                      | Integrasjon med PowerBI.com                                                              | Ja       | Nei              |
|                                      | Integrasjon med PowerBI Desktop                                                          | Nei        | Ja             |
|                                      | Analytiske arbeidsområder                                                                     | Ja       | Nei              |
|                                      | Intelligent forretningsprosess: Anbefalinger                                             | Ja       | Nei              |
|                                      | Forfatte Power BI-rapporter med OData ved hjelp av Power BI-skrivebords- eller Excel PowerQuery-verktøy    | Ja       | Nei              |
|                                      | SQL Server Reporting Services (SSRS) støtter skalering ut                                 | Ja       | Ja             |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Ingen              |
| Livssyklustjenester                   |                                                                                           | Ja       | Ja             |
|                                      | Konfigurerbare forretningsprosesser                                                           | Ja       | Nei              |
| Lokaliseringer                        |                                                                                           | Ja       | Ja             |
| Mobilapp, arbeidsområde og plattform |                                                                                           | Ja       | Ja             |
| Office-integrering                   |                                                                                           | Ja       | Ja             |
| Organisasjonsstyring          |                                                                                           | Ja       | Ja             |
| Lønn                              |                                                                                           | Ja       | Ja             |
|                                      | Direkteinnskudd                                                                            | Ja       | Nei              |
| Prosjektstyring og regnskap    |                                                                                           | Ja       | Ja             |
| Sikkerhet                             |                                                                                           | Ja       | Ja             |
| Servicestyring                   |                                                                                           | Ja       | Ja             |
| Webklient                           |                                                                                           | Ja       | Ja             |
|                                      | Oppgaveopptaker – Lagre eller last inn oppgavepptak fra BPM-biblioteket                         | Ja       | Antall              |
| Støtte                              |                                                                                           | Ja       | Ja             |
|                                      | Tilgang til support via hjelp- og støttemeny                                             | Ja       | Nei              |
|                                      | Forretningshendelser                                                                           | Ja       | Ja (enten kreves en Internett-tilkobling, eller det må implementeres egendefinerte endepunkter for å sende/motta forretningshendelser i intranettet)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Areal**                | **Funksjon**             | **Sky** | **Lokalt** |
|-------------------------|-------------------|-----------|-----------------|
| Ressursbehandling                     |                                                                                           | Ja       | Ja             |
| Overholdelse og sertifiseringer        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1-sertifisering                                                                | Ja       | Nei              |
| Kostnadsregnskap                      |                                                                                           | Ja       | Ja             |
|                                      | Innholdspakke for kostnadsregnskap for Power BI                                                 | Ja       | Nei              |
|                                      | Mobilapp for arbeidsområde for kostnadsregnskap                                                  | Ja       | Nei              |
| Kostnadsstyring                      |                                                                                           | Ja       | Ja             |
|                                      | Innholdspakke for kostnadsstyring for Power BI                                                 | Ja       | Nei              |
| Databehandling og integrering      |                                                                                           | Ja       | Ja             |
|                                      | Konfigurasjonsdrevet utvidelse                                                            | Ja       | Antall              |
|                                      | Eksporter data til ditt eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport av inkrementelle oppdateringer til en dataenhet                                 | Ja       | Ja             |
|                                      | Dataintegreringer                                                                         | Ja       | Ja             |
| Dokumentstyring                  |                                                                                           | Ja       | Ja             |
| Hjelp                                 |                                                                                           | Ja       | Nei              |
| Intelligens                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronisk rapportering (ER)                                                                 | Ja       | Ja             |
|                                      | ER: Integrering med LCS                                                                  | Ja       | Nei              |
|                                      | ER: Integrering med SharePoint                                                           | Ja       | Nei              |
|                                      | ER: Integrasjon med Regulatory Configuration Services (RCS)                              | Ja       | Nei              |
|                                      | ER: Bruker lokalt filsystem som lagring for ER-konfigurasjoner som er tilgjengelige via ER-repositorier | Nei        | Ja             |
|                                      | Integrasjon med PowerBI.com                                                              | Ja       | Nei              |
|                                      | Integrasjon med PowerBI Desktop                                                          | Nei        | Ja             |
|                                      | Analytiske arbeidsområder                                                                     | Ja       | Nei              |
|                                      | Intelligent forretningsprosess: Anbefalinger                                             | Ja       | Nei              |
|                                      | Forfatte Power BI-rapporter med OData ved hjelp av Power BI-skrivebords- eller Excel PowerQuery-verktøy    | Ja       | Nei              |
|                                      | SQL Server Reporting Services (SSRS) støtter skalering ut                                 | Ja       | Ja             |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Ingen              |
| Beholdningsstyring                 |                                                                                           | Ja       | Ja             |
| Livssyklustjenester                   |                                                                                           | Ja       | Ja             |
|                                      | Konfigurerbare forretningsprosesser                                                           | Ja       | Antall              |
| Lokaliseringer                        |                                                                                           | Ja       | Ja             |
| Produksjon                        |                                                                                           | Ja       | Ja             |
| Hovedplanlegging og prognostisering      |                                                                                           | Ja       | Ja             |
| Planleggingsoptimalisering                |                                                                                           | Ja       | Nei              |
| Mobilapp, arbeidsområde og plattform |                                                                                           | Ja       | Ja             |
| Office-integrering                   |                                                                                           | Ja       | Ja             |
| Organisasjonsstyring          |                                                                                           | Ja       | Ja             |
| Innkjøp og leverandører             |                                                                                           | Ja       | Ja             |
|                                      | Hullstansing til ekstern katalog fra kjøpsrekvisisjon                                   | Ja       | Nei              |
|                                      | Power BI-rapporter for analyse av innkjøp og forbruk                                                  | Ja       | Nei              |
| Behandling av produktinformasjon       |                                                                                           | Ja       | Ja             |
| Produkthoveddata                  |                                                                                           | Ja       | Ja             |
| Produksjon                           |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for produksjonsytelse                                                   | Ja       | Nei              |
| Prosjektstyring og regnskap    |                                                                                           | Ja       | Ja             |
| Salg                                |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for resultat av salg og fortjeneste                                      | Ja       | Nei              |
| Sikkerhet                             |                                                                                           | Ja       | Ja             |
| Servicestyring                   |                                                                                           | Ja       | Ja             |
| Forsyningskjedeadministrasjon              |                                                                                           | Ja       | Ja             |
| Transportstyring            |                                                                                           | Ja       | Ja             |
| Leverandørsamarbeid                 |                                                                                           | Ja       | Antall              |
| Lagerstyring                 |                                                                                           | Ja       | Ja             |
|                                      | Lagerapp for mobil                                                                      | Ja       | Ja             |
|                                      | Power BI-rapporter for lager                                                              | Ja       | Nei              |
| Webklient                           |                                                                                           | Ja       | Ja             |
|                                      | Oppgaveopptaker – Lagre eller last inn oppgavepptak fra BPM-biblioteket                         | Ja       | Antall              |
| Støtte                              |                                                                                           | Ja       | Ja             |
|                                      | Tilgang til support via hjelp- og støttemeny                                             | Ja       | Nei              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Hvis du vil se en liste over funksjonene som er tilgjengelige i lokale distribusjoner, kan du se [Commerce-funksjoner som er tilgjengelige i lokale distribusjoner](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Areal**         | **Funksjon**         | **Sky** | **Lokalt** |
|------------------|---------------------|-----------|-----------------|
| Alle personaleområder | Alle personalefunksjoner | Ja       | Nei              |

## <a name="development-and-administration-features"></a>Funksjoner for utvikling og administrasjon

| **Areal**                   | **Funksjon**                               | **Sky** | **Lokalt** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Sett sammen og test             |                                           | Ja       | Ja             |
| Utvidelsesmulighet              |                                           | Ja       | Ja             |
| Overvåking og telemetri   |                                           | Ja       | Ja             |
| Plattformkompatibilitet     |                                           | Ja       | Ja             |
| Service                  |                                           | Ja       | Ja             |
|                            | Betjeningsmiljøer                    | Ja       | Nei              |
| Trace Parser               |                                           | Ja       | Ja             |
| PerfTimer                  |                                           | Ja       | Ja\*           |
| Oppgrader                    |                                           | Ja       | Ja             |
|                            | Oppgrader                                   | Ja       | Nei              |
|                            | Oppgradering og støtte for tidligere versjoner | Ja       | Nei              |
| Visual Studio-utvikling  |                                           | Ja       | Ja             |

\* I lokale miljøer viser PerfTimer bare resultatene for klienten.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
