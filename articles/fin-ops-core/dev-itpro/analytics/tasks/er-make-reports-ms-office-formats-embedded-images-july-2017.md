---
title: Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder
description: Fremgangsmåten i dette emnet viser hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner som genererer elektroniske dokumenter i Microsoft Office-formater (Excel og Word) som inneholder innebygde bilder.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52ed5677890555775961c0c23b46713d99090983
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184813"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Utforme konfigurasjoner for å generere rapporter i Office-format med innebygde bilder

[!include [task guide banner](../../includes/task-guide-banner.md)]

For å fullføre trinnene i denne prosedyren må du først fullføre prosedyren "ER Opprette en konfigurasjonsleverandør og merke den som aktiv". Denne fremgangsmåten forklarer hvordan du utformer elektronisk rapportering (ER)-konfigurasjoner for å generere et Microsoft Excel- eller Word-dokument som inneholder innebygde bilder. I denne prosedyren skal du opprette de nødvendige ER-konfigurasjonene for eksempelfirmaet, Litware, Inc. Disse trinnene kan fullføres ved å bruke USMF-datasettet. Denne fremgangsmåten er opprettet for brukere med rollen som systemansvarlig eller elektronisk rapportering utvikler. Før du begynner må du laste ned og lagre filene oppført i hjelpeemnet [Bygge inn bilder og figurer i forretningsdokumenter som blir generert ved hjelp av verktøyet for elektronisk rapportering](../electronic-reporting-embed-images-shapes.md). Filene er: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png og Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Kontrollere forhåndskrav  
 1. Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.  
 2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet "Litware, Inc." er tilgjengelig og merket som aktiv. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren "Opprette en konfigurasjonsleverandør og merke den som aktiv".   
 3. Klikk Rapporteringskonfigurasjoner.  
 
## <a name="add-a-new-er-model-configuration"></a>Legg til en ny ER-konfigurasjon  
 1. I stedet for å opprette en ny modell kan du laste ER-modellkonfigurasjonsfilen (modell for cheques.xml) som du lagret tidligere. Denne filen inneholder eksempeldatamodellen for betalingssjekker og tilordningen av datamodellen til datakomponentene i Dynamics 365 for Operations-programmet.   
 2. Klikk Veksle på hurtigfanen Versjoner.   
 3. Klikk Last fra XML-fil.  
 4. Klikk Bla gjennom, og velg deretter Modell for cheques.xml.   
 5. Klikk OK.  
 6. Den lastede modellen brukes som en datakilde med informasjon for å generere dokumenter som inneholder bilder i Excel og Word.  

## <a name="add-a-new-er-format-configuration"></a>Legg til en ny ER-formatkonfigurasjon  
 1. I stedet for å opprette et nytt format kan du laste ER-formatkonfigurasjonsfilen (Cheques printing format.xml) som du lagret tidligere. Denne filen inneholder eksempelutformingen på formatet for å skrive ut sjekker ved hjelp av det forhåndstrykte skjemaet og tilordningen av dette formatet til "Modell for sjekker"-datamodellen.   
 2. Klikk Veksle.  
 3. Klikk Last fra XML-fil.  
 4. Klikk Bla gjennom og velg Cheques printing format.xml-filen.   
 5. Klikk OK.  
 6. Utvid Modell for sjekker i treet.  
 7. Velg 'Modell for sjekker\Utskriftsformat for sjekker' i treet.  
 8. Det lastede formatet brukes for å generere dokumenter som inneholder bilder i Excel og Word.   

## <a name="configure-er-user-parameters"></a>Konfigurere ER-brukerparametere  
 1. Klikk Konfigurasjoner i handlingsruten.  
 2. Klikk Brukerparametere.  
 3. Velg Ja i feltet Kjøringsinnstillinger.  
  Aktiver flagget Kjøringsutkast for å starte utkastversjonen av det valgte formatet i stedet for den fullførte.  
 4. Klikk OK.  

## <a name="configure-cash--bank-management-parameters"></a>Konfigurere Parametere for kontant- og bankbehandling  
 1. Gå til Kontant- og bankbehandling > Bankkontoer > Bankkontoer.  
 2. Bruk hurtigfilteret til å filtrere på Bankkonto-feltet med en verdi lik USMF OPER.  
 3. Klikk Oppsett i handlingsruten.  
 4. Klikk Kontroller.  
 5. Utvid Oppsett-delen.  
 6. Klikk Rediger.  
 7. Velg Ja i Firmalogo-feltet.  
 8. Klikk på Firmalogo.  
 9. Klikk Endre.  
 10. Klikk Bla gjennom og velg filen du lastet ned tidligere, Company logo.png.   
 11. Klikk Lagre.  
 12. Lukk siden.  
 13. Utvid seksjonen Signatur.  
 14. Velg Ja i feltet Skriv ut første signatur.  
 15. Klikk Endre.  
 16. Klikk Bla gjennom og velg filen du lastet ned tidligere, Signature image.png.   
 17. Utvid Kopier-seksjonen.  
 18. Velg et alternativ i feltet Vannmerke.  
 19. Velg Ja i feltet Generelt elektronisk eksportformat.  
 20. Velg Cheques printing form-konfigurasjonen.  
 21. Nå brukes det valgte ER-formatet for utskrift av sjekker.  
 22. Klikk Vedlegg.  
 23. Klikk Ny.  
 24. Klikk Fil.  
 25. Klikk Bla gjennom og velg filen du lastet ned tidligere, Signature image 2.png.   
 26. Lukk siden.  
 27. Lukk siden.  
 28. Lukk siden.  
 29. Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.  
 30. Velg Ja i feltet Tillat oppretting av forhåndsmerknader for inaktive bankkontoer.  
 31. Klikk Lagre.  
 32. Lukk siden.  