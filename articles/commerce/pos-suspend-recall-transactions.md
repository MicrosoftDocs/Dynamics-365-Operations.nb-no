---
title: Suspendere og gjenoppta en transaksjon på salgsstedet
description: Dette emnet forklarer hvordan brukere kan avbryte pågående transaksjoner og deretter gjenoppta dem senere eller i en annen kasse ved hjelp av Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023599"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Suspendere og gjenoppta en transaksjon på salgsstedet

[!include [banner](includes/banner.md)]


Salgsstedsbrukere kan avbryte pågående transaksjoner og deretter gjenoppta dem senere eller i en annen kasse. Transaksjoner suspenderes ofte for å frigjøre en kasse raskt til en annen oppgave uten å miste arbeidet i gjeldende transaksjon. En butikkmedarbeider begynner for eksempel å behandle en kundetransaksjon på en mobil enhet, men må fullføre den i en kasse som har kassaskuffe. I dette tilfellet kan butikkmedarbeideren avbryte transaksjonen på den mobile enheten, og deretter gjenoppta og fortsette den i en kasse.

## <a name="configure-suspend-and-resume-functionality"></a>Konfigurere suspenderings- og gjenopptagelsesfunksjonalitet

### <a name="pos-operations"></a>POS-operasjoner

To [salgsstedsoperasjoner](pos-operations.md) lar salgsstedet støtte suspenderings- og gjenopptagelsesscenarioer. Du kan tilordne disse operasjonene til [knappegrupper](pos-screen-layouts.md) på transaksjonssiden eller velkomstsiden.

- 503: Suspender transaksjon
- 504: Tilbakekall transaksjon

### <a name="receipt-template"></a>Kvitteringsmal

Salgsstedet kan konfigureres til å generere en utskrevet seddel når en transaksjon blir suspendert. Denne seddelen kan brukes til å identifisere og tilbakekalle transaksjonen raskt senere.

Hvis du vil la salgsstedet kunne skrive ut en seddel, må du legge til **Suspendert transaksjon**-kvitteringsformatet i butikkens kvitteringsprofil. Du kan utforme kvitteringsformatet slik at det inkluderer eller utelukker spesifikke detaljer om transaksjonen. Formatet kan for eksempel inkludere en strekkode som støtter skanning.

### <a name="receipt-numbering"></a>Kvitteringsnummerering

Som for andre salgsstedstransaksjonstyper som genererer en utskrevet kvittering, kan du definere en nummerserie for suspenderte transaksjoner i **Kvitteringsnummerering**-delen i butikkens funksjonalitetsprofil.

### <a name="void-when-closing-shift"></a>Annuller ved avslutning av skift

Du kan bruke **Annuller ved avslutning av skift**-alternativet for å kreve at brukerne enten fullfører eller annullerer alle suspenderte transaksjoner før de avslutter skiftet. Under **Lukk skift**-operasjonen vil salgsstedet be brukerne om å enten vise eller annullere utestående suspenderte transaksjoner.

## <a name="suspend-and-resume-a-transaction"></a>Suspendere og gjenoppta en transaksjon

### <a name="suspend-a-transaction"></a>Suspendere en transaksjon

Brukere som har tilstrekkelige rettigheter og som har et skjermoppsett som inneholder **Suspender transaksjon**-operasjonen, kan avbryte en transaksjon slik at den kan tilbakekalles senere eller i en annen kasse.

Transaksjoner kan bare suspenderes hvis de **ikke** inneholder følgende typer linjer:

- Aktive betalingslinjer
- Gavekortlinjer (enten for å utstede et gavekort eller for å legge til på gavekortsaldoen)

En suspendert transaksjon påvirker ikke salgsinformasjon eller informasjon om lagertilgjengelighet for butikken.

### <a name="resume-a-suspended-transaction"></a>Gjenoppta en suspendert transaksjon

Suspenderte transaksjoner kan tilbakekalles og gjenopptas i den samme butikken av alle brukere som har tilstrekkelige rettigheter, og som også har et oppsett som inneholder **Tilbakekall transaksjon**-operasjonen.

Skann strekkoden på den utskrevne seddelen hvis du vil tilbakekalle en suspendert transaksjon raskt og enkelt, mens du viser listen over transaksjoner fra **Tilbakekall transaksjon**-operasjonen.

### <a name="considerations-for-offline-mode"></a>Hensyn ved frakoblet modus

- Transaksjoner som suspenderes når salgsstedet er i tilkoblet modus, kan ikke gjenopptas i frakoblet modus fordi dataene ikke er synkronisert til den frakoblede databasen.
- Hvis du suspenderer en transaksjon når salgsstedet er i frakoblet modus, kan du tilbakekalle den i frakoblet modus, forutsatt at salgsstedet ikke ble satt tilbake til tilkoblet modus når som helst etter du suspenderte transaksjonen. Når salgsstedet settes tilbake til tilkoblet modus, flyttes data om suspenderte transaksjoner til den tilkoblede databasen og fjernes fra den frakoblede databasen. Derfor kan du bare gjenoppta transaksjonene i tilkoblet modus. Hvis du setter salgsstedet tilbake til frakoblet modus, kan du ikke gjenoppta disse suspenderte transaksjonene fordi de allerede har blitt fjernet fra den frakoblede databasen.

### <a name="void-a-suspended-transaction"></a>Annullere en suspendert transaksjon

Du kan annullere suspenderte transaksjoner enten ved å tilbakekalle transaksjonen og deretter utføre **Annuller transaksjon**-operasjonen, eller ved å velge transaksjonen i **Tilbakekall transaksjon**-listen og velge **Annuller** i programfeltet. Eventuelt kan butikken konfigureres til å be brukerne om å annullere suspenderte transaksjoner når de avslutter skiftet.
