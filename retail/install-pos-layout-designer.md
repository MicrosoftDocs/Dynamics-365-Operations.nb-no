---
title: Installere utforming av oppsett for Retail POS
description: "Du kan bruke ettklikksutformingen til å utforme forskjellige oppsett for Moderne salgssted (MPOS) og Skybaser salgssted i liggende eller stående modus for butikker, kasser, kasserere og ledere."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Installere utforming av oppsett for Retail POS

Du kan bruke ettklikksutformingen til å utforme forskjellige oppsett for Moderne salgssted (MPOS) og Skybaser salgssted i liggende eller stående modus for butikker, kasser, kasserere og ledere.

Den grensesnittet for grafiske utformingen for MPOS og skybasert POS styres av oppsettet for kasseapparat. Et oppsett styrer plasseringen av ulike objekter. Eksempler omfatter det totale oppsettet, varerutenettoppsettet, kundeoppsettet, betalingsoppsettet og oppsettet av ulike menyknapper. Oppsett omfatter også det generelle utseendet i salgsgrensesnittet som er vises for ansatte.

## <a name="install-the-oneclick-designer"></a>Installere oneclick-designer
1.  I Microsoft Dynamics 365 for operasjoner, bruker du menyen øverst til venstre til å navigere til **Retail****og commerce**&gt;**kanaloppsett**&gt;**installasjonsprogrammet for POS**&gt;**POS**&gt;**skjerm oppsett**.
2.  Velg et oppsett som har programtypen **Moderne salgssted for Windows** eller **Skybasert salgssted**, og klikk deretter **Utforming av oppsett**.
3.  I varslingsfeltet som vises nederst i Internet Explorer-vinduet, klikker du **Åpne** for å installere ettklikksutformingen. (Varslingsfeltet vises kanskje et annet sted i andre lesere.)
4.  I meldingsboksen **Programinstallasjon – sikkerhetsvarsel** som vises, klikker du **Kjør** for å installere utformingsverten for detaljhandel. En fremdriftsindikator viser fremdriften for installasjonen.
5.  Når installasjonen er fullført, angir du brukernavnet og passordet for Microsoft Dynamics 365 for Operations på siden **Logg på**, og deretter klikker du **Logg på** for å starte utformingen.
6.  Når legitimasjonen er validert og utformingen starter, kan du begynne å utforme ditt eget oppsett eller endre det eksisterende oppsettet. [![Oppsettet i ett klikk designer](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Feilsøking i forbindelse med installasjon av utformingen av oppsett
-   Når du klikker **Utforming**, vises ikke meldingen om å laste ned (eller kjøre) installasjonsprogrammet, eller gjeldende sikkerhetsinnstillinger tillater ikke at du laster ned filen. **Løsninger:**
    -   I Internet Explorer kontrollerer du at popup-blokkering er deaktivert for dette området. Klikk **innstillinger**&gt;**alternativer**&gt;**personvern**&gt;**finne popup-blokkering**, og endre innstillingen, hvis en endring er nødvendig.
    -   I Internet Explorer legger du til URL-adressen for Dynamics 365 for Operations i klarerte områder. Klikk **innstillinger**&gt;**alternativer**&gt;**sikkerhet**&gt;**klarerte områder**&gt;**områder**&gt;**Legg til**.
-   Programmet starter ikke, og du blir bedt om å kontakte leverandøren. **Løsning:** I Internet Explorer legger du til URL-adressen for Dynamics 365 for Operations i klarerte områder. Klikk **innstillingen**&gt;**alternativer**&gt;**sikkerhet**&gt;**klarerte områder**&gt;**områder**&gt;**Legg til**.

**Kjent problem:** Utformingen fungerer ikke slik den skal i nettleserne Google Chrome eller Mozilla Firefox. Vi arbeider for å løse dette problemet.

<a name="see-also"></a>Se også
--------

[Konfigurere, laste ned, installere og aktivere moderne salgssted for detaljhandel](retail-modern-pos-device-activation.md)


