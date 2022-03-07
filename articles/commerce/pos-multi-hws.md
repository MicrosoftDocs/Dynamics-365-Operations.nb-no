---
title: Dedikerte betalingsterminaler og spørringer for en skriver og kassaskuff
description: Dette emnet gir informasjon om muligheten til å ha en dedikert betalingsterminal og å be brukeren velge en kassaskuff og en kvitteringsskriver.
author: rubendel
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a3c7eb9580f9155dd33f6351f37eb1edd269a3d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018639"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Dedikerte betalingsterminaler og spørringer for en skriver og kassaskuff

[!include [banner](includes/banner.md)]

Dette emnet gir informasjon om muligheten til å ha en dedikert betalingsterminal og å be brukeren velge en kassaskuff og en kvitteringsskriver.

## <a name="overview"></a>Oversikt

Moderne forhandlere søker etter måter å effektivisere kasseopplevelsen i butikken på. Trenden i retning av papirløs utsjekking ved hjelp av elektroniske betalinger gjør det ikke bare kjøpsopplevelsen enklere – det gir også redusert behov for å ha en rekke eksterne enheter tilgjengelig for alle ansatte i butikkene.

Microsoft Dynamics 365 Commerce støtter disse trendene ved å muliggjøre et scenario der en salgsstedsenhet (POS) har en dedikert betalingsterminal som er tilordnet hele tiden, men ikke en egen kvitteringsskriver eller kassaskuff. Når medarbeidere trenger å skrive ut en kvittering eller ta imot kontantbetaling, blir de bedt om å velge en maskinvarestasjon der disse enhetene er konfigurert.

## <a name="key-terms"></a>Viktige termer

| Semester | beskrivelse |
|---|---|
| Meld på | Enheten som brukes til å konfigurere en forekomst av en POS-kasse. |
| Enhet | En representasjon av den fysiske forekomsten av en POS-kasse og et moderne POS-program som er tilordnet kassen. |
| Dedikert maskinvarestasjon | Forretningslogikken for maskinvarestasjonen som er bygget inn i programmene Modern POS for Windows og Modern POS for Android. |
| Skuffeport (d/k) | En tradisjonell metode for å koble en kassaskuff til en kvitteringsskriver. |
| Nettverksenheter | Innebygd støtte for nettverksaktiverte betalingsterminaler, kvitteringsskrivere og kassaskuffer. |

## <a name="supported-pos-clients-and-devices"></a>Støttede POS-klienter og -enheter

Funksjonaliteten som beskrives i dette emnet, støttes av Moderne salgssted for Windows- og Moderne salgssted for Android-klienter.

Denne funksjonaliteten støtter nettverksaktiverte betalings terminaler og kvitteringsskrivere. Du kan gi kassaskuffstøtte ved å koble kassaskuffen til den nettverksaktiverte kvitteringsskriveren via d/k-porten.

Kunderettet støtte for denne funksjonaliteten leveres av [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3). Det kan imidlertid hende at andre betalingskoblinger støttes via Commerce-SDK for betalinger. Støttede kvitteringsskrivere inkluderer nettverksaktiverte kvitteringsskrivere fra Star Micronics og Epson.

For å konfigurere Star Micronics-kvitteringsskrivere bruker du verktøyet Star Micronics Printer Utility for å konfigurere enheten slik at den kan brukes over nettverket. Dette verktøyet oppgir også IP-adressen til enheten.

Hvis du vil konfigurere skrivere med Epson-kvitteringer, bruker du Epson ePOS-verktøyet til å konfigurere enheten til å bruke nettverks protokoller.

Hvis du vil ha mer informasjon om hvordan du konfigurerer nettverksenheter, kan du se [Oversikt over støtte for eksterne nettverksenheter](./dev-itpro/network-peripherals.md).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Konfigurer en dedikert betalingsterminal og en spørring for en skriver og kassaskuff

### <a name="set-up-hardware-profiles"></a>Konfigurere maskinvareprofiler

