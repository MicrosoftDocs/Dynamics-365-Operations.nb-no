---
title: Bruke arbeidsflyter til å administrere informasjon om ansatte
description: Dette emnet forklarer hvordan du kan bruke arbeidsflyter til å administrere informasjon om ansatte.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d80ed49a4f423179997ac35562284a4e28af803f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068091"
---
# <a name="use-workflows-to-manage-employee-information"></a>Bruke arbeidsflyter til å administrere informasjon om ansatte


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.

Arbeidsflytfunksjonen for personale inneholder flere arbeidsflyter for administrasjon av personalaktiviteter. I tillegg finnes mange tilgjengelige alternativer, slik at du kan endre bestemte arbeidsflyter og knytte dem til et rapporteringshierarki. Arbeidsflyter er tilgjengelige for å bidra til å administrere endringer i flere informasjonstyper om ansatte. Du kan knytte en arbeidsflyt til en stilling. Hvis ansatte endrer sine ansattpost, startes en arbeidsflyt som krever godkjenning før den nye informasjonen lagres. Arbeidsflyter er forhåndsdefinerte for følgende typer informasjon for å bidra til effektivt å administrere endringer og holde de ansattes data nøyaktige:

-   Identifikasjonsnumre
-   Kurs
-   Utdanning
-   Bilde
-   Utlånte varer
-   Yrkeserfaring
-   Prosjekterfaring
-   Kompetanse
-   Tillitsverv
-   Personalhandlinger
-   Kursregistrering

Når ansatte ansettes, overføres eller slutter, kan arbeidsflyten inneholde en gjennomgangsprosess. På denne måten kan et dokument revideres eller vilkårene i en handling kan defineres som en del av arbeidsflyten. Når gjennomgangsprosessen er fullført, fullføres dokumentet eller handlingen, og arbeidsflyten går til et trinn for endelig godkjenning.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Knytte en arbeidsflyt til et stillingshierarki
Du kan knytte en arbeidsflyt til hvilket som helst hierarki som du konfigurerer. Hvis en stilling for eksempel er tilknyttet et matriserapporteringshierarki, kan du konfigurere en arbeidsflyt som ruter utgifter for et bestemt prosjekt til prosjektleder i stedet for lederen for ansatt som er knyttet til denne stillingen. Hvis du vil opprette en ny arbeidsflyt eller endre en eksisterende arbeidsflyt, går du til siden **Personalarbeidsflyter** og velger **Ny**. Velg en arbeidsflyt i listen for å åpne arbeidsflytutformingen. Du kan bruke utformingen til å opprette en ny arbeidsflyt eller endre trinnene i en eksisterende arbeidsflyt. Når du endrer en eksisterende arbeidsflyt, lagres endringene som en ny versjon. Derfor kan du alltid gå tilbake til en tidligere versjon hvis du må.

## <a name="configure-a-human-resources-workflow"></a>Konfigurere en personalarbeidsflyt
Følg fremgangsmåten nedenfor hvis du vil konfigurere en grunnleggende arbeidsflyt som startes når ansatte be om endringer av sin personlige ID.

1.  På siden **Personalarbeidsflyter** velger du **Ny**.
2.  I listen over tilgjengelige arbeidsflyter velger du **Identifikasjonsnumre**.
3.  Velg **Kjør** for å åpne arbeidsflytutformingen, og angi deretter brukernavn og passord når du blir bedt om det.
4.  Dra elementet **Godkjenn identifikasjonsnummer** fra listen over arbeidsflytelementer til utformingslerretet.
5.  Koble godkjenningselement til **Start** og **Fullfør**.
6.  Dobbelttrykk (eller dobbeltklikk) på **Godkjenn element**, velg og hold (eller høyreklikk), og velg deretter **Egenskaper**.
7.  Følg denne fremgangsmåten for å legge til instruksjoner for arbeidselement:

    1.  Velg **Tilordning**, og velg deretter **Hierarki** under tilordningstypen.
    2.  Under **Hierarki**-delen velger du **Konfigurerbart hierarki**.
    3.  Legge til et stoppvilkår, og lukke siden.

8.  Fyll ut eventuelle instruksjoner (ingen ekstra advarsler skal finnes).
9.  Velg **Lagre og lukk**. Aktivere den nye arbeidsflyten når dialogboksen åpnes, og velger **Gjør aktiv**.
10. Gå til **Personale** &gt; **Stillinger** &gt; **Stillingshierarkityper**.
11. Velg **Matrise**.
12. Legg til arbeidsflyten **Arbeideridentifikasjonsnummer** i listen.

## <a name="additional-resources"></a>Tilleggsressurser

[Vise og administrere adresseendringer](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
