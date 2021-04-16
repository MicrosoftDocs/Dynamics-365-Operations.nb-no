---
title: Sikkerhetsdiagnostikk for oppgaveregistreringer
description: Dette emnet inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak.
author: Peakerbl
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: cb4d544d8d74ad10432901381253f84ec9331ae7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745771"
---
# <a name="security-diagnostics-for-task-recordings"></a>Sikkerhetsdiagnostikk for oppgaveregistreringer

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Før du begynner

Dette emnet inneholder informasjon om hvordan du analyserer og administrerer krav til sikkerhetstillatelse basert på et oppgaveopptak. Før du fullfører trinnene i dette emnet må du ha en oppgaveregistrering for forretningsprosessen du vil analysere. Hvis du vil registrere en forretningsprosess, se [Ressurser for Oppgaveregistrering](../../user-interface/task-recorder.md). 

## <a name="manage-security-for-a-task-recording"></a>Behandle sikkerhet for et oppgaveopptak

1. Gå til **Systemadministrasjon** > **Sikkerhet** > **Sikkerhetsdiagnostikk for oppgaveopptak**.
2. Åpne oppgaveopptaket fra plasseringen. Velg **Åpne fra denne PC-en** eller **Åpne fra Lifecycle Services**, og velg deretter **Lukk**.
3. Dette vil åpne siden for **elementdetaljer for sikkerhetsmeny** som viser sikkerhetsobjektene som kreves for prosessen.

 > [!NOTE]
 > Menyelementene **Handling** og **Utdata** er ikke inkludert i listen.

4. Velg en bruker i feltet **Bruker-ID**. Hvis brukeren ikke har tillatelser for noen menyelementer, vil feltet **Manglende tillatelser** oppdateres til **Ja**.
  
  ![Side for elementdetaljer for sikkerhetsmeny](../media/Security-Menu-Item-Details.png)

5. Velg **Legg til referanse** for å vise en liste over sikkerhetsobjektene, inkludert roller, plikter og rettigheter, som gir den manglende tillatelsen.
6. Velg et sikkerhetsobjekt fra listen:

    - Hvis **Rolle** er valgt, velger du **Legg til rolle for bruker**. Dette vil åpne siden **Tilordne brukere til roller**. Hvis du vil ha mer informasjon, kan du se siden [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md).
    - Hvis **Plikt** er valgt, velger du **Legg til plikt i rollen**, velger rollene som plikten skal legges til, og velg deretter **OK**.
    - Hvis **Rettighet** er valgt, velger du **Legg til rettighet i plikter**, velger rollene som plikten skal legges til, og velg deretter **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]