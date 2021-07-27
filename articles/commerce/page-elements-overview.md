---
title: Ordliste for sidemodell
description: Dette emnet beskriver de ulike elementene som brukes på sidene på et område for Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4823bec149b7256960752824496ed7958586398
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339389"
---
# <a name="page-model-glossary"></a>Ordliste for sidemodell


[!include [banner](includes/banner.md)]

Dette emnet beskriver de ulike elementene som brukes på sidene på et område for Microsoft Dynamics 365 Commerce.

## <a name="page-element-definitions"></a>Sideelementdefinisjoner

Følgende tabell gir et sammendrag av termene du bør være kjent med når du endrer utseendet, følelsen og innholdet på området. Følg koblingene for mer grundige forklaringer og prosedyrer.

| Semester | Beskrivelse og merknader |
|------|-----------------------|
| [Modul](work-with-modules.md) | <p>**Definisjon:** Moduler er byggeblokker som kan forfattes og utgjør skjelettet til en webside. Eksempler kan være topptekst-, hovedbanner- og karusellmoduler.</p><p>**Hvor den velges:** Distribuerte moduler kan velges og konfigureres i ulike stadier i redigeringsarbeidsflyten for området, for eksempel i redigeringstrinnene for mal, oppsett, side og fragment.</p><p>**Hvor den redigeres:** Egendefinerte moduler opprettes i kode ved hjelp av SDK (Software Development Kit). Deretter lastes de opp til området, der de blir tilgjengelige for valg.</p> |
| Modulegenskap | <p>**Definisjon:** Modulegenskaper er bestemte innstillinger som defineres av modulen. De kan redigeres i redigeringsverktøyene for e-handel. Modulegenskaper brukes for eksempel til å angi overskrifts- og bakgrunnsbildet for en bannermodul.</p><p>**Hvor de konfigureres:** Det velges og konfigureres modulegenskaper i egenskapsruten som vises i redigeringsmiljøene (redigeringsprogrammer) for maler, oppsett, sider, fragmenter og appinnstillinger.</p> |
| [Mal](templates-layouts-overview.md) | <p>**Definisjon:** Maler definerer modulkombinasjonene og alternativene som skal brukes for en kategori med sider (for eksempel markedsføringssider, kategorisider og produktsider).</p><p>**Hvor de velges:** Maler kan velges under opprettingsarbeidsflyter for side eller oppsett.</p><p>**Hvor de redigeres:** Maler redigeres i redigeringsprogrammet for maler. Det kreves ingen kode for å opprette eller endre dem.</p> |
| [Oppsett](templates-layouts-overview.md) | <p>**Definisjon:** Oppsett definerer det endelige utvalget og ordningen av moduler fra settet med alternativer for den overordnede malen. Et oppsett kan konfigureres for en enkelt side (*egendefinert oppsett*), eller den kan deles av flere sider (*forhåndsdefinert oppsett*).</p><p>**Hvor de velges:** Oppsett kan velges ved oppretting av nye sider eller når det er nødvendig med et annet oppsett for en eksisterende side.</p><p>**Hvor de redigeres:** Oppsett redigeres i redigeringsprogrammet for oppsett. Det kreves ingen kode for å opprette eller endre dem.</p> |
| [Sideforekomst](modify-existing-page.md) | <p>**Definisjon:** Sideforekomster definerer det endelige, sidespesifikke lokaliserte innholdet for én enkelt side. Dette innholdet er avledet fra verdiene i modulegenskapene.</p><p>**Hvor de velges:** Sider velges når URL-adresser tilordnes.</p><p>**Hvor de redigeres:** Sider redigeres i redigeringsprogrammet for side. Det kreves ingen kode for å opprette eller endre dem.</p> |
| [Tema](select-site-theme.md) | <p>**Definisjon:** Temaer definerer det gjennomgripende stilarket (CSS) og bestemmer utseendet og funksjonaliteten til modulene som vises på en side.</p><p>**Hvor de velges:** Når et tema lastes opp til området ved hjelp av Microsoft Dynamics Lifecycle Services (LCS), kan det velges som en egenskap for sidecontainermodulen.</p><p>**Hvor de redigeres:** Temaer opprettes og redigeres for øyeblikket ved hjelp av SDK. Deretter lastes de opp til området ved hjelp av LCS.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definisjon:** Fragmenter er fullstendig konfigurerte moduler som har lokalisert innhold som kan brukes på nytt, og sentralt oppdateres på tvers av flere sider. Et fragment som er opprettet fra en topptekstmodul, kan for eksempel brukes i alle maler og på alle sider på tvers av området, og oppdateres sentralt på ett sted.</p><p>**Hvor de velges:** Fragmenter kan velges der moduler kan velges. De kan erstattes for en modul for å bidra til å øke effektiviteten via redigering som er sentralisert og kan brukes på nytt.</p><p>**Hvor de redigeres:** Fragmenter redigeres i redigeringsprogrammet for fragment. Det kreves ingen kode for å opprette eller endre dem.</p> |
| [URL-adresse](create-page-URL.md) | <p>**Definisjon:** Uniform Resource Locator (URL) er adresser som peker til nettsider eller andre URL-adresser.</p><p>**Hvor de velges:** URL-adresser velges hvis det kreves koblinger mellom sider.</p><p>**Hvor de redigeres:** URL-adresser redigeres i redigeringsprogrammet for URL-adresser. Det kreves ingen kode for å opprette eller endre dem.</p> |
| Aktivum | <p>**Definisjon:** Aktiva er binære filer med filtyper som jpg, docx, pdf eller mpg.</p><p>**Hvor de velges:** Aktiva velges som modulegenskaper for moduler som krever dem.</p><p>**Hvor de redigeres:** Aktivva lastes opp, og tilknyttede metadata redigeres i aktivabehandling.</p> |

## <a name="additional-resources"></a>Tilleggsressurser

[Måter å legge til innhold på](add-manage-content.md)

[Dokumentere statuser og livssyklus](document-states-overview.md)

[Arbeide med publiseringsgrupper](publish-groups.md)

[Aktivere og bruke deling på tvers av kanal](cross-channel-sharing.md)

[Arbeide med moduler](work-with-modules.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Tilpasse områdenavigering](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]