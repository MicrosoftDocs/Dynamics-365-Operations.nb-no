---
title: Arbeide med fragmenter
description: Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 017cdc76368ae4f80131471a289aa03ab06c99bf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350214"
---
# <a name="work-with-fragments"></a>Arbeide med fragmenter 

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvorfor, når og hvordan du bruker fragmenter i Microsoft Dynamics 365 Commerce.

Fragmenter muliggjør en sentralisert redigeringsopplevelse for modulkonfigurasjoner som må brukes på nytt på hele området. Topptekst, bunntekst og bannere er for eksempel ofte konfigurert som fragmenter, fordi de deles på tvers av mange sider. Du kan betrakte fragmenter som små websider som kan settes inn i andre sider på området. Fragmenter har sin egen livssyklus. De opprettes, refereres til, oppdateres og slettet med andre ord som uavhengige enheter i redigeringsverktøyene.

Når fragmentene er konfigurert, kan de brukes overalt der moduler kan brukes i områdestrukturen. Fragmenter kan refereres til på sider, i oppsett, i maler og i andre fragmenter.

> [!NOTE]
> Fragmenter kan nestes opp til sju nivåer i andre fragmenter.

Hvis du for eksempel vil fremme en sesonghendelse på mange sider på området, kan du bruke et fragment. Det første trinnet i prosessen med å opprette et nytt fragment er å velge typen modul du vil starte fra. I dette eksemplet kan du bygge fragmentet fra en hovedbannermodul.

> [!NOTE]
> Fragmenter kan bygges fra en hvilken som helst modultype.

Du kan deretter konfigurere hovedbannerfragmentet med ditt bestemte kampanjeinnhold. Du kan også lokalisere den slik du ønsker. Det nye fritt stående hovedbannerfragmentet kan deretter brukes som en forhåndskonfigurert modul i området. Det er enkelt å legge den til i maler, til bestemte sider eller til andre fragmenter som kan inneholde hovedbannermoduler.

Alle steder der fragmentet legges til, er referanser til det sentrale hovedbannerfragmentet du opprettet. Hvis du publiserer endringer i fragmentet, vises disse endringene umiddelbart på alle steder der fragmentet blir referert på tvers av området. Fragmenter kan derfor være en virkningsfull og effektiv måte å bruke modulkonfigurasjoner på nytt og administrere modulkonfigurasjoner på et område sentralt. Ved å bruke dem på en effektiv måte kan du øke allsidigheten betraktelig og redusere kostnadene som er knyttet til administrasjon av områdeinnhold.

Illustrasjonen nedenfor viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.

![En illustrasjon som viser hvordan fragmenter kan brukes til å sentralisere redigering av delte modulkonfigurasjoner på tvers av et e-handelsområde.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Opprette et fragment

Du kan enten opprette et nytt fragment eller lagre en eksisterende modulkonfigurasjon som et fragment.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Lagre en eksisterende modulkonfigurasjon som et fragment

Følg denne fremgangsmåten for å konvertere en tidligere konfigurert modul til et fragment i Commerce-områdebyggeren som kan brukes på nytt.

1. Åpne en side eller mal som inneholder modulen du vil konvertere til et fragment.
1. I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du den tidligere konfigurerte modulen.
1. Velg ellipsen (**...**) ved siden av navnet på modulen enten i disposisjonsruten eller den valgte modulens verktøylinje i den visuelle sidebyggeren. 
1. Velg **Del som fragment**. 
1. I dialogboksen **Lagre som fragment** angir du et navn på fragmentet.
1. Velg **OK** for å lagre modulkonfigurasjonen som et fragment som kan legges til andre sider.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Opprett et nytt fragment

Følg denne fremgangsmåten for å opprette et nytt fragment i Commerce-områdebygger.

1. Velg **Fragmenter** i navigasjonsruten til venstre.
1. Velg **Ny**. Det vises en dialogboks **Nytt fragment** som viser alle de tilgjengelige modultypene. Som ble nevnt tidligere kan fragmenter opprettes fra en hvilken som helst modultype.
1. Velg en modultype for fragmentet.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Når du velger en generisk containermodultype, får du størst fleksibilitet når du må oppdatere og konfigurere fragmentet senere.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Legge til, fjerne eller redigere fragmenter på en side

Følgende prosedyrer beskriver hvordan du legger til, fjerner eller redigerer fragmenter.

### <a name="add-a-fragment"></a>Legg til et fragment

Følg denne fremgangsmåten for å legge til et fragment i en side i Commerce-områdebygger.

1. I disposisjonsruten til venstre eller direkte i den visuelle sidebyggeren, velger du en container eller et spor der underordnede moduler kan legges til.
1. Velg ellipsen (**...**) ved siden av navnet på containeren eller sporet.  Hvis du bruker den visuelle sidebyggeren, kan du eventuelt velge plusstegnet (**+**).  
1. Velg **Legg til fragment**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Hvis containeren eller sporet ikke støtter nye underordnede moduler, er alternativet **Legg til fragment** ikke tilgjengelig.
    
1. Søk etter og velg et fragment du vil legge til, i dialogboksen **Velg fragment**. Hvis det ikke finnes noen tilgjengelige fragmenter, kan det være at du først må opprette et fragment fra en modultype som valgt container eller spor støtter.
1. Velg det ønskede fragmentet for å legge det til i containeren eller sporet på siden.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Modulene som er tillatt i en container eller et spor, er definert av malen for siden eller modulenes egne definisjoner.

### <a name="remove-a-fragment"></a>Fjerne et fragment

Hvis du vil fjerne et fragment fra et spor eller en container på en side i Commerce-områdebyggeren, følger du denne fremgangsmåten.

1. I disposisjonsruten til venstre velger du ellipsen (**...**) ved siden av navnet på fragmentet som skal fjernes, og deretter velger du papirkurvsymbolet.  Du kan også velge fragmentet i den visuelle sidebyggeren og velge papirkurvsymbolet på verktøylinjen til fragmentet.
1. Når du blir bedt om å bekrefte at du vil fjerne fragmentet, velger du **OK**.

> [!NOTE]
> Når du fjerner et fragment fra en side, fjerner du bare referansen til det fra den siden. Du sletter **ikke** fragmentet fra området ditt. Hvis du vil slette fragmenter fra området, må du bruke brukergrensesnittet for fragmentinspeksjonen. Du kan bare slette fragmenter fra et område hvis de ikke er referert til av sider, maler eller andre fragmenter.

### <a name="edit-a-fragment"></a>Redigere et fragment

Hvis du vil redigere fragmenter, må du bruke brukergrensesnittet for fragmentredigering. Denne begrensningen er standard. Den hjelper til med å garantere at forfattere ikke forveksler prosessen med å redigere modulene for en bestemt side med prosessen med å redigere fragmenter som kan deles på mange sider.

Følg denne fremgangsmåten for å redigere et nytt fragment i Commerce-områdebygger.

1. Velg **Fragmenter** i navigasjonsruten til venstre.
1. Under **Fragmenter** velger du fragmentet du vil redigere.
1. Rediger fragmentets modulegenskaper og struktur etter behov. Prosessen ligner på redigeringsprosessen for moduler som redigeres i sideredigeringsvisning.

Du kan også redigere et fragment ved å velge det på en side, i en mal, eller i et overordnet fragment, og deretter velge **Rediger fragment** i egenskapsruten til høyre.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med maler](work-with-templates.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)

[Arbeide med publiseringsgrupper](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
