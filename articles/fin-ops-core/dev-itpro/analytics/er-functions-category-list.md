---
title: Liste over ER-funksjoner i listekategorien
description: Dette emnet inneholder informasjon om listefunksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9adc8c40926864ab86421a38c3a135d837391b40
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749471"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Liste over ER-funksjoner i listekategorien

[!include [banner](../includes/banner.md)]

Listefunksjoner for elektronisk rapportering (ER) kan brukes til å trekke ut informasjon fra, og utføre operasjoner på, datakilder for datatypene *Postliste* *og Container (post)*. Dette emnet inneholder et sammendrag av disse funksjonene.

## <a name="list-of-supported-functions"></a>Liste over funksjoner som støttes

| Funksjon | Beskrivelse |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Denne funksjonen kjøres som et minneinternt valg. Den returnerer en ny *Postliste*-verdi som er flatet ut, og består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Denne funksjonen kjøres som en koblet SQL-spørring. Den returnerer en ny *Postliste*-verdi som er flatet ut, og består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen. |
| [Antall](er-functions-list-count.md)                       | Denne funksjonen returnerer en *Heltall*-verdi som representerer antall poster i den angitte listen, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funksjonen **0** (null). |
| [EmptyList](er-functions-list-emptylist.md)               | Denne funksjonen returnerer en tom *Postliste*-verdi ved hjelp av den angitte listen som en kilde for listestrukturen.|
| [Opplisting](er-functions-list-enumerate.md)               | Denne funksjonen returnerer en ny *Postliste*-verdi som består av opplistede poster i den angitte listen. |
| [Filter](er-functions-list-filter.md)                     | Denne funksjonen returnerer den angitte listen som en *Postliste*-verdi etter at spørringen er endret, slik at den filtrerer etter den angitte betingelsen. |
| [Fornavn](er-functions-list-first.md)                       | Denne funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne listen ikke er tom. Hvis listen er tom, genererer denne funksjonen et unntak. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Denne funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne posten ikke er tom. Hvis posten er tom, returnerer denne funksjonen en nullverdi for *Container (post)*. |
| [Index](er-functions-list-index.md)                       | Denne funksjonen returnerer en *Container (post)*-verdi som er valgt ved hjelp av den angitte numeriske indeksen i den angitte listen. Det oppstår et unntak hvis indeksen er utenfor området til postene i den angitte listen. |
| [IsEmpty](er-functions-list-isempty.md)                   | Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis den angitte listen ikke inneholder noen poster. Hvis ikke returneres den *boolske* verdien **USANN**. |
| [Liste](er-functions-list-list.md)                         | Denne funksjonen returnerer en *Postliste*-verdi som består av en ny liste som er opprettet fra de angitte argumentene.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Denne funksjonen beregner det angitte uttrykket som en velger for hver post i den angitte listen. Den returnerer en ny *Postliste*-verdi som inneholder én enkelt post for hver unike velgerverdi.|
| [ListJoin](er-functions-list-listjoin.md)                 | Denne funksjonen returnerer en *Postliste*-verdi som representerer en ny sammenkoblet liste som er opprettet fra de angitte argumentene.|
| [ListOfFields](er-functions-list-listoffields.md)         | Denne funksjonen returnerer en *postliste*-verdi som opprettes basert på strukturen til det angitte argumentet for typen *Opplisting* eller *Container (post)*. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Denne funksjonen returnerer en *Postliste*-verdi som består av bare den første posten i den angitte listen.|
| [OrderBy](er-functions-list-orderby.md)                   | Denne funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er sortert i henhold til de angitte argumentene. Disse argumentene kan defineres som uttrykk. |
| [Tilbakefør](er-functions-list-reverse.md)                   | Denne funksjonen returnerer den angitte listen som en *postliste*-verdi i reversert sorteringsrekkefølge. |
| [Del](er-functions-list-split.md)                       | Denne funksjonen deler den angitte inndatastrengen inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi. |
| [SplitList](er-functions-list-splitlist.md)               | Denne funksjonen deler den angitte listen i underlister (eller grupper), der hver inneholder det angitte antallet poster. Deretter returneres resultatet som en ny *postliste*-verdi som består av partiene. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Denne funksjonen deler den angitte listen inn i en ny liste over underlister (grupper). Antall poster i hvert parti beregnes dynamisk. Denne funksjonen returneres resultatet som en ny *postliste*-verdi som består av partiene. |
| [StringJoin](er-functions-list-stringjoin.md)             | Denne funksjonen returnerer en *streng*-verdi som består av sammenkoblede verdier for det angitte feltet fra den angitte listen. Verdiene kan skilles med det angitte skilletegnet. |
| [Hvor](er-functions-list-where.md)                       | Denne funksjonen returnerer den angitte listen som en *postliste*-verdi etter at den er filtrert i henhold til den angitte betingelsen. |

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelspråk i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]