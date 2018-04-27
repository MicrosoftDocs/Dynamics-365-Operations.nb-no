---
title: Rapportdefinisjoner i Utforming av finansrapport
description: "Denne artikkelen gir informasjon om rapportdefinisjoner. En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58030df8db467f754ec93ecc3f41585b20f03893
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinisjoner i Utforming av finansrapport

[!INCLUDE [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om rapportdefinisjoner. En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport. 

En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også flere alternativer og innstillinger for å tilpasse en rapport. Når du har definert raddefinisjoner og kolonnedefinisjoner, må du kombinere dem i en rapportdefinisjon. Nå kan du også definere andre deler av definisjonene, for eksempel detaljnivået og rapportdatoen. Du kan deretter lagre og generere en rapport. Finansrapportering tilbyr følgende detaljnivåer for rapportering:

-   Økonomisk
-   Økonomisk og konto
-   Økonomisk, konto og transaksjon

Det kan imidlertid hende at transaksjonsdetaljer ikke er tilgjengelig i rapporter, avhengig av hvordan dataene er lagret i Microsoft Dynamics ERP-systemet.

## <a name="create-a-report-definition"></a>Opprette en rapportdefinisjon
1.  Gå til **Fil** -menyen i Rapportutforming og klikk **Ny**, og velg deretter **Rapportdefinisjon**.
2.  Angi riktig informasjon i kategoriene **Rapport**, **Utdata og distribusjon**, **Topptekst og bunntekst** og **Innstillinger**.

## <a name="contents-of-a-report-definition"></a>Innholdet i en rapportdefinisjon
Tabellen nedenfor beskriver kategoriene i en rapportdefinisjon og hvordan informasjonen brukes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabulator</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rapporter</td>
<td>Opprett en rapport, konfigurer en rapport eller endre en eksisterende rapport.</td>
</tr>
<tr class="even">
<td>Utdata og distribusjon</td>
<td>Endre utdatatype og mål for rapporten.</td>
</tr>
<tr class="odd">
<td>Topptekst og bunntekst</td>
<td>Definer og formater topptekst og bunntekst for rapporten. Du kan for eksempel legge til tekst eller bilder i toppteksten eller bunnteksten. Finansrapportering støtter BMP-, JPG- og PNG-filer for bilder. Du kan også legge til autotekstkoder for å sette inn tilleggsinformasjon, for eksempel et firmanavn, rapportnavn eller sidetall.</td>
</tr>
<tr class="even">
<td>Innstillinger</td>
<td>Angi innstillinger for rapportdefinisjon, for eksempel følgende innstillinger:
<ul>
<li>Formatering og avrundingsbeløp</li>
<li>Formater detaljrapporter</li>
<li>Formater rapporteringtrær</li>
<li>Generer unntaksrapport</li>
<li>Angi valutaomregning</li>
<li>Delsum- og filterkontodetaljer</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Se også
--------

[Finansrapportering](financial-reporting-intro.md)




