---
title: Tekniske versjoner og kategorier for teknisk produkt
description: Denne artikkelen inneholder informasjon om konseptet med tekniske versjoner. Tekniske versjoner sikrer at forskjellige tilstander på et produkt og tilhørende data holdes oppdatert og klare, og at de kan vises i systemet.
author: t-benebo
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a98ead81a61ceac2ed721848847164f76e758f80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872072"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Tekniske versjoner og kategorier for teknisk produkt

[!include [banner](../includes/banner.md)]

Tekniske produkter utvikler seg under produktlivssyklusen, av mange årsaker. Endringer kan for eksempel introduseres for å forbedre produktbetjening, endre en komponent, fordi leverandøren ikke lenger tilbyr den, svare på nye innsikter eller rette feil i den opprinnelige utformingen. Det er også mange grunner til at disse endringene kan lagres som en del av et pågående produkt, slik at tidligere data ikke skrives over. Her er noen av disse årsakene:

- Du vil følge med på produktet mens det ble produsert og levert til kundene i tidligere statuser.
- Du trenger en leveringstid før du godkjenner og bruker endringene.
- Du vil ha et timestamp for hver endring, og du vil kunne levere produkter som er produsert tidligere, fra hverandre.

*Tekniske versjoner* sikrer at ulike tilstander på et produkt og tilhørende data holdes oppdatert og klare, og at de kan vises i systemet. Dette konseptet hjelper deg med å opprettholde konsekvensen, låse stykklisten for produksjon, eliminere variasjon og identifisere endringer på en enkel måte.

Vanligvis brukes regelen for *form-tilpasning-funksjon* til å fastslå om en endring krever et nytt produkt, en ny versjon eller en oppdatering til en eksisterende versjon. Hver av de tre termene i navnet på denne regelen refererer til et bestemt aspekt ved en del, noe som hjelper teknikere med å sammenligne deler etter behov. Denne regelen øker fleksibiliteten i utformingsendringer, fordi det er nødvendig med minimal dokumentasjons- og utformingskostnad for å endre en del, forutsatt at tilpasningen, skjemaet og funksjonen til produktet opprettholdes.

- **Tilpasning** betyr muligheten for delen eller funksjonen til å koble til, pares med, eller bli med i en annen funksjon eller del i en samling. Tilpasning gjør at delen kan oppfylle de nødvendige monteringstoleransene, slik at den kan være nyttig.
- **Form** refererer til egenskaper for en del eller samling, for eksempel eksterne dimensjoner, vekt, størrelse og utseende. Formen er den som mest påvirkes av teknikerens estetiske valg. Den omfatter kapsling, kabinett og kontrollpanel, som blir ansiktet utad for produktet.
- **Funksjon** er et kriterium som oppfylles når delen effektivt og pålitelig utfører tiltenkt formål. I et elektronikkprodukt kan funksjon for eksempel være avhengig av hvilke solid-state-komponenter som brukes, og programvaren eller fastvaren. Ofte kan det også være avhengig av funksjonene til den valgte kapslingen. To av de vanligste grunnene til at en kapsling ikke oppfyller funksjon-kriteriet, er dårlig plassert eller porter med dårlig størrelse, og villedende eller manglende merking. 

## <a name="engineering-versions"></a>Tekniske versjoner

Når du bruker tekniske produkter, har hvert produkt minst én teknisk versjon. Den første tekniske versjonen opprettes automatisk når du oppretter et teknisk produkt. Hver tekniske versjon lagrer de tekniske data som er relevante for denne versjonen. Her er noen eksempler på disse dataene:

