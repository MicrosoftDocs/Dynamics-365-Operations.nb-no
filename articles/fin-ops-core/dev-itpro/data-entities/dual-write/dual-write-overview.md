---
title: Oversikt over dobbel skriving
description: Dette emnet gir en oversikt over dobbel skriving, som er en integrert infrastruktur som gir interaksjon med minimal forsinkelse mellom kundeengasjementsapper og Finance and Operations-apper.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3937850a9df716113591e49b25373beb48e3acdd
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130011"
---
# <a name="dual-write-overview"></a>Oversikt over dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a>Hva er dobbel skriving?

Dobbel skriving er en integrert infrastruktur som gir nær sanntids interaksjon mellom Customer Engagement-apper og Finance and Operations-apper. Når data om kunder, produkter, personer og operasjoner flyter utenfor applikasjonens grenser, kan alle avdelingene i en organisasjon være på.

Dobbel skriving gir tett sammenkoblet, toveis integrering mellom Finance and Operations-apper og Dataverse. Alle dataendringer i Finance and Operations-apper fører til skriving til Dataverse, og alle dataendringer i Dataverse fører til skriving til Finance and Operations-apper. Denne automatiserte dataflyten gir en integrert brukeropplevelse på tvers av appene.

![Datarelasjon mellom apper](media/dual-write-overview.jpg)

Dobbel skriving har to aspkter: *infrastruktur* og *app*.

### <a name="infrastructure"></a>Infrastruktur

Infrastrukturen for dobbel skriving er utvidbar og pålitelig, og inneholder følgende nøkkelfunksjoner:

+ Synkron og toveis dataflyt mellom programmer
+ Synkronisering sammen med modus for avspilling, pause og oppsamling for å støtte systemet under tilkoblet og frakoblet/asynkron modus.
+ Mulighet til å synkronisere innledende data mellom apper
+ Kombinert visning av aktivitets- og feillogger for dataadministratorer
+ Mulighet til å konfigurere egendefinerte varsler og terskler og abonnere på varslinger
+ Intuitivt brukergrensesnitt (UI) for filtrering og transformasjoner
+ Mulighet til å angi og vise tabellavhengigheter og relasjoner
+ Utvidelse for både standard og egendefinerte tabeller og tilordninger
+ Pålitelig livssyklus administrasjon for app
+ Integrert installasjonsopplevelse for nye kunder

### <a name="application"></a>Søknad

Ved dobbel skriving opprettes det en tilordning mellom konsepter i Finance and Operations-apper og konsepter i Customer Engagement-apper. Denne integreringen støtter følgende scenarier:

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
+ Data fra kunder, produkter, operasjoner, prosjekter og tingenes Internett flyter automatisk til Dataverse via dobbel skriving. Denne tilkoblingen er nyttig for bedrifter som er interessert i Power Platform-utvidelser.
+ Infrastrukturen for dobbel skriving følger koden for ingen kode / lav kode. Det kreves minimalt teknisk arbeid for å utvide standardtilordninger fra tabell til tabell og inkludere tilpassede tilordninger.
+ Dobbel skriving støtter både tilkoblet og frakoblet modus. Microsoft er det eneste firmaet som tilbyr støtte for tilkoblet og frakoblet modus.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Hva innebærer toveis skriving av utviklere og arkitekter for Customer Engagement-apper?

Dobbel skriving automatiserer dataflyten mellom Finance and Operations-apper og Customer Engagement-apper. Dobbel skriving består av to AppSource-løsninger som er installert på Dataverse. Løsningene utvider tabellskjemaet, programtilleggene og arbeidsflytene på Dataverse slik at de kan skaleres til ERP-størrelse. For å få en vellykket implementering, må utviklere og utarbeidere av Customer Engagement-apper forstå disse endringene og samarbeide med sine motparter om Finance and Operations-apper.

For å opprette paritet med Finance and Operations-apper, gjør dobbelt skriving noen viktige endringer i Dataverse-skjemaet. Hvis du forstår planen, kan du unngå noe utformings- og utviklingsarbeid er i fremtiden.

+ Når du har installert pakken for dobbel skriving AppSource, vil Dataverse ha de nye begrepene, for eksempel firma og part. Disse konseptene hjelper apper som er bygget på Dataverse, inkludert Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, til å samhandle sømløst med Finance and Operations-apper.

+ Aktiviteter og notater er enhetlig og utvides for å støtte både C1-ere (brukere av systemet) og C2-ere (kunder av systemet).

+ Hvis du vil hindre tap av data under overføring av valuta mellom Finance and Operations-apper og Dataverse, kan du utvide antallet desimaler i valutadatatypen for Customer Engagement-apper. Funksjonen oversetter eksisterende rader automatisk til den nye utvidede tilstanden på metadatalaget. I løpet av denne prosessen blir valutaverdien oversatt til desimaldata i stedet for pengedata, og valutaverdien støtter 10 desimalplasser. Denne funksjonen er valgfri, og organisasjoner som ikke trenger mer enn fire desimaler med presisjon, trenger ikke å velge den. Hvis du vil ha mer informasjon, kan du se [Overføring av valutadatatype for dobbel skriving](currrency-decimal-places.md).

+ [Datoeffektivitet](../../dev-tools/date-effectivity.md) blir lagt til i Dataverse. Den vil støtte tidligere, nåværende og fremtidige data i samme tabell.

+ [Enhetskonverteringer](../../../../supply-chain/pim/tasks/manage-unit-measure.md) for produkt støttes for produkter, tilbud, ordrer og fakturaer.

Hvis du vil ha mer informasjon om kommende endringer, kan du se [Nyheter eller endringer i dobbel skriving](whats-new-dual-write.md).

