---
title: Tekstblokkmodul
description: Denne artikkelen dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270489"
---
# <a name="text-block-module"></a>Tekstblokkmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

En tekstblokkmodul er en modul som brukes til å legge til tekstinnhold. Dette innholdet kan være informasjon eller kampanje.

Tekstblokkmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side. De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Eksempler på tekstblokkmoduler i e-handel

Tekstblokkmoduler kan brukes på følgende måter:

* For å vise produktfunksjoner på en produktdetaljside.
* Til informasjonsformål på en hvilken som helst side. De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.
* Legge til egendefinerte meldinger på en produktdetaljside. (for eksempel "Gratis levering ved bestilling over 500 kroner").
* For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").

Bildet nedenfor viser et eksempel på en tekstblokkmodul som brukes på en hjemmeside.

![Eksempel på en tekstblokkmodul.](./media/ecommerce-textblock.PNG)

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
1. I dialogboksen **Legg moduler** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du en **Innholdside**, og velger deretter **Neste**.
1. Velg **Innholdsmal** under **Velg en mal**, og velg deretter **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du har behov for å redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**. 
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Tekstblokk**-modulen, og deretter velger du **OK**. 
1. I egenskapsruten for tekstblokkmodulen legger du til tekst i feltet **Rik tekst**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Promobannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsblokkmodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
