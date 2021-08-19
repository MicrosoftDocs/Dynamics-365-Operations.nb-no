---
title: Hva er nytt eller endret i mobilappen Warehouse Management
description: Dette emnet inneholder en liste over de nye og endrede funksjonene for hver utgitte versjon av mobilappen Warehouse Management for Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 43d1381e73d5659bfd6ae6c6d944b7e6918b681a4f89df7ad23abbed5b4a0d3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720090"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Hva er nytt eller endret i mobilappen Warehouse Management

[!include [banner](../includes/banner.md)]

Dette emnet inneholder en liste over nye funksjoner, reparasjoner, forbedringer og kjente problemer for hver utgitte versjon av mobilappen Warehouse Management for Microsoft Dynamics 365 Supply Chain Management.

## <a name="2070"></a>2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Nye funksjoner, reparasjoner og forbedringer i versjon 2.0.7.0

- La til en del på siden **Om** som kontrollerer den nyeste utgitte versjonen av appen.
- Gjorde det enklere å dra og sveipe mellom sider.
- Endret ikonet for stigende/synkende-knappen i arbeidslisten.
- Reduserte margene på **Detaljer**-kortet slik at det får plass til mer informasjon.
- Brukte forskjellige ytelsesforbedringer for å redusere problemet med at appen blir tregere over tid.
- Hvis det er flere kontroller enn det er plass til på skjermen, noe som resulterer i sideveksling, ruller ikke spinnerkontrollen lenger på samme måte som siden.
- Prioriter visning av den sist skannede verdien over visning av aktivitetstittelen, slik at hvis de overlapper aktivitetstittelen, blir den avkortet.
- Løste ulike problemer som førte til at systemet sluttet å svare.
- Tekst på forskjellige steder er ikke lenger forkortet på enkelte språk.
- Appen kjører nå i fullskjermmodus som standard.
- Løste et problem som av og til ville føre til at skanninger ble ignorert på hovedsiden med bestemte enheter.

### <a name="known-issues-in-version-2070"></a>Kjente problemer i versjon 2.0.7.0

- På noen enheter får du følgende feilmelding når du starter appen eller starter en oppgave: Finner ikke en passende visning for den angitte størrelsen. Hvis du ser denne feilmeldingen på noen av enhetene dine, må du nedgradere Warehouse Management-mobilappen til versjon 2.0.6.0 på den enheten og vente med å oppgradere til neste versjon av appen er utgitt.

## <a name="version-2060"></a>Versjon 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nye funksjoner, reparasjoner og forbedringer i versjon 2.0.6.0

Denne versjonen inneholder følgende nye funksjoner, reparasjoner og forbedringer:

- Demomodus viser nå alle etikettene på enhetsspråket.
- Det er mindre sannsynlig at du får følgende feilmelding: "Finner ikke en passende visning for den angitte størrelsen."
- Minimumshøyden for arbeidskort er økt (for tilfeller der tre eller færre felt er konfigurert til å vises i arbeidslisten).
- Margene (tones ut) nederst på detaljkortene er forbedret.
- Ugyldige symboler i XML-filer som utveksles med serveren, håndteres nå på en elegant måte. (Tegn som ikke kan skrives ut, håndteres nå elegant og fører ikke lenger til at appen slutter å svare.)
- HTTP-feil (for eksempel "feil 503") når en serverforespørsel sendes, håndteres nå på en elegant måte.
- Når det vises en feil, vises ikke lenger alternativlisten automatisk for kombinasjonsbokskontroller.
- Appen slutter ikke lenger å svare på grunn av skjermretningen som er valgt i brukerinnstillinger.
- Produktbilder vises nå i selvbetjeningsmiljøer. (Denne endringen gjelder bare versjoner med lav oppløsning. Filbehandlingstjenesten støtter ikke bilder i full størrelse i selvbetjeningsmiljøer.)
- Et problem som involverte korte plukkinger med null antall, er løst.
- Appen slutter ikke lenger å svare når et detaljkort viser flere identiske felt.