- Versjonsnummeret og det forrige versjonsnummeret (hvis det er aktuelt)
- Gyldig fra- og Gyldig til-datoer
- Aktivstatus for produktversjon, som angir om versjonen kan frigis og brukes i transaksjoner (Hvis du vil ha mer informasjon, kan du se [Produktklargjøring](product-readiness.md) .)
- Det tekniske firmaet som opprettet og eier produktet (Hvis du vil ha mer informasjon, kan du se [Tekniske firmaer og dataeierskapsregler](engineering-org-data-ownership-rules.md) .)
- Tilknyttede tekniske dokumenter, for eksempel en monteringshåndbok, brukerveiledninger, bilder og koblinger
- De tekniske attributtene (Hvis du vil ha mer informasjon om tekniske attributter, kan du se [Tekniske attributter og søk i tekniske attributter](engineering-attributes-and-search.md).)
- Stykkliste for tekniske produkter
- Formler for prosessproduksjonprodukter
- De tekniske rutene

Du kan oppdatere disse dataene på en eksisterende versjon, eller opprette en ny versjon ved å bruke en *ordre om teknisk endring*. (Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).) Hvis du oppretter en ny versjon av et produkt, kopierer systemet alle teknisk relevante data til den nye versjonen. Deretter kan du endre dataene for den nye versjonen. På denne måten kan du spore bestemte data for hver påfølgende versjon. Hvis du vil sammenligne forskjellene mellom påfølgende tekniske versjoner, kontrollerer du ordren om teknisk endring, som omfatter endringstyper som angir alle endringer.

Som nevnt opprettes den første tekniske versjonen automatisk når du oppretter et teknisk produkt. Versjonsnummeret for denne versjonen følger versjonsnummerregelen som er definert i den tekniske kategorien for produktet. Hvis du vil gå over til en senere versjon, må du legge til produktet i en ordre om teknisk endring som en linje, og du må sette **Innvirkning**-feltet til *Ny versjon*. Ordren om teknisk endring vil inneholde informasjon om endringen fra gjeldende versjon til den neste versjonen.

Legg merke til at et teknisk produkt bare kan være i én ordre om teknisk endring om gangen. Denne begrensningen sikrer nøyaktigheten av data og bidrar til å unngå overlappende eller motsigende endringer i produktet. Legg også merke til at **Tekniker**-feltet i **Topptekst**-visningen for ordre om teknisk endring viser teknikeren som er ansvarlig for endringsordren. Hvis teknikeren tilhører en gruppe som er definert i systemet, viser feltet **Ansvarlig** lederen for teamet.

## <a name="track-versions-in-transactions"></a>Spor versjoner i transaksjoner

