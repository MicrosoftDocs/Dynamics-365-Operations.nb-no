---
title: Arbeide med publiseringsgrupper
description: Denne artikkelen beskriver funksjonen for publiseringsgrupper i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 5a19d25b0b34ea3d452cacdd51ea071747ff1d90
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279012"
---
# <a name="work-with-publish-groups"></a>Arbeide med publiseringsgrupper

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver funksjonen for publiseringsgrupper i Microsoft Dynamics 365 Commerce.

E-handelsnettsteder er kontinuerlig oppdatert med nytt innhold gjennom hele året. Oppdateringer publiseres ofte i grupper rundt travle e-handelshendelser, for eksempel ferier, sesongbaserte markedsføringskampanjer eller kampanjelanseringer. Disse oppdateringene krever ofte at grupper av webområdeinnhold (for eksempler sider, bilder, fragmenter og maler) kan klargjøres, valideres og publiseres samtidig i én enkelt handling.

Muligheten til å gruppere elementer i logiske sett som publiserer elementer sammen, der hvert sett har sin egen livssyklus, gir mange fordeler for områdeforfattere. I Commerce er disse logiske settene kjent som publiseringsgrupper. De lar nettstedsforfattere spore sett med oppdateringer som sine egne konfigurerbare, testbare og publiserbare enheter.

Redigerere kan forhåndsvise oppdateringer i en trinnvis publiseringsgruppe uten å påvirke det publiserte området eller andre publiseringsgrupper som er selvstendige. Forfattere kan deretter planlegge publiseringshandlingen for å publisere alle elementene i publiseringsgruppen samtidig på det aktive området. Muligheten til å gruppere, forhåndsvise og planlegge oppdateringer for publisering er viktig for mange selskaper på foretaksnivå som genererer betydelig årlig omsetning rundt milepæler for hendelsesbasert områdeoppdatering.

Bedrifter kan pådra seg kostnader fra langsomme eller ugyldige innholdsutrullinger som ikke går greit. Publiseringsgrupper bidrar til å garantere at lanseringer organiseres, valideres og publiseres i tide. Enten de er store eller små, gir publiseringsgrupper et verdifullt verktøysett som hjelper forfattere med å organisere og forenkle pågående oppgaver for områdeoppdatering.

## <a name="when-to-use-publish-groups"></a>Når du bør bruke publiseringsgrupper

Du kan bruke publiseringsgrupper når du må klargjøre og publisere flere dokumenter samtidig. Hvis nettstedet for eksempel oppdaterer innhold hver sesong, kan du opprette publiseringsgrupper for disse sesongbaserte markedsføringsbevegelsene. Publiseringsgruppen "Oppdatering høstsesong" kan inneholde nye sesongbilder, fragmenter som inneholder sesongbaserte markedsføringsmeldinger, sider med sesongbaserte produktsamlinger, eller andre sesongbaserte nettstedsoppdateringer.

En fordel med publiseringsgrupper er at du kan klargjøre flere oppdateringer parallelt. Kort tid etter oppdateringen for publiseringsgruppen "Oppdatering høstsesong" kan det for eksempel være en innholdsoppdatering for en bestemt feriehelg. I dette tilfellet kan du klargjøre innhold for publiseringsgruppen "Oppdatering høstsesong" samtidig som du klargjør innhold for en etterfølgende "Oppdatering høstsesong"-publiseringsgruppe. Hver publiseringsgruppe inneholder et unikt sett med sider, bilder, fragmenter, maler og så videre. Du kan sette opp, forhåndsvise og validere disse to publiseringsgruppene uavhengig av hverandre, men på en samtidig tidslinje. Hver publiseringsgruppe kan deretter planlegges å publiseres på området ditt på bestemte datoer og tidspunkter.

## <a name="turn-on-the-publish-groups-feature"></a>Aktivere funksjonen for publiseringsgrupper

Funksjonen publiseringsgrupper er valgfri og må være aktivert for området.

