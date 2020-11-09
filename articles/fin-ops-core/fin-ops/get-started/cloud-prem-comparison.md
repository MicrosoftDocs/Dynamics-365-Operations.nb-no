---
title: Sammenligning av skyfunksjoner og lokale funksjoner
description: Emnet viser hvilke funksjoner som støttes i skyen og lokalt.
author: sericks007
manager: AnnBe
ms.date: 10/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: fd73dd649e7c10916835fbb4573dd2e65bbdb39c
ms.sourcegitcommit: 1329b3b98854422c4c3773ede44a5cefa7d07085
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/19/2020
ms.locfileid: "4040105"
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
| Databehandling og integrering      |                                                                                           | Ja       | Ja             
|                                      | Eksporter data til ditt eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport av inkrementelle oppdateringer til en dataenhet                                 | Ja       | Ja              |
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
|                                      | ER: Bruker lokalt filsystem som lagring for ER-konfigurasjoner som er tilgjengelige via ER-repositorier | Nr.        | Ja             |
|                                      | Integrasjon med PowerBI.com                                                              | Ja       | Nr.              |
|                                      | Integrasjon med PowerBI Desktop                                                          | Nr.        | Ja             |
|                                      | Analytiske arbeidsområder                                                                     | Ja       | Nr.              |
|                                      | Intelligent forretningsprosess: Anbefalinger                                             | Ja       | Nr.              |
|                                      | Forfatte Power BI-rapporter med OData ved hjelp av Power BI-skrivebords- eller Excel PowerQuery-verktøy    | Ja       | Nr.              |
|                                      | SQL Server Reporting Services (SSRS) støtter skalering ut                                 | Ja       | Nei              |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Nei              |
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
| Objektbehandling                     |                                                                                           | Ja       | Nr. |
| Overholdelse og sertifiseringer        |                                                                                           | Ja       | Ja             |
|                                      | SOC 1 Type 1-sertifisering                                                                | Ja       | Nr.              |
| Kostnadsregnskap                      |                                                                                           | Ja       | Ja             |
|                                      | Innholdspakke for kostnadsregnskap for Power BI                                                 | Ja       | Nr.              |
|                                      | Mobilapp for arbeidsområde for kostnadsregnskap                                                  | Ja       | Nr.              |
| Kostnadsstyring                      |                                                                                           | Ja       | Ja             |
|                                      | Innholdspakke for kostnadsstyring for Power BI                                                 | Ja       | Nr.              |
| Databehandling og integrering      |                                                                                           | Ja       | Ja             |
|                                      | Konfigurasjonsdrevet utvidelse                                                            | Ja       | Antall              |
|                                      | Eksporter data til ditt eget datalager                                                    | Ja       | Ja             |
|                                      | Aktiver eksport av inkrementelle oppdateringer til en dataenhet                                 | Ja       | Ja              |
|                                      | Dataintegreringer                                                                         | Ja       | Ja             |
| Dokumentstyring                  |                                                                                           | Ja       | Ja             |
| Hjelp                                 |                                                                                           | Ja       | Nei              |
| Intelligens                         |                                                                                           | Ja       | Ja             |
|                                      | Elektronisk rapportering (ER)                                                                 | Ja       | Ja             |
|                                      | ER: Integrering med LCS                                                                  | Ja       | Nei              |
|                                      | ER: Integrering med SharePoint                                                           | Ja       | Nei              |
|                                      | ER: Integrasjon med Regulatory Configuration Services (RCS)                              | Ja       | Nei              |
|                                      | ER: Bruker lokalt filsystem som lagring for ER-konfigurasjoner som er tilgjengelige via ER-repositorier | Nr.        | Ja             |
|                                      | Integrasjon med PowerBI.com                                                              | Ja       | Nr.              |
|                                      | Integrasjon med PowerBI Desktop                                                          | Nr.        | Ja             |
|                                      | Analytiske arbeidsområder                                                                     | Ja       | Nr.              |
|                                      | Intelligent forretningsprosess: Anbefalinger                                             | Ja       | Nr.              |
|                                      | Forfatte Power BI-rapporter med OData ved hjelp av Power BI-skrivebords- eller Excel PowerQuery-verktøy    | Ja       | Nr.              |
|                                      | SQL Server Reporting Services (SSRS) støtter skalering ut                                 | Ja       | Antall              |
|                                      | Telemetri overføres til skyen                                                   | Ja       | Antall              |
| Lagerstyring                 |                                                                                           | Ja       | Ja             |
| Livssyklustjenester                   |                                                                                           | Ja       | Ja             |
|                                      | Konfigurerbare forretningsprosesser                                                           | Ja       | Antall              |
| Lokaliseringer                        |                                                                                           | Ja       | Ja             |
| Produksjon                        |                                                                                           | Ja       | Ja             |
| Hovedplanlegging og prognostisering      |                                                                                           | Ja       | Ja             |
| Mobilapp, arbeidsområde og plattform |                                                                                           | Ja       | Ja             |
| Office-integrering                   |                                                                                           | Ja       | Ja             |
| Organisasjonsstyring          |                                                                                           | Ja       | Ja             |
| Innkjøp og leverandører             |                                                                                           | Ja       | Ja             |
|                                      | Hullstansing til ekstern katalog fra kjøpsrekvisisjon                                   | Ja       | Nr.              |
|                                      | Power BI-rapporter for analyse av innkjøp og forbruk                                                  | Ja       | Nr.              |
| Behandling av produktinformasjon       |                                                                                           | Ja       | Ja             |
| Produkthoveddata                  |                                                                                           | Ja       | Ja             |
| Produksjon                           |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for produksjonsytelse                                                   | Ja       | Nr.              |
| Prosjektstyring og regnskap    |                                                                                           | Ja       | Ja             |
| Salg                                |                                                                                           | Ja       | Ja             |
|                                      | Power BI-rapporter for resultat av salg og fortjeneste                                      | Ja       | Nr.              |
| Sikkerhet                             |                                                                                           | Ja       | Ja             |
| Servicestyring                   |                                                                                           | Ja       | Ja             |
| Forsyningskjedeadministrasjon              |                                                                                           | Ja       | Ja             |
| Transportstyring            |                                                                                           | Ja       | Ja             |
| Leverandørsamarbeid                 |                                                                                           | Ja       | Antall              |
| Lagerstyring                 |                                                                                           | Ja       | Ja             |
|                                      | Lagerapp for mobil                                                                      | Ja       | Ja             |
|                                      | Power BI-rapporter for lager                                                              | Ja       | Nr.              |
| Webklient                           |                                                                                           | Ja       | Ja             |
|                                      | Oppgaveopptaker – Lagre eller last inn oppgavepptak fra BPM-biblioteket                         | Ja       | Antall              |
| Støtte                              |                                                                                           | Ja       | Ja             |
|                                      | Tilgang til support via hjelp- og støttemeny                                             | Ja       | Nei              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Hvis du vil se en liste over funksjonene som er tilgjengelige i lokale distribusjoner, kan du se [Commerce-funksjoner som er tilgjengelige i lokale distribusjoner](../../../retail/retail-onprem.md).

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
|                            | Betjeningsmiljøer                    | Ja       | Antall              |
| Trace Parser og PerfTimer |                                           | Ja       | Antall              |
| Oppgrader                    |                                           | Ja       | Ja             |
|                            | Oppgrader                                   | Ja       | Nr.              |
|                            | Oppgradering og støtte for tidligere versjoner | Ja       | Nei              |
| Visual Studio-utvikling  |                                           | Ja       | Ja             |

