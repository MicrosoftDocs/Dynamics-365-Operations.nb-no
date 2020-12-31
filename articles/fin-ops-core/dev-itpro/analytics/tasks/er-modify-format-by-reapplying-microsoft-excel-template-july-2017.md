---
title: Endre formater ved å bruke Excel-maler på nytt
description: For å fullføre trinnene i denne prosedyren må du først fullføre trinnene i prosedyren "ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format".
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: c5b1bc5f227a0944c513dee2c12a5042decde872
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684241"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Endre formater ved å bruke Excel-maler på nytt

[!include [banner](../../includes/banner.md)]

For å fullføre trinnene i denne prosedyren må du først fullføre trinnene i prosedyren "ER Utforme en konfigurasjon for generering av rapporter i OPENXML-format".

Denne fremgangsmåten beskriver hvordan du endrer en elektronisk rapportering (ER)-formatkonfigurasjonen ved å utføre en Microsoft Excel-mal som er endret. I denne prosedyren må du importere en endret Excel-mal til ER formatet konfigurasjonene som er opprettet for eksempel firmaer, Litware, Inc, og deretter generere elektroniske dokumenter. Denne fremgangsmåten er ment for brukere som har den systemansvarlige eller elektronisk rapportering utvikler-rolle. Disse trinnene kan fullføres ved hjelp av GBSI-datasettet. Før du begynner, last ned og lagre filen, SampleVendPaymWsReport2.xlsx, som er oppført i Hjelpemnet. Modifiser elektronisk rapporteringsformat ved å gjenta en Excel-mal (modify-electronic-reporting-format-reapply-excel-template/).

1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.
    * Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".  

## <a name="select-the-er-format"></a>Velg ER-formatet
1. Klikk Rapporteringskonfigurasjoner.
2. Utvid Betalingsmodell i treet.
3. Velg Betalingsmodell\Regnearkeksempelrapport i treet.
4. Klikk Vedlegg.
    * Legg merke til at SampleVendPaymWsReport.xlsx Excel-filen blir brukt som en mal for betalingsbehandling for journalen.   
5. Klikk Åpne.
    * Klikk Åpne for å utforske oppsettet for Excel-malen.  
    * Gå gjennom malen. Legg merke til at den for øyeblikket inneholder følgende detaljer for hver betalingslinje: leverandørens kontonummer, leverandørnavn, bank, rutingdnummer, kontonummer, debet, kredit og valuta. I dette eksemplet ønsker vi å utvide listen ved å legge til detaljer om betaling.   
6. Lukk siden.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Bruk en ny Excel-mal på ER-formatet på nytt
1. Klikk Utforming.
    * Åpne utkastversjonen av det valgte ER formatet for redigering.  
2. Klikk Import i handlingsruten.
3. Klikk Oppdater fra Excel.
    * Klikk "Oppdater mal", og velg deretter filen SampleVendPaymWsReport2.xlsx.  
    * Klikk Oppdater mal, og bla gjennom for å få den nedlastede tidligere SampleVendPaymWsReport2.xlsx-filen.  
4. Klikk OK.
    * SampleVendPaymWsReport2.xlsx malen brukes. Strukturen i Er-formatet synkroniseres med innholdet i malen, der elementene blir lagt til ER-formatet. Alle elementer i ER-formatet som ikke er inkludert i malen, blir fjernet fra formatdefinisjonen.  
5. Velg 'Excel' i treet.
    * Legg merke til at Mal-feltet nå inneholder en referanse til den nye malen.   
6. Klikk Vedlegg.
7. Klikk Åpne.
    * Klikk Åpne for å utforske oppsettet for den modifiserte Excel-malen.  
    * Gå gjennom malen. Legg merke til at teksten nå inneholder en linje for betalingsdato.   
8. Lukk siden.
9. Utvid 'Excel' i treet.
10. Vis Excel\PaymLines i treet.
11. Velg 'Excel\PaymLines\PaymDate' i treet.
    * Legg merke til at ER-formatet nå inneholder ett element til. En celle, PaymDate, er lagt til Excel-malen.  
12. Klikk kategorien Tilordning.
13. Utvid noden 'model' i treet.
14. Utvid modell\Betalinger i treet.
15. I treet velger du modell\Betalinger\Transaksjonsdato(TransactionDate).
16. Klikk Bind.
    * Angi hvilke data som legges til den nye cellen under kjøring.  
17. Klikk Lagre.
18. Lukk siden.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Aktiver den endrede utkastversjonen av ER-formatet for bruk i journalen for betalingsbehandling
1. Klikk Konfigurasjoner i handlingsruten.
2. Klikk Brukerparametere.
3. Velg Ja i feltet Kjøringsinnstillinger.
4. Klikk OK.
5. Klikk Rediger.
6. Velg Ja i feltet Kjøringsutkast.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Bruk den endrede utkastversjonen av ER-formatet i journalen for betalingsbehandling

Gå gjennom det opprettede regnearket, inkludert nye detaljer over betalingslinjer – betalingsdato.  
