---
title: Bruk arbeidsflyter til å administrere informasjon om ansatte
description: Denne artikkelen forklarer hvordan du kan bruke arbeidsflyter til å administrere informasjon om ansatte.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750741"
---
# <a name="use-workflows-to-manage-employee-information"></a>Bruk arbeidsflyter til å administrere informasjon om ansatte

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen forklarer hvordan du kan bruke arbeidsflytfunksjonen for personal til å administrere informasjon om ansatte. Du kan for eksempel knytte en arbeidsflyt til en stilling, og konfigurere en godkjenningsarbeidsflyt som startes når ansatte endrer sin post.

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

Du kan knytte en arbeidsflyt til et hvilket som helst stillingshierarki du konfigurerer. To hierarkityper brukes til arbeidsflytruting: **Leder** og **Konfigurerbart**.

- Et **Leder** hierarki representerer rapporteringsstrukturen i firmaet eller organisasjonen. Hvis du vil ha mer informasjon om denne hierarkitypen, kan du se [Rapporterer til stilling](hr-personnel-positions.md#reports-to-position).
- Et **Konfigurerbart** hierarki representerer en matrise eller et egendefinert hierarki. Hvis du vil ha mer informasjon om denne hierarkitypen, kan du se [Relasjoner](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Eksempel på lederhierarki

Du kan konfigurere en arbeidsflyt slik at når en ansatt sender inn en innkjøpsforespørsel om en ny datamaskin, rutes forespørselen til den ansattes leder og lederen høyere oppe. Når du konfigurerer arbeidsflyttrinnet, angir du **Hierarki** for feltet **Tilordningstype**. Fanen **Hierarkitype** blir deretter tilgjengelig. I dette eksemplet velger du **Leder** hierarkiet.

### <a name="configurable-hierarchy-example"></a>Eksempel på konfigurerbart hierarki

Hvis en stilling for eksempel er knyttet til et matriserapporteringshierarki, kan du konfigurere en arbeidsflyt som ruter utgifter for et bestemt prosjekt til prosjektlederen i stedet for den ansattes leder. I dette tilfellet angir du **Hierarki** i feltet **Tilordningstype**. I **Hierarkitype**-fanen velger du deretter **Konfigurerbart** hierarki. Når arbeidsflyten er definert, velger du **Tilknytt** hierarki på siden **Arbeidsflytoppsett** for å velge hierarkiet som skal brukes i arbeidsflytrutingen.

> [!IMPORTANT]
> Når et dokument, en transaksjon eller en hovedpost sendes inn til arbeidsflytgodkjenning, brukes senderens primære stilling til å beslutte hvem dokumentet skal sendes til i neste omgang.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Hierarkiinnstilling i Arbeidsflytparametere

1. Gå til **Hierarkiruting** på siden **Arbeidsflytparametere**.
2. Som standard er alternativet **Bruk stillingshierarki** satt til **Nei**. I dette tilfellet vil arbeidsflyten bruke arbeiderens primære stilling når den navigerer i hierarkiet. Sett alternativet til **Ja** for å gjøre at arbeidsflyten bruker stillingens overordnede når den navigerer i hierarkiet.

### <a name="additional-example"></a>Tilleggseksempel 

Ansatt Grace Sturman har to stillinger: konsulent og instruktør. Instruktør er den primære stillingen til Grace. Når hun ikke lærer opp nye ansatte, er hun tilgjengelig for konsulentarbeid. Grace rapporterer til Claire, personaldirektøren, via den primære stillingen. Claire rapporterer til Charlie. I konsulentstillingen foretar Grace indirekte rapportering til sekundære ledere, avhengig av prosjektet.

Firmaet til Grace lager arbeidsflytrutingsregler som er basert på et **konfigurerbart** hierarki (matrise-/prosjektbaserte hierarkier). Dette hierarkiet bruker konsulentstillingen til Grace. Hvis **Nei** er angitt for alternativet **Bruk stillingshierarki** når et dokument rutes til Grace for godkjenning, ser arbeidsflyten på den primære stillingen (instruktør) for å avgjøre hvor dokumentet skal rutes i neste omgang. I dette tilfellet blir det først rutet til Claire og deretter til Charlie. Hvis **Ja** er angitt for alternativet og arbeidsflyten bruker et **Konfigurerbart** hierarki, ser arbeidsflyten på konsulentstillingen og rapporteringsrelasjonen til Grace for å avgjøre hvor dokumentet skal rutes i neste omgang.

### <a name="configure-a-human-resources-workflow"></a>Konfigurere en personalarbeidsflyt
Følg fremgangsmåten nedenfor hvis du vil konfigurere en grunnleggende arbeidsflyt som startes når ansatte be om endringer av sin personlige ID.

1.  På siden **Personalarbeidsflyter** velger du **Ny**.
2.  I listen over tilgjengelige arbeidsflyter velger du **Identifikasjonsnumre**.
3.  Velg **Kjør** for å åpne arbeidsflytutformingen, og angi deretter brukernavn og passord.
4.  Flytt elementet **Godkjenn identifikasjonsnummer** fra listen over arbeidsflytelementer til utformingslerretet.
5.  Koble godkjenningselement til **Start** og **Fullfør**.
6.  Dobbelttrykk (eller dobbeltklikk) på **Godkjenn element**, velg og hold (eller høyreklikk), og velg deretter **Egenskaper**.
7.  Følg denne fremgangsmåten for å legge til instruksjoner for arbeidselement:

    1.  Velg **Tilordning**, og velg deretter **Hierarki** under tilordningstypen.
    2.  Under **Hierarki**-delen velger du **Konfigurerbart hierarki**.
    3.  Legge til et stoppvilkår, og lukke siden.

8.  Fullfør eventuelle tilleggsinstruksjoner.
9.  Velg **Lagre og lukk**. Aktivere den nye arbeidsflyten når dialogboksen åpnes, og velger **Gjør aktiv**.
10. Gå til **Personale** &gt; **Stillinger** &gt; **Stillingshierarkityper**.
11. Velg **Matrise**.
12. Legg til arbeidsflyten **Arbeideridentifikasjonsnummer** i listen.

## <a name="additional-resources"></a>Tilleggsressurser

[Vise og administrere adresseendringer](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
