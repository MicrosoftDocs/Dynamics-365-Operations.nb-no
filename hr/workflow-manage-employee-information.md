---
title: "Bruke arbeidsflyter til å administrere informasjon om ansatte"
description: "Dette emnet forklarer hvordan du kan bruke arbeidsflyten muligheten for menneskelige ressurser til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Bruke arbeidsflyter til å administrere informasjon om ansatte

Dette emnet forklarer hvordan du kan bruke arbeidsflyten muligheten for menneskelige ressurser til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.

Mulighet for arbeidsflyt for menneskelige ressurser inneholder flere arbeidsflyter for administrasjon av Personalaktiviteter. I tillegg finnes mange alternativer slik at du kan endre bestemte arbeidsflyter og knytte dem til et rapporteringshierarki. Arbeidsflyter er tilgjengelige for å administrere endringer i standard typer informasjon om ansatte. Du kan knytte en arbeidsflyt for en stilling. Deretter, hvis ansatte endrer sine ansattpost, startes en arbeidsflyt som krever godkjenning før den nye informasjonen lagres. Arbeidsflyter som er forhåndsdefinert for følgende typer informasjon for å hjelpe deg med å administrere endringer og holde de ansattes data nøyaktig:

-   Identifikasjonsnumre
-   Kurs
-   Utdanning
-   Bilde
-   Utlånte varer
-   Yrkeserfaring
-   Prosjekterfaring
-   Kompetanse
-   Tillitsverv
-   Handlinger for menneskelige ressurser
-   Kursregistrering

Når ansatte ble ansatt, overføres eller avsluttet, kan arbeidsflyten inkludere en gjennomgangsprosess. På denne måten kan et dokument kan revideres eller vilkårene i en handling kan defineres som en del av arbeidsflyten. Når kontrollprosessen er fullført, dokumentet eller handlingen er fullført, og går til et endelig godkjenning-trinn i arbeidsflyten.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Knytt en arbeidsflyt med et stillingshierarki
Du kan knytte et hvilket som helst hierarki som du konfigurerer en arbeidsflyt. Hvis en posisjon er forbundet med et rapporteringshierarki i matrisen, kan du for eksempel konfigurere en arbeidsflyt som ruter utgifter for et bestemt prosjekt til project-emnet i stedet for lederen for ansatt som er knyttet til denne plasseringen. Å opprette en ny arbeidsflyt eller endre en eksisterende arbeidsflyt på den **Personale arbeidsflyt** klikker du **ny**. Velg en arbeidsflyt i listen for å starte Workflow designer. Du kan bruke designer til å opprette en ny arbeidsflyt eller endre trinnene i en eksisterende arbeidsflyt. Når du endrer en eksisterende arbeidsflyt, lagres endringene som en ny versjon. Derfor kan du alltid gå tilbake til en tidligere versjon hvis du må.

## <a name="configure-a-human-resources-workflow"></a>Konfigurere en arbeidsflyt for menneskelige ressurser
Hvis du vil konfigurere en grunnleggende arbeidsflyt startes når ansatte be om endringer i sine personlige ID, følger du denne fremgangsmåten.

1.  På den **Personalarbeidsflyter** klikker du **ny**.
2.  I listen over tilgjengelige arbeidsflyter, kan du velge **identifikasjonsnumre**.
3.  Klikk **kjører** å starte Workflow designer, og angi deretter brukernavn og passord når du blir bedt om.
4.  Dra den **godkjenne identifikasjonsnummeret** elementet fra listen over arbeidsflytelementer til designer lerret.
5.  Koble godkjenningselement til **Start** og **er ferdig med**.
6.  Dobbeltklikk **godkjenne elementet**, og deretter høyreklikker og velger **Egenskaper**.
7.  Følg denne fremgangsmåten for å legge til element Arbeidsinstruksjoner:
    1.  Velg **tildeling**, og velg deretter **hierarki** under tilordningstypen.
    2.  Under den **hierarki** utvalget, velg **konfigurerbare hierarkiet**.
    3.  Legge til et stoppvilkår, og lukke siden.

8.  Fyll ut eventuelle instruksjoner (ingen ekstra advarsler skal finnes).
9.  Klikk **Lagre og lukk**. Aktivere den nye arbeidsflyten når dialogboksen åpnes, og velger **gjøre aktiv**.
10. Gå til **Personale**&gt;**posisjoner**&gt;**Plasser hierarkityper**.
11. Velg **matrise**.
12. Legg til den **arbeider identifikasjonsnummeret** arbeidsflyten til listen.



