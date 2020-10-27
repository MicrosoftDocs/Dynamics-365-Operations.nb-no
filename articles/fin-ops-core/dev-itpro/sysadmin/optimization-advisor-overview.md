---
title: Oversikt over optimaliseringsrådgiver
description: Dette emnet beskriver hvordan du kan bruke Optimaliseringsrådgiver for å sikre optimal konfigurering av Finance and Operations.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 25ca62466c00b038e0d7e1758fd4f13f776cb2f0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982558"
---
# <a name="optimization-advisor-overview"></a>Oversikt over optimaliseringsrådgiver

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan bruke Optimaliseringsrådgiver for å sikre optimal konfigurering av Finance and Operations.

## <a name="overview"></a>Oversikt

Ugyldig konfigurasjon og oppsett av en modul kan påvirke tilgjengeligheten av programfunksjoner, systemytelsen og smidig drift av forretningsprosesser. Kvaliteten på forretningsdata (for eksempel i hvilken grad data er nøyaktige, fullstendige og ryddige) kan også påvirke systemytelsen, og organisasjonens beslutningsmuligheter, produktivitet og så videre.

Arbeidsområdet **Optimaliseringsrådgiver** er et verktøy som lar privilegerte brukere, forretningsanalytikere, funksjonelle konsulenter og IT-støtte finne problemer i modulkonfigurasjon og forretningsdata. Optimaliseringsrådgiver foreslår anbefalte fremgangsmåter for modulkonfigurasjon og identifiserer forretningsdata som er foreldet eller feil.

Optimaliseringsrådgiver kjører et sett med regler for anbefalt fremgangsmåte med jevne mellomrom. Et standardsett med regler er tilgjengelig, men brukere kan imidlertid også opprette regler som gjelder for deres tilpasninger, løsninger fra uavhengige programvareleverandører (ISVer) og forretningsdata. Hvis du vil ha mer informasjon om hvordan du oppretter regler, kan du se [Opprette regler for optimaliseringsrådgiver](./create-rules-optimization-advisor.md).

Når det er oppdaget et brudd på en regel, genereres en optimaliseringssalgsmulighet som vises i arbeidsområdet **Optimaliseringsrådgiver** . En bruker kan iverksette passende korrigerende tiltak direkte fra **Optimaliseringsrådgiver** -arbeidsområdet.

Salgsmuligheter kan være firmaspesifikke eller på tvers av firmaer, avhengig av typen oppsett og data som valideres. Salgsmuligheter på tvers av firmaer kan vises fra alle firmaer. Du må først velge firmaet før du kan vise salgsmulighetene for et bestemt firma.

Standard sikkerhetspolicyer gjelder for optimaliseringsmuligheter. Optimaliseringsmuligheter som er knyttet til konfigurasjon av **Lagerstyring** -modulen, er for eksempel bare synlig for brukere som har tilgang til lagerstyring, og kan endre oppsettet.

Når du gjør noe med noen optimaliseringsmuligheter, beregner systemet virkningen av salgsmuligheten når det gjelder reduksjonen i kjøretiden for forretningsprosesser. Denne funksjonen er dessverre ikke tilgjengelig for alle optimaliseringsmuligheter.

