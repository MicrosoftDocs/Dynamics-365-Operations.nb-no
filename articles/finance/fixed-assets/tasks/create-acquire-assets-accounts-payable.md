---
title: Opprette og anskaffe anleggsmidler som opprettes fra kunder
description: Denne prosedyren går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.
author: moaamer
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4290ced6bcf4432583cffc9122a4bba86266a559
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713620"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Opprette og anskaffe anleggsmidler som opprettes fra kunder

[!include [banner](../../includes/banner.md)]

Denne prosedyren går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.  Den bruker regnskapsføreren og regnskapsassistenten og demonstrasjonsselskapet USMF.


## <a name="set-fixed-assets-parameters"></a>Angi parametere for anleggsmidler
1. I **navigasjonsruten** går du til **Moduler > Anleggsmidler > Oppsett > Parametere for anleggsmidler**.
2. Vis hurtigfanen **Bestillinger**.
3. Merk av for **Tillat anleggsmiddelanskaffelse fra innkjøp**.
4. Merk av for **Opprett anleggsmiddel under postering av produktkvittering eller faktura**.

## <a name="create-a-new-vendor-invoice"></a>Opprette en ny leverandørfaktura
1. I **navigasjonsruten** går du til **Moduler > Leverandører > Arbeidsområder > Leverandørfakturaregistrering**.
2. Klikk **Ny leverandørfaktura**.
3. Klikk rullegardinknappen i **Fakturakonto**-feltet for å åpne oppslaget.
4. Klikk koblingen i den valgte raden i listen.
5. Skriv inn en verdi i **Nummer**-feltet.
6. Angi en dato i **Posteringsdato**-feltet.
7. Klikk **Legg til linje**.
8. Klikk rullegardinknappen i **Varenummer**-feltet for å åpne oppslaget. Både varer som ikke er lagerført, og innkjøpskategorier kan brukes til anleggsmiddelanskaffelse.  
9. Klikk koblingen i den valgte raden i listen.
10. Angi et tall i **Antall**-feltet. Én fakturalinje oppretter bare ett anleggsmiddel, uavhengig av antallet. Verdien i feltet Fakturaantall overføres til antallet anleggsmidler.  
11. Angi et tall i **Enhetspris**-feltet.
12. Utvid hurtigfanen **Linjedetaljer**.
13. Klikk kategorien **Anleggsmidler**.
14. Merk av i avmerkingsboksen **Opprett et nytt anleggsmiddel**.
15. Klikk rullegardinknappen i feltet **Anleggsmiddelgruppe** for å åpne oppslaget.
16. I listen velger du anleggsmiddelgruppen som skal brukes til å opprette det nye anleggsmiddelet.
17. Klikk koblingen i den valgte raden i listen.
18. Klikk **Poster**. Anleggsmidlet opprettes og anskaffes når fakturaen posteres.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
