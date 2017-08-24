--- 
title: Velge definisjon av datamodell under oppretting av format for elektronisk rapportering (ER)
description: "For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren \"ER Opprette en konfigurasjonsleverandør og merke den som aktiv\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9820888a6ab0b3eafcd4d8c95982900b2719b2ec
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a>Velge definisjon av datamodell under oppretting av format for elektronisk rapportering (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv". 

Denne fremgangsmåten viser hvordan en modell rotelementet kan velges som en modell for datadefinisjon for å sette inn en elektronisk rapportering (ER)-formatkonfigurasjonen som er utformet for å generere elektroniske dokumenter. I denne prosedyren skal du legge til en ny ER-formatkonfigurasjon for eksempelfirmaet "Litware, Inc". 

Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle tilordnet. Trinnene kan fullføres ved hjelp av ethvert datasett.

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  
2. Klikk Rapporteringskonfigurasjoner.

## <a name="add-a-new-er-data-model-configuration"></a>Legg til en ny ER-datamodellkonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
    * Vi legger til en ny ER-modellkonfigurasjon som inneholder en datamodell som skal brukes som datakilde for generering av ER-rapporter.  
2. I Navn-feltet skriver du inn "Betalingingsmodell (fiktiv)".
    * Betalingsmodell (fiktiv)  
3. Klikk Opprett konfigurasjon.
4. Klikk Utforming.
    * Åpne ER-utforming for å angi strukturen for datamodellen av denne konfigurasjonen.  
    * Anta at vi utformer datamodellen for betalinger virksomheten domene til å støtte 2 betalingsmåter – Overfør kreditt og AvtaleGiro som.  
5. Klikk Ny for å åpne nedtrekksdialogen.
6. I Navn-feltet skriver du inn "Betalinger – Overfør kreditt".
    * Betalinger – Overfør kreditt  
7. Klikk Legg til.
8. Klikk Ny for å åpne nedtrekksdialogen.
9. I feltet Ny node som en for angir du Modellrot.
10. I Navn-feltet skriver du inn "Betalinger – avtalegiro".
    * Betalinger – direktedebet  
11. Klikk Legg til.
12. Klikk Lagre.
13. Lukk siden.
14. Klikk Endre status.
    * Fullfør utkastversjonen av modellen for å gjøre den tilgjengelig i nye modellen tilordningene og formater.  
15. Klikk Fullført.
16. Klikk OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Start for å angi en ny ER-formatkonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I feltet Ny angir du Format basert på datamodellen Betalingsmodell (fiktiv).
3. Angi eller velg en verdi i feltet Definisjon av datamodell.
    * Legg merke til at alle varer i roten av valgte datamodellen som er tilgjengelige som en modell datadefinisjon. Du kan fortsette å lage formatet ved å bruke noen av elementene som nødvendig roten av datamodellen. En manglende tilordning av modellen for valgte rotelementet hindre ikke deg i å fortsette.  
4. Lukk siden.

## <a name="add-a-new-er-model-mapping-configuration"></a>Legg til en ny ER-modelltilordningskonfigurasjon
1. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
2. I feltet Ny angir du Modeltilordning basert på datamodellen Betalingsmodell (fiktiv).
3. I Navn-feltet skriver du inn "Betalingingsmodelltilordninger (fiktive)".
    * Betalingsmodelltilordninger (fiktive)  
4. Angi eller velg en verdi i feltet Definisjon av datamodell.
5. Klikk Opprett konfigurasjon.

## <a name="design-er-model-mappings"></a>Utforme ER-modelltilordninger
1. Klikk Utforming.
    * Bruk ER designer til å angi modelltilordningene for de nødvendige rotelementene.  
2. Klikk Utforming.
    * Simuler innstillingen for den valgte modelltilordningen for rotelementet til den valgte modellen.  
3. I treet velger du Dynamics 365 for Operations\Tabellposter.
4. Klikk Legg til rot.
5. I Navn-feltet skriver du inn "Finans".
6. Skriv inn 'LedgerJournalTrans' i Tabell-feltet.
    * LedgerJournalTrans  
7. Klikk OK.
8. Klikk Lagre.
9. Lukk siden.
10. Lukk siden.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Start for å angi en annen ny ER-formatkonfigurasjon
1. Velg Betalingsmodell (fiktiv) i treet.
2. Klikk Opprett konfigurasjon for å åpne nedtrekksdialogen.
3. I feltet Ny angir du Format basert på datamodellen Betalingsmodell (fiktiv).
4. Angi eller velg en verdi i feltet Definisjon av datamodell.
    * Merk at nå er det bare ett rotelement som er tilgjengelig til å tilordne til datakildene til programmet. Når minst én modelltilordning er introdusert, kan bare modellens rotelementer som er tilordnet til programmets datakilder, velges som en modelldefinisjon når ER-formatet er lagt til.   
5. Lukk siden.


