---
title: Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet
description: Kostnadsfordelingsregler brukes til å distribuere kostnader som er økonomisk opptelt i et kollektivt kostsenter.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: CAMCostDistributionRule
ms.openlocfilehash: 23adea279cad3fcf69cc6926d6f8dee485150221
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272406"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Opprette og tilordne en kostnadsdistribusjonspolicy til en kostnadskontrollenhet

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
