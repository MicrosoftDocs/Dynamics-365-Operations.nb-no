---
title: Opprette oppgavelister og legge til oppgaver
description: Dette emnet beskriver hvordan du oppretter oppgavelister og legger til oppgaver i dem i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e7964181a739a8138011abca77d0321d819e0a98
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354499"
---
# <a name="create-task-lists-and-add-tasks"></a>Opprette oppgavelister og legge til oppgaver

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter oppgavelister og legger til oppgaver i dem i Microsoft Dynamics 365 Commerce.

En *oppgave* definerer en bestemt del av arbeidet eller en handling som noen må fullføre på eller før en angitt forfallsdato. I Dynamics 365 Commerce kan en oppgave inneholde detaljerte instruksjoner og informasjon om en kontaktperson. Den kan også inneholde koblinger til Back-Office-operasjoner, salgsstedsoperasjoner (POS) eller områdesider, for å forbedre produktiviteten og gi den konteksten som oppgaveeieren trenger for å fullføre oppgaven effektivt.

En *oppgaveliste* er en samling oppgaver som må fullføres som en del av en forretningsprosess. Det kan for eksempel finnes en oppgaveliste som en ny arbeider må fullføre under opplastingen, en oppgaveliste for kasserere som arbeider kveldsskift, eller en oppgaveliste som må fullføres for å forberede butikken for en forestående høytid. I Commerce kan alle oppgavelister som har en måldato, tilordnes til et hvilket som helst antall butikker eller ansatte, og den kan konfigureres til å gjentas.

Både ledere og arbeidere kan opprette oppgavelister i Commerce Back Office, og deretter tilordne dem til et sett med butikker.

## <a name="create-a-task-list"></a>Opprett en oppgaveliste

Hvis du vil opprette en oppgaveliste, gjør du følgende:

1. Gå til **Retail og Commerce \> Oppgavebehandling \> Administrasjon av oppgavebehandling**.
1. Velg **Ny**, og angi deretter verdier i feltene **Navn**, **Beskrivelse** og **Eier**.
1. Velg **Lagre**.

## <a name="add-tasks-to-a-task-list"></a>Legge til oppgaver i en oppgaveliste

Hvis du vil legge til oppgaver i en oppgaveliste, følger du disse trinnene.
 
1. På hurtigfanen **Oppgaver** i en eksisterende oppgaveliste velger du **Ny** for å legge til en oppgave.
1. I dialogboksen **Opprett en ny oppgave** skriver du inn et navn på oppgaven i **Navn**-feltet.
1. I feltet **Forfallsdato samsvarer ikke med måldato** angir du en positiv eller negativ heltallsverdi. Angi for eksempel **-2** hvis oppgaven skal fullføres to dager før oppgavelistens forfalls dato.
1. I feltet **Merknader** angir du detaljerte instruksjoner.
1. I feltet **Kontaktperson** angir du navnet på en emneekspert som oppgaveeieren kan kontakte hvis oppgaveeieren trenger hjelp.
1. I feltet **Oppgavekobling** angir du en kobling basert på typen oppgave.

> [!TIP]
> Selv om du kan bruke feltet **Tilordnet til** til å tilordne oppgaver til noen når du oppretter en oppgaveliste, anbefaler vi at du unngår å tilordne oppgaver når oppgavelisten opprettes. Du må i stedet tilordne oppgavene etter at listen er opprettet for enkeltbutikker.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Bruke oppgavekoblinger til å forbedre arbeiderproduktiviteten

Med Commerce kan du koble oppgaver til bestemte POS-operasjoner, for eksempel å kjøre en salgsrapport, vise en elektronisk opplæringsvideo for orientering til ansatte eller utføre en Back-Office-operasjon. Denne funksjonen hjelper oppgaveeiere med å få den informasjonen de trenger for å fullføre en oppgave effektivt.

Hvis du vil legge til oppgavekoblinger mens du oppretter en oppgave, følger du disse trinnene.

1. På hurtigfanen **Oppgaver** i en eksisterende oppgaveliste velger du **Rediger**.
1. I dialogboksen **Rediger oppgave**, i feltet **Oppgavekobling** velger du ett eller flere av følgende alternativer:

    - Velg **Menyelement** for å konfigurere en Back-Office-operasjon, for eksempel "Produktsett".
    - Velg **POS-operasjon** for å konfigurere en POS-operasjon, for eksempel "Salgsrapporter".
    - Velg **URL-adresse** for å konfigurere en absolutt URL-adresse.

Følgende illustrasjon viser valget av oppgavekoblinger i dialog boksen **Rediger oppgave**.

![Velge oppgavekoblinger i dialogboksen Rediger oppgave.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Konfigurere en POS-operasjon slik at den kan kobles til en oppgave

Gjør følgende for å konfigurere en POS-operasjon slik at den kan kobles til en oppgave.

1. Gå til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> POS-operasjoner**.
1. Velg **Rediger**, finn POS-operasjonen, og merk deretter av for **Aktiver oppgavebehandling** for den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over oppgavebehandling](task-mgmt-overview.md)

[Konfigurere oppgavebehandling](task-mgmt-configure.md)

[Tilordne oppgavelister til butikker eller ansatte](task-mgmt-assign-lists.md)

[Oppgavebehandling på salgsstedet](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
