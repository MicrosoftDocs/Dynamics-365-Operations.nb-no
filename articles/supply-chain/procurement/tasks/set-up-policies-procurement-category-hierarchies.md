---
title: Definere policyer for innkjøpskategorihierarkier
description: Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori.
author: kamaybac
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 242dd46e8b54504924f5bd13404dd9780c112cff8339d0a645785b2d4243871a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760448"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a>Definere policyer for innkjøpskategorihierarkier

[!include [banner](../../includes/banner.md)]

Bruk denne fremgangsmåten for å konfigurere regler for bestilling av produkter i en kategori. Reglene er definert for en bestemt innkjøpspolicy. Regelen for kategoritilgang kontrollerer hvilke innkjøpskategorier ansatte har tilgang til når de oppretter en rekvisisjon. Når en rekvisisjon opprettes, avgjør systemet hvilken innkjøpspolicy og regel for kategoritilgang som gjelder, basert på den juridiske enheten og driftsenheten som den ansatte tilhører. Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF. Denne oppgaven utføres vanligvis av en innkjøpssjef.


## <a name="find-the-procurement-policy"></a>Finne innkjøpspolicyen
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer**.
2. Klikk koblingen på siden "Policy for innkjøpspolicy for USMF". Dette er policyen som du vil legge til en regel i. Det må være en aktiv policy.  

## <a name="create-a-category-access-rule"></a>Opprette en regel for kategoritilgang
1. Utvid hurtigfanen **Policyregler**.
2. i listen **Type policyregel** velger du **Policyregel for kategoritilgang**. Hvis knappen **Opprett policyregel** er nedtonet, er det fordi det allerede finnes en aktiv policyregel for kategoritilgang. Kontroller feltene **Gyldighet** og **Utløp** for å finne ut hvilken det er, velg den og klikk på **Avslutt policyregel**. Hvis knappen **Opprett policyregel** er tilgjengelig, trenger du ikke gjøre noe.  
3. Klikk på **Opprett policyregel**.
4. Angi dato og klokkeslett i feltet **Gyldighetsdato**. Tidspunktet må ikke overlappe med en annen regel som allerede er aktiv.  
5. Velg en kategori som regelen skal gjelde for. Merk deg hvilken kategori dette er. Du trenger det senere. Når du velger en kategori, legges alle overordnede kategorier også til i listen Valgte kategorier. Hvis du vil at regelen skal gjelde for alle underkategorier for den valgt kategorien, merker du av for **Inkluder underkategorier**.
6. Klikk på pil høyre for å legge til listen **Valgte kategorier**.  
4. Klikk på **OK**. Hvis du vil sette alternativet **Inkluder overordnet regel** til Ja, vil policyregelen du konfigurerer for en overordnet kategori, også tilordnes de underordnede kategoriene hvis ingen policyregel er konfigurert for de underordnede kategoriene.

## <a name="create-a-category-policy-rule"></a>Opprette en policyregel for kategori
1. i listen **Type policyregel** velger du **Kategoripolicyregel**. Velg den aktive policyregelen hvis knappen **Opprett policyregel** er nedtonet, og klikk deretter **Avslutt policyregel**.  
2. Klikk på **Opprett policyregel**.
3. Angi dato og klokkeslett i feltet **Gyldighetsdato**.
4. Klikk på **Legg til**.
5. I **Kategori**-feltet velger du den samme kategorien som du brukte for **kategoritilgangsregelen**.
6. Velg et alternativ i **Leverandørvalg**-feltet. Velg en regel for å kontrollere hvilke type leverandører som kan velges for kategorien når rekvisisjoner opprettes.  
7. Klikk på **Lukk**. Policyreglene du har definert, har vært for rekvisisjoner av typen Forbruk. Hvis du vil definere policyer for rekvisisjoner av typen Etterfylling, kan du opprette en regel for policyregeltypen kalt Policyregel for tilgang til etterfyllingskategori.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]