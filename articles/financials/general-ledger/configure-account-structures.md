---
title: Konfigurer kontostrukturer
description: Dette emnet gir informasjon om kontostrukturer og finansdimensjoner.
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c278cefd47b14c44c1949505404d08628cb7f52f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839503"
---
# <a name="configure-account-structures"></a>Konfigurer kontostrukturer

[!include[banner](../includes/banner.md)]

Kontostrukturer bruker hovedkontoen og finansdimensjonene for å opprette et sett med regler som bestemmer rekkefølgen og verdiene som brukes når du skriver inn kontonummeret. Du kan definere så mange kontostrukturer du trenger, for bedriften. Kontostrukturene tilordnes et firmas finansoppsett, slik at de kan deles.

Når du oppretter en kontostruktur, er det maksimale antallet segmenter 11. Hvis du trenger flere segmenter enn dette, må du nøye vurdere oppsettet og kravene, fordi det påvirker brukeropplevelsen. Vurder om et segment kan hentes ut i et rapporteringsscenario med et hierarki i stedet for under dataregistrering, eller ved å bruke et brukerdefinert felt. Hvis du for eksempel vil rapportere om sted, men du kan bruke sted etter avdeling eller kostsenter, trenger du ikke sted som en finansdimensjon. Hvis etter evaluering bestemmer at mer enn 11 segmenter kreves, kan du legge til flere segmenter ved hjelp av avanserte regler.

Kontostrukturer krever hovedkontoen. Hovedkontoen behøver ikke å være det første segmentet i strukturen, men det identifiserer hvilken kontostruktur som brukes under kontonummeroppføring. Derfor kan en hovedkontoverdi bare finnes i én struktur som er tilordnet til finans, slik at de ikke overlapper. Når kontostrukturen er identifisert, filtreres listen over tillatte verdier for å veilede brukeren til å plukke bare gyldige dimensjonsverdier, og dermed redusere muligheten for en feil journaloppføring.

> [!NOTE] 
> Hvis du planlegger å budsjettere mot en finansdimensjon, må den være en del av en kontostruktur. Budsjettering tar ikke i bruk avanserte regler for øyeblikket.

## <a name="example"></a>Eksempel
For å illustrere en anbefalt fremgangsmåte for å definere en kontostruktur, la oss anta at et selskap vil spore balansekontoene (100000..399999) på finansdimensjonsnivå for konto- og forretningsenhet. For inntekts- og utgiftskontoer (400000..999999) sporer de finansdimensjonene Forretningsenhet, Avdeling og Kostsenter. Hvis de gjør et salg, vil de også spore Kunde. Hvis du bruker dette scenariet, er det anbefalt å ha to kontostrukturene som er tilordnet firmaets finans – én for balansekontoer og én for resultatkonto. Hvis du vil optimalisere brukeropplevelsen og validering, bør kunden være en avansert regel som bare brukes når en salgskonto brukes.

**Balansekontostruktur**

|Hovedkonto          | Forretningsenhet    |
|----------------------|-----------|
|100000..399999 | *;” “|

**Resultatkontostruktur**

|Hovedkonto          | Forretningsenhet    |Avdeling          | Kostsenter    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | *;” “|*;” “|*;” “|*;” “|

**Avansert regel for å legge til en kunde**

Vilkår: Der hovedkontoen er mellom 400000 og 499999, legg til kunde. Den kan ikke stå tom.

|Kunde         |
|-----------------|
|* |

I dette forenklede eksempelet er alle verdier og tomme tillatt, så * og “ “ brukes.

## <a name="segments-and-allowed-values"></a>Segmenter og tillatte verdier
**Segmenter** og **Tillatte verdidetaljer**-delen inneholder en rutenettlignende opplevelse for å angi reglene som skal følges om validering under postering. Du kan skrive direkte i cellene i rutenettet, importere det fra Excel eller bruke **Tillatte verdidetaljer**-delen for å lede deg gjennom det.

**Tillatte verdidetaljer**-delen leder deg gjennom opprettingen av kriterier ved hjelp av **Operatorer** som begynner med, er mellom, inkluderer og mange flere.

[![Tillat verdier](./media/account.png)](./media/account.png) 

Tillatte verdier skal brukes på en journal- eller en regnskapsdistribusjonside der det ikke er noen andre mulige verdier å velge i henhold til kontostrukturoppsettet.

Her er et eksempel på **Resultatkontostruktur**.

|Hovedkonto          | Forretningsenhet    |Avdeling          | Kostsenter    |
|----------------------|-----------|----------------------|-----------|
|400000..999999 | 002 | 022 | 014 |

Når du angir en journal og velger en konto i resultatområdet, vil valg av forretningsenhet "002" gjøre at verdiene 022 og 014 er standard på kontokontrollen. Dette vil også oppstå med siden for regnskapsdistribusjon. 

## <a name="more-than-7-criteria-needed"></a>Mer enn 7 kriterier er nødvendig

Hvis du har mer enn 7 vilkår som kreves, kan du fortsette å legge dem på neste linje. Du vil se når du arbeider i **Tillatte verdidetaljer**-delen at **+Legg til ny**-vilkåret ikke lenger er aktivt etter at det syvende vilkåret er angitt. Dette skyldes mange faktorer som: 
 - Kolonnebredde 
 - Hvordan dataene er lagret 
 - Ytelsen til **Tillatte verdidetaljer**-kontrollen
 - Brukervennlighet  
 
For å fortsette å legge til flere vilkår, klikk på **Duplikat i segmentet** og **Tillatte verdier-del**. Dette kopierer kriteriene til en ny linje. Du kan deretter skrive over eller endre **Tillatt verdidetaljer**-delen.

## <a name="best-practices"></a>Anbefalte fremgangsmåter
Når du definerer kontostrukturer, finnes det noen gode fremgangsmåter du kan følge. Dette er imidlertid bare veiledning, så en helhetlig diskusjon om virksomheten, plan for vekst og vedlikeholdsplan må betraktes som en del av diskusjonen.

- Gjør hovedkontoen til første eller så nær begynnelsen av kontostrukturen som mulig, slik at brukere får den best veiledede opplevelsen de kan, under kontooppføringen.

- Bruk kontostrukturer på nytt i så stor grad som mulig for å redusere vedlikehold på tvers av juridiske enheter.

- For variasjoner på tvers av juridiske enheter kan du vurdere å bruke avanserte regler, slik at kontostrukturer kan brukes på nytt.

- Når du definerer tillatte verdier, bruker du områder og jokertegn så mye som mulig. Dermed kan du utvide og endre uten vedlikehold, men systemet yter også mer ideelt uten denne konfigurasjonen.

- Ikke bare sett inn en stjerne for hvert segment i kontostrukturen og bare stol på de avanserte reglene. Dette kan være vanskelig å administrere og fører ofte til brukerfeil under vedlikehold som kan gjøre at systemet ikke kan postere.

## <a name="account-structure-activation"></a>Aktivering av kontostruktur
Når du er fornøyd med det nye oppsettet eller en endring i en kontostruktur, må du aktivere den. Hvis en kontostruktur tilordnes en finanskonto, kan denne aktiveringen være en tidkrevende prosess, fordi alle ikke-posterte transaksjoner i systemet må være synkronisert med den nye strukturen. Posterte transaksjoner påvirkes ikke av kontostrukturendringer.

Hvis du vil ha mer informasjon, se [Planlegge kontoplanen](plan-chart-of-accounts.md), [Finansdimensjoner](financial-dimensions.md) og [Angi kombinasjoner av konto og dimensjon (segmentert oppføringskontroll)](enter-account-dimension-combinations-segmented-entry-control.md).