Hvis du vil aktivere funksjonen publiseringsgrupper for området i redigeringsverktøy for handel, følger du denne fremgangsmåten.

1. Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Funksjoner** under **Områdeinnstillinger**.
1. Sett alternativet **Publiseringsgrupper** til **På**.

## <a name="create-a-publish-group"></a>Opprette en publiseringsgruppe

Hvis du vil opprette en publiseringsgruppe for området i redigeringsverktøy for handel, følger du denne fremgangsmåten.

1. Velg **Publiseringsgrupper** i navigasjonsruten til venstre.
1. På den øverste kommandolinjen velger du **Nytt**.
1. Skriv inn et beskrivende navn i dialogboksen **Opprett publiseringsgruppe** under **Navn på publisringsgruppe**. Velg deretter **OK**.

## <a name="set-the-publish-group-authoring-context"></a>Angi redigeringskontekst for publiseringsgruppe

I Commerce er standard redigeringskontekst den aktive områdekonteksten. Redigeringskonteksten for publiserte områder er standardvisningen der du kan vise og gjøre endringer direkte på webområdet uten å bruke en publiseringsgruppe. Den representerer de nyeste direkte oppdateringene til den publiserte versjonen av webområdet ditt. Hvis kontekstkontrollen under **Publiseringsgrupper** i venstre navigasjonsrute viser navnet **Aktivt område**, arbeider du i redigeringskonteksten for aktivt område. **Aktiv område** er standardnavnet på kontekstkontrollen. Hvis ikke viser kontekstkontrollen navnet på en publiseringsgruppe.

Hvis du vil arbeide i en publiseringsgruppe, må du bytte til publiseringsgruppens redigeringskontekst for den. Hvis du vil angi konteksten for publiseringsgruppen, følger du ett av disse trinnene.

- I den venstre navigasjonsruten velger du kontekstkontrollen direkte under **Publiseringsgrupper**, og deretter velger du navnet på publiseringsgruppen i listen over alternativer som vises. Kontekstkontrollen gis nytt navn og viser navnet på publiseringsgruppen.
- Velg **Publiseringsgrupper** i venstre navigasjonsrute, og velg deretter navnet på publiseringsgruppen under **Publiseringsgrupper**. Kontekstkontrollen gis nytt navn og viser navnet på publiseringsgruppen.

Når du har angitt redigeringskonteksten for publiseringsgruppen, arbeider du i denne publiseringsgruppe-konteksten når du forhåndsviser og redigerer områdeinnhold.

Hvis du vil gå tilbake til standard redigeringskontekst for aktive områder, velger du kontekstkontrollen og deretter **Aktivt område**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Legge til sider eller andre elementer i en publiseringsgruppe

Når du har valgt en redigeringskontekst for publiseringsgruppe, og kontekstkontrollen i den venstre navigasjonsruten viser navnet, kan du opprette innhold på samme måte som i standardkonteksten for aktive områder. Du kan også legge til eksisterende sider eller andre elementer fra andre publiseringsgrupper, eller fra den aktive områdekonteksten.

Hvis du vil kopiere eksisterende sider til en publiseringsgruppe, følger du fremgangsmåten nedenfor.

1. Velg redigeringskonteksten du vil kopiere fra, og velg deretter **Sider** i navigasjonsruten til venstre.
1. Velg siden som skal legges til i en publiseringsgruppe.
1. Velg **Kopier til publiseringsgruppe** på kommandolinjen.
1. I dialogboksen **Velg en publiseringsgruppe** velger du publiseringsgruppen du vil legge til siden i, og deretter velger du **OK**.

Du kan bruke de samme grunnleggende trinnene til å opprette tilpassede produktsider, URL-adresser, maler, oppsett, fragmenter og mediebibliotek-ressurser, eller til å legge til eksisterende elementer av disse typene i en publiseringsgruppe.

## <a name="validate-a-publish-group"></a>Validere en publiseringsgruppe

Hvis du vil forsikre deg om at alle avhengigheter i publiseringsgruppeinnhold er oppfylt, og at alle valideringer er sendt, kan du kjøre validering for å identifisere eventuelle problemer som må løses før du planlegger en publiseringshandling.

Hvis du vil validere publiseringsgruppen før du planlegger den, følger du fremgangsmåten nedenfor.

1. Velg **Publiseringsgrupper** i navigasjonsruten til venstre.
1. Velg publiseringsgruppen som skal valideres.
1. På kommandolinjen velger du **Valider**.

Validering kjøres på alt innhold i publiseringsgruppen. Eventuelle problemer som vil hindre en vellykket publiseringshandling, vises i en varslingsboks øverst til høyre.

> [!NOTE]
> Validering kjøres alltid automatisk når en publiseringsgruppe planlegges. **Valider**-knappen på kommandolinjen er imidlertid nyttig fordi den hjelper deg med å identifisere problemer som må rettes opp før du prøver å planlegge at en publiseringsgruppe skal publiseres.

## <a name="schedule-a-publish-group-to-go-live"></a>Planlegge at en publiseringsgruppe skal publiseres

Hvis du vil planlegge at en publiseringsgruppe skal publiseres på området, følger du fremgangsmåten nedenfor.

1. Velg **Publiseringsgrupper** i navigasjonsruten til venstre.
1. Velg publiseringsgruppen som skal planlegges, under **Publiseringsgrupper**.
1. På kommandolinjen velger du **Rediger tidsplan**. Dialogboksen **Rediger tidsplan** vises.
1. Velg datoen og klokkeslettet da publiseringsgruppen skal publiseres, og velg deretter **OK**.

Hvis du vil oppheve planleggingen av en publiseringsgruppe, følger du de samme trinnene, men velger **Opphev planlegging av publiseringsgruppe** i dialogboksen **Rediger tidsplan**.

> [!NOTE]
> Svært store publiseringsgrupper kan ta opptil et minutt eller to for å publiseres når den planlagte tiden kommer. Vær oppmerksom på at en publiseringshandling ikke er umiddelbar, og at mindre publiseringsgrupper vil publiseres raskere.

## <a name="publish-groups-faq"></a>Vanlige spørsmål om publiseringsgrupper

**Hvor mange elementer kan være i en publiseringsgruppe?**

For øyeblikket er det en grense på 2 000 elementer per publiseringsgruppe. Vær oppmerksom på at svært store publiseringsgrupper kan ta minutter for å publiseres når den planlagte tiden kommer.

**Er publiseringsgrupper som kode"grener" i programvareutviklingsterminologi?**

Ja og nei. Publiseringsgrupper kan betraktes som forgrenede versjoner av området. På den måten opptrer de som grener. Det finnes imidlertid ikke noe begrep for en sammenslåing på nivået for enkeltelementer. Elementet som publiseres sist, overskriver bare det som fantes tidligere, og den siste publiseringshandlingen erstatter alltid tidligere publiseringshandlinger.

**Kan jeg planlegge at to publiseringsgrupper skal publiseres samtidig?**

Nei. For ytelses- og konfliktårsaker vil systemet tvinge deg til å forskyve planlagte publiseringsgrupper minst fem minutter fra hverandre.

**Kan jeg bruke publiseringsgrupper til å planlegge omnikanal Back Office-elementer, for eksempel rabatter og produktoppdateringer?**

Publiseringsgrupper-funksjonen støtter for øyeblikket bare webområdeinnhold. Microsoft er imidlertid klar over at integrasjon med Back-Office-varehandelscenarier kan være verdifullt for koordinering og automatisering av lansering av omnikanalkampanjer.

## <a name="additional-resources"></a>Tilleggsressurser

[Måter å legge til innhold på](add-manage-content.md)

[Ordliste for sidemodell](page-elements-overview.md)

[Dokumentere statuser og livssyklus](document-states-overview.md)

[Aktivere og bruke deling på tvers av kanal](cross-channel-sharing.md)

[Arbeide med moduler](work-with-modules.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Tilpasse områdenavigering](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