Du må ha to typer maskinvareprofiler. Den første er tilordnet registeret. Den andre er tilordnet en maskinvarestasjon på butikknivå, og brukes til å gruppere nettverkskvitteringsskrivere og kassaskuffer på en logisk måte.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Konfigurere en maskinvareprofil for registeret

Følg denne fremgangsmåten for å konfigurere maskinvareprofilen som er tilordnet registeret.

1. I Dynamics 365 Commerce søker du etter **Maskinvareprofil**.
2. Velg **Ny**.
3. Tilordne et maskinvareprofilnummer, og angi en beskrivelse. Denne maskinvareprofilen tilordnes selve registret. Derfor vil en beskrivelse som for eksempel **Dedikert med reserve** være tilstrekkelig.
4. Konfigurer følgende enhetstyper i hurtigkategoriene for ulike enhetstyper.

    | Enhet | Type | Enhetsnavn | Ytterligere detaljer |
    |---|---|---|---|
    | Skriver | Nettverk | *Vilkårlig* | Enhetsnavnet skiller mellom store og små bokstaver. **Kvitteringsprofil-ID-en** må være den samme som **Kvitteringsprofil-ID-en** som er tilordnet nettverksskriveren som er konfigurert i maskinvareprofilen som er tilordnet maskinvarestasjonen på kanalnivået. |
    | Kassaskuff | Nettverk | *Vilkårlig* | Enhetsnavnet skiller mellom store og små bokstaver. Angi alternativet **Bruk delte skift** til **Ja**. |
    | EFT-tjeneste | Adyen | Gjelder ikke | Hvis du vil ha informasjon om hvordan du konfigurerer den bruksklare Adyen-betalingskoblingen, kan du se [Adyen-betalingskobling i Dynamics 365](./dev-itpro/adyen-connector.md?tabs=8-1-3). Andre betalingskoblinger kan være støttet via [Commerce-SDK for betalinger](./dev-itpro/end-to-end-payment-extension.md). |
    | PIN-kodetastatur | Nettverk | **MicrosoftAdyenDeviceV001** | Ingen. |

5. I Dynamics 365 Commerce søker du etter **Registre**.
6. Velg et register ved å velge registernummeret, og velg deretter **Rediger**.
7. Tilordne maskinvareprofilen du nettopp opprettet, til kassen som skal bruke en dedikert betalingsterminal. Enheten som er tilordnet denne kassen, må enten bruke moderne Modern POS for Windows-programmet eller Modern POS for Android-programmet.
8. Velg **Lagre**.
9. I handlingsruten går du til **Kasser**-kategorien og velger **Konfigurer IP-adresser**.
10. I hurtigkategorien for **PIN-kodetastatur** angir du IP-adressen til betalingsterminalen. Hvis du vil ha informasjon om hvordan du får tak i IP-adressen for betalingsterminalen ved å bruke Adyen-koblingen, se [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).
11. Velg **Lagre**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Konfigurere en maskinvareprofil for kvitteringsskriveren og kassaskuffen

Følg denne fremgangsmåten for å konfigurere maskinvareprofilen som brukes til å gruppere kvitteringsskriveren og kassaskuffen i nettverket.

1. I Dynamics 365 Commerce søker du etter **Maskinvareprofil**.
2. Velg **Ny**.
3. Tilordne et maskinvareprofilnummer, og angi en beskrivelse. Denne maskinvareprofilen brukes til å gruppere kvitteringsskriveren og kassaskuffen. Derfor vil en beskrivelse som **Nettverksskriver og kassaskuff** være tilstrekkelig.
4. Konfigurer følgende enhetstyper i hurtigkategoriene for ulike enhetstyper.

    | Enhet | Type | beskrivelse | Flere detaljer |
    |---|---|---|---|
    | Skriver | Nettverk | **Epson** eller **Star** | Enhetsnavnet skiller mellom store og små bokstaver. **Kvitteringsprofil-ID-en** må være den samme som **Kvitteringsprofil-ID-en** som er tilordnet skriveren som er konfigurert i maskinvareprofilen som er tilordnet kassen. |
    | Kassaskuff | Tilbakefall | **Epson** eller **Star** | Enhetsnavnet skiller mellom store og små bokstaver. Angi alternativet **Bruk delte skift** til **Ja**. |

