---
title: Lageropptelling på et lager
description: Denne artikkelen beskriver prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret.
author: yufeihuang
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c8712b88867dc4be48bbdb4b905993e3ccbc73f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870644"
---
# <a name="count-inventory-in-a-warehouse"></a>Lageropptelling på et lager

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver prosessen med å opprette og postere en lageropptellingsjournal for å telle en bestemt vare på en lokasjon i lageret. Fremgangsmåten gjelder for "grunnleggende lageraktiviteter"-funksjoner, tilgjengelige i lagerstyringsmodulen, ikke for lagerstyringsfunksjonaliteten som er tilgjengelig i lagerstyringsmodulen. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Hvis du bruker dine egne data, må du kontrollere at du har produkter og lokasjoner definert, og at du har opprettet et beholdningsjournalnavn for opptellingsjournaler. Beholdningsopptelling utføres vanligvis av en lageransatt.


## <a name="create-an-inventory-counting-journal"></a>Opprette en lageropptellingsjournal
1. Gå til **Navigasjonsrute > Moduler > Lagerstyring > Loggoppføringer > Vareopptelling > Opptelling**.
2. Velg **Ny**.
3. I **Navn**-feltet velger du navnet på lageropptellingsjournalen du vil bruke, fra rullegardinlisten. Noen andre felt fylles ut basert på oppsettet av standardnavn for lageropptellingsjournal som du velger.  
4. Klikk på rullegardinknappen i feltet **Arbeider** for å åpne oppslaget.
5. **Velg** arbeideren du vil bruke, i listen.
6. Velg **OK**.

## <a name="create-journal-lines"></a>Opprette journallinjer
1. Velg **Ny**.
2. Velg det ønskede oppslaget fra rullegardinlisten i **Varenummer**-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, velger du **A0001**.  
3. Velg det ønskede oppslaget fra rullegardinlisten i **Område**-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, velger du område **2**.
4. Velg det ønskede oppslaget fra rullegardinlisten i **Lager**-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lager **24**.  
5. Velg det ønskede oppslaget fra rullegardinlisten i **Sted**-feltet. Hvis du bruker demonstrasjonsdataselskapet USMF, velger du lokasjon **BULK-001**.  
6. Angi et tall i feltet Opptelt. Hvis du angir et opptelt nummer som er forskjellig fra nummeret som vises i feltet **Beholdning**, oppdateres feltet **Antall** for å vise avviket.  
7. Velg **Lagre**.

## <a name="post-the-inventory-counting-journal"></a>Postere lageropptellingsjournalen
1. Velg **Poster**. Når du posterer en lageropptellingsjournal, og hvis det opptelte beløpet er forskjellig fra beløpet som rapporteres i feltet **Beholdning**, blir det postert et lagermottak eller en lageravgang, lagernivå og lagerverdi endres og finanstransaksjoner blir generert.
2. Velg **OK**.

## <a name="view-inventory-transactions"></a>Vis lagertransaksjoner
1. Velg **Lager**.
2. Velg **Transaksjoner**. Her kan du se relaterte transaksjoner som opprettes når du posterer lageropptellingsjournalen.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]