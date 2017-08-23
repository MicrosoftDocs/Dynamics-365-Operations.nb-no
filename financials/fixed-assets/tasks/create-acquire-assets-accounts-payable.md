--- 
title: "Opprette og anskaffe anleggsmidler fra leverandører"
description: "Denne oppgaveveiledningen går gjennom oppretting og anskaffelse av et anleggsmiddel med innkjøpsprosessen."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Opprette og anskaffe anleggsmidler fra leverandører

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

