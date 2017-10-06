--- 
title: Opprette en produktstandard
description: "Opprett en produktstandard for de forhåndsdefinerte variantene."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b783c41459163ab5a0644a1ff5c39b6933bcdb1b
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-master"></a>Opprette en produktstandard

[!include[task guide banner](../../includes/task-guide-banner.md)]

Opprett en produktstandard for de forhåndsdefinerte variantene. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne fremgangsmåten er ment for produktdesigneren.


## <a name="create-a-new-product-master"></a>Opprette en ny produktstandard
1. Gå til Behandling av produktinformasjon > Produkter > Produktstandarder.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Produktnummer.
    * Nummeret må være unikt. Du kan angi en nummerserie for feltet Produktnummer. I så fall trenger ikke brukeren å angi en verdi.  
4. Skriv inn en verdi i feltet Produktnavn.
    * Angi et beskrivende produktnavn. Verdien angis som standard til søkenavnet, men dette kan endres av brukeren.  
5. Klikk rullegardinknappen i Produktdimensjonsgruppe-feltet for å åpne oppslaget.
    * Produktdimensjonsgruppen bestemmer hvilke 4 produktdimensjoner som kan brukes til å opprette produktvarianter. Dette eksemplet brukes en gruppe med farge og størrelse.  
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
    * Standardkonfigurasjonsteknologien er Forhåndsdefinert variant. Denne vil bli brukt i dette eksemplet.  
8. Klikk OK.

## <a name="select-product-dimension-groups"></a>Velg produktdimensjonsgrupper
1. Klikk rullegardinknappen i feltet Fargegruppe for å åpne oppslaget.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk rullegardinknappen i feltet Størrelsesgruppe for å åpne oppslaget.
5. Finn og velg ønsket post i listen.
6. Klikk koblingen i den valgte raden i listen.

## <a name="add-dimension-groups"></a>Legge til dimensjonsgrupper
1. Klikk Produkt i handlingsruten.
2. Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.
3. Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.
    * Lagringsdimensjoner hjelper deg styre hvordan varer lagres og hentes fra lageret. En lagringsdimensjon kan for eksempel inkludere Område og lager.  
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.
    * Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du kan legge til et produkt. Parti- eller serienummer brukes for eksempel til å spore varer på lager.  
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Klikk OK.
10. Klikk Lagre.
11. Lukk siden.

