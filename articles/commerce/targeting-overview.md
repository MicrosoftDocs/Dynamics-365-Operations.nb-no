---
title: Målretting av enheter, markeder og geografisk plassering
description: Denne artikkelen beskriver hvordan du oppretter, redigerer og behandler målgrupper og mål i Microsoft Dynamics 365 Commerce-områdebyggeren ved hjelp av informasjon om enhet, marked og geografisk plassering.
author: sushma-rao
ms.date: 02/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ebac0f4ee98f36027f8cb50a368b9b6dcbb24623
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279428"
---
# <a name="device-market-and-geolocation-targeting"></a>Målretting av enheter, markeder og geografisk plassering

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter, redigerer og behandler målgrupper og mål i Microsoft Dynamics 365 Commerce-områdebyggeren ved hjelp av informasjon om enhet, marked og geografisk plassering.

I Dynamics 365 Commerce kan du tilpasse variasjoner av sideinnholdet (kjent som *mål*) for bestemte kundegrupper (kjent som *målgrupper*) for å øke brukerengasjement og -tilfredshet. Du kan opprette enten en målgruppe eller et mål først. En vellykket målrettingsopplevelse krever imidlertid begge disse komponentene.

Du oppretter og administrerer målgrupper i Commerce-områdebyggeren, basert på kundedata som plassering, enhetsinformasjon, påloggingsstatus og annen dynamisk avledet informasjon fra kundens nettforespørsler. Du oppretter og administrerer også mål på e-handelsmoduler og fragmenter i Commerce-områdebyggeren.

**Ansvarsfraskrivelse:** Du er ansvarlig for å bruke denne funksjonen i samsvar med alle gjeldende lover og forskrifter, inkludert de som er relatert til målretting og profilering. 

## <a name="audiences"></a>Målgrupper

En målgruppe er en gruppe brukere, og medlemskap i gruppen bestemmes av et sett med dynamiske regler. Disse reglene er enkle logikktester som kjøres mot informasjon som er tilgjengelig i kundeforespørsler eller andre tilgjengelige segmenter. Du kan kombinere flere regler ved hjelp av AND/OR-operatorer.

Commerce støtter opprinnelig grunnleggende segmenter som enhetsinformasjon, påloggingsstatus, referent og spørringsstrengparametere. Den støtter også utvidbare segmenter gjennom tilkoblinger til tredjepartsleverandører.

### <a name="basic-segments"></a>Grunnleggende segmenter

Som standard er følgende segmenter tilgjengelige og kan inkluderes i målgruppedefinisjoner:

- **Påloggingsstatus** – Test om en bruker er godkjent.
- **Enhetsplattform** – Test for følgende enhetstyper:

    - Mobil
    - Stasjonær PC
    - Nettbrett
    - Annet

- **Enhetsoperativsystem** – Test for følgende operativsystemer:

    - Windows
    - Linux
    - iOS
    - Android, annet

- **Spørringsstrengparametere** – Test om det finnes et nøkkelverdipar i en spørringsstrengparameter for en nettadresse for forespørsel. For nettadressen kan for eksempel `www.fabrikam.com/en-us/request?promo=true` en regel skrives for å teste at **promo**-parameteren har verdien **true**.
- **Informasjonskapsel** – Test for en verdi for informasjonskapsler som er angitt for domenet i nettadressen for forespørselen. En forespørsel om Fabrikam.com kan for eksempel inneholde en informasjonskapsel som har navnet **CustomLayout** og verdien **1**. Informasjonskapseltesten kontrollerer om det finnes en informasjonskapsel, men oppretter ikke eksplisitt en. I det forrige eksemplet må JavaScript tidligere ha angitt **CustomLayout**-informasjonskapselen fra en annen modul eller en annen forretningsprosess.

    > [!NOTE]
    > Sørg for at din bruk av informasjonskapsler er i samsvar med gjeldende lover.

- **Referent** – Hvis en bruker følger en kobling for å be om siden, er henviseren nettadressen til siden som var vert for koblingen.

### <a name="extensible-segments"></a>Utvidbare segmenter

