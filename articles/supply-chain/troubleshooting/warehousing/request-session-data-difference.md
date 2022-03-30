---
title: Uventet forskjell mellom forespørsels- og øktdata under testing
description: Det oppstår en uventet forskjell mellom valideringsresultatene for forespørsels- og øktdata i lageroppgaven.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456942"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Uventet forskjell mellom forespørsels- og øktdata under testing

Feilkode: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Symptomer

Når du bruker [valideringsrammeverket for lagerappoppgave](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), får du følgende feilmelding:

> Uventet forskjell mellom forespørsels- og øktdata. XML-protokoll for lagermobilenheter er brutt. REQUEST_XML_TAMPERING

## <a name="cause"></a>Årsak

Feilen oppstår når resultatet av det siste trinnet som ble kjørt i testkjøringen, ikke samsvarer med de registrerte inndataene for det neste trinnet. Denne situasjonen kan oppstå fordi oppgavevalidereren ikke bruker resultatet av et tidligere trinn som inndata for et etterfølgende trinn. I stedet bruker det registrert XML som inndata for hvert trinn.

I de fleste tilfeller oppstår feilen når du kjører en oppgave på nytt, men testen krever noen poster som ble endret eller fjernet av en tidligere kjøring av den samme oppgaven.

## <a name="resolution"></a>Oppløsning

Testkjøringen av valideringen av lagerappoppgaven kjører ikke en idempotent operasjon, men endrer de underliggende dataene. Derfor må du tilbakestille de relevante dataene før du kjører en oppgave på nytt.

1. Gå gjennom utdata-XML-en for det siste vellykkede testtrinnet for å finne ut hvor testkjøringen sluttet.
1. Inspiser testen, og kontroller at alle de nødvendige salgsordrene, overføringsordrene, arbeidshodene og andre poster fremdeles finnes og har forventet status.
1. Opprett på nytt eller rediger de manglende eller endrede postene. Du kan også opprette et nytt testoppsett og utforme testen for å bruke gyldige eksisterende poster.
