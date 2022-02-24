---
title: Definere en detaljhandelskanal
description: Dette emnet beskriver hvordan du oppretter en ny detaljhandelskanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414606"
---
# <a name="set-up-a-retail-channel"></a>Definere en detaljhandelskanal


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny detaljhandelskanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce støtter flere kanaler for detaljhandel. Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker). Hver detaljhandelsbutikkanal kan ha sine egne betalingsmåter, prisgrupper, salgsstedskasser, inntekts- og utgiftskontoer og ansatte. Du må sette opp alle disse elementene før du kan opprette en detaljhandelsbutikkanal. 

Før det opprettes en detaljhandelskanal, må du kontrollere at du følger [forutsetningene for kanal](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Opprette og konfigurere en ny detaljhandelskanal

1. I navigasjonsruten går du til **Moduler \> Kanaler \> Butikker \> Alle butikker**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-feltet oppgir du et navn for den nye kanalen.
1. Oppgi et unikt butikknummer i **Butikknummer**-feltet. Nummeret kan være alfanumerisk med opptil 10 tegn.
1. Angi den riktige juridiske enheten i rullegardinlisten **Juridisk enhet**.
1. Angi det riktige lageret i rullegardinlisten **Lager**.
1. Velg riktig tidssone i feltet **Tidssone for butikk**.
1. I rullegardinlisten **Merverdiavgiftsgruppe** velger du riktig merverdiavgiftsgruppe for butikken.
1. Velg riktig valuta i **Valuta**-feltet.
1. Angi en gyldig adressebok i feltet **Adressebok for kunde**.
1. Angi en gyldig standardkunde i feltet **Standardkunde**.
1. I feltet **Funksjonalitetsprofil** velger du en funksjonalitetsprofil hvis det er aktuelt.
1. I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser opprettelsen av en ny detaljhandelskanal.

![Ny detaljhandelskanal](media/channel-setup-retail-1.png)

Bildet nedenfor viser et eksempel på en detaljhandelskanal.

![Eksempel på detaljhandelskanal](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Andre innstillinger

Det finnes mange andre valgfrie innstillinger som kan angis i delene **Utdrag/avslutning/** og **Diverse**, basert på behovene til detaljhandelsbutikken.

I tillegg kan du se [Skjermoppsett for salgssted](pos-screen-layouts.md) for informasjon om hvordan du konfigurerer standard skjermoppsett i delen **Skjermoppsett**, og [Konfigurere og installere Retail Hardware Station](retail-hardware-station-configuration-installation.md) for konfigurasjonsinformasjon om delen **Maskinvarestasjoner**.

Bildet nedenfor viser et eksempel på en konfigurasjon av et detaljhandelskanaloppsett.

![Eksempel på konfigurasjon av detaljhandelskanal](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Ekstra kanaloppsett

Du finner flere elementer som må konfigureres for en kanal, i **handlingsruten** under **Oppsett**-delen.

Andre oppgaver som kreves for oppsett av Internett-kanal, omfatter definere betalingsmåter, kontantoppgjør, leveringsmåter, inntekts-/utgiftskonto, inndelinger, gruppetilordning for oppfyllelse og safer.

Følgende bilde viser diverse tilleggsalternativer for detaljhandelskanaloppsett i kategorien **Oppsett**.

![Definere kanal](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Definere betalingsmåter

Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.
1. I handlingsruten velger du **Ny**.
1. Velg en ønsket betalingsmåte i navigasjonsruten.
1. I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.
1. Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Definere kKontantoppgjør

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Kontantoppgjør**.
1. Velg **Ny** i handlings ruten, og opprett deretter alle aktuelle **Mynt**- og **Seddel**-størrelser.

Bildet nedenfor viser et eksempel på et kontantoppgjør.

![Definere kontantoppgjør](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Definer leveringsmåter

Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.  

Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.
1. Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.
1. I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen. Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler

Bildet nedenfor viser et eksempel på en leveringsmåte.

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Definere inntekts-/utgiftskonto

Gjør følgende for å konfigurere en inntekts-/utgiftskonto.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Inntekts-/utgiftskonto**.
1. I handlingsruten velger du **Ny**.
1. Under **Navn** skriver du inn et navn.
1. Under **Søkenavn** skriver du inn et søkenavn.
1. Under **Kontotype** angir du kontotypen.
1. Skriv inn tekst for **Meldingslinje 1**, **Meldingslinje 2**, **Bilagstekst 1** og **Bilagstekst 2** etter behov.
1. Angi posteringsinformasjon under **Postering**.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en inntekts/utgiftskonto.

![Definere inntekts-/utgiftskontoer](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Definere seksjoner

Gjør følgende for å konfigurere seksjoner.

1. I handlingsruten velger du kategorien **Oppsett** og klikker deretter **Seksjoner**.
1. I handlingsruten velger du **Ny**.
1. Under **Seksjonsnummer** angir du et seksjonsnummer.
1. Angi en beskrivelse under **Beskrivelse**.
1. Under **Seksjonsstørrelse** angir du en seksjonsstørrelse.
1. Konfigurer tilleggsinnstillinger for **Generelt** og **Salgsstatistikk** etter behov.
1. Velg **Lagre** i handlingsruten.

### <a name="set-up-a-fulfillment-group-assignment"></a>Definere en gruppetilordning for oppfyllelse

Hvis du vil konfigurere en gruppetilordning for oppfyllelse, gjør du følgende.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Gruppetilordning for oppfyllelse**.
1. I handlingsruten velger du **Ny**.
1. I rullegardinlisten **Oppfyllelsesgruppe** velger du en oppfyllelsesgruppe.
1. Angi en beskrivelse i rullegardinlisten **Beskrivelse**.
1. Velg **Lagre** i handlingsruten.

Det følgende bildet viser et eksempel på et oppsett for gruppetilordning for oppfyllelse.

![Definere gruppetilordninger for oppfyllelse](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Definere safer

Gjør følgende for å konfigurere safer.

1. I handlingsruten velger du kategorien **Oppsett** og klikker deretter **Safer**.
1. I handlingsruten velger du **Ny**.
1. Angi et navn for safen.
1. Velg **Lagre** i handlingsruten.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Definere en Internett-kanal](channel-setup-online.md)

[Definere en telefonsenterkanal](channel-setup-callcenter.md)

