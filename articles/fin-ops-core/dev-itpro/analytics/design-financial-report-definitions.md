---
title: Rapportdefinisjoner i Utforming av finansrapport
description: Denne artikkelen gir informasjon om rapportdefinisjoner.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802559"
---
# <a name="report-definitions-in-financial-report-designer"></a>Rapportdefinisjoner i Utforming av finansrapport

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om rapportdefinisjoner. En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også alternativer og innstillinger for å tilpasse en rapport. 

En rapportdefinisjon er en rapportkomponent (eller byggeblokk) som bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å opprette en rapport. En rapportdefinisjon inneholder også flere alternativer og innstillinger for å tilpasse en rapport. Når du har definert raddefinisjoner og kolonnedefinisjoner, må du kombinere dem i en rapportdefinisjon. Nå kan du også definere andre deler av definisjonene, for eksempel detaljnivået og rapportdatoen. Du kan deretter lagre og generere en rapport. Finansrapportering tilbyr følgende detaljnivåer for rapportering:

- Økonomisk
- Økonomisk og konto
- Økonomisk, konto og transaksjon

Alt etter hvordan data er lagret i Microsoft Dynamics ERP-systemet, kan det hende at transaksjonsdetaljer ikke er tilgjengelige i rapporter.

## <a name="create-a-report-definition"></a>Opprette en rapportdefinisjon
1. Gå til **Fil** -menyen i Report Designer og klikk **Ny**, og velg deretter **Rapportdefinisjon**.
2. Angi riktig informasjon i fanene **Rapport**, **Utdata og distribusjon**, **Topptekst og bunntekst** og **Innstillinger**.

## <a name="contents-of-a-report-definition"></a>Innholdet i en rapportdefinisjon
Tabellen nedenfor beskriver fanene i en rapportdefinisjon og hvordan informasjonen brukes.

<table>
<thead>
<tr>
<th>Tabulator</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rapporter</td>
<td>Opprett en rapport, konfigurer en rapport eller endre en eksisterende rapport.</td>
</tr>
<tr>
<td>Utdata og distribusjon</td>
<td>Endre utdatatype og mål for rapporten.</td>
</tr>
<tr>
<td>Topptekster og bunntekster</td>
<td>Definer og formater topptekst og bunntekst for rapporten. Du kan for eksempel legge til tekst eller bilder i toppteksten eller bunnteksten. Finansrapportering støtter BMP-, JPG- og PNG-filer for bilder. Du kan også legge til autotekstkoder for å sette inn tilleggsinformasjon, for eksempel et firmanavn, rapportnavn eller sidetall.</td>
</tr>
<tr>
<td>Innstillinger</td>
<td>Angi innstillinger for rapportdefinisjon, for eksempel følgende innstillinger:
<ul>
<li>Formatering og avrundingsbeløp</li>
<li>Formater detaljrapporter</li>
<li>Formater rapporteringtrær</li>
<li>Generer unntaksrapport</li>
<li>Angi valutaomregning</li>
<li>Delsum- og filterkontodetaljer</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