Når du bruker behandling av teknisk endring, inneholder produkthoveddataene alltid én eller flere tekniske versjoner. Ved oppsett av tekniske produkter kan du velge om teknisk versjon også er en del av *logistikktransaksjoner*. (Hvis du vil ha mer informasjon, kan du se [Definer kategorier for teknisk produkt](#product-category) senere i denne artikkelen.) Hvis logistikkinnvirkningen er relevant, er den forskjellig per produkt og per firma. Noen ganger brukes bare den siste versjonen av et produkt. Når du introduserer en ny versjon, kan derfor ikke den tidligere versjonen brukes lenger. I andre tilfeller kreves den forrige versjonen i logistikktransaksjoner for å løse følgende utfordringer:

- Logistikkavdelingen må levere to deler av et produkt til en kunde. I så fall må du bestemme om du vil at to ulike versjoner skal sendes.
- Senere oppdages det at det oppstår et problem, og at den er knyttet til en bestemt endring. I dette tilfellet kan det være nyttig å finne ut nøyaktig hvilken versjon som ble levert i hver ordre.
- Firmaer vil vanligvis levere gamle versjoner først, for å fase dem ut av lageret. Spesielt for produkter med små volumer kan denne fremgangsmåten administreres ved å fastslå gyldighetsdatoene for den nye versjonen i forbindelse med prediksjoner om når lageret av den gamle versjonen blir tomt. Noen ganger kan det imidlertid hende at du ikke kan gjøre denne sammenligningen, eller du kan vurdere at lagernivåprediksjoner er for høy.

Avgjørelsen om å gjøre versjoner synlige i lageret, avhenger av faktorer som tidligere nevnt, pluss firmapraksis og andre hensyn som er spesifikke for hvert firma. Du kan angi virkemåten for *kategorien for teknisk produkt*. Den vil deretter gjelde for alle produkter som opprettes fra denne kategorien, for alle firmaer som produktet er frigitt til.

For produkter som er definert slik at de har en logistikkinnvirkning, må teknisk versjon angis på hver transaksjon. Selv om systemet vil foreslå den *nyeste aktive versjonen*, kan du velge mellom alle de aktive versjonene som er tilgjengelige for firmaet. For produkter som er definert slik at de ikke har en logistikkinnvirkning, er ikke teknisk versjon angitt på transaksjoner. Systemet bruker imidlertid den nyeste aktive versjonen. Når du for eksempel legger til et produkt i en produksjonsstykkliste, vil den nyeste versjonen bli brukt, og når du kjører hovedplanlegging, vil den nyeste versjonen bli antatt.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Konfigurere kategorier for teknisk produkt

En kategori for teknisk produkt gir et grunnlag for oppretting av et bestemt teknisk produkt. Hver kategori etablerer et sett med standardverdier og -policyer. Når du oppretter et teknisk produkt, må du derfor først velge kategorien du vil opprette det fra.

Legg merke til at en ny kategorihierarkitype (*hierarki for teknisk produkt*) automatisk konfigureres for deg. Du kan opprette kategoriene manuelt ved å gå til **Behandling av teknisk endring \> Oppsett \> Detaljer om kategori for teknisk produkt**.

Hver kategori for teknisk produkt etablerer standardvirkemåten til de tekniske produktene som opprettes basert på denne kategorien. Når du har opprettet et teknisk produkt, kan du ikke endre det i kategorien for teknisk produkt. Hvis du imidlertid velger feil kategori, kan du slette produktet og opprette det på nytt.

Når det opprettes en kategori for teknisk produkt, kan du ikke endre følgende innstillinger:

- Teknisk firma
- Produkttype
- Produktets undertype
- Produktdimensjonsgruppe
- Konfigurasjonsteknologi
- Versjonsnummerregel

Andre innstillinger kan arve standardverdier som er konfigurert for kategorien for teknisk produkt. I henhold til systemreglene kan imidlertid disse verdiene endres.

For å arbeide med kategorier for teknisk produkt går du til **Behandling av teknisk endring \> Oppsett \> Detaljer om kategori for teknisk produkt**. Følg deretter ett av disse trinnene.

- Hvis du vil opprette en ny kategori, velger du **Nytt** i handlingsruten, og deretter angir du feltene som beskrevet i følgende underavsnitt.
- Hvis du vil redigere en eksisterende kategori, velger du det i listeruten, velger **Rediger** i handlingsruten og angir deretter feltene som beskrevet i følgende underavsnitt.
- Hvis du vil slette en eksisterende kategori, velger du det i listeruten, og deretter velger du **Slett** i handlingsruten.

### <a name="header"></a>Hode

Angi følgende felter i toppteksten til en kategori for teknisk endring.

| Felt | beskrivelse |
|---|---|
| Navn | Angi et navn for kategorien for teknisk produkt. |
| Teknisk firma | Velg det tekniske firmaet der produkter i denne kategorien for teknisk produkt kan opprettes og hvor de skal vedlikeholdes. |

### <a name="details-fasttab"></a>Hurtigfanen Detaljer

Angi følgende felter i hurtigfanen **Detaljer** for en kategori for teknisk endring.

| Felt | beskrivelse |
|---|---|
| Produkttype | Velg om kategorien gjelder for produkter eller tjenester. |
| Produksjonstype | Dette feltet vises bare når du har aktivert [formelendringsbehandling](manage-formula-changes.md) i systemet. Velg produksjonstypen som denne tekniske produktkategorien gjelder for:<ul><li>**Planleggingselement** - Bruk denne ingeniørkategorien til å gjøre formelendringsbehandling for planleggingselementer. Planleggingselementer bruker formler. De ligner formelvarer, men de brukes til å produsere bare koprodukter og biprodukter, ikke ferdige produkter. Formler brukes under prosessproduksjon.</li><li>**Stykkliste** – Bruk denne tekniske kategorien til å administrere tekniske produkter, som ikke bruker formler og vanligvis (men ikke nødvendigvis) omfatter stykklister.</li><li>**Formel** - Bruk denne tekniske kategorien til å gjøre formelendringsbehandling for ferdige produkter. Disse varene vil ha en formel, men ikke en stykkliste. Formler brukes under prosessproduksjon.</li></ul> |
| Faktisk vekt | Dette alternativet vises bare når du har aktivert [formelendringsbehandling](manage-formula-changes.md) i systemet. Det er bare tilgjengelig når **Produksjonstype**-feltet er satt til *Planleggingselement* eller *Formel*. Sett dette alternativet til *Ja* hvis du vil bruke denne tekniske kategorien til å administrere varer som krever støtte for faktisk vekt. |
| Spor versjoner i transaksjoner | Velg om produktversjonen skal stemples inn på alle transaksjoner (logistikkinnvirkning). Hvis du for eksempel sporer versjonen i transaksjoner, vil hver salgsordre vise hvilken versjon av produktet som er solgt, i den aktuelle salgsordren. Hvis du ikke sporer versjonen i transaksjoner, viser ikke salgsordrer hvilken bestemt versjon som ble solgt. I stedet viser de alltid den nyeste versjonen.<ul><li>Hvis dette alternativet er satt til *Ja*, opprettes det en produktstandard for produktet, og hver versjon av produktet vil være en variant som bruker *versjonsproduktdimensjonen*. Feltet **Produktets undertype** settes automatisk til *Produktstandard*, og i feltet **Produktdimensjonsgruppe** må du velge en produktdimensjonsgruppe der *versjon*-dimensjonen er aktiv. Bare produktdimensjonsgrupper der *versjon* er en aktiv dimensjon, vil vises. Du kan opprette nye produktdimensjonsgrupper ved å velge **Rediger**-knappen (blyantsymbolet).</li><li>Hvis dette alternativet er satt til *Nei*, brukes ikke *versjonsproduktdimensjonen*. Du kan deretter velge om du vil opprette et produkt eller en produktstandard som bruker de andre dimensjonene.</li></ul><p>Dette alternativet brukes ofte for produkter som har en kostnadsforskjell mellom versjoner eller produkter der forskjellige betingelser gjelder i forbindelse med kunden. Derfor er det viktig å angi hvilken versjon som ble brukt i hver transaksjon.</p> |
| Produktets undertype | Velg om kategorien skal inneholde produkter eller produktstandarder. For produktstandarder brukes produktdimensjoner.
| Produktdimensjonsgruppe | Med innstillingen **Spor versjoner i transaksjoner** kan du velge produktets dimensjonsgruppe. Hvis du har angitt at du vil spore versjonen i transaksjoner, vises produktdimensjonsgruppene der *versjonsdimensjonen* brukes. Ellers vises bare produktdimensjonsgrupper der *versjonsdimensjonen* ikke brukes. |
| Produktlivssyklustilstand ved opprettelse | Definer standardstatusen for produktstatusen som et teknisk produkt skal ha når det opprettes først. Hvis du vil ha mer informasjon, kan du se [Produktstatuser og transaksjoner](product-lifecycle-state-transactions.md). |
| Versjonsnummerregel | Velg versjonsnummerregelen som gjelder for kategorien:<ul><li>**Manuell** – Du velger versjonsnummeret for hver nye versjon.</li><li>**Automatisk** – Systemet angir versjonsnummeret, basert på et format du definerer. Når du definerer formatet, bruker du et nummertegn (\#) til å representere et siffer og et hvilket som helst annet tegn til å representere en konstant verdi. Hvis du for eksempel definerer formatet som *V-\#\#*, vil den første versjonen være V-01, den andre versjonen være V-02 og så videre.</li><li>**Liste** – Systemet bruker neste nummer fra en forhåndsdefinert liste over egendefinerte verdier som du definerer.</li></ul> |
| Håndhev gyldighet | Velg om de gyldighetsdatoene til tekniske versjoner må være sammenhengende, eller om det kan være tomrom og overlappinger. Denne innstillingen påvirker hvordan du kan bruke feltene **Gyldig fra** og **Gyldig til** i hver tekniske versjon der kategorien gjelder.<ul><li>Hvis dette alternativet er angitt til *Ja*, må en **Gyldig fra**-verdi angis for hver versjon, og verken overlappinger eller tomrom er tillatt mellom versjoner. Datointervallet for hver tekniske versjon er koblet direkte til de tidligere og neste tekniske versjoner, hvis de finnes. I dette scenarioet brukes alltid den nyeste versjonen, og eldre versjoner brukes ikke lenger.</li><li>Hvis dette alternativet er satt til **Nei**, er det ingen begrensninger i gyldighetsdatofeltene for tekniske versjoner, og både overlappinger og tomrom er tillatt. I dette scenarioet kan flere versjoner være aktive samtidig, og du kan arbeide med alle aktive versjoner.</li></ul><p>Dette alternativet påvirker også stykklister og ruter som er koblet til en produktversjon. Hvis du vil ha mer informasjon, kan du se avsnittet [Koble stykklister og ruter til tekniske versjoner](#boms-routes) senere i denne artikkelen.</p> |
| Bruk terminologi for nummerregel | Sett dette alternativet til *Ja* for å aktivere regler for å definere et produktnummer ved hjelp av nummerserier, tekniske attributtnavn og verdier, og tekstkonstanter som segmenter. Hvis du vil opprette eller endre regler, velger du **Rediger**. |
| Bruk terminologi for navneregel | Sett dette alternativet til *Ja* for å aktivere regler for å definere et navn ved hjelp av navn på teknisk attributt, tekniske attributtverdier og tekstkonstanter som segmenter. Hvis du vil opprette eller endre regler, velger du **Rediger**. |
| Bruk terminologi for beskrivelsesregel | Sett dette alternativet til *Ja* for å aktivere regler for å definere beskrivelsen ved hjelp av navn på teknisk attributt, tekniske attributtverdier og tekstkonstanter som segmenter. Hvis du vil opprette eller endre regler, velger du **Rediger**. |

### <a name="attributes-fasttab"></a>Hurtigfanen Attributter

Bruk rutenettet på hurtigfanen **Attributter** for å definere hvilke tekniske attributter som gjelder for produkter som hører til denne kategorien. Hvis du vil ha informasjon om hvordan du oppretter tekniske attributter, kan du se [Tekniske attributter og søk i tekniske attributter](engineering-attributes-and-search.md).

Bruk knappene i hurtigfanen **Attributter** for å legge til, fjerne og ordne attributter i rutenettet.

Hvis du endrer utvalget av attributter for en teknisk kategori, og det allerede finnes produkter som er basert på denne kategorien, må du bestemme om du vil bruke endringene på disse produktene. Hvis du vil at eksisterende produkter skal gjenspeile endringene, velger du **Oppdater eksisterende produkter** på hurtigfanen **Attributter**.

For hver rad du legger til i rutenettet, angir du følgende felter:

| Felt | beskrivelse |
|---|---|
| Navn | Velg attributtet du vil legge til. |
| Verdi | Velg standardverdien for attributtet. |
| Obligatorisk | Velg om attributtet er obligatorisk, noe som betyr at brukere må angi en gyldig verdi for attributtet før de kan lagre et produkt. Virkningen av denne innstillingen kan variere litt, avhengig av datatypen til det valgte attributtet, som definert i listen nedenfor.<ul><li>**Boolsk** – Sett dette til *Ja* hvis du vil kreve at attributtet har verdien *Ja* (systemet vil avvise å lagre et produkt der attributtet er satt til *Nei*). Sett dette til *Nei* for å godta verdien *Ja* eller *Nei*. (Attributter av typen *Boolsk* kan ikke ha en tom verdi.)</li><li>**Heltall eller Desimal** – Sett dette til *Ja* hvis du vil kreve at brukere angir en verdi som ikke er null for dette attributtet. Sett dette til *Nei* hvis du vil tillate at brukerne lagrer med verdien null.  (Attributter av disse typene kan ikke ha en tom verdi.)</li><li>**Liste** – Lister har datatypen *Tekst*, men inneholder også en forhåndsdefinert liste over mulige verdier. Derfor er det ikke mulig å angi en tom verdi for attributter av denne typen, så denne innstillingen har ingen virkning og er bare til informasjon.</li><li>**Alle andre datatyper** – Sett dette til *Ja* for å gjøre attributtet obligatorisk. Sett dette til *Nei* for å tillate at brukerne kan lagre et produkt uten å angi en verdi for dette attributtet.</li></ul> |
| Partiattributt | Velg om attributtet skal overføres via den satsvise funksjonaliteten. |

### <a name="readiness-policy-fasttab"></a>Hurtigfanen Klargjøringspolicy

Bruk feltet for **Policy for produktklargjøring** til å velge klargjøringspolicyen som skal brukes på produkter som opprettes basert på denne tekniske kategorien. Hvis du vil ha mer informasjon, kan du se [Produktklargjøring](product-readiness.md).

> [!NOTE]
> Feltet **Policy for produktklargjøring** fungerer litt annerledes hvis du har aktivert funksjonen for *Produktberedskapskontroller* i systemet. (Med denne funksjonen kan du bruke beredskapspolicyer på standard \[ikke-tekniske\] produkter). Hvis du vil ha mer informasjon, kan du se [Tilordne beredskapspolicyer til standardprodukter og tekniske produkter](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Hurtigfanen Frigivelsespolicy

Bruk feltet for **Policy for produktfrigivelse** til å velge frigivelsespolicyen som gjelder for produkter som hører til denne kategorien. Hvis du vil ha mer informasjon, kan du se [Frigi produktstrukturer](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Koble stykklister og ruter til tekniske versjoner

Innstillingen for alternativet **Håndhev gyldighet** er viktig for tilkobling av stykklister og ruter til hver tekniske versjon. Du kan bare aktivere flere stykklister eller ruter per produkt hvis det er en forskjell i noen av følgende innstillinger:

- Produktdimensjon
- Antall
- Site
- Gyldighetsdatoer

Tekniske stykklister og ruter opprettes fra den tekniske versjonen der de gjelder. De kan gjenkjennes ved å merke av for avmerkingsboksen **Teknisk kontrollert**. Når du arbeider med tekniske stykklister og ruter, vil du ikke vanligvis utforme dem ved å bruke ulike antall. Du vil heller ikke vanligvis utforme forskjellige stykklister per område. I tillegg hentes alltid gyldighetsdatoene fra den tekniske versjonen for tekniske stykklister og ruter. Derfor vil en teknisk versjon, dens stykkliste og rute, ha samme gyldighetsdatoer.

For produkter der du bruker *versjonsproduktdimensjonen* (sammen med logistikkinnvirkning på transaksjonene), blir også versjonen lagt til i stykklistene og rutene. Denne virkemåten kan skille mellom stykklister og ruter i påfølgende versjoner, uavhengig av innstillingen **Håndhev gyldighet**.

For produkter der du ikke bruker *versjonsproduktdimensjonen* (uten logistikkinnvirkning på transaksjonene), blir ikke versjonen lagt til i stykklistene eller rutene. Det vil derfor ikke være noen forskjell mellom stykklister og ruter i påfølgende versjoner. I dette tilfellet anbefaler vi på det sterkeste at du setter alternativet **Håndhev gyldighet** til *Ja*. På denne måten bidrar du til å forhindre at tekniske versjoner overlapper, og du kan også aktivere stykklisten og ruten til en nyere versjon uten først å deaktivere stykklisten og ruten for den tidligere versjonen. Hvis du setter alternativet **Håndhev gyldighet** til *Ja* i dette tilfellet, må du deaktivere stykklistene og rutene i eldre versjoner manuelt før du kan aktivere den siste versjonen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