Hvis du vil vite mer om optimaliseringrådgiveren, kan du se den korte videoen [Optimaliseringsrådgiver i Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Optimaliseringsregler

Du kan vise den fullstendige listen over regler for Optimaliseringsrådgiver og se hvor ofte reglene blir evaluert, ved å gå til **Systemadministrasjon** &gt; **Periodiske oppgaver** &gt;**Vedlikehold valideringsregel for diagnostikk** . Bare regler som har statusen **Aktiv** , evalueres. Evalueringsfrekvensen kan settes til **Daglig** , **Ukentlig** , **Månedlig** eller **Ikke planlagt** .

For å starte evalueringen av ikke-planlagte regler eller evaluere periodiske regler på nytt utenfor den forhåndsdefinerte planen, kan du gå til **Systemadministrasjon**&gt; **Periodiske oppgaver** &gt; **Planlegg valideringsregel for diagnostikk** . Velg deretter en valueringsfrekvens i dialogboksen **Validering av diagnoseregel** . Alle regler som har den angitte frekvensen, evalueres på nytt.

Gjeldende sett med regler for optimalisering kan deles inn i følgende kategorier.

### <a name="module-configuration-and-setup"></a>Oppsett og konfigurasjon av modul

Oppsettet av Lagerstyring er en komplisert prosess. For å forenkle prosessen er noen regler introdusert for å hjelpe til med validere at oppsettet er riktig. En regel validerer for eksempel oppsettet av lagerplasseringsretningslinjer for faste produktvariantlokasjoner for salgsordrer og overføringsordrer.

I tillegg kontrollerer noen regler om aktiverte funksjoner faktisk brukes. En regel bestemmer for eksempel om du bruker **Hovedplanlegging** -modulen. Hvis regelen bestemmer at du ikke bruker modulen, genereres en optimaliseringsmulighet for å foreslå at du slår av planleggingsprosessene.

### <a name="system-configuration"></a>Systemkonfigurasjon

Hvis det ikke er brukt bestemte funksjoner som styres av en konfigurasjonsnøkkel, genereres en optimaliseringsmulighet for å foreslå at du deaktiverer konfigurasjonsnøkkelen. Eksempler på konfigurasjonsnøkler er **faktisk vekt** , **budsjettplanlegging** , **prosjekt** og **liste over godkjente leverandører** .

### <a name="business-data-consistency-and-cleanup"></a>Forretningsdatakonsistens og opprydding

Hvis hoveddata ikke er riktig (for eksempel hvis du har måleenhetskonverteringer for enheter som ikke er definert, eller hvis du har måleenhetskonverteringer som har en divisjon med 0 \[null\]), genereres en optimaliseringsmulighet for å foreslå at du retter dataene. 

Hvis du har for mange loggoppføringer for satsvis jobb, foreldede varer, lukkede beholdningsoppføringer for lageraktiverte varer og så videre, eller hvis disse oppføringene og elementene er for gammel, genereres optimaliseringsmuligheter for å foreslå at du rydder opp dataene. Ved å holde dataene rene kan du forbedre systemytelsen.

### <a name="best-practices"></a>Anbefalte fremgangsmåter

Hvis du ikke kjører enkelte forretningsprosesser i samsvar med anbefalte fremgangsmåter (for eksempel hvis du kjører lagerlukking før lageret er lukket, eller hvis du bruker den planlagte satsvise jobben for partioverføring for underfinansjournaler), informerer optimaliseringsmuligheter deg om anbefalte fremgangsmåter og ber deg følge dem.

## <a name="optimization-opportunities"></a>Optimaliseringsmuligheter

Hvis du vil vise optimaliseringsmulighetene som genereres under evaluering av optimaliseringdregler, kan du åpne **Optimaliseringsrådgiver** -arbeidsområdet.

I dette arbeidsområdet kan du vise mer informasjon om en salgsmulighet ved å velge **Mer informasjon** . Hvis du vil at systemet skal handle og korrigere oppsettet, rydde dataene og så videre, slik at du ikke trenger å åpne de tilsvarende sidene selv, velger du **Utfør handling** .

Det finnes ingen arbeidsflyt for optimaliseringsmuligheter. Når du har valgt **Utfør handling** eller en navigasjonsbane i dialogboksen **Mer informasjon** , fjernes optimaliseringsmuligheten fra listen. Hvis den korrigerende handlingen ikke løser et problem fullstendig, genereres salgsmuligheten på nytt neste gang regelen evalueres.

Hvis en salgsmulighet ikke gjelder for din rolle, kan du velge **Skjul i listen** . Selv om regelen bak denne salgsmuligheten utløses på nytt senere, kan du ikke se salgsmuligheten i listen.

Hvis du vil deaktivere evalueringen av bestemte regler, velger du salgsmuligheten som ble generert av regelen, og velg deretter **Deaktiver analyse** .

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette regler for optimaliseringsrådgiver](./create-rules-optimization-advisor.md)

[Optimaliseringsrådgiver i Dynamics 365 for Finance and Operations (video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
