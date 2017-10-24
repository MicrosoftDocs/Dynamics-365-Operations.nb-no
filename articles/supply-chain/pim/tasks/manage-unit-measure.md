--- 
title: "Administrere måleenhet"
description: "Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a>Administrere måleenhet

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter. Du kan gå gjennom denne fremgangsmåten ved hjelp av demonstrasjonsdata eller ved hjelp av dine egne data.

1. Gå til Vedlikehold av frigitt produkt.
2. Velg enheter.

## <a name="create-a-unit-of-measure"></a>Opprett en måleenhet
1. Klikk Ny.
2. Skriv inn en verdi i feltet Enhet.
    * Angi ID eller symbol som skal brukes ved referanse til måleenheten.  
3. Skriv inn en verdi i feltet Beskrivelse.
    * Angi et beskrivende navn for måleenheten på systemspråket.  
4. Velg et alternativ i feltet Enhetsklasse.
    * Enhetsklassen definerer hvilken logisk gruppering, for eksempel område, masse eller antall, måleenheten er en del av.  
5. Angi et tall i feltet Desimalpresisjon.
    * Angi antallet desimaler som den konverterte måleenheten må avrundes til når en beregning er fullført for måleenheten.  
6. Klikk Lagre.

## <a name="define-unit-translations"></a>Definer enhetsoversettelser
1. Klikk Enhetstekster.
2. Klikk Ny.
    * Bruk enhetsteksten til å opprette en oversettelse av ID-en eller et symbol som representerer måleenheten for bruk på eksterne dokumenter på kunde- eller leverandørspesifikke språk.  
3. Angi eller velg en verdi i feltet Språk.
4. Skriv inn en verdi i Tekst-feltet.
5. Klikk Lagre.
6. Lukk siden.
7. Klikk Oversatte enhetsbeskrivelser.
8. Klikk Ny.
    * Definer språkspesifikke beskrivelser for måleenheten.  
9. Angi eller velg en verdi i feltet Språk.
10. Skriv inn en verdi i feltet Beskrivelse.
11. Klikk Lagre.
12. Lukk siden.

## <a name="define-unit-conversion-rules"></a>Definer enhetsomregningsregler
1. Klikk Enhetsomregninger.
    * Definere regler for å konvertere måleenheten til og fra andre enheter i den valgte enhetsklassen.  
2. Klikk Ny for å åpne nedtrekksdialogen.
3. Angi et tall i feltet Faktor.
    * Omregningsfaktor mellom fra-enheten og til-enheten. Omregningsfaktoren fra centimeter til meter er for eksempel 100, fordi det er 100 centimeter i én meter.  
4. Angi eller velg en verdi i feltet Til enhet.
5. Velg et alternativ i feltet Avrunding.
    * Definer hvordan den omregnede verdien skal avrundes.  
6. Klikk OK.
7. Lukk siden.


