---
title: Oversikt over dobbel skriving
description: Denne artikkelen gir en oversikt over dobbel skriving, som er en integrert infrastruktur som gir interaksjon med minimal forsinkelse mellom kundeengasjementsapper og økonomi- og driftsapper.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289646"
---
# <a name="dual-write-overview"></a>Oversikt over dobbel skriving

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Hva er dobbel skriving?

Dobbel skriving er en bruksklar infrastruktur som gir interaksjon med minimal forsinkelse mellom kundeengasjementsapper og økonomi- og driftsapper. Når data om kunder, produkter, personer og operasjoner flyter utenfor applikasjonens grenser, kan alle avdelingene i en organisasjon være på.

Dobbel skriving gir tett sammenkoblet toveisintegrering mellom økonomi- og driftsapper og Dataverse. Alle dataendringer i økonomi- og driftsapper fører til skriving til Dataverse, og alle dataendringer i Dataverse fører til skriving til økonomi- og driftsapper. Denne automatiserte dataflyten gir en integrert brukeropplevelse på tvers av appene.

![Datarelasjon mellom apper.](media/dual-write-overview.jpg)

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

### <a name="application"></a>Program

Ved dobbel skriving opprettes det en tilordning mellom konsepter i økonomi- og driftsapper og konsepter i kundeengasjementsapper. Denne integreringen støtter følgende scenarier:

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


## <a name="top-reasons-to-use-dual-write"></a>Gode grunner til å bruke dobbel skriving

Dobbel skriving gir dataintegrering på tvers av Microsoft Dynamics 365-apper. Dette robuste rammeverket kobler sammen miljøer og gjør det mulig for forskjellige forretningsapper å fungere sammen. Her er de viktigste grunnene til at du bør bruke dobbel skriving:

+ Dobbel skriving gir tett sammenkoblet toveis integrering nær sagt i sanntid mellom Finance and Operations-apper og kundeengasjementsapper. Denne integreringen gjør at Microsoft Dynamics 365 kan brukes til alle forretningsløsningene dine. Kunder som bruker Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruker løsninger fra andre enn Microsoft for Customer Relationship Management (CRM), går over til å bruke Dynamics 365 for støtte for dobbel skriving.
+ Data fra kunder, produkter, operasjoner, prosjekter og tingenes Internett flyter automatisk til Dataverse via dobbel skriving. Denne tilkoblingen er nyttig for bedrifter som er interessert i Power Platform-utvidelser.
+ Infrastrukturen for dobbel skriving følger koden for ingen kode / lav kode. Det kreves minimalt teknisk arbeid for å utvide standardtilordninger fra tabell til tabell og inkludere tilpassede tilordninger.
+ Dobbel skriving støtter både tilkoblet og frakoblet modus. Microsoft er det eneste firmaet som tilbyr støtte for tilkoblet og frakoblet modus.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Hva innebærer toveis skriving av utviklere og arkitekter for Customer Engagement-apper?

Dobbel skriving automatiserer dataflyten mellom økonomi- og driftsapper og kundeengasjementsapper. Dobbel skriving består av to AppSource-løsninger som er installert på Dataverse. Løsningene utvider tabellskjemaet, programtilleggene og arbeidsflytene på Dataverse slik at de kan skaleres til ERP-størrelse. For å få en vellykket implementering, må utviklere og utarbeidere av kundeengasjementsapper forstå disse endringene og samarbeide med sine motparter om økonomi- og driftsapper.

For å opprette paritet med økonomi- og driftsapper gjør dobbel skriving noen viktige endringer i Dataverse-skjemaet. Hvis du forstår planen, kan du unngå noe utformings- og utviklingsarbeid er i fremtiden.

+ Når du har installert pakken for dobbel skriving AppSource, vil Dataverse ha de nye begrepene, for eksempel firma og part. Disse konseptene hjelper apper som er bygget på Dataverse, inkludert Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, til å samhandle sømløst med økonomi- og driftsapper.

+ Aktiviteter og notater er enhetlig og utvides for å støtte både C1-ere (brukere av systemet) og C2-ere (kunder av systemet).

+ Hvis du vil hindre tap av data under overføring av valuta mellom økonomi- og driftsapper og Dataverse, kan du utvide antallet desimaler i valutadatatypen for kundeengasjementsapper. Funksjonen oversetter eksisterende rader automatisk til den nye utvidede tilstanden på metadatalaget. I løpet av denne prosessen blir valutaverdien oversatt til desimaldata i stedet for pengedata, og valutaverdien støtter 10 desimalplasser. Denne funksjonen er valgfri, og organisasjoner som ikke trenger mer enn fire desimaler med presisjon, trenger ikke å velge den. Hvis du vil ha mer informasjon, kan du se [Overføring av valutadatatype for dobbel skriving](currrency-decimal-places.md).

+ [Datoeffektivitet](../../dev-tools/date-effectivity.md) blir lagt til i Dataverse. Den vil støtte tidligere, nåværende og fremtidige data i samme tabell.

+ [Enhetskonverteringer](../../../../supply-chain/pim/tasks/manage-unit-measure.md) for produkt støttes for produkter, tilbud, ordrer og fakturaer.

Hvis du vil ha mer informasjon om kommende endringer, kan du se [Nyheter eller endringer i dobbel skriving](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

