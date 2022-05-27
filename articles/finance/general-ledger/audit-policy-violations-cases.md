---
title: Overvåkingspolicybrudd og -saker
description: Artikkelen forklarer hvordan overvåkingssaker genereres basert på brudd på overvåkingspolicyregler. Den inneholder også informasjon om de forskjellige måtene overvåkingspolicyer bruker datoområdet for dokumentvalg.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbef92865c0a463b3922d7cc6c3f46759ffdc9ad
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711124"
---
# <a name="audit-policy-violations-and-cases"></a>Overvåkingspolicybrudd og -saker

[!include [banner](../includes/banner.md)]

Artikkelen forklarer hvordan overvåkingssaker genereres basert på brudd på overvåkingspolicyregler. Den inneholder også informasjon om de forskjellige måtene overvåkingspolicyer bruker datoområdet for dokumentvalg.

## <a name="how-audit-cases-are-generated"></a>Hvordan overvåkingssaker genereres

Overvåkingspolicyer brukes til å identifisere utgiftsrapporter, bestillinger og leverandørfakturaer som ikke er i tråd med forretningsregler du definerer og konfigurerer som overvåkingspolicyregler. 

Overvåkingspolicyer kjører i satsvis modus. Når du kjører en overvåkingspolicy, kjøres alle policyreglene som er en del av policyen, samtidig.

Hver policyregel vurderer et sett med dokumenter. Policyregelen velger dokumenter som er i datoområdet for dokumentutvalg og oppfyller de angitte kriteriene. En policyregel kan for eksempel velge utgiftsrapporter som har måltider som overskrider 500,00. En annen policyregel kan velge leverandørfakturaer som betales til en bestemt leverandør. Det genereres et brudd for hvert dokument som velges i settet. Dette bruddet er en post der et bestemt dokument, for eksempel faktura 12345, ikke er i tråd med policyregelen. 

Flere poster for overvåkingsbrudd grupperes og knyttes til overvåkingssaker. Saker for hver overvåkingspolicy grupperes som standard etter overvåkingspolicyregel. Hvis du vil, kan du velge andre grupperingskriterier ved på siden **Kriterier for saksgruppering**. Du kan for eksempel gruppere utgiftshoder etter prosjekt-ID og leverandørfakturaer etter leverandørkonto. I dette tilfellet grupperes alle utgiftshodebrudd som har samme prosjekt-ID, i samme sak, og alle leverandørfakturaer som har samme leverandørkonto, grupperes i samme sak. 

> [!NOTE]
> Når det gjelder overvåkingspolicyregler som er basert på spørringstypen **Duplikat**, grupperes ikke brudd etter policyregel eller kriteriene som er angitt på siden **Kriterier for saksgruppering**. I stedet grupperes de etter kriteriene som er innebygd i overvåkingspolicyregelen. Hvis en policyregel for eksempel evaluerer utgiftsrapporter for dupliserte utgifter av samme beløp, forretningsenhets-ID og dato, er alle utgifter som har de samme verdiene i disse feltene, én sak. Alle utgifter som har andre verdier, er en separat sak.

Etter at overvåkingssakene er generert, behandles de ved hjelp av de vanlige fremgangsmåtene for saksbehandling.

## <a name="document-selection-date-ranges"></a>Datoområder for dokumentutvalg
Når en overvåkingspolicy kjøres, velger hver policyregel dokumenter av den angitte typen som har en dato som er i datoområdet for dokumentutvalg. Datoområdet for dokumentvalg angis på **Tilleggsalternativer**-siden. Mange dokumenter har flere datoer tilknyttet. Datofeltet som overvåkingspolicyregelen bruker, er angitt på siden **Type policyregel**.

Her er noen andre måter en overvåkingspolicy bruker datoområdet for dokumentvalg på:

-   Policyen bruker versjonen av hver policyregel som gjelder på den siste dagen i datoområdet for dokumentvalg. Du kan vise gyldighetsdatoene for hver policyregel på listesiden **Overvåkingspolicyer**.
-   Policyen bruker organisasjonsnodene som er knyttet til policyen, på den siste dagen i datoområdet for dokumentvalg. Bare organisasjonsnodene som for øyeblikket er knyttet til policyen, vises på listesiden **Overvåkingspolicyer**.
-   Når det gjelder policyregler som er basert på spørringstypen **Listesøk**, evaluerer policyen dokumenter basert på overvåkede enheter som er gyldige på den siste dagen i datoområdet for dokumentvalg.


Hvis du vil ha mer informasjon, se [Overvåkingspolicyregler](audit-policy-rules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
