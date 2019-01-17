---
title: Hva er nytt eller endret i Dynamics AX-programversjon 7.0.1 (mai 2016)
description: Denne artikkelen beskriver funksjoner som enten er nye eller har blitt endret i Microsoft Dynamics AX-programversjon 7.0.1. Denne versjonen ble utgitt i mai 2016, og har build-nummeret 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: c830952b5d9e4887a816b5ab66d0944bddf5b505
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2018

---

# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Hva er nytt eller endret i Dynamics AX-programversjon 7.0.1 (mai 2016)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller har blitt endret i Microsoft Dynamics AX-programversjon 7.0.1. Denne versjonen ble utgitt i mai 2016, og har build-nummeret 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronisk rapportering (ER)

| Hva kan du gjøre? | Hvorfor er dette viktig? |
|------------------|------------------------|
| Konfigurer en dialogboks for kjøretid for utforming av rapporter for elektronisk rapportering (ER), slik at brukere kan velge finansdimensjonene de ønsker. | Ved kjøretid kan brukere velge flere finansdimensjoner i dialogboksen for å kjøre en ER-rapport. Detaljer om de valgte finansdimensjonene vises i det elektroniske dokumentet som genereres. |
| Konfigurer tilgang til flere finansdimensjoner under utformingen av en ER-rapport via en enkelt tilordning til den aktuelle datakilden. | Samme ER-rapportkonfigurasjon kan brukes til å generere elektroniske dokumenter som presenterer transaksjonsdata sammen med detaljer for finansdimensjoner, uavhengig av hvor mange finansdimensjoner som er valgt av brukeren eller konfigurert for gjeldende juridiske enhet eller forekomst. |
| Konfigurer en ER-rapport for å skrive inn data i dynamisk genererte kolonner i et elektronisk dokument som er opprettet i OPENXML-regnearkformat. | En ER-rapport kan registrere data i et OPENXML-regneark som genereres, via vannrett replikering av kolonner. Derfor kan den samme ER-rapportkonfigurasjonen brukes på nytt for å generere elektroniske dokumenter som har et annet antall dynamisk genererte kolonner. |
| Konfigurer ER-mål slik at utdataresultatet av et format rettes mot bestemte mål: fil, e-post eller arkiv (Microsoft SharePoint-mappe eller Microsoft Azure Storage). | Tidligere, da du kjørte en ER-konfigurasjon, ble det vist en meldingsboks som krevde at brukerhandling for å lagre eller åpne en fil. Du kan forhåndskonfigurere separat et mål for hver formatkonfigurasjon og utdatakomponent (en mappe eller en fil). Brukere som har riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>Salgssted – Microsoft Dynamics AX Retail

| Hva kan du gjøre? | Hvorfor er dette viktig? |
|------------------|------------------------|
| Bruk Google Chrome-nettleseren. | Forhandlere kan nå starte Skysalgssted fra Chrome-nettleseren, og kan bruke alle funksjoner som er tilgjengelige i Microsoft Edge og Internet Explorer-versjonen av Skysalgssted. |

## <a name="financial-reporting"></a>Finansrapportering

| Hva kan du gjøre? | Hvorfor er dette viktig? |
|------------------|------------------------|
| Bygg data for finansrapportering på nytt. | Når du flytter Dynamics AX-databasene mellom miljøer eller gjør andre omfattende endringer i miljøet, kan det hende den økonomiske rapporteringsdatabasen må bygges på nytt. Et Windows PowerShell-skript følger nå med for å bygge databasen på nytt for deg. |
| Du kan ikke lenger velge alternativer for rapportutforming som ikke er gyldige. | Flere alternativer for rapportutforming som ble brukt i markedsversjoner av Management reporter, gjelder ikke for denne versjonen av Dynamics AX. Disse alternativene er knyttet til økonomisk rapportutforming, utdata og kobling. Disse alternativene er fjernet fra Utforming av finansrapport for å hindre at brukerfeil. |

## <a name="financial-management"></a>Økonomistyring

| Hva kan du gjøre? | Hvorfor er dette viktig? |
|------------------|------------------------|
| Generer positive pay-filer for leverandørbetalinger. | Positive pay-filer kan genereres for å hjelpe banker med å forhindre sjekksvindel. |

## <a name="warehouse-and-production"></a>Lager og produksjon

<table>
<thead>
<tr>
<th>Hva kan du gjøre?</th>
<th>Hvorfor er dette viktig?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definere en arbeidspolicy for lager som styrer opprettingen av arbeidet for sett produkter på bestemte lokasjoner.</td>
<td>Lagerprosesser inkluderer ikke alltid arbeid. Ved å bruke den nye arbeidspolicyen for lager, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</td>
</tr>
<tr>
<td>Angi at en målplassering for produksjon ikke styres av nummerskilt.</td>
<td>Du kan nå angi at en målplassering for produksjon ikke styres av nummerskilt. Denne funksjonen er for eksempel nyttig når en foregående produksjonsordre rapporterer varer som ferdige direkte til en lokasjon som fungerer som produksjonsinnleveringslokasjon for en etterfølgende produksjonsordre.</td>
</tr>
<tr>
<td>Støtte for stykklister som inneholder varer med ulike produktdimensjoner av den samme varen.</td>
<td>Når du bruker ett eller flere av produktdimensjonene i produksjon, kan det oppstå situasjoner der du vil produsere en vare basert på en annen variant av den samme varen. Hvis du vil ha mer informasjon, kan du se <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">denne bloggen</a>.</td>
</tr>
<tr>
<td>Produksjonsordrer med sirkelstrukturer på første nivå av stykklistene, utelates fra stykklistenivåberegning for planlegging av materialressurs.</td>
<td>Det er ikke mulig å tilordne riktige stykklistenivåer til produktvarianter for produksjonsordrer som kan forårsake sirkularitet i stykklistehierarkiet.</td>
</tr>
<tr>
<td>Beregne separate stykklistenivåer for planlegging av materialressur og kostnadsberegning:
<ul>
<li>For planlegging av materialressurs beregnes stykklistenivåer i den nye <strong>ReqItemLevel</strong>-tabellen. Avsluttede produksjonsordrer ignoreres i beregningen.</li>
<li>For beregning av produksjonskostnader, beregnes stykklistenivåer i <strong>InventTable</strong>. Avsluttede produksjonsordrer inkluderes i beregningen.</li>
</ul>
</td>
<td>
<ul>
<li>Når du kjører planlegging av materialressurser, for eksempel hovedplanlegging, planlegging og nedbryting, må bare stykklistenivåer for planlegging av materialressurs beregnes på nytt. Det er med andre ord ikke nødvendig å beregne stykklistenivåer som brukes for etterkalkulering av produksjon.</li>
<li>Når du kjører etterkalkuleringsoperasjoner, for eksempel lageravslutning, må bare stykklistenivåer som brukes for etterkalkulering av produksjonen beregnes på nytt.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Tilleggsressurser

[Hva er nytt eller endret?](whats-new-changed.md)

[Nye eller oppdaterte oppgaveveiledninger (mai 2016)](new-updated-task-guides-available-may-2016.md)

