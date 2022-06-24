---
title: Dataagnostisk testing ved hjelp av Regression Suite Automation Tool
description: Denne artikkelen beskriver anbefalinger for dataagnostisk testing ved hjelp Regression Suite Automation Tool.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 9463a69b6c1b273c6d37b6f4cf6eac19441da682
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860017"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Dataagnostisk testing ved hjelp av Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Selv om den funksjonelle valideringen av et ERP-program ikke kan være fullstendig dataagnostisk, finnes det flere faser og metoder for testing. Disse testfasene omfatter følgende:  

- SysTest-rammeverk
- ATL-rammeverk
- Regression Suite Automation Tool (RSAT)

[![Pyramide for testklassifisering.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Oversikt
-   **SysTest-rammeverk** – SysTest-rammeverket er pålitelig for skriving av enhetstester. Fordi enhetstester vanligvis tester en metode eller funksjon, bør de alltid være dataaknostisk og bare avhengige av inndataene som leveres som en del av testen.
-   **ATL-rammeverk** – Microsoft har et ATL-rammeverk som er en abstraksjon av SysTest-rammeverket og gjør funksjonell testskriving mye enklere og mer pålitelig. Dette rammeverket bør brukes til å skrive komponenttester eller enkle integreringstester.
-   **RSAT** – RSAT brukes til integreringstester og forretningssyklustester. Forretningssyklustestene, også kalt regresjonsanalysetester, er avhengige av eksisterende data. Disse testene kan imidlertid bli dataagnostisk hvis du tar hensyn til flere faktorer. 

    - o Der enhetstester og komponenttester er på lavt nivå og kan være fullstendig dataagnostisk (ikke avhengig av eksisterende datasett), er forretningssyklusen eller valideringstestene for regresjon avhengige av eksisterende data. Disse dataene inkluderer oppsett, konfigurasjonsinnstillinger (parametere) og hoveddata (kunde, leverandører, varer og så videre), men aldri transaksjonsdata. Kontroller under testen at hvis noen av disse endres, tilbakestilles de som en del av den siste testen.
    - Velg hoveddata basert på bestemte kriterier i stedet for å velge en bestemt post. Hvis du for eksempel vil velge en vare basert på dimensjonsverdiene og lagertilgjengeligheten, filtrerer du produktlisten med disse verdiene, velger den første varen og kopierer nummeret som skal brukes for fremtidige tester. Hvis det er en enkel hoveddatakilde, for eksempel kunde, leverandør eller vare, kan den opprettes som en del av automatiseringen og brukes i fremtidige tester ved hjelp av kjeding. 
    - o Angi de unike ID-ene, for eksempel fakturanumre, i nummerserien eller ved å bruke Microsoft Excel-funksjoner som = TEXT(NOW(),"ååååmmddttmm"). Denne funksjonen vil gi et unikt nummer hvert minutt, som gjør at du kan spore når handlingen skjedde. Dette kan for eksempel brukes for variabler som produktkvitteringsnumre og leverandørfakturanumre. Disse testene fortsetter å arbeide med samme database på nytt uten å kreve noen gjenopprettinger.
    - Du bør alltid sette **Redigeringsmodus** for miljøet til **Lese** eller **Redigere** som første testtilfelle, fordi standardalternativet **Automatisk**. Alternativet **Automatisk** bruker alltid den forrige innstillingen og kan føre til upålitelige tester. 
 
    [![Siden Alternativer, fanen Ytelse.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Valider bare etter at du har filtrert etter en bestemt transaksjon i stedet for å bruke generell validering. For antall poster filtrerer du for eksempel etter transaksjonsnummeret eller transaksjonsdatoen, slik at valideringen utelater alle andre transaksjoner. 
    - Hvis du kontrollerer en kundesaldo eller budsjettkontroll, må du først lagre verdien og deretter legge til transaksjonsverdien for å validere det forventede resultatet i stedet for å validere en fast forventet verdi. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]