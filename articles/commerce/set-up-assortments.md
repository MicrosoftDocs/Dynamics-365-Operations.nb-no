---
title: Definere sortimenter
description: Denne artikkelen beskriver hva et utvalg er, og forklarer hvordan du setter opp sortimenter i Dynamics 365 Commerce.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 447c5f580e5d925efbfeaabc3890e2d67f9688f5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344353"
---
# <a name="set-up-assortments"></a>Definere sortimenter

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hva et utvalg er, og forklarer hvordan du setter opp sortimenter i Dynamics 365 Commerce.

Et sortiment er et utvalg av beslektede produkter som du tilordner en handelskanal, for eksempel en fysisk butikk eller en nettbutikk. Sortimenter brukes til å identifisere produktene som er tilgjengelige i hver butikk. Et sortiment kan omfatte kategorier av produkter. Alle produkter som tilordnes til en bestemt kategori, inkluderes derfor i sortimentet. Et sortiment kan også inkludere bestemte produkter og bestemte varianter av produkter. Ved å sette opp et sortiment kan du tilordne tusenvis av produkter til handelskanaler samtidig, i enhver kombinasjon som butikkene ønsker. Du kan definere så mange produktsortimenter du trenger. Hvert produkt kan inkluderes i én eller flere sortimenter, og hvert sortiment kan tilordnes til én eller flere kanaler. Du definerer for eksempel et sortiment som inneholder et grunnleggende sett med produkter. Alle butikker får dette sortimentet. Deretter definerer du et nytt utvalg som bare inneholder store sportsartikler. Bare større butikker får dette sortimentet. Diagrammet nedenfor viser hvordan produktene kan tilordnes til sortimenter, og hvordan disse sortimentene kan tilordnes til kanaler.

![Produktsortimentsrelasjoner.](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Forutsetninger

Før du kan definere et sortiment og tilordne det til en handelskanal, må du fullføre følgende oppgaver.

| Oppgave                              | Beskrivelse |
|-----------------------------------|-------------|
| Definere en kanal.          | Kanaler representerer fysiske butikker, nettbutikker eller markedsplasser på Internett. Du må definere minst én kanal og konfigurere alternativene for butikken. Sortimenter tilordnes til butikker for å identifisere produktene som en bestemt butikk fører. |
| Opprett et organisasjonshierarki. | Når du definerer handelskanalene for organisasjonen, må du konfigurere et organisasjonshierarki som representerer organisasjonsstrukturen i kanalene. Et organisasjonshierarki kan brukes for sortimenter, etterfyllinger og rapportering. Ved å legge til kanaler i et organisasjonshierarki kan du tilordne sortimenter til grupper av butikker. I stedet for å tilordne sortimentet individuelt for hver butikk, kan du tilordne sortimentet til organisasjonsnoden på høyt nivå. Når en ny kanal er lagt til organisasjonsnoden på høyt nivå, arver denne kanalen automatisk alle sortimenter som ble tilordnet til organisasjonsnoden på høyt nivå. Du kan bare tilordne sortimenter til kanaler som er inkludert i et organisasjonshierarki som er tilordnet **Handelsortiment**-formålet. |
| Definer produkter.                  | Før du legger til produkter i et sortiment må du legge dem til i Commerce. Du kan legge til produkter manuelt, eller du kan importere dem fra en leverandør. Når du har lagt produktene, må du frigi dem til en juridisk enhet. Det er bare produkter som er frigitt til en juridisk enhet som kan gjøres tilgjengelig for kanalene. Produkter som ennå ikke er frigitt til en juridisk enhet, kan legges til et sortiment, og sortimentet kan godkjennes. Før produktene er frigitt til en juridisk enhet, kan de imidlertid ikke gjøres tilgjengelige for kanalene. |
| Definer et kategorihierarki.      | Når du oppretter handelsproduktene, kan du gruppere og kategorisere dem ved hjelp av funksjonen for kategorihierarki. Du kan opprette ett kjernehierarki for å gruppere og kategorisere alle produkter som distribueres gjennom kanalene. Du kan også opprette ekstra kategorihierarkier separat hvis du vil gruppere eller kategorisere produktene til spesielle formål, for eksempel kampanjer eller sortimenter. Du kan tilordne alle produktene i en bestemt kategori til et sortiment ved å bruke kategorihierarkier. Produkter som legges til kategorien som er inkludert i sortimentet, inkluderes automatisk i sortimentet. Neste gang sortimentsplanleggeren kjøres, blir disse produktene tilgjengelige for kanalene som sortimentet er tilordnet til. |

## <a name="setting-up-an-assortment"></a>Definere et sortiment

Når du har fullført forhåndskravene, kan du opprette et sortiment og tilordne det til kanalene. Du må fullføre følgende oppgaver hvis du vil definere et sortiment.

1. Opprett et nytt sortiment eller kopier et eksisterende sortiment.
2. Velg kanalene eller gruppene på høyt nivå for kanaler som sortimentet gjelder for.
3. Legg til produktkategorier, individuelle produkter eller produktvarianter i sortimentet. Du kan inkludere alle produkter i en bestemt kategori, eller du kan utelate bestemte produkter fra en kategori som er inkludert i sortimentet.
4. Publiser sortimentet. Når du publiserer et sortiment, kjøres sortimentsplanleggeren automatisk. Denne prosessen genererer listen over produkter. Når denne prosessen er fullført, blir produktene tilgjengelige i kanalene som produktsortimentet er tilordnet til. Hvis du endrer et sortiment som er publisert, eller kanalene som sortimentet er tilordnet til, må sortimentet oppdateres. Du kan kjøre sortimentsplanleggeren som en satsvis jobb for å oppdatere sortimentet ved endringer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]