---
title: Definere prosjektressurser
description: Dette emnet gir informasjon om hvordan du konfigurerer eller ber om prosjektressurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760628"
---
# <a name="set-up-project-resources"></a>Definere prosjektressurser

[!include [banner](../includes/banner.md)]

Du må opprette en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet. Under kalenderoppsett kan prosjektledere gjøre ressursnivåering som en del av ressursoptimalisering. Basert på kalenderplanen kan restriksjoner legges på ressurser. Du kan opprette en kalender på siden **Kalendere**.

Når du setter opp en arbeidstaker som en prosjektressurs, kan du velge blant arbeidere som jobber i selskapet som du setter opp ressurser til. Alternativt kan du velge arbeidstakere fra andre selskaper i organisasjonen din. Disse arbeidstakere er kjent som konserninterne ressurser.

Følgende prosedyrer forklarer hvordan du setter opp en arbeidstaker som en prosjektressurs i firmaet ditt, og hvordan du oppretter en konsernintern prosjektressurs.

## <a name="set-up-a-worker-as-a-project-resource"></a>Definere en arbeider som en prosjektressurs

1. I **Arbeidere**-listen på siden **Arbeidere**, velger du arbeideren som du legger til som en prosjektressurs, og åpner arbeiderposten.
2. På Handling-panelet velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.
3. Velg en kalender, og lukk deretter siden.

Du kan også angi standardprosjekter for en ressurs som en type førtilordning. Førtildelinger kan brukes når ressursansvarlig eller prosjektleder vet hvilke prosjekter som ressursen vil arbeide med på forhånd. Førtildelinger kan også være basert på forespørsel fra en prosjektsponsor eller kunde. Hvis du vil førtilordne et prosjekt, på siden **Tilordne prosjekter** i kategorien **Prosjekter** i lsietn **Gjenværende prosjekter**, velger du det aktuelle prosjektet.

## <a name="set-up-an-intercompany-resource"></a>Definere en konsernintern ressurs

Når du setter opp en arbeidstaker som en konsernintern ressurs, må du fullføre oppsettet i både utlånsfirmaet og lånefirmaet.

### <a name="in-the-lending-company"></a>I utlånsselskapet

1. Kontroller at utlånsfirmaet er valgt i Finance, og fullfør deretter prosedyren i forrige avsnitt, «Sett opp en arbeidstaker som en prosjektressurs».
2. På siden **Konserninternt regnskap**, velg **Ny**.
3. I feltet **ID for juridisk enhet**, velg utlånsselskapet. Fyll ut de resterende feltene etter behov, og velg deretter **Lagre**.
4. På siden **Overføringspris**, velg **Ny**.
5. I feltet **Lånende juridisk enhet**, velg riktig selskap.
6. For å låne kun den ressursen du opprettet i begynnelsen av denne delen fra utlånsselskapet, gå til feltet **Ressurs**, og velg navnet på ressursen du har opprettet. For å gjøre alle ressurser i det lånende selskapet tilgjengelig til utlånsselskapet lar du feltet **Ressurs** være tomt.
7. På siden **Parametere for prosjektledelse og regnskap**, i kategorien **Konsernintern**, velg **Aktiver konsernintern ressursplanlegging og tidsskjemaer**-alternativet som **Ja**.

### <a name="in-the-borrowing-company"></a>I det lånende selskapet

- I søkefiltere på siden **Ressursliste**, skriv inn navnet på den ressursen du har opprettet for det lånende selskap for å bekrefte at navnet er inkludert i ressurslisten for det lånende selskap.

## <a name="request-project-resources"></a>Be om prosjektressurser
Funksjonaliteten for prosjektressursplanlegging lar kun ressursforvaltere distribuere bemannede ressurser på engasjementer eller prosjekter. For å aktivere denne funksjonaliteten, fullfør følgende oppgaver, eller bekreft at de er fullført:

- Definer nummerserier.
- Definer arbeidsflyter for prosjektstyring og regnskap.
- Aktiver arbeidsflyten for ressursforespørsel.

Etter at de foregående oppgavene er fullført, kan du fullføre følgende oppgaver som du trenger:

- Opprett en ressursforespørsel fra en ikke-forpliktende bemannet ressurs.
- Overvåk ressursforespørsler.
- Oppfyll ressursforespørsler.
- Etterspør en bemannet ressurs fra en WBS.
- Bestill ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.
