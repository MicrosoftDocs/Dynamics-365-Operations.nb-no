---
title: "Bruke arbeidsflyter til å administrere informasjon om ansatte"
description: "Dette emnet forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2dc4671e0b68dffe30fe73d8c95113481673a27a
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="use-workflows-to-manage-employee-information"></a>Bruke arbeidsflyter til å administrere informasjon om ansatte

[!include[banner](includes/banner.md)]


Dette emnet forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.

Arbeidsflytfunksjonen for personale inneholder flere arbeidsflyter for administrasjon av personalaktiviteter. I tillegg finnes mange tilgjengelige alternativer, slik at du kan endre bestemte arbeidsflyter og knytte dem til et rapporteringshierarki. Arbeidsflyter er tilgjengelige for å bidra til å administrere endringer i standard informasjonstyper om ansatte. Du kan knytte en arbeidsflyt til en stilling. Hvis ansatte endrer sine ansattpost, startes en arbeidsflyt som krever godkjenning før den nye informasjonen lagres. Arbeidsflyter er forhåndsdefinerte for følgende typer informasjon for å bidra til effektivt å administrere endringer og holde de ansattes data nøyaktige:

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
Du kan knytte en arbeidsflyt til hvilket som helst hierarki som du konfigurerer. Hvis en stilling for eksempel er tilknyttet et matriserapporteringshierarki, kan du konfigurere en arbeidsflyt som ruter utgifter for et bestemt prosjekt til prosjektleder i stedet for lederen for ansatt som er knyttet til denne stillingen. Hvis du vil opprette en ny arbeidsflyt eller endre en eksisterende arbeidsflyt, går du til siden **Personalarbeidsflyter** og klikker på **Ny**. Velg en arbeidsflyt i listen for å starte arbeidsflytutformingen. Du kan bruke utformingen til å opprette en ny arbeidsflyt eller endre trinnene i en eksisterende arbeidsflyt. Når du endrer en eksisterende arbeidsflyt, lagres endringene som en ny versjon. Derfor kan du alltid gå tilbake til en tidligere versjon hvis du må.

## <a name="configure-a-human-resources-workflow"></a>Konfigurere en personalarbeidsflyt
Følg fremgangsmåten nedenfor hvis du vil konfigurere en grunnleggende arbeidsflyt som startes når ansatte be om endringer av sin personlige ID.

1.  På siden **Personalarbeidsflyter** klikker du på **Ny**.
2.  I listen over tilgjengelige arbeidsflyter velger du **Identifikasjonsnumre**.
3.  Klikk på **Kjør** for å starte arbeidsflytutformingen, og angi deretter brukernavn og passord når du blir bedt om det.
4.  Dra elementet **Godkjenn identifikasjonsnummer** fra listen over arbeidsflytelementer til utformingslerretet.
5.  Koble godkjenningselement til **Start** og **Fullfør**.
6.  Dobbeltklikk på **Godkjenn element**, og deretter høyreklikker du på og velger **Egenskaper**.
7.  Følg denne fremgangsmåten for å legge til instruksjoner for arbeidselement:
    1.  Velg **Tilordning**, og velg deretter **Hierarki** under tilordningstypen.
    2.  Under **Hierarki**-delen velger du **Konfigurerbart hierarki**.
    3.  Legge til et stoppvilkår, og lukke siden.

8.  Fyll ut eventuelle instruksjoner (ingen ekstra advarsler skal finnes).
9.  Klikk **Lagre og lukk**. Aktivere den nye arbeidsflyten når dialogboksen åpnes, og velger **Gjør aktiv**.
10. Gå til **Personale** &gt; **Stillinger** &gt; **Stillingshierarkityper**.
11. Velg **Matrise**.
12. Legg til arbeidsflyten **Arbeideridentifikasjonsnummer** i listen.





