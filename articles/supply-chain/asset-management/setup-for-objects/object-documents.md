---
title: Aktivadokumenter
description: Dette emnet beskriver aktivadokumenter i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783477"
---
# <a name="asset-documents"></a>Aktivadokumenter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet beskriver aktivadokumenter i Aktivastyring.

I Aktivastyring kan du definere dokumenter slik at de automatisk er knyttet til jobbtyper, aktivaprodusenter, aktivatyper eller aktiva. Denne funksjonaliteten er nyttig når det utgis oppdaterte dokumentversjoner. I så fall må du bare plassere det oppdaterte dokumentet på standardstedet du bruker for Microsoft Dynamics 365 for Finance and Operations-dokumentene, og knytte dokumentet til aktivadokumentposten du har opprettet. Du får da tilgang til det oppdaterte dokumentet fra menyelementene **Alle aktiva**, **Aktive aktiva**, **Mine aktiva aktiva**, **Alle arbeidsordrer** og **Aktive arbeidsordrejobber**. Prosessen for å knytte dokumenter til en aktivadokumentpost bruker standardsystemet for dokumenthåndtering i Finance and Operations.

**Eksempel 1:** Et dokument som er relatert til en jobbtype, kan beskrive en fremgangsmåte for denne jobbtypen.

**Eksempel 2:** Et dokument som er knyttet til en kombinasjon av en aktivatype, -produsent og -modell, kan være standardhåndboken for den valgte aktivaleverandørmodellen.

## <a name="create-asset-document-relation"></a>Opprett relasjon til aktivadokument

1. Velg **Aktivastyring** \> **Oppsett** \> **Aktivadokumenter**.
2. Velg **Ny** for å opprette en aktivadokumentpost.
3. Avhengig av hvor spesifikk du ønsker dokumentrelasjonen skal være, kan du foreta relevante valg i ett eller flere av følgende felt: **Aktivatype**, **Produsent**, **Modell**, **Aktivum**, **Jobbtypekategori**, **Jobbtype**, **Jobbtypevariant** og **Jobbehov**. Alternativene som er tilgjengelige i feltene **Jobbtypevariant** og **Jobbehov**, avhenger av hva du velger i **Jobbtype**-feltet.

    > [!NOTE]
    > Når systemet søker etter dokumenter som skal knyttes til et aktivum eller en arbeidsordre, går Aktivastyring gjennom alle aktivadokumentposter for å se etter en mulig match. Den kontrollerer alltid den mest spesifikke kombinasjonen først. Med andre ord ser Aktivastyring først etter et treff i **Jobbehov**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Jobbtypevariant**-feltet. Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Jobbtype**-feltet, og så videre. Som du kan se i oppsettet av **Aktivadokumenter**-siden, betyr dette at for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff. Flere dokumenter kan være knyttet til et aktivum eller en arbeidsordre. Du kan redigere servicenivået i en vedlikeholdsanmodning eller en arbeidsordre etter behov.

4. Velg **Vedlegg**. Standardsiden for **Dokumenthåndtering** i Finance and Operations vises.
5. Definer dokumentene eller notatene som skal knyttes til aktivadokumentposten. Når du har tilknyttet dokumenter, viser **Vedlegg**-feltet antallet dokumenter som er knyttet til posten.