Med Commerce kan du utvide listen over tilgjengelige segmenter ved å koble til tredjeparts segmenteringsleverandører. En segmenteringsleverandør vil beskrive hvilke typer segmenter som er tilgjengelige. Hvis du vil ha mer informasjon om hvordan du kobler til en leverandør av geografisk plassering eller segmentering, kan du se [Konfigurer og aktiver koblinger](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Hvis en ekstern leverandør er aktivert, kan den koble til en tjeneste som har uforutsigbar ytelse. Hvis en bruker ber om en side som inneholder målretting, og denne siden refererer til en målgruppe som kontrollerer en tredjeparts segmentleverandør, vises standardversjonen av siden for å sikre en bedre brukeropplevelse.
> - Brukeren må samtykke til å tillate informasjonskapsler. Brukerens nettleser ber deretter om alle segmenter fra relevante leverandører, og resultatene legges inn i en informasjonskapsel som returneres til brukeren. Etterfølgende forespørsler til siden vil bruke denne informasjonen til å levere målrettet innhold til brukeren. Hvis du vil ha mer informasjon om overholdelse av informasjonskapsler, kan du se [Informasjonskapselsamsvar](cookie-compliance.md).

**Ansvarsfraskrivelse:** Hvis du aktiverer denne funksjonen, deles dataene dine med tredjepartssystemer du velger. Du kontrollerer hvilke data du eventuelt oppgir til tredjeparten. Du forstår at datahåndterings- og samsvarsstandardene til tredjeparten kan avvike fra standardene i Microsoft Dynamics 365 Commerce. Personvernet ditt er viktig for Microsoft. Les [merknaden om personvern og informasjonskapsler](https://privacy.microsoft.com/privacystatement) for å finne ut mer.

### <a name="create-an-audience-in-site-builder"></a>Opprett en målgruppe i områdebyggeren

Følg denne fremgangsmåten for å opprette en målgruppe i Commerce-områdebygger.

1. Velg **Målgrupper** i navigasjonsruten til venstre.
1. Velg **Ny**.
1. Skriv inn et navn for målgruppen. Du kan også legge til koder og en beskrivelse.
1. Velg **Opprett** og deretter **Legg til ny regelblokk**. En regelblokk er en samling regler som er forbundet med AND-betingelser. Du kan også opprette flere regelblokker som har OR-betingelser mellom seg.
1. Velg en datakilde for segmentene, og angi deretter segmentnavnet, operatoren og verdiene. Du kan opprette og slette flere regler i en regelblokk, eller du kan opprette og slette hele regelblokker. Du kan også flytte regelblokker opp eller ned etter behov.

    > [!NOTE]
    > Du kan ha opptil 100 verdier i en liste, og hvert listeelement kan inneholde opptil 50 tegn.

1. Når du er fornøyd med målgruppekonfigurasjonen, velger du **Fullfør redigering**. Du kan deretter velge **Publiser** for å gjøre målgruppen tilgjengelig for bruk i et publisert mål. Alternativt kan du publisere målgruppen sammen med målet. 

Hvis du vil redigere en målgruppe, velger du hyperkoblingen for fanen **Målgrupper**, og deretter velger du **Rediger** i redigeringsprogrammet for målgruppe som vises. Hvis du vil vise listen over mål og sider som refererer til en målgruppe, velger du målgruppen i målgruppelistevisningen, og deretter velger du **Vis tildelinger**. Hvis du vil slette en målgruppe i målgruppelistevisningen eller redigeringsprogrammet for målgrupper, opphever du publiseringen hvis den allerede er publisert, og deretter velger du **Slett** på kommandolinjen.

> [!NOTE]
> Målgrupper er et konsept på områdenivå i Commerce-områdebyggeren. Du kan dele samme målgruppe på tvers av flere mål.

### <a name="rename-an-audience-in-site-builder"></a>Gi nytt navn til en målgruppe i områdebyggeren

Følg denne fremgangsmåten for å gi nytt navn til en eksisterende målgruppe i Commerce-områdebygger.

1. Velg **Målgrupper** i navigasjonsruten til venstre.
1. Velg navnet på målgruppesegmentet du vil gi nytt navn til.
1. Velg **Rediger** for å begynne å redigere målgruppen.
1. Velg pennesymbolet ved siden av navnet på målgruppen i egenskapsruten.
1. Rediger navnet på målgruppen etter behov.
1. Merk av for å bekrefte navneendringen.
1. Velg **Fullfør redigering**.

## <a name="targets"></a>Mål

Et mål er brukeropplevelsen som vises til medlemmer av en eller flere utvalgte målgrupper. Det kan inneholde variasjoner av en eller flere moduler på en side eller i et fragment. 

Du kan definere en tidsplan for målene for å angi hvor lenge de skal være aktive. Legg merke til at denne handlingen er atskilt fra handlingen med å planlegge en publiseringsgruppe som bestemmer når en samling innhold skal publiseres. Du kan også forhåndsvise målene dine for å se hvordan de vil se ut for medlemmer av utvalgte målgrupper. I tillegg kan du prioritere målene for å angi hvilket mål som skal vises i tilfelle en konflikt.

### <a name="create-a-target"></a>Opprett et mål

Følg denne fremgangsmåten for å opprette et målskall for sidemoduler i Commerce-områdebyggeren.

1. Velg **Sider** i navigasjonsruten til venstre. Velg deretter hyperkoblingen for siden som har modulene du vil målrette mot.
1. Velg **Rediger** for å sjekke ut siden for redigering.
1. Velg **Nytt mål** på **Mål**-menyen for å opprette et nytt målskall. Du kan opprette flere mål på en side etter behov.
1. Angi et navn og en beskrivelse av målet, og velg deretter **Neste**.
1. Velg **Legg til** for å inkludere målgruppene som skal se det målrettede innholdet, eller for å ekskludere målgrupper. Velg deretter **Neste**.

    > [!NOTE]
    > Målgruppetilordning er et valgfritt trinn under måloppretting. Før du publiserer målet, må du imidlertid inkludere minst én målgruppe for å sikre at de tiltenkte brukergruppene vil se det målrettede innholdet.

1. Definer tidsperioden for visningen av målet ved å velge tidssonen og dato og klokkeslett for start og slutt. Du kan angi målet slik at det vises til enhver tid i løpet av perioden, eller du kan velge bestemte dager og klokkeslett. Når du er ferdig, velg **Neste**.

    > [!NOTE]
    > Klokkeslettene og tidssonen du angir, er globale. Hvis du vil målrette mot forskjellige plasseringer på forskjellige tidspunkter eller i forskjellige tidssoner, må du opprette forskjellige mål og definere ønsket tidsplan for hver plassering.

1. Se gjennom detaljene, og når alt ser riktig ut, velger du **Opprett målopplevelse** og deretter **Gå til mål**. Målskallet er opprettet. Du kan nå legge til moduler i det.
1. Velg modulen som skal målrettes, velg ellipsen (**...**), og velg deretter **Legg til i gjeldende mål**. Når du målretter mot en overordnet modul, blir alle underordnede moduler en del av dette målet. De målrettede modulene er uthevet i grønt.
1. Gjør de nødvendige innholdsoppdateringene i målmodulen, og legg til flere moduler i målet etter behov. Velg **Lagre** for å lagre alle endringene.
1. Før du publiserer målet, må du passe på å velge **Forhåndsvisning** på kommandolinjen for å se gjennom det. Du kan deretter velge et av følgende alternativer:

    - **Grunnleggende forhåndsvisning** – Velg dette alternativet for å forhåndsvise bare den valgte variasjonen (standardside eller mål), uten tilknyttede målgrupper.
    - **Avansert forhåndsvisning** – Velg dette alternativet hvis du har flere mål på en side og vil forhåndsvise dem som en bruker som tilhører et valgt sett med målgrupper, eller på bestemt dato/klokkeslett. Velg **Neste** for å velge fra en liste over relevante målgrupper. Du kan også fjerne filteret for å velge blant alle målgrupper.

1. Når du er fornøyd med målkonfigurasjonen, må du publisere siden for å få målet til å bli tilkoblet. Velg **Publiser** for å få målet til å bli tilkoblet umiddelbart. Du kan også bruke en publiseringsgruppe til å planlegge når siden publiseres. Hvis du vil ha informasjon om publiseringsgrupper, kan du se [Arbeide med publiseringsgrupper](publish-groups.md).

Du kan også angi fragmenter. Fremgangsmåten er lik. I trinn 1 velger du imidlertid **Fragmenter** i stedet for **Sider** i den venstre navigasjonsruten.

> [!NOTE]
> For å unngå negativ innvirkning på beregningene dine, kan du enten ha et eksperiment eller mål på en side eller i et fragment. Du kan ikke ha både et eksperiment og mål.

### <a name="manage-targets"></a>Administrer mål

Hvis du vil redigere, duplisere eller slette mål, går du til standardsiden eller -fragmentet og følger denne fremgangsmåten.

1. Velg **Mål** på rullegardinmenyen, og velg deretter **Behandle mål**.
1. Velg et mål du vil redigere, duplisere eller slette.
1. Hvis du har flere mål i samme modul, eller hvis flere mål har motstridende tidsplaner, velger du **Prioriter mål** for å angi rekkefølgen de skal vises i. Hvis du legger til mer enn ett mål på en side eller i et fragment, vises knappen **Prioriter mål** også på varslingslinjen for å minne deg på å prioritere målene. Hvis ingen prioritet er angitt, velges det nyeste målet som standard.

### <a name="localize-targets"></a>Lokaliser mål

Mål på sider og fragmenter inkluderes automatisk når XLIFF-filer eksporteres og importeres til lokaliseringsformål. Hvis det imidlertid ikke er nødvendig med nasjonale innstillinger, kan du slette målene for dem etter at de lokaliserte XLIFF-filene er importert.

> [!NOTE]
> Mål administreres per kanal og nasjonal innstilling. Endringer du gjør i mål i en kanal eller nasjonal innstilling, overføres ikke automatisk til andre kanaler eller nasjonale innstillinger.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
