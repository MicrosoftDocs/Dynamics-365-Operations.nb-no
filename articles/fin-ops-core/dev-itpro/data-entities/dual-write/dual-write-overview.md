---
title: Oversikt over dobbel skriving
description: Dette emnet gir en oversikt over dobbel skriving. Dobbel skriving er en infrastruktur som gir nær sanntids interaksjon mellom modelldrevne Microsoft Dynamics 365-apper og Finance and Operations-apper.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075997"
---
# <a name="dual-write-overview"></a>Oversikt over dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Hva er dobbel skriving?

Dobbel skriving er en integrert infrastruktur som gir nær sanntids interaksjon mellom modelldrevne apper i Microsoft Dynamics 365 og Finance and Operations-apper. Når data om kunder, produkter, personer og operasjoner flyter utenfor applikasjonens grenser, kan alle avdelingene i en organisasjon være på.

Dobbel skriving gir tett sammenkoblet, toveis integrering mellom Finance and Operations-apper og Common Data Service. Alle dataendringer i Finance and Operations-apper fører til skriving til Common Data Service, og alle dataendringer i Common Data Service fører til skriving til Finance and Operations-apper. Denne automatiserte dataflyten gir en integrert brukeropplevelse på tvers av appene.

![Datarelasjon mellom apper](media/dual-write-overview.jpg)

Dobbel skriving har to aspkter: *infrastruktur* og *app*.

### <a name="infrastructure"></a>Infrastruktur

Infrastrukturen for dobbel skriving er utvidbar og pålitelig, og inneholder følgende nøkkelfunksjoner:

+ Synkron og toveis dataflyt mellom programmer
+ Synkronisering sammen med modus for avspilling, pause og oppsamling for å støtte systemet under tilkoblet og frakoblet/asynkron modus.
+ Mulighet til å synkronisere innledende data mellom apper
+ Konsolidert visning av aktivitets- og feillogger for dataadministratorer
+ Mulighet til å konfigurere egendefinerte varsler og terskler og abonnere på varslinger
+ Intuitivt brukergrensesnitt (UI) for filtrering og transformasjoner
+ Mulighet til å angi og vise enhetsavhengigheter og relasjoner
+ Utvidelse for både standard og egendefinerte enheter og tilordninger
+ Pålitelig livssyklus administrasjon for app
+ Integrert installasjonsopplevelse for nye kunder

### <a name="application"></a>Søknad

Ved dobbel skriving opprettes det en tilordning mellom konsepter i Finance and Operations-apper og konsepter i modelldrevne apper i Dynamics 365. Denne integreringen støtter følgende scenarier:

+ Integrert original for kunde
+ Tilgang til kundefordelskort og belønningspoeng
+ Samlet produktstandardopplevelse
+ Forståelse av organisasjonshierarkiet
+ Integrert original for leverandør
+ Tilgang til referansedata for finan og avgift
+ Prismotoropplevelse etter behov
+ Integrert opplevelse for kundeemne til kontant
+ Mulighet til å betjene både interne aktiva og kundeaktiva via feltagenter
+ Integrert opplevelse for innkjøp til betaling
+ Integrerte aktiviteter og notater for kundedata og dokumenter
+ Mulighet til å slå opp tilgjengelighet og detaljer for lagerbeholdning
+ Opplevelse for prosjekt til kontanter
+ Mulighet til å håndtere flere adresser og roller via partskonseptet
+ Administrasjon av enkelt kilde for brukere
+ Integrerte kanaler for detaljsalg og markedsføring
+ Innsyn i kampanjer og rabatter
+ Funksjoner for å be om service
+ Strømlinjeformede serviceoperasjoner

## <a name="top-reasons-to-use-dual-write"></a>Gode grunner til å bruke dobbel skriving

Dobbel skriving gir dataintegrering på tvers av Microsoft Dynamics 365-apper. Dette robuste rammeverket kobler sammen miljøer og gjør det mulig for forskjellige forretningsapper å fungere sammen. Her er de viktigste grunnene til at du bør bruke dobbel skriving:

+ Dobbel skriving gir tett sammenkoblet toveis integrering nær sagt i sanntid mellom Finance and Operations-apper og modelldrevne apper i Dynamics 365. Denne integreringen gjør at Microsoft Dynamics 365 kan brukes til alle forretningsløsningene dine. Kunder som bruker Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruker løsninger fra andre enn Microsoft for Customer Relationship Management (CRM), går over til å bruke Dynamics 365 for støtte for dobbel skriving.
+ Data fra kunder, produkter, operasjoner, prosjekter og tingenes Internett flyter automatisk til Common Data Service via dobbel skriving. Denne tilkoblingen er svært nyttig for bedrifter som er interessert i Microsoft Power Platform-utvidelser.
+ Infrastrukturen for dobbel skriving følger koden for ingen kode / lav kode. Det kreves minimalt teknisk arbeid for å utvide standardtilordninger fra tabell til tabell og inkludere tilpassede tilordninger.
+ Dobbel skriving støtter både tilkoblet og frakoblet modus. Microsoft er det eneste firmaet som tilbyr støtte for tilkoblet og frakoblet modus.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Hva betyr dobbel skriving for brukere av og arkitekter for CRM-produkter?

Dobbel skriving automatiserer dataflyten mellom Finance and Operations-apper og Common Data Service. I fremtidige versjoner vil begrepene i modelldrevne apper i Dynamics 365 (for eksempel kunde, kontakt, tilbud og ordre) for skaleres til kunder i mellomsjiktet og det øvre sjiktet.

I den første versjonen håndteres det meste av automatiseringen av løsninger for dobbel skriving. I fremtidige versjoner blir disse løsningene en del av Common Data Service. Ved å forstå de kommende endringene i Common Data Service kan du spare deg selv for innsats på lang sikt. Her er noen av de viktige endringene:

+ Common Data Service vil ha nye konsepter, for eksempel firma og part. Disse konseptene vil påvirke alle apper som er utviklet med Common Data Service, for eksempel Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.
+ Aktiviteter og notater er enhetlig og utvides for å støtte både C1-ere (brukere av systemet) og C2-ere (kunder av systemet).
+ Her er noen av de kommende endringene i Common Data Service:

    - Datatypen for desimaler erstatter datatypen for penger.
    - Datoeffektivitet vil støtte tidligere, nåværende og fremtidige data på samme sted.
    - Det vil være mer støtte for valuta og valutakurser, og API-et (Application Programming Interface) **Valutakurs** vil bli revidert.
    - Enhetskonverteringer vil støttes.

Hvis du vil ha mer informasjon om kommende endringer, kan du se [Data i Common Data Service – fase 1 og 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).
