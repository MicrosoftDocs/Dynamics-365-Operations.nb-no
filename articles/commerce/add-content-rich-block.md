---
title: Tekstblokkmodul
description: Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 93ad09a05d188a30b099b9a44c35e15839be80a7
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411141"
---
# <a name="text-block-module"></a>Tekstblokkmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En tekstblokkmodul er en modul som brukes til å legge til tekstinnhold. Dette innholdet kan være informasjon eller kampanje.

Tekstblokkmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side. De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Eksempler på tekstblokkmoduler i e-handel

Tekstblokkmoduler kan brukes på følgende måter:

* For å vise produktfunksjoner på en produktdetaljside.
* Til informasjonsformål på en hvilken som helst side. De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.
* Legge til egendefinerte meldinger på en produktdetaljside. (for eksempel "Gratis levering ved bestilling over 500 kroner").
* For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").

Bildet nedenfor viser et eksempel på en tekstblokkmodul som brukes på en hjemmeside.

![Eksempel på en tekstblokkmodul](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Egenskaper for tekstblokkmodul

| Egenskapsnavn     | Verdi                                            | beskrivelse |
|-------------------|--------------------------------------------------|-------------|
| Rik tekst         | Rik tekst                                        | Avsnittstekst. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst. |
| Egendefinert klassenavn | Et CSS-klassenavn (Cascading Style Sheets)        | Navnet på en egendefinert CSS-klasse som en utvikler tilbyr for å formatere denne modulen. Klassenavnet bør defineres i temapakken. |
| Skriftstørrelse         | **Liten**, **middels**, **stor** eller **ekstra stor** | Skriftstørrelse for innholdet. |

## <a name="add-a-text-block-module-to-a-page"></a>Legge til en tekstblokkmodul på en side

Hvis du vil legge til en tekstblokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Innholdsmal**.
1. I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I **Velg en mal**-dialogboksen velger du **Innholdsmal**. Under **Sidenavn** angir du **Innholdsside**, og velger deretter **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**. 
1. I egenskapsruten for tekstblokkmodulen legger du til tekst i feltet **Rik tekst**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Promobannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsblokkmodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)

