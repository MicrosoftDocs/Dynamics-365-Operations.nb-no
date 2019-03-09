---
title: Opprette og anskaffe anleggsmidler som opprettes fra kunder
description: Denne oppgaveveiledningen går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "316424"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Opprette og anskaffe anleggsmidler som opprettes fra kunder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen.  Den bruker regnskapsføreren og regnskapsassistenten og demonstrasjonsselskapet USMF.


## <a name="set-fixed-assets-parameters"></a>Angi parametere for anleggsmidler
1. Gå til Anleggsmidler > Oppsett > Parametere for anleggsmidler.
2. Vis eller skjul delen Bestillinger.
3. Merk av for Tillat anleggsmiddelanskaffelse fra innkjøp.
4. Merk av for Opprett anleggsmiddel under postering av produktkvittering eller faktura.

## <a name="create-a-new-vendor-invoice"></a>Opprette en ny leverandørfaktura
1. Gå til Leverandører > Arbeidsområder > Leverandørfakturaregistrering.
2. Klikk Ny leverandørfaktura.
3. Klikk rullegardinknappen i Fakturakonto-feltet for å åpne oppslaget.
4. Klikk koblingen i den valgte raden i listen.
5. Skriv inn en verdi i Nummer-feltet.
6. Angi en dato i Posteringsdato-feltet.
7. Klikk Legg til linje.
8. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
    * Både varer som ikke er lagerført, og innkjøpskategorier kan brukes til anleggsmiddelanskaffelse.  
9. Klikk koblingen i den valgte raden i listen.
10. Angi et tall i feltet Antall.
    * Én fakturalinje oppretter bare ett anleggsmiddel, uavhengig av antallet.  Verdien i feltet Fakturaantall overføres til antallet anleggsmidler.  
11. Angi et tall i feltet Enhetspris.
12. Vis eller skjul Linjedetaljer-delen.
13. Klikk kategorien Anleggsmidler.
14. Merk av i avmerkingsboksen Opprett et nytt anleggsmiddel.
15. Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.
16. I listen velger du anleggsmiddelgruppen som skal brukes til å opprette det nye anleggsmiddelet.
17. Klikk koblingen i den valgte raden i listen.
18. Klikk Poster.
    * Anleggsmidlet opprettes og anskaffes når fakturaen posteres.  

