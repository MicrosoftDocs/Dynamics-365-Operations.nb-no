--- 
title: Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet
description: "Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 492e4a94ec0caef8c51a691043a1ffb9e6a04758
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter. Regnskapsføreren sørger for at kostnaden fordeles til kostsentrene, basert på den valgte fordelingen grunnleggende. En policy og de tilsvarende reglene er tilordnet en kontrollenhet for kost. Denne håndboken oppgaven bruker et eksempel for å vise hvordan du oppretter en policy for distribusjon av kostnadene og de tilsvarende.


## <a name="create-a-policy"></a>Opprette en policy
1. Gå til Kostnadsregnskap > Policyer > Kostnadsdistribusjonspolicyer.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Policynavn.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadsobjekt.
    * Velg Organisasjon.  
6. Angi eller velg en verdi i feltet Dimensjonshierarki for kostnadselement.
    * Velg CD P/L.  
7. Angi eller velg en verdi i feltet Statistisk dimensjon.
    * Velg Statistiske elementer.  
8. Klikk Lagre.

## <a name="create-rules-for-the-policy"></a>Opprette regler for policyen
1. Klikk Ny.
2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Utvid hierarkiet for å velge 094.  
4. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Velg Andre driftsutgifter, og velg deretter 605110 rengjøring.  
5. Velg et alternativ i feltet Kostnadsatferd.
    * Velg Fast kostnad.  
6. Angi eller velg en verdi i feltet Tildelingsgrunnlag.
7. Klikk Ny.
8. Merk den valgte raden i listen.
9. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadsobjekt.
    * Utvid hierarkiet for å velge 094.  
10. Angi eller velg en verdi i feltet Dimensjonshierarkinode for kostnadselement.
    * Velg Andre driftsutgifter, og velg deretter 605150 leie.  
11. Velg et alternativ i feltet Kostnadsatferd.
    * Velg Fast kostnad.  
12. Angi eller velg en verdi i feltet Tildelingsgrunnlag.
13. Klikk Lagre.

## <a name="assign-rules-to-a-cost-control-unit"></a>Tilordne regler til en kostnadskontrollenhet
1. Klikk Policytilordninger for kostnadskontrollenhet.
2. Klikk Ny.
3. Merk den valgte raden i listen.
4. Angi en dato i feltet Gyldig fra regnskapsdato.
    * Velg 1. September i gyldige regnskapsåret.  
5. Angi eller velg en verdi i feltet Kostnadskontrollenhet
6. Klikk Lagre.


