---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a885ba924137c56583db9f81b34db9a20f33bc4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569439"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]