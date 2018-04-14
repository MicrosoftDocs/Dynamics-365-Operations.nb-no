--- 
title: "Definere policyer for innkjøpskategorihierarkier"
description: "Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 50764f99be04d27e04047824f870e724336cb452
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Definere policyer for innkjøpskategorihierarkier

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori. Reglene er definert for en bestemt innkjøpspolicy. Regelen for kategoritilgang kontrollerer hvilke innkjøpskategorier ansatte har tilgang til når de oppretter en rekvisisjon. Når en rekvisisjon opprettes, avgjør systemet hvilken innkjøpspolicy og regel for kategoritilgang som gjelder, basert på den juridiske enheten og driftsenheten som den ansatte tilhører. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne oppgaven utføres vanligvis av en innkjøpssjef.


## <a name="find-the-procurement-policy"></a>Finne innkjøpspolicyen
1. Gå til Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer.
2. Klikk koblingen på siden Policy for innkjøpspolicy for USMF.
    * Dette er policyen som du vil legge til en regel i. Det må være en aktiv policy.  

## <a name="create-a-category-access-rule"></a>Opprette en regel for kategoritilgang
1. Velg policyregelen for kategoritilgang.
    * Hvis knappen Opprett policyregel er nedtonet, er det fordi det allerede finnes en aktiv policyregel for kategoritilgang. Kontroller feltene Gyldighetsdato og Utløpsdato for å finne ut hvilken det er, velg den og klikk Avslutt policyregel. Hvis knappen Opprett policyregel er tilgjengelig, trenger du ikke gjøre noe.  
2. Klikk Opprett policyregel.
3. Angi dato og klokkeslett i feltet Gyldighetsdato.
    * Tidspunktet må ikke overlappe med en annen regel som allerede er aktiv.  
    * Velg en kategori som regelen skal gjelde for. Merk deg hvilken kategori dette er. Du trenger det senere. Når du velger en kategori, legges alle overordnede kategorier også til i listen Valgte kategorier.  
    * Hvis du vil at regelen skal gjelde for alle underkategorier for den valgt kategorien, merker du av for Inkluder underkategorier.  
4. Klikk Legg til.
    * Hvis du vil sette alternativet Inkluder overordnet regel til Ja, vil policyregelen du konfigurerer for en overordnet kategori, også tilordnes de underordnede kategoriene hvis ingen policyregel er konfigurert for de underordnede kategoriene.  
5. Klikk OK.

## <a name="create-a-category-policy-rule"></a>Opprette en policyregel for kategori
1. Velge kategoripolicyregel
    * Velg den aktive policyregelen hvis knappen Opprett policyregel er nedtonet, og klikk deretter Avslutt policyregel.  
2. Klikk Opprett policyregel.
3. Angi dato og klokkeslett i feltet Gyldighetsdato.
4. Klikk Legg til.
5. Velg den samme kategorien som du brukte for kategoritilgangsregelen.
6. Velg et alternativ i Leverandør-feltet.
    * Velg en regel for å kontrollere hvilke type leverandører som kan velges for kategorien når rekvisisjoner opprettes.  
7. Klikk Lukk.
    * Policyreglene du har definert, har vært for rekvisisjoner av typen Forbruk. Hvis du vil definere policyer for rekvisisjoner av typen Etterfylling, kan du opprette en regel for policyregeltypen kalt Policyregel for tilgang til etterfyllingskategori.  


