---
title: "Følge opp provisjon i POS ved hjelp av salgsgrupper"
description: "Det er vanlig praksis å spore salg etter Knytt som har jobbet med kunden retail – gir assistanse, opp-selger, selge på tvers og behandling av transaksjonen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Følge opp provisjon i POS ved hjelp av salgsgrupper

Det er vanlig praksis å spore salg etter Knytt som har jobbet med kunden retail – gir assistanse, opp-selger, selge på tvers og behandling av transaksjonen.

Spore salg etter selger er et mål på associates selge ferdigheter, mens salg etter kassereren er et mål på hastighet og effektivitet. Salg sporet som salgsrepresentant blir også ofte brukt til å beregne provisjon eller andre insentiver.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfigurere en arbeider for å være en selger i POS
Når en arbeider er lagt til en salgsgruppe, de blir kvalifisert for provisjon og kan identifiseres som en selger i systemet. En arbeider som ikke finnes i en mva-gruppe er ikke kvalifisert for provisjon og vil ikke være oppført som en selger i poenget med salg (POS) program. POS, er listen over selgere avledet fra alle salg grupper som inneholder minst én arbeider som er tilordnet til butikken. Listen vises i POS som en kombinasjon av mva-gruppe-ID og navn (ID: navn). En standard mva-gruppe kan tilordnes til arbeidere støtter scenarier der forhandleren velger å angi selgeren på POS-linjer automatisk. Brukere kan velge fra salgsgruppen arbeideren er medlem av.

## <a name="functionality-profile-settings"></a>Profilinnstillinger funksjonalitet
Det finnes en rekke funksjonalitet profilinnstillinger for en butikk som bestemmer flyt og prosess i POS som involverer selgere.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Hvis dette alternativet er aktivert, POS vil automatisk fylle ut transaksjonslinjer med gjeldende kassereren standard mva-gruppe. Hvis en kasserer ikke har en standard salgsgruppe angitt, kan verdien ikke angis. En bruker kan angi salgsgruppen fortsatt manuelt ved hjelp av en POS knappen rutenett-knappen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Dette alternativet har tre mulige verdier: ** Ingen **-hvis dette alternativet er valgt, brukeren ikke bli bedt om å velge en mva-gruppe. Verdien kan fremdeles angis ved hjelp av en kasserer standard mva-gruppe eller ved å bruke en POS-knappen manuelt rutenett-knappen. **Begynnelsen av transaksjonen** - Hvis dette alternativet er valgt, og enten den **kassereren som standard** ikke er aktivert eller gjeldende kassereren har ikke en standard mva-gruppe, brukeren blir bedt om å velge en mva-gruppe i begynnelsen av hver transaksjon. Hvis du velger en mva-gruppe fra denne som standard alle etterfølgende linjer til den valgte mva-gruppen. En bruker kan angi salgsgruppen fortsatt manuelt ved hjelp av en POS knappen rutenett-knappen. **For hver linje** - Hvis dette alternativet er valgt, og enten den **kassereren som standard** ikke er aktivert eller gjeldende kassereren har ikke en standard mva-gruppe, brukeren blir bedt om å velge en mva-gruppe når du har lagt til hver linje. En bruker kan angi mva-gruppen fremdeles manuelt ved hjelp av en POS knappen rutenett-knappen. |
| **Krever**                           | Dette alternativet gjelder bare når POS er konfigurert til å be om en salgsrepresentant. Hvis aktivert, må brukeren velge en salgsgruppe før du fortsetter. Hvis ikke, brukeren blir bedt om, men kan avbryte og fortsette uten å gjøre et valg. Når linjen er lagt til, kan en bruker med tilstrekkelige tillatelser fortsatt fjerne salgsgruppen fra linjen. "Krever salgsrepresentant" gjennomføres ikke i denne situasjonen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Viser informasjon om mva-salgsrepresentant på transaksjoner POS-skjermen
POS transaksjonen skjermoppsettet og innholdet kan konfigureres ved hjelp av skjermen layout designer og tildelte skjermoppsett til butikker, kasser eller arbeidere. Den **selger** felt kan legges til kategorien linjer i ruten mottak.  Dette viser IDen til angitt mva-gruppe for hver linje i skjermbildet for transaksjonen.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Legger til Sales knappen representative operasjoner til POS rutenett
POS gjør det mulig for brukere å konfigurere knappen rutenett, som er inkludert i et skjermoppsett for for å gi tilgang til POS-operasjoner. Følgende POS-operasjoner kan tilordnes til knapper for knappegruppe som gjelder for selgere.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operasjon**                             | **Description**                                                                                                                                                                                                                                                                              |
| Angi selger på linje          | Operasjonen POS viser en liste over berettigede mva-grupper (ID: navn) for butikken. Hvis du velger en mva-gruppe fra listen for å angi verdien på den gjeldende transaksjonslinjen.                                                                                                            |
| Fjern selger på linje        | Denne POS-operasjonen fjerner gjeldende verdi for mva-gruppen fra den gjeldende transaksjonslinjen.                                                                                                                                                                                                  |
| Sett salgsrepresentant på transaksjonen   | Operasjonen POS viser en liste over berettigede mva-grupper (ID: navn) for butikken. Hvis du velger en mva-gruppe fra listen for å angi standardverdien for gjeldende transaksjon. Eventuelle eksisterende linjer uten en salgsgruppe tilordnet blir sett, i tillegg til eventuelle senere lagt til linjer. |
| Fjern salgsrepresentant på transaksjonen | Denne POS-operasjonen fjerner den gjeldende verdien for standard mva-gruppen fra den gjeldende transaksjonen. Det påvirker ikke noen linjer som allerede finnes i transaksjonen.                                                                                                                             |

## <a name="calculating-commissions"></a>Beregning av provisjon
Provisjonen beregnes for arbeidere i de angitte salgsgruppene samtidig som postere utdrag eller salgsordre postering. Provisjonsbeløpet bestemmes basert på arbeiderens provisjon delt ressurs, som definert i salgsgruppen og tilknyttede provisjon beregningsinnstillingene for kunde og/eller produkter på transaksjonen.


