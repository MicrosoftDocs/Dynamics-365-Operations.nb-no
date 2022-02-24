---
title: Gå gjennom konfigurasjoner for å generere rapporter i Office-format som inneholder innebygde bilder
description: 'For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 1: Definere parametere)".'
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c41ff1ba99411b97ea2b5d9f31bdee7c7701315
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684361"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Gå gjennom konfigurasjoner for å generere rapporter i Office-format som inneholder innebygde bilder

[!include [banner](../../includes/banner.md)]

For å fullføre disse trinnene, må du først fullføre trinnene i oppgaveveiledningen "ER lage rapporter i MS Office-formater med innebygde bilder (del 1: Definere parametere)".

Denne fremgangsmåten viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere elektroniske dokumenter som inneholder innebygde bilder i Microsoft Excel og Microsoft Word. I dette eksemplet skal du gå gjennom ER-konfigurasjoner for eksempelfirmaet "Litware, Inc". 

Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet. Trinnene kan fullføres ved hjelp av USMF-datasett.


## <a name="review-the-imported-data-model"></a>Gå gjennom den importerte datamodellen
1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Velg Modell for sjekker i treet.
3. Klikk Utforming.
    * Denne modellen er utviklet for å representere sjekker for betaling med tanke på bedrifter og tilordning av denne modellen til programmets datakilder. Se gjennom denne modellen som operasjoner ER utformingen. Legg merke til attributtene for modellelementene presenteres: strukturen, navn, beskrivelse, datatypen og så videre.   
4. Utvid 'root' i treet.
5. Velg 'rot\sjekker' i treet.
6. Utvid 'rot\sjekker' i treet.
7. Utvid 'rot\sjekker\attributter' i treet.
8. Utvid 'rot\betaler' i treet.
9. Velg 'rot\istestrun' i treet.
10. Velg 'rot\oppsett' i treet.
    * I oppsettet av elementene i denne modellen representerer informasjon om utskrift sjekk skjemaoppsettet for den valgte bankkontoen. Det inneholder også to noder av typen beholder for lagring av bilder.   
11. Utvid 'rot\oppsett' i treet.
12. Velg 'rot\oppsett\firmalogo' i treet.
13. Utvid 'rot\oppsett\firmalogo' i treet.
14. Velg 'rot\oppsett\firmalogo\bilde' i treet.
15. Velg 'rot\oppsett\firmalogo\isprinted' i treet.
16. Velg 'rot\oppsett\signatur' i treet.
17. Utvid 'rot\oppsett\signatur' i treet.
18. Velg 'rot\oppsett\signatur\bilde' i treet.
19. Velg 'rot\oppsett\signatur\isprinted' i treet.
    * Legg merke til at to bilde dataelementer er bundet til feltene i tabellene som inneholder bilder av firmalogoen og godkjente personens signatur i binært format.  
20. Utvid 'rot\oppsett\vannmerke' i treet.
21. Klikk Tilordne modell til datakilde.
22. Klikk Utforming.
23. Utvid 'chequesselected' i treet.
24. Utvid "oppsett" i treet.
25. Utvid 'oppsett\firmalogo' i treet.
26. Utvid "oppsett\signatur" i treet.
27. Utvid 'oppsett\vannmerke' i treet.
28. Aktiver Vis detaljer.
    * Legg merke til at modellelementet sjekker data er bundet til tabellen for TmpChequePrintout som under kjøringen inneholder poster for sjekker som brukeren har valgt for utskrift.   
29. Lukk siden.
30. Lukk siden.
31. Lukk siden.

## <a name="review-the-imported-format"></a>Gå gjennom det importerte formatet
1. Utvid Modell for sjekker i treet.
2. Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.
3. Klikk Utforming.
4. Klikk Vedlegg.
5. Klikk Åpne.
    * Åpne den vedlagte rapportmalen i Excel.  
    * Se gjennom vedlagte rapportens Excel-malen som skal brukes til å skrive ut sjekker. Malen inneholder to sjekker per side, og er utformet for å skrive ut sjekker til det fortrykte skjemaet. Legg merke til at to tomme bilder bygges. Disse tomme bildene er for firmalogoen og signaturen til personen som godkjenner en betaling. Kontroller at bildene kalles CompLogo og SignatureImage, henholdsvis i Excel.   
6. Lukk siden.
7. Utvid 'Report' i treet.
8. Utvid 'Rapport\ChequeLines' i treet.
9. Velg 'Rapport\ChequeLines\CompLogo' i treet.
10. Aktiver Vis detaljer.
    * Legg merke til at formatet "CompLogo" celleobjekt representerer Excel varen som skal brukes til å fylle ut bildet for bedriftslogo i rapporten. Dette formatet elementet bundet bilde data modellelement som inneholder et bilde for bedriftslogo i binært format under kjøringen.   
11. Klikk kategorien Tilordning.
12. Klikk på Redigering aktivert.
    * Vær oppmerksom på at du kan gjøre celleobjekt formatet "CompLogo" slik at den ikke lenger er aktivert. I dette tilfellet skjuler det tilknyttede elementet for Excel-bildet en firmalogo i den genererte rapporten. Hvis aktivert uttrykket returnerer SANN, og den definerte bindingen gir ikke noe bilde, viser det tilknyttede elementet for Excel-bilde et bilde som er lagret i Excel-malen.   
13. Lukk siden.
14. Utvid 'labels: Container' i treet.
    * Enkelte etiketter vises i skjemaet forhåndstrykt sjekk inkluderes i rapporten når den opprettes for testformål. Imidlertid skrives disse ikke ut ved reell utskrift, fordi det forhåndstrykte skjemaet allerede inneholder dem.  
15. Lukk siden.

