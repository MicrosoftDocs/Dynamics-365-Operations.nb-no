---
title: "Arbeidsområde for anleggsmiddelbehandling"
description: "Dette emnet gir informasjon om arbeidsområdet Anleggsmiddelbehandling. Arbeidsområdet viser informasjon som er knyttet til anleggsmidler som er angitt i systemet. Det omfatter visning av et sammendrag og en visning for analyse."
author: saraschi
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c544ae60433dd14d061bc1a78d5cad6577cf579d
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-management-workspace"></a>Arbeidsområde for anleggsmiddelbehandling

[!include[banner](../includes/banner.md)]

Arbeidsområdet **Anleggsmiddelbehandling** viser informasjon som er knyttet til anleggsmidler som er angitt i systemet. Arbeidsområdet inneholder en sammendrag-visning og en analysevisning. Kategorien **Mitt arbeid** viser sammendragsfliser, anleggsmiddeldetaljer og relatert informasjon om anleggsmidler i det gjeldende firmaet. Du kan også legge til analyse i analysedeen av Power BI, direkte i arbeidsområdet. Kategorien **Analytics – alle firmaer** bruker funksjoner i Microsoft Power BI for å vise bilder som er knyttet til anleggsmidler i alle firmaer.

## <a name="my-work"></a>Mitt arbeid

### <a name="summary"></a>Sammendrag

FLisene i **sammendrag**-avsnittet gir en oversikt over anleggsmidlene. Informasjonen inkluderer metrikk om aktiva som ennå ikke er anskaffet, aktiva som er anskaffet i løpet av inneværende år og aktiva som er solgt i løpet av inneværende år. **Sammendrag**-delen har også rask navigering til listesiden **Anleggsmiddel**, satsvis avskrivningsforslag og anleggsmiddeljournalen.

### <a name="find-fixed-assets"></a>Søk etter anleggsmidler

Med **Søk etter anleggsmidler**-delen kan du raskt søke etter aktiva ved å angi anleggsmiddelnummer, gruppe, navn, plassering eller personen som er ansvarlig. Alle anleggsmidler som oppfyller søkekriteriene, vises i listen.

Du kan vise disse sidene fra listen:

 - **Detaljer**-siden for anleggsmidlet
 - **Tablåer**-siden for alle tablåer som er tilknyttet anleggsmidlet
 - Siden **Verdivurdering av anleggsmidler**

### <a name="valuations"></a>Vurderinger

På siden **Verdivurderinger av anleggsmidler** kan du se den viktigste informasjonen om et anleggsmiddel, på én side, og også detaljer for alle tablåer som er knyttet til anleggsmidlet. **Saldoer**-alternativet øverst til venstre på siden viser gjeldende verdivurdering for hvert tablå som er knyttet til anleggsmidlet. Du kan gå tilbake fra verdiene for å vise de detaljerte transaksjonene som utgjør sammendragsverdien. **Profil**-alternativet øverst til venstre på siden viser avskrivningsplan for hvert tablå som er knyttet til anleggsmidlet.

Du får tilgang til **Verdivurdering av anleggsmidler**-siden fra arbeidsområdet **Anleggsmiddelbehandling** eller listesiden **Anleggsmiddel**.

### <a name="related-information"></a>Beslektet informasjon

Du kan navigere direkte til **Tablåoppsett**-siden, siden for **Forespørsel om anleggsmiddeltransaksjon**, og flere rapporter ved hjelp av koblingene i **relatert informasjon**-delen i arbeidsområdet.

### <a name="analytics--all-companies"></a>Analyse – alle firmaer

**Analyse**-siden inneholder viktig metrikk om anleggsmidler i alle juridiske enheter i systemet. Tilgang til denne kategorien styres av sikkerhetsrettigheten Vis analyse for anleggsmiddel for alle firmaer.

Tabellen nedenfor viser visuaiseringene som er tilgjengelig på hver rapportside.

| Rapportside            | Visualisering        |
|------------------------|----------------------|
| Verdivurdering av anleggsmidler | Total netto bokført verdi |
| Verdivurdering av anleggsmidler | Netto bokført veri etter anleggsmiddelgruppe |
| Verdivurdering av anleggsmidler | Anskaffelsesverdier |
| Verdivurdering av anleggsmidler | Avhendingsverdier |
| Verdivurdering av anleggsmidler | Anleggsmiddeldetaljer |
| Vurderingskart        | Total netto bokført verdi |
| Vurderingskart        | Anleggsmiddelplasseringer |
| Vurderingskart        | Anleggsmiddeldetaljer |

Hvis du vil vise analyse med data, må du først fornye AssetTransactionMeasure samlet målene på siden **Enhetslager**.

