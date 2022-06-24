---
title: Konfigurer en e-postkanal
description: Denne artikkelen forklarer hvordan du konfigurerer en e-postkanal slik at den kan motta elektroniske fakturaer.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9227b032ffe896ad6a67962e5047fd797a883ae1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902392"
---
# <a name="configure-an-email-channel"></a>Konfigurer en e-postkanal

[!include [banner](../includes/banner.md)]

Hvis funksjonen for elektronisk fakturering du opprettet, importerer elektroniske leverandørfakturaer fra vedlagte filer som mottas via e-post, bør du konfigurere en e-postkontokanal.

1. Velg funksjonen for elektronisk fakturering du opprettet, i Regulatory Configuration Service (RCS). Kontroller at du velger versjonen som har statusen **Utkast**.
2. Velg **Legg til** i **Oppsett**-fanen.
3. Velg alternativet **Egendefinert oppsett** i feltgruppen **Ny** i rullegardinboksen **Opprett funksjonsoppsett**:
4. Velg alternativet **Datakanal** i feltgruppen **Oppsettype**.
5. Angi **Innkommende e-post** i feltet **Velg datakanal**.
6. Velg **Opprett**.
7. Velg linjen du opprettet, og velg deretter **Rediger**.
8. Angi følgende obligatoriske felter i **Parametere**-delen i **Datakanal**-fanen.

    | Felt                | Beskrivelse |
    |----------------------|-------------|
    | Datakanal         | Angi et unikt navn for å identifisere datakanalen. Navnet kan ha maksimum 10 tegn. Det refereres til dette i relevansregler og i tilkoblede programmer i løpet av kommunikasjonen. |
    | Serveradresse       | Angi serveradressen til leverandøren av e-postkontoen. Serveradressen for leverandøren `https://outlook.live.com` er for eksempel imap-mail.outlook.com. |
    | Serverport          | Angi nummeret på porten som leverandøren av e-postkontoen bruker. Serverporten for leverandøren `https://outlook.live.com` er for eksempel 993. |
    | Hemmelighet for brukernavn     | Angi navnet på Microsoft Azure Key Vault-hemmeligheten som inneholder ID-en til e-postbrukerkontoen. Denne nøkkelen må opprettes i Key Vault og konfigureres i tjenestemiljøet. |
    | Hemmelighet for brukerpassord | Angi navnet på Key Vault-hemmeligheten som inneholder passordet til e-postbrukerkontoen. |
    | Tidsavbrudd              | Den lengste tiden, i millisekunder (ms), som systemet skal vente på svar. Standardverdien er 10 000 ms (10 sekunder). |
    | Hovedmappe          | Angi importkilden for e-post eller mappen som tjenesten skal behandle e-postmeldinger fra. |
    | Arkivmappe       | Angi mappen der behandlede e-postmeldinger skal lagres. Hvis du ikke angir denne mappen, opprettes den automatisk av systemet. |
    | Feilmappe         | Angi mappen som systemet skal flytte e-postmeldinger til, hvis behandlingen mislykkes. Hvis du ikke angir denne mappen, opprettes den automatisk av systemet. |
    | Maksimal meldingsstørrelse     | Angi maksimumsstørrelsen for enkeltmeldinger som behandles, i byte. Standardverdien er 20 000 000 byte. |
    | Maksimalt meldingsnummer   | Angi maksimalt antall meldinger som skal behandles for én handling. Hvis du ikke vil begrense antall meldinger, angir du **0** (null) for verdien. |
    | Fra-filter          | Angi en streng for å filtrere etter avsenderadresse. Bare e-postmeldinger der avsenderadressen samsvarer med filteret, behandles. Dette feltet er valgfritt. Hvis du vil angi flere avsenderadresser, bruker du semikolon (;) som skilletegn. |
    | Emnefilter       | Angi en streng for å filtrere etter emne. Bare e-postmeldinger der emnet samsvarer med filteret, behandles. Dette feltet er valgfritt. Det er støtte for en enkel maske som **\*smth\*.ext**, der hver stjerne (\*) representerer null eller flere forekomster av et tegn. |
    | Datofilter          | Angi en dato for å definere maksimumsalderen på meldinger som behandles, i dager. Dette feltet er valgfritt. Standardverdien er 30 dager. |
    | Behandlingsmodus      | <p>Velg ett av følgende alternativer for å angi om alle vedleggene i en e-postmelding kan behandles sammen, eller om hvert vedlegg skal behandles separat:</p><ul><li><b>Etter vedlegg</b> – Det opprettes et nytt elektronisk dokument for hvert vedlegg i e-postmeldingen. Hvis én e-postmelding for eksempel omfatter flere filer som inneholder e-fakturadata, blir hver fil regnet for å være en ny e-faktura i systemet.</li><li><b>Etter e-post</b> – Ett vedlegg blir regnet for å være et basisvedlegg, og det opprettes én elektronisk faktura i systemet. Andre vedlegg kan brukes som støttefiler.</li></ul> |

9. I delen **Vedleggsfilter** legger du til filfiltreringsinformasjonen. Bare vedlegg som oppfyller det definerte filteret, blir behandlet. Hvis du for eksempel bruker **\*.xml**, filtreres vedlegg som har filtypen XML. Navnet på vedlegget brukes i Dynamics 365 Finance eller Dynamics 365 Supply Chain Management under oppsett.

    - Hvis du angir **Etter e-post** for feltet **Behandlingsmodus** i det forrige trinnet, kan du legge til flere filtre her. Navnet identifiserer det bestemte dokumentet.
    - Hvis du angir **Etter vedlegg** for feltet **Behandlingsmodus**, kan du bare legge til ett filter.

10. Gå gjennom og oppdater kriteriene i **Relevansregler**-fanen etter behov. Verdien i **Kanal**-feltet må være lik verdien du angav i **Datakanal**-feltet i trinn 8.
11. Velg **Lagre**, og lukk siden.