5. Velg **Lagre**.

### <a name="set-up-hardware-stations"></a>Konfigurere maskinvarestasjoner

Du må ha to maskinvarestasjoner. Den første tilordnes registeret. Den andre blir valgt ved behov hver gang en kvittering må skrives ut eller en kassaskuff må åpnes.

#### <a name="register-a-hardware-station"></a>Registrere en maskinvarestasjon

1. I Dynamics 365 Commerce søker du etter **Alle butikker**.
2. Velg en butikk ved å velge **ID for detaljhandelskanal**-verdiene dens og deretter **Rediger**.
3. Velg **Legg til** i hurtigkategorien **Maskinvarestasjoner**.
4. Angi **Maskinvarestasjonstype**-feltet til **Dedikert**.
5. Angi en beskrivelse, men ikke angi andre verdier for denne maskinvarestasjonen. Denne maskinvarestasjonen brukes alltid til registeret. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Konfigurere en maskinvarestasjon for kvitteringsskriveren og kassaskuffen

1. I Dynamics 365 Commerce søker du etter **Alle butikker**.
2. Velg en butikk ved å velge **ID for detaljhandelskanal**-verdiene dens og deretter **Rediger**.
3. Velg **Legg til** i hurtigkategorien **Maskinvarestasjoner**.
4. Angi **Maskinvarestasjonstype**-feltet til **Dedikert**.
5. Angi en beskrivelse. Denne maskinvarestasjonen brukes til kvitteringsskriveren og kassaskuffen.
6. I **Maskinvareprofil**-feltet velger du maskinvareprofilen du tidligere opprettet for kvitteringsskriveren og kassaskuffen.
7. Velg **Lagre**.
8. Mens maskinvarestasjonen for kvitteringsskriveren og kassakuffen fortsatt er valgt, velger du **Konfigurer IP-adresser**.
9. Hent IP-adressen for skriveren, og angi den som IP-adresse for både kvitteringsskriveren og kassaskuffen.
10. Velg **Lagre**
11. Søk etter **Distribusjonsplaner**.
12. Velg distribusjonsplanen **1090**, og velg deretter **Kjør nå**.
13. Velg distribusjonsplanen **1070**, og velg deretter **Kjør nå**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Angi at systemet skal spørre etter kvitteringsskriveren og kassaskuffen ved behov

1. Lukk det gjeldende skiftet i en støttet POS-klient hvis et skift er åpent.
2. Logg på, og velg deretter **Skuffeoperasjoner uten skuff**.
3. Bruk **Administrer maskinvarestasjoner**-operasjonen til å slå på en maskinvarestasjon.
4. Velg maskinvarestasjonen du opprettet for kassen, slik at den blir aktiv.
5. Logg av salgsstedet, og logg deretter på igjen og åpne et skift.

Betalingsterminalen som er tilordnet maskinvareprofilen, vil nå alltid være aktiv, og du blir spurt om det kreves en kvitteringsskriver eller kassaskuff.

Mange butikker som har etterspurt denne funksjonen, er interesserte i å redusere avfall ved å sende e-postkvitteringer og oppmuntre til elektroniske betalinger. Avhengig av konfigurasjonen til salgsstedet blir butikkansatte bedt om å velge en kvitteringsskriver eller kassaskuff bare når en kunde ønsker en fysisk kvittering eller å betale med kontanter.

Butikkmedarbeidere blir bare bedt om å velge en maskinvarestasjon én gang per transaksjon, med mindre en kvittering må skrives ut og kontanter brukes til betaling, men maskinvareprofilen som opprinnelig ble valgt, inkluderer ikke begge enhetene. I så fall blir butikkmedarbeideren igjen bedt om å velge en maskinvarestasjon som kan brukes til å fullføre transaksjonen.

## <a name="related-articles"></a>Relaterte artikler

- [Definere POS Hybrid-app på Android og iOS](./dev-itpro/hybridapp.md)
- [Dynamics 365 Payment Connector for Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [Oversikt over støtte for eksterne nettverksenheter](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
