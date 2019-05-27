---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566439"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Godkjenne leverandører for spesifikke innkjøpskategorier

[!include [task guide banner](../../includes/task-guide-banner.md)]

Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert. Denne fremgangsmåten viser hvordan du angir at en leverandør er godkjent eller foretrukket for en spesifikk innkjøpskategori. Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.

1. Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.
2. Velg leverandøren du vil angi som en godkjent eller foretrukket leverandør for en kategori.
3. Klikk Generelt i handlingsruten.
4. Klikk Kategorier.
5. Klikk Legg til kategori.
6. I Kategori-feltet velger du KONTOR- OG SKRIVEBORDSTILBEHØR (KONTOR- OG SKRIVEBORDSTILBEHØR).
7. I feltet Status for leverandørkategori velger du Foretrukket.
    * Det er mulig å angi flere enn én foretrukket leverandør for en kategori.  
8. Klikk Lagre.
9. Gå til Innkjøp og leverandører > Innkjøpskategorier.
10. Velg FIRMAINNKJØPSKATEGORIER\KONTOR- OG SKRIVEBORDSTILBEHØR i treet.
11. Vis Leverandør-delen.
    * Kontroller om leverandøren du har valgt, vises som en foretrukket leverandør for kategorien Kontor- og skrivebordtilbehør. Hvis du kjører denne fremgangsmåten som en oppgaveveiledning, må du kanskje klikka Lås opp for å kunne bla gjennom listen over leverandører.  Det er også mulig å legge til foretrukne og godkjente leverandører på denne siden.  
12. Vis KONTOR- OG SKRIVEBORDSTILBEHØR i treet.
13. Velg Sakser i treet .
14. Velg Nei i feltet Arv leverandører fra overordnet kategori.
15. Velg Ja i feltet Arv leverandører fra overordnet kategori.

