---
title: Definere verdimodeller
description: Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727068"
---
# <a name="set-up-value-models"></a>Definere verdimodeller

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe.

## <a name="create-a-book"></a>Opprette et tablå
1. Gå til **Anleggsmidler \> Oppsett \> Tablåer**.
2. Velg **Ny**.
3. Angi en verdi i feltet **Tablå**.
4. Angi en verdi i feltet **Beskrivelse**.
5. Sett alternativet **Beregn avskrivning** til **Ja**.

    Hvis **Beregn avskrivning** er satt til **Ja**, så vil det tilknyttede anleggsmiddeltablået inkluderes i avskrivningsforslag. Hvis det er satt til **Nei**, vil anleggsmiddeltablået ikke automatisk avskrives.

6. Angi eller velg en verdi i feltet **Avskrivningsprofil**.

    * En alternativ avskrivningsprofil er også kjent som en avskrivningsmetode for avskrivning. Avskrivningsforslaget vil bytte til denne profilen når den alternative profilen beregner et avskrivningsbeløp som er lik eller større enn standard avskrivningsprofil.
    * Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter. Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.
    * Hvis du velger **Opprett avskrivningsjusteringer med basisjusteringer**, opprettes avskrivningsjusteringer automatisk når verdien til anleggsmidlet blir oppdatert. Ellers vil den oppdaterte anleggsmiddelverdien bare påvirke fremtidige avskrivningsberegninger.

7. Sett alternativet **Opprett avskrivningsjusteringer med basisjusteringer** til **Ja**.

    * Som standard posteres anleggsmiddeltablåtransaksjoner til økonomimodulen. Du kan imidlertid deaktivere postering i økonomimodulen for tablået ved å sette alternativet **Poster i økonomimodul** til **Nei**. Tablåer som ikke posteres i økonomimodulen, brukes vanligvis for mva-rapportering. Dette alternativet gir deg mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået, fordi transaksjonene ikke er lagret i økonomimodulen.
    * Som standard er feltet **Posteringslag** satt til **Gjeldende lag** hvis tablået posterer til økonomimodulen og **Ingen** hvis tablået ikke posteres til økonomimodulen. Oppdater verdien for **Posteringslag**-feltet hvis transaksjoner for dette tablået skal posteres til et annet lag.

8. Beregn positiv avskrivning.

    * Som standard er **Beregn positiv avskrivning**-alternativet satt til **Nei**. Denne innstillingen angir at avskrivningen vil kreditere det valgte anleggsmiddeltablået. I tillegg er både alternativer for **Tillat netto bokført verdi høyere enn anskaffelsesprisen** og **Tillat negativ netto bokført verdi** angitt til **Nei**, og innstillingene kan endres uavhengig. 
    * For å beregne positiv avskrivning setter du alternativet **Beregn positiv avskrivning** til **Ja**. Denne innstillingen angir at avskrivningen vil debitere anleggsmiddeltablået. Når alternativet **Beregn positiv avskrivning** er satt til **Ja**, vil alternativene **Tillat netto bokført verdi høyere enn anskaffelsesprisen** og **Tillat negativ netto bokført verdi** automatisk settes til **Ja**, og de vil bli låst. Denne låsen hjelper til med å sikre at positiv avskrivning bare blir brukt på anleggsmidler som ble anskaffet med negativ bokført verdi (kredit). 

10. Angi eller velg en verdi i **Kalender**-feltet.

    Avledede tablåer vil postere transaksjoner til forskjellige tablåer samtidig. Du oppretter transaksjonene med det primære tablået og under posteringen posteres en nøyaktig kopi av transaksjonen til det avledede tablået. Det er ingen omberegning med avledede tablåtransaksjoner, og må derfor ikke brukes for avskrivningstransaksjoner.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knytte tablået til en anleggsmiddelgruppe

1. Velg **Anleggsmiddelgrupper**.
2. Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**.
3. Angi et tall i **Levetid**-feltet.

    * Avskrivningsperioder beregnes etter at levetiden til aktivumet er angitt.
    * Avskrivningskonvensjonen kan angis etter behov for skatte-og avgiftsformål.
    * For anleggsmidler som er knyttet til utleie, vil verdien i **Levetid**-feltet overstyres av det som er minst av utleieperioden i anleggsmiddeltablået og anleggsmidlets levetid. Hvis alternativet **Overføring av eierskap** er satt til **Ja** for leieboken, blir verdien i **Levetid**-feltet alltid levetiden til aktivumet.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
