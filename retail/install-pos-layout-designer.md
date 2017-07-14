---
title: Installere utforming av oppsett for Retail POS
description: "Du kan bruke ettklikksutformingen til å utforme forskjellige oppsett for Moderne salgssted (MPOS) og Skybaser salgssted i liggende eller stående modus for butikker, kasser, kasserere og ledere."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 52a16be4b07eafb493c7fd7ad52a6d9d1bb9ee89
ms.openlocfilehash: 4308e7bad71271f242def93d587e4a0c1f7c06cc
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Installere utforming av oppsett for Retail POS
<a id="install-the-retail-pos-layout-designer" class="xliff"></a>

[!include[banner](includes/banner.md)]


Du kan bruke ettklikksutformingen til å utforme forskjellige oppsett for Moderne salgssted (MPOS) og Skybaser salgssted i liggende eller stående modus for butikker, kasser, kasserere og ledere.

Den grensesnittet for grafiske utformingen for MPOS og skybasert POS styres av oppsettet for kasseapparat. Et oppsett styrer plasseringen av ulike objekter. Eksempler omfatter det totale oppsettet, varerutenettoppsettet, kundeoppsettet, betalingsoppsettet og oppsettet av ulike menyknapper. Oppsett omfatter også det generelle utseendet i salgsgrensesnittet som er vises for ansatte.

## Installere ettklikksutformingen
<a id="install-the-one-click-designer" class="xliff"></a>
1.  I Microsoft Dynamics 365 for Retail bruker du menyen øverst til venstre til å navigere til **Detaljhandel** **og handel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.
2.  Velg et oppsett som har programtypen **Moderne salgssted for Windows** eller **Skybasert salgssted**, og klikk deretter **Utforming av oppsett**.
3.  I varslingsfeltet som vises nederst i Internet Explorer-vinduet, klikker du **Åpne** for å installere ettklikksutformingen. (Varslingsfeltet vises kanskje et annet sted i andre lesere.)
4.  I meldingsboksen **Programinstallasjon – sikkerhetsvarsel** som vises, klikker du **Kjør** for å installere utformingsverten for detaljhandel. En fremdriftsindikator viser fremdriften for installasjonen.
5.  Når installasjonen er fullført, angir du brukernavnet og passordet for Microsoft Dynamics 365 for Retail på siden **Logg på**, og deretter klikker du **Logg på** for å starte utformingen.
6.  Når legitimasjonen er validert og utformingen starter, kan du begynne å utforme ditt eget oppsett eller endre det eksisterende oppsettet. [![Oppsett i ettklikksutformingen](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## Feilsøking i forbindelse med installasjon av utformingen av oppsett
<a id="troubleshoot-the-installation-of-the-layout-designer" class="xliff"></a>
-   Når du klikker **Utforming**, vises ikke meldingen om å laste ned (eller kjøre) installasjonsprogrammet, eller gjeldende sikkerhetsinnstillinger tillater ikke at du laster ned filen. **Løsninger:**
    -   I Internet Explorer kontrollerer du at popup-blokkering er deaktivert for dette området. Klikk **Innstillinger** &gt; **Alternativer** &gt; **Personvern** &gt; **Finn popup-blokkering**, og endre innstillingen, hvis det kreves en endring.
    -   I Internet Explorer legger du til URL-adressen for Dynamics 365 for Retail i klarerte områder. Klikk **Innstillinger** &gt; **Alternativer** &gt; **Sikkerhet** &gt; **Klarerte områder** &gt; **Områder** &gt; **Legg til**.
-   Programmet starter ikke, og du blir bedt om å kontakte leverandøren. **Løsning:** I Internet Explorer legger du til URL-adressen for Dynamics 365 for Retail i klarerte områder. Klikk **Innstilling** &gt; **Alternativer** &gt; **Sikkerhet** &gt; **Klarerte områder** &gt; **Områder** &gt; **Legg til**.

**Kjent problem:** Utformingen fungerer ikke slik den skal i nettleserne Google Chrome eller Mozilla Firefox. Vi arbeider for å løse dette problemet.

Se også
<a id="see-also" class="xliff"></a>
--------

[Konfigurere, laste ned, installere og aktivere moderne salgssted for detaljhandel](retail-modern-pos-device-activation.md)




