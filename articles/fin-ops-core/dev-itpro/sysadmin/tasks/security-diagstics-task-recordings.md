---
title: Sikkerhetsdiagnostikk for oppgaveregistreringer
description: Denne artikkelen inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.search.form: ''
ms.openlocfilehash: e564a0499cb1a5dc00fc027c20a027f9b454600c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272528"
---
# <a name="security-diagnostics-for-task-recordings"></a>Sikkerhetsdiagnostikk for oppgaveregistreringer

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Før du begynner

Denne artikkelen inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak. Før du fullfører trinnene i denne artikkelen må du ha en oppgaveregistrering for forretningsprosessen du vil analysere. Hvis du vil registrere en forretningsprosess, se [Ressurser for Oppgaveregistrering](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Behandle sikkerhet for et oppgaveopptak

1. Gå til **Systemadministrasjon** > **Sikkerhet** > **Sikkerhetsdiagnostikk for oppgaveopptak**.
2. Åpne oppgaveopptaket fra plasseringen. Velg **Åpne fra denne PC-en** eller **Åpne fra Lifecycle Services**, og velg deretter **Lukk**.
3. Dette vil åpne siden for **elementdetaljer for sikkerhetsmeny** som viser sikkerhetsobjektene som kreves for prosessen.

 > [!NOTE]
 > Menyelementene **Handling** og **Utdata** er ikke inkludert i listen.

4. Velg en bruker i feltet **Bruker-ID**. Hvis brukeren ikke har tillatelser for noen menyelementer, vil feltet **Manglende tillatelser** oppdateres til **Ja**.
  
  ![Side for elementdetaljer for sikkerhetsmeny.](../media/Security-Menu-Item-Details.png)

5. Velg **Legg til referanse** for å vise en liste over sikkerhetsobjektene, inkludert roller, plikter og rettigheter, som gir den manglende tillatelsen.
6. Velg et sikkerhetsobjekt fra listen:

    - Hvis **Rolle** er valgt, velger du **Legg til rolle for bruker**. Dette vil åpne siden **Tilordne brukere til roller**. Hvis du vil ha mer informasjon, kan du se siden [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).
    - Hvis **Plikt** er valgt, velger du **Legg til plikt i rollen**, velger rollene som plikten skal legges til, og velg deretter **OK**.
    - Hvis **Rettighet** er valgt, velger du **Legg til rettighet i plikter**, velger rollene som plikten skal legges til, og velg deretter **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