### <a name="known-issues-in-version-2060"></a>Kjente problemer i versjon 2.0.6.0

Følgende kjente problemer finnes i denne versjonen:

- Appen (spesielt arbeidslisten) blir tregere over tid.
- **Windows-versjon:** Når et USB-drev brukes til skanning på Windows, fører inkonsekvente resultater til at skannede symboler blandes sammen.

## <a name="version-2050"></a>Versjon 2.0.5.0

Denne versjonen inneholder følgende nye funksjoner, reparasjoner og forbedringer:

- Klienthemmeligheten er ikke lenger skjult i installasjonsprogrammet for tilkoblingsinnstillinger.
- Du kan nå trykke lenge på hvilken som helst tekst for å se den fullt ut.
- Feilmeldingen når lagringstillatelser mangler, er forbedret.
- Nye kontrollsekvenser er lagt til for noen flyter.
- Send-knappen blir ikke lenger tilgjengelig ved en feil på grunn av vindusstørrelsen.
- Glidebrytere kan nå fortsette på mindre skjermer når større knappestørrelser brukes.
- Fireknappsoverlegget er ikke lenger avskåret.
- Tastaturet støtter nå sletteknappen.
- Et problem med lysstyrken som kan oppstå når du trykker på tastaturet, er løst.
- Ulike demodataproblemer er løst.
- Et problem som påvirket numeriske felt på detaljsiden, er løst.
- Skjermtastaturet forsvinner ikke lenger enkelte ganger på noen enheter.
- Ulike brukergrensesnittfeil er rettet, for eksempel feil som påvirket bakgrunnsfargen og plasseringen.
- Det russiskspråklige brukergrensesnittet er forbedret.
- Ulike problemer som førte til at systemet sluttet å svare, er løst.
- Et problem som var relatert til å åpne kalkulatoren på nytt, er løst.
- **Android-versjon:** Et problem som førte til at Android 4.4 sluttet å svare ved oppstart, er løst.
- **Android-versjon:** Minimumsskalering er redusert til 50 prosent.

## <a name="version-2040"></a>Versjon 2.0.4.0

Versjon 2.0.4.0 var den første generelt tilgjengelige utgivelsen av Warehouse Management-mobilappen.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nye funksjoner, reparasjoner og forbedringer i versjon 2.0.4.0

Denne versjonen introduserer følgende nye funksjoner, reparasjoner og forbedringer som ikke var tilgjengelige i forhåndsvisningsversjonen:

- Hvis et detaljkort inneholder to etiketter som har identiske data, skjules en av etikettene.
- Spesialtegn vises nå som standard, og alternativet for å skjule dem er fjernet fra brukerinnstillingene.
- Deaktiverte send-knapper vises nå som ikke tilgjengelige i kompakt armholdt visning.
- En endring i sekvenseringslogikken for kontroller sikrer jevnere skalering på tvers av enheter. Derfor er det mindre behov for å justere skaleringen av skrifter eller knapper.
- Standard fargetema er endret til *Mørk*.
- Det manglende ikonet for den deaktiverte Send-knappen er lagt til i båndvisning.
- Tidsavbruddsunntak tar deg nå til tilkoblingssiden i stedet for å vise en innebygd feil.
- Hvis ingen sendehandling er tilgjengelig (for eksempel **OK**, **Ja**, **Godta**, **Ferdig** eller **Ferdig**), deaktiveres Send-knappen.
- Appstabiliteten er forbedret.
- Det finnes en hurtigreparasjon for sikkerhetsproblemet [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows-versjon:** Et problem på Windows, der menyer ikke reagerte etter at vinduet ble endret, er løst.

### <a name="known-issue-in-version-2040"></a>Kjent problem i versjon 2.0.4.0

Følgende kjente problem finnes i denne versjonen:

- Denne versjonen har et problem med enheter som bruker Android 4.4. Det kan oppstå problemer når du bruker appen på denne Android-versjonen.
