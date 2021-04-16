---
title: Foreslå anleggsmiddelanskaffelser
description: Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817177"
---
# <a name="propose-fixed-asset-acquisitions"></a>Foreslå anleggsmiddelanskaffelser

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen. Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF. Hvis du vil anskaffe et anleggsmiddel via en journal for forslag til anleggsmidler, må du først opprette anleggsmiddelposten og deretter definere anskaffelsesprisen i anleggsmiddelboken.

## <a name="create-an-asset-acquisition-proposal"></a>Opprette et forslag om anskaffelse av aktiva

Fullfør fremgangsmåten nedenfor for å opprette et forslag om anskaffelse av aktiva. 

1. I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.
2. Velg **Ny**.
3. Angi eller velg en verdi i **Navn**-feltet.
4. Velg **Linjer** i handlingsruten.
5. Velg **Forslag**.
6. Velg **Anskaffelsesforslag**.
7. Velg **Filter**. Velg **Tilbakestill** for å fjerne tidligere verdier.
8. Velg raden **Anleggsmidlets** nummer.
9. Angi eller velg en verdi i **Kriterier**-feltet. Angi de gjenværende vilkårene for anleggsmidlene du vil anskaffe med dette forslaget.  
10. Velg **OK** to ganger for å gå ut av ruten.
- Kontroller at transaksjonslinjene er opprettet.  
- Bare anleggsmidler med anskaffelsesdato og anskaffelsespris som er angitt i tablået, inkluderes i anskaffelsesforslaget.  
11. Velg kategorien **Tablåer** på siden.
12. Velg **Poster**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Ta med standard finansdimensjoner i et anskaffelsesforslag.

Anskaffelsestransaksjonen kan opprettes ved hjelp av Excel-tillegg ved å gå til **Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**. Opprett en ny journal, gå til **Linjer**-delen på siden, velg Excel-ikonet og velg deretter en anleggsmiddeljournallinje. Systemet oppretter og åpner en Excel-mal som representerer journallinjer. Du kan legge til data for journallinjene du legger til i malen, og deretter publisere informasjonen tilbake i systemet. 

Hvis det er definert standarddimensjoner for det valgte anleggsmiddelboken og tilsvarende anleggsmidler som ble angitt i Excel-malen, blir de standard finansdimensjonene kalt fra hoveddataene for anleggsmiddelboken når journalen publiseres fra Excel til systemet. Hvis du vil inkludere finansdimensjoner i et anleggsmiddelbok automatisk mens du publiserer anleggsmiddeljournalen fra Excel-tillegget, må standarddimensjonene defineres på forhånd.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
