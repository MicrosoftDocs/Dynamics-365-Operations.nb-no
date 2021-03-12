---
title: Spore provisjoner på salgssted (POS) ved hjelp av salgsgrupper
description: Det er vanlig praksis i detaljhandelen å spore salg etter kontakten som har jobbet med kunden – med assistanse, oppsalg, kryssalg og behandling av transaksjonen.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b020618036951e7033baadbf58b806df7877bdb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976595"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a>Spore provisjoner på salgssted (POS) ved hjelp av salgsgrupper

[!include [banner](includes/banner.md)]

Det er vanlig praksis i detaljhandelen å spore salg etter kontakten som har jobbet med kunden – med assistanse, oppsalg, kryssalg og behandling av transaksjonen.

Sporing av salg etter selger er et mål på selgerens salgsferdigheter, mens salg etter kasserer er et mål på hastighet og effektivitet. Salg sporet etter selger blir også ofte brukt til å beregne provisjon eller andre insentiver.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Konfigurere en arbeider for å være en selger på et salgssted

Når en arbeider er lagt til i en salgsgruppe, de blir kvalifisert for provisjon og kan identifiseres som en selger i systemet. En arbeider som ikke finnes i en salgsgruppe, er ikke kvalifisert for provisjon og vil ikke være oppført som en selger i programmet på salgsstedet. På salgsstedet er listen over selgere avledet fra alle salgsgrupper som inneholder minst én arbeider som er tilordnet til butikken. Listen vises på salgsstedet som en kombinasjon av salgsgruppe-ID og navn (ID: navn). En standard salgsgruppe kan tilordnes til arbeidere for å støtte scenarier der forhandleren velger å angi selgeren på salgsstedslinjer automatisk. Brukere kan velge fra salgsgruppen arbeideren er medlem av.

## <a name="functionality-profile-settings"></a>Innstillinger for funksjonalitetsprofil

Det finnes en rekke innstillinger for funksjonalitetsprofiler for en butikk som bestemmer flyt og prosess på salgsstedet som involverer selgere.

<table>
<thead>
<tr>
<th>Profil</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Gå til kasserer som standard når tilgjengelig</td>
<td>Hvis dette alternativet er aktivert, vil salgsstedet automatisk fylle ut transaksjonslinjer med standard salgsgruppe for gjeldende kasserer. Hvis en kasserer ikke har en standard salgsgruppe angitt, kan verdien ikke angis. En bruker kan fortsatt angi salgsgruppen manuelt ved hjelp av en rutenettknapp for salgssted.</td>
</tr>
<tr>
<td>Be om selger</td>
<td>Dette alternativet har tre mulige verdier:
<ul>
<li><strong>Ingen</strong> – Hvis dette alternativet er valgt, blir ikke brukeren bedt om å velge en salgsgruppe. Verdien kan fremdeles angis ved hjelp av en kasserers standard salgsgruppe eller ved å bruke en rutenettknapp for salgssted.</li>
<li><strong>Transaksjonsstart</strong> – Hvis dette alternativet er valgt, og enten <strong>Gå til kasserer som standard</strong> ikke er aktivert eller den gjeldende kassereren ikke har en standard salgsgruppe, blir brukeren bedt om å velge en salgsgruppe i starten av hver transaksjon. Hvis du velger en salgsgruppe fra denne, går som standard alle etterfølgende linjer til den valgte salgsgruppen. En bruker kan fortsatt angi salgsgruppen manuelt ved hjelp av en rutenettknapp for salgssted.</li>
<li><strong>For hver linje</strong> – Hvis dette alternativet er valgt, og enten <strong>Gå til kasserer som standard</strong> ikke er aktivert eller den gjeldende kassereren ikke har en standard salgsgruppe, blir brukeren bedt om å velge en salgsgruppe etter at hver linje legges til. En bruker kan fortsatt angi salgsgruppen manuelt ved hjelp av en rutenettknapp for salgssted.</li>
</ul>
</td>
</tr>
<tr>
<td>Krev</td>
<td>Dette alternativet gjelder bare når salgsstedet er konfigurert til å be om en selger. Hvis aktivert, må brukeren velge en salgsgruppe før fortsetter. Hvis ikke, brukeren blir bedt om, men kan avbryte og fortsette uten å gjøre et valg. Når linjen er lagt til, kan en bruker med tilstrekkelige tillatelser fortsatt fjerne salgsgruppen fra linjen. "Krev selger" gjennomføres ikke i denne situasjonen.</td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Vise informasjon om selger på skjermbildet for transaksjoner på salgssted

Oppsettet og innholdet på skjermen for transaksjoner på salgssted kan konfigureres ved hjelp av skjermoppsettdesigneren og tilordnede skjermoppsett til butikker, kasser eller arbeidere. **Selger**-feltet kan legges til kategorien Linjer i ruten Mottak.  Dette viser ID-en til angitt salgsgruppe for hver linje i skjermbildet for transaksjonen.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Legge til selgeroperasjoner for POS-knappegrupper

Salgssted gjør det mulig for brukere å konfigurere knapperutenett, som er inkludert i skjermoppsett for å gi tilgang til salgsstedsoperasjoner. Følgende salgsstedsoperasjoner kan tilordnes til knappegrupper som gjelder for selgere.

| Operasjon                                 | beskrivelse |
|-------------------------------------------|-------------|
| Angi selger på linje          | Denne salgsstedsoperasjonen viser en liste over berettigede salgsgrupper (ID: navn) for butikken. Hvis du velger en salgsgruppe fra listen, angis verdien på den gjeldende transaksjonslinjen. |
| Fjern selger på linje        | Denne salgsstedsoperasjonen fjerner verdien for den gjeldnede salgsgruppen fra den gjeldende transaksjonslinjen. |
| Angi selger i transaksjon   | Denne salgsstedsoperasjonen viser en liste over berettigede salgsgrupper (ID: navn) for butikken. Hvis du velger en salgsgruppe fra listen, angis standardverdien på den gjeldende transaksjonen. Eventuelle eksisterende linjer uten en salgsgruppe tilordnet angis, i tillegg til eventuelle senere tilføyde linjer. |
| Fjern selger i transaksjon | Denne salgsstedsoperasjonen fjerner verdien for den gjeldende standardsalgsgruppen fra den gjeldende transaksjonen. Den påvirker ikke linjer som allerede finnes i transaksjonen. |

## <a name="calculating-commissions"></a>Beregne provisjon

Provisjon beregnes for arbeidere i de angitte salgsgruppene samtidig som postering av utdrag eller salgsordre. Provisjonsbeløpet bestemmes basert på arbeiderens provisjonsandel, som definert i salgsgruppen og tilknyttede provisjon beregningsinnstillingene for kunde og/eller produkter på transaksjonen.
