---
title: Sammenslåing av anleggsmidler, verdimodeller og avskrivningstablåer
description: 'I tidligere versjoner var det to vurderingskonsepter for anleggsmidler: verdimodeller og avskrivningstablåer. I versjonen Microsoft Dynamics 365 for Operations (1611) er verdimodellfunksjonaliteten og funksjonaliteten for avskrivningstablå slått sammen til ett enkelt konsept som kalles et tablå.'
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f4f06b7916fb2eeed802b2dce95edfce448dcd97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880852"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Sammenslåing av anleggsmidler, verdimodeller og avskrivningstablåer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver den gjeldende tablåfunksjonaliteten i Anleggsmidler. Denne funksjonen er basert på verdimodellfunksjonalitet som var tilgjengelig i tidligere versjoner, men inneholder også all funksjonalitet som tidligere ble angitt i avskrivningstablåer.

Med tablåfunksjonalitet kan du bruke ett enkelt sett med sider, forespørsler og rapporter for alle organisasjonens anleggsmiddelprosesser. Tabellen i denne artikkelen beskriver den tidligere funksjonaliteten for avskrivningstablåer og verdimodeller, sammen med den gjeldende funksjonaliteten for tablåer.

## <a name="setup"></a>Installasjon
Som standard posterer tablåer både i økonomimodulen (Finans) og underfinansjournalen for anleggsmiddel. Tablåer har et nytt alternativ, **Poster i økonomimodul**, som lar deg deaktivere postering i økonomimodulen og postere bare til underfinansjournal for anleggsmiddel. Denne funksjonen ligner tidligere posteringsvirkemåte for avskrivningstablåer. Journalnavnoppsettet har et nytt posteringslag som heter Ingen. Dette posteringslaget ble lagt til spesifikt for anleggsmiddeltransaksjoner. Hvis du vil postere transaksjoner for tablåer som ikke poster til økonomimodulen, må du bruke et journalnavn med posteringslaget satt til **Ingen**.


| &nbsp;                                           | Avskrivningstablå               | Verdimodell                     | Tablå (ny)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Postere til økonomimodulen                                   | Aldri                           | Alltid                          | Alternativ for å postere til økonomimodulen                                |
| Posteringslag                                   | Gjelder ikke                  | 3. Gjeldende, Operasjoner og Mva | 11: Gjeldende, Operasjoner, Mva, 7 egendefinerte lag og Ingen |
| Journalnavn                                    | Journalnavn for avskrivningstablå | Økonomimodul – journalnavn              | Økonomimodul – journalnavn                                      |
| Avledede tablåer                                    | Ikke tillatt                     | Tillatt                         | Tillatt                                                 |
| Avskrivningsprofiloverstyring på anleggsmiddelnivået | Tillatt                         | Ikke tillatt                     | Tillatt                                                 |

## <a name="processes"></a>Prosesser
Prosesser bruker nå en felles side. Noen prosesser tillates bare hvis alternativet **Poster til økonomimodul** er satt til **Ingen** i tablåoppsettet.

| &nbsp;                                           | Avskrivningstablå               | Verdimodell                     | Tablå (ny)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Transaksjonsoppføring              | Journal for avskrivningstablå | Anleggsmiddeljournal | Anleggsmiddeljournal                      |
| Bonusavskrivning             | Tillatt                   | Ikke tillatt         | Tillatt                                  |
| Slett historiske transaksjoner | Tillatt                   | Ikke tillatt         | Tillatt, med mindre du legger til i økonomimodulen |
| Masseoppdatering                    | Tillatt                   | Ikke tillatt         | Tillatt, med mindre du legger til i økonomimodulen |

## <a name="inquiries-and-reports"></a>Forespørsler og rapporter
Forespørsler og rapporter støtter alle tablåer. Rapporter som ikke finnes i tabellen nedenfor støttet tidligere både avskrivningstablåer for verdimodeller, og fortsetter å støtte alle tablåtyper. **Posteringslag**-feltet er også lagt til i rapporter, slik at du lettere kan gjenkjenne transaksjonsposteringene.

| &nbsp;                                           | Avskrivningstablå               | Verdimodell                     | Tablå (ny)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Forespørsler                             | Avskrivningstablåtransaksjoner | Anleggsmiddeltransaksjoner | Anleggsmiddeltransaksjoner |
| Anleggsmiddelutdrag                 | Ikke tillatt                    | Tillatt                  | Tillatt                  |
| Anleggsmiddelbasis                     | Tillatt                        | Ikke tillatt              | Tillatt                  |
| Relevans av anleggsmidler i midten av kvartalet | Tillatt                        | Ikke tillatt              | Tillatt                  |

## <a name="upgrade"></a>Oppgrader
Oppgraderingsprosessen flytter eksisterende oppsett og alle eksisterende transaksjoner til den nye tablåstrukturen. Verdimodeller forblir slik de er for øyeblikket, som et tablå som posterer til økonomimodulen. Avskrivningstablåer flyttes imidlertid til et tablå bok med alternativet **Poster til økonomimodul** satt til **Ingen**. Journalnavn for avskrivningstablå flyttes til et journalnavn for økonomimodul med posteringslaget satt til **Ingen**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
