---
title: Definere verdimodeller
description: Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe.
author: moaamer
ms.date: 08/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c26e5fad3c5c60d87c2fea2b29043c69b82b5d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344664"
---
# <a name="set-up-value-models"></a>Definere verdimodeller

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]


Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe. Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.

## <a name="create-a-book"></a>Opprette et tablå
1. Gå til Anleggsmidler > Oppsett > Tablåer.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Tablå.
4. Skriv inn en verdi i feltet Beskrivelse.
    * Hvis Beregn avskrivning er valgt, inkluderes det tilknyttede anleggsmiddeltablået i avskrivningsforslag. Hvis det ikke er valgt, vil anleggsmiddeltablået ikke automatisk avskrives.  
5. Velg Ja i feltet Beregn avskrivning.
6. Angi eller velg en verdi i feltet Avskrivningsprofil.
    * En alternativ avskrivningsprofil er også kjent som en avskrivningsmetode for avskrivning. Avskrivningsforslaget vil bytte til denne profilen når den alternative profilen beregner et avskrivningsbeløp som er lik eller større enn standard avskrivningsprofil.  
    * Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter. Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.  
    * Hvis Opprett avskrivningsjusteringer med basisjusteringer er valgt, opprettes avskrivningsjusteringer automatisk når verdien til anleggsmidlet blir oppdatert. Hvis det ikke er valgt, påvirker den oppdaterte anleggsmiddelverdien bare avskrivningsberegninger fremover.  
7. Velg Ja i feltet Opprett avskrivningsjusteringer med basisjusteringer.
    * Som standard posteres anleggsmiddeltablåtransaksjoner til økonomimodulen. Du kan deaktivere postering i Finans for tablået ved å sette Poster i økonomimodul til Nei. Tablåer som ikke posteres i Finans brukes vanligvis for mva-rapporteringsformål. Dette gir deg mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået fordi de ikke er lagret i Finans.  
    * Posteringslaget er som standard det gjeldende laget hvis tablået posterer til Finans, og Ingen hvis det ikke bokføres i økonomimodulen. Oppdater posteringslaget hvis du må postere transaksjoner for dette tablået til et annet lag.  
8. Angi eller velg en verdi i Kalender-feltet.
    * Avledede tablåer vil postere transaksjoner til forskjellige tablåer samtidig. Du oppretter transaksjonene med det primære tablået og under posteringen posteres en nøyaktig kopi av transaksjonen til det avledede tablået. Det er ingen omberegning med avledede tablåtransaksjoner, og må derfor ikke brukes for avskrivningstransaksjoner.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knytte tablået til en anleggsmiddelgruppe
1. Klikk Anleggsmiddelgrupper.
2. Angi eller velg en verdi i feltet Anleggsmiddelgruppe.
3. Angi et tall i Levetid-feltet.

  - Avskrivningsperioder beregnes etter at levetiden til aktivumet er angitt.  
  - Avskrivningskonvensjonen kan angis etter behov for skatte-og avgiftsformål.
  - For anleggsmidler som er knyttet til utleie, vil verdien i **Levetid**-feltet overstyres av det som er minst av utleieperioden i anleggsmiddeltablået eller anleggsmidlets levetid. Hvis feltet **Overføring av eierskap** er satt til **Ja** for leieboken, blir verdien i **Levetid**-feltet alltid levetiden til aktivumet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
