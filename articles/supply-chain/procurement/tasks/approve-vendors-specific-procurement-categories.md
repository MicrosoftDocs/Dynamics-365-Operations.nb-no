---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204936"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Godkjenne leverandører for spesifikke innkjøpskategorier

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management. Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert. Denne fremgangsmåten viser hvordan du angir at en leverandør er godkjent eller foretrukket for en spesifikk innkjøpskategori. Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.

1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.
2. Velg leverandøren du vil angi som en godkjent eller foretrukket leverandør for en kategori.
3. Klikk på **Generelt** i handlingsruten.
4. Velg **Kategorier**.
5. Velg **Legg til kategori**.
6. I **Kategori**-feltet velger du **KONTOR- OG SKRIVEBORDSTILBEHØR (KONTOR- OG SKRIVEBORDSTILBEHØR)**.
7. I feltet **Status for leverandørkategori** velger du **Foretrukket**. Det er mulig å angi flere enn én foretrukket leverandør for en kategori.  
8. Velg **Lagre**.
9. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpskategorier**.
10. Velg **FIRMAINNKJØPSKATEGORIER\KONTOR- OG SKRIVEBORDSTILBEHØR i treet**.
11. Vis **Leverandør**-delen. Kontroller om leverandøren du har valgt, vises som en foretrukket leverandør for kategorien Kontor- og skrivebordtilbehør. Hvis du kjører denne fremgangsmåten som en oppgaveveiledning, må du kanskje klikke **Lås opp** for å kunne bla gjennom listen over leverandører.  Det er også mulig å legge til foretrukne og godkjente leverandører på denne siden.  
12. Vis **KONTOR- OG SKRIVEBORDSTILBEHØR** i treet, og velg **Saks**.
13. Velg **Nei** i feltet **Arv leverandører fra overordnet kategori**.
14. Velg **Ja** i feltet **Arv leverandører fra overordnet kategori**.

