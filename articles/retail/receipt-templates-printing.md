---
title: Kvitteringsmaler og utskrift
description: "Denne artikkelen beskriver hvordan du oppretter og endrer skjemaoppsett for å styre hvordan kvitteringer, fakturaer og andre dokumenter blir skrevet ut. Microsoft Dynamics 365 for Retail inneholder en skjemaoppsettutforming der du enkelt og grafisk kan opprette og endre ulike typer skjemaoppsett."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 76cc7f873b99874ef6f2c4bc2ebc3f87fa065647
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="receipt-templates-and-printing"></a>Kvitteringsmaler og utskrift

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver hvordan du oppretter og endrer skjemaoppsett for å styre hvordan kvitteringer, fakturaer og andre dokumenter blir skrevet ut. Microsoft Dynamics 365 for Retail inneholder en skjemaoppsettutforming der du enkelt og grafisk kan opprette og endre ulike typer skjemaoppsett.

**Viktig!** Du må konfigurere skjemaoppsett og kvitteringsprofiler for å skrive ut kvitteringer og andre dokumenter fra moderne salgssted for detaljhandel og skysalgssted. Du kan inkludere flere skjemaoppsett i en kvitteringsprofil. Deretter kan du tilordne kvitteringsprofilen til en skriver ved å endre en maskinvareprofil.

## <a name="set-up-a-receipt-format"></a>Konfigurere en kvitteringsprofil
1.  Klikk på **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Kvitteringsformater**.
2.  På siden **Kvitteringsformat** klikker du **Ny** for å opprette et nytt skjemaoppsett, eller velger et eksisterende skjemaoppsett.
3.  I **Kvitteringsformat**-feltet skriver du inn en ID for skjemaoppsettet, og deretter velger du kvitteringstypen som oppsettet brukes for. Du kan også skrive inn en beskrivelse og et kort navn for kvitteringen i **Tittel**-feltet.
4.  På hurtigkategorien **Generelt** velg et alternativ for å definere virkemåten for utskrift:
    -   **Skrives alltid ut** – Kvitteringen skrives automatisk ut etter behov.
    -   **Ikke skriv ut** – Kvitteringen skrives ikke ut.
    -   **Spør bruker** – Brukeren blir spurt om å skrive ut kvitteringen.
    -   **Etter behov** – Dette alternativet brukes bare for gavekvitteringer. Når dette alternativet er valgt, kan brukeren skrive ut en gavekvittering fra siden **Endre**, hvis en gavekvittering er nødvendig.

## <a name="design-a-receipt-format"></a>Utforme et kvitteringsformat
Bruke skjemaoppsettutformingen til grafisk å opprette oppsettet for skjemadokumentet. Siden **Utforming av kvitteringsformat** består av tre deler: **hode**, **linjer** og **bunntekst**. Noen typer skjemaoppsett bruker elementer fra alle tre delene, mens andre typer bruker elementer fra bare én eller to deler. Hvis du vil vise elementene som er tilgjengelige for hver del, klikker du den aktuelle knappen i navigasjonsruten til venstre på siden.

1.  Klikk på **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Kvitteringsformater**.
2.  På siden **Kvitteringsformat** velger du et skjemaoppsett, og klikk deretter **Utforming**.
3.  Klikk **Kjør** for å installere utformingsverten for detaljhandel.
4.  I varslingsfeltet som vises nederst i Internet Explorer-vinduet, klikker du **Åpne** for å installere ettklikksutformingen. (Varslingsfeltet vises kanskje et annet sted i andre lesere.) Fremdriftsindikatoren viser fremdriften for installasjonen.
5.  Når installasjonen er fullført, angir du Microsoft Dynamics 365 for Retail-brukernavnet og passordet, og klikk deretter på **Logg på** for å starte utformingen.
6.  Når legitimasjonen er validert og utformingen starter, kan du begynne å utforme kvitteringsformatet eller endre et eksisterende format.
7.  Hvis du vil opprette elementene for skjemaet, velger du delen **Hode**, **Linjer** eller **Bunntekst**, og deretter drar du et element fra denne delen til arbeidsområdet. De fleste elementene inneholder variabler som automatisk fylles ut med data fra databasen. Andre elementer, for eksempel **Tekst**, lar deg skrive ut egendefinert tekst på kvitteringen. **Obs!** Du kan angi hvor mange linjer som hver del skal omfatte, ved å justere antallet nederst til høyre i denne delen. For å gjøre det lettere å endre en del kan du øke høyden ved å dra størrelseslinjen nederst i delen. Høyden på delen i arbeidsområdet påvirker ikke antall linjer på selve kvitteringen.
8.  Når du har dratt et element til arbeidsområdet, angir du egenskapene for delen i **Objektinformasjon**-ruten nederst på siden. Angi én eller flere av følgende innstillinger:
    -   **Juster** – Sett justeringen for feltet til **Venstre** eller **Høyre**.
    -   **Fylltegn** – Angi mellomromstegnet. Det brukes et tomt felt som standard, men du kan angi hvilket som helst tegn.
    -   **Prefiks** – Angi verdien som vises i begynnelsen av det valgte feltet. Denne innstillingen gjelder bare for **Linjer**-delen av oppsettet.
    -   **Tegn** – Angi maksimalt antall tegn som feltet kan inneholde hvis elementet har en variabel. Hvis teksten i feltet er lengre enn de antallet tegn du angir, avkortes teksten for å få plass i feltet.
    -   **Variabel** – Det merkes automatisk av for dette alternativet hvis elementet inneholder en variabel og ikke kan tilpasses.
    -   **Skrifttype** – Sett skriftstilen til **Vanlig** eller **Fet**. Fete bokstaver bruker dobbelt så mye plass som vanlige bokstaver. Derfor kan det hende at enkelte tegn blir avkortet.
    -   **Skriftstørrelse** – Sett skriftstørrelsen til **Vanlig** eller **Stor**. Store bokstaver er to ganger høyere enn vanlige bokstaver. Bruk av store bokstaver kan derfor føre til overlappende tekst i kvitteringen.
    -   **Slett** – Klikk denne knappen for å fjerne den valgte delen fra skjemaoppsettet.

## <a name="assign-receipt-profiles"></a>Tilordne kvitteringsprofiler
Kvitteringsprofiler tilordnes direkte til skrivere i maskinvareprofilen.

1.  Åpne maskinvareprofilen ved å klikke på **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofil**.
2.  Velge skriveren, og deretter i feltet **Kvitteringsprofil** tilordne kvitteringsprofilen som skal brukes for kassen.

**Obs!** Hvis det brukes to skrivere, kan én skriver brukes til å skrive ut standard 40-kolonners termiske kvitteringer. Den andre skriveren brukes vanligvis til å skrive ut helsides kvitteringstyper som trenger mer informasjon. Disse kvitteringstypene omfatter kundeordrekvitteringer og kundefakturaer.




