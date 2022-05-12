---
title: Veiledning for Dynamics 365 Commerce-netthandelslokalisering
description: Dette emnet beskriver hvordan du lokaliserer et Microsoft Dynamics 365 Commerce-netthandelsområde til flere språk og konfigurerer området for å støtte flere kanaler.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661529"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Veiledning for Dynamics 365 Commerce-netthandelslokalisering

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du lokaliserer et Microsoft Dynamics 365 Commerce-netthandelsområde til flere språk og konfigurerer området for å støtte flere kanaler, og dekker også begrepene og terminologien som er knyttet til prosessen.

Netthandelsfunksjonene i Dynamics 365 Commerce er utformet for å gjøre det mulig å tilpasse nettopplevelser som kan tilpasses bestemte land og språk, men samtidig tillate for maksimal gjenbruk av maler, sider, innhold og medier. Du kan også opprette et grunnleggende område, og deretter utvide til nye markeder ved å legge til støtte for flere land og språk over tid.

## <a name="definitions"></a>Definisjoner

**Nasjonal innstilling, ID for nasjonal innstilling**: En nasjonal innstilling (kalles også en ID for nasjonal innstilling) definerer et språk som er tilknyttet et land eller område. ID-en for nasjonal innstilling fr-ca er for eksempel tilknyttet kanadisk fransk.

**Originalspråk**: Språket du utvikler områdeinnholdet på før du eksporterer det for lokalisering.

**Kanal, nettbutikk**: En kanal (også kalt en nettbutikk) definerer betalingsmåtene, prisgruppene, produkthierarkiene, sortimentene og produktene for en nettbutikk.

## <a name="concepts"></a>Begreper

### <a name="url-driven-experience"></a>Nettadressedrevet opplevelse

Dynamics 365 Commerce-netthandelsområder leverer unike markedsførte og lokaliserte opplevelser for kunder via kanaler og ID-er for nasjonale innstillinger. Kanaler definerer de unike produktene, kategoriene, valutaene og betalingsmåtene for et marked, og ID-er for nasjonale innstillinger bestemmer språket for innholdet som kundene ser. Et netthandelsområde bruker nettadresser til å skille mellom markedsførte og lokalisert erfaringer. Nettadresser for områder for disse unike kanalopplevelsene og de nasjonale innstillingene defineres for et område på siden **Områdeinnstillingene \> Kanaler** i Dynamics 365 Commerce-områdebyggeren.

I områdebyggeren er en nettadresse en kombinasjon av et domene og en bane som definerer startpunktet for en unik kombinasjon av en kanal og en nasjonal innstilling. I dette eksemplet definerer en fiktiv nettbutikk kalt Fabrikam Inc. fire unike kombinasjoner av en kanal og en nasjonal innstilling, og tildeler hver kombinasjon til en unik nettadresse som betjener innhold til kunder.

| Domene                     |  Bane      | Kanal       |   Nasjonal innstilling     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam-utvidet nettbutikk | nb-NO  |
| `https://fabrikam.com` | /es    | Fabrikam-utvidet nettbutikk | es     |
| `https://fabrikam.ca`  | /      | Contoso-nettbutikk    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso-nettbutikk    | en-ca  |

#### <a name="domain"></a>Domene

Domener opprettes når du konfigurerer netthandelsområdet i Microsoft Dynamics Lifecycle Services (LCS). Når netthandelsmiljøet er klargjort, kan du legge til flere domener ved å åpne en serviceforespørsel. Hvis du vil ha mer informasjon om hvordan du konfigurerer domener for netthandelsområdet, kan du se [Domener i Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Bane

- En bane er en vilkårlig streng som, sammen med domenet, er tildelt en unik kombinasjon av en kanal og en nasjonal innstilling. I det forrige eksemplet er strengen som brukes som bane, i samsvar med ID-en for nasjonal innstilling som banen er tildelt. Du kan imidlertid bruke en annen metode.
- En kombinasjon av en kanal og en nasjonal innstilling kan tildeles et domene og en tom bane ("/"). I det forrige eksemplet vil kunder som besøker `https://fabrikam.ca/`, få produktene og sortimentet for det kanadiske markedet på kanadisk fransk.
- Commerce-områdebyggeren hindrer at du oppretter duplikatkombinasjoner av et domene og en bane. Du kan imidlertid tildele dupliserte kombinasjoner av en kanal og en nasjonal innstilling til en annen kombinasjon av et domene og en bane.

#### <a name="channel"></a>Kanal

- Kanaler (også kalt nettbutikker) definerer betalingsmåtene, prisgruppene, produkthierarkiene, sortimentene og produktene for en nettbutikk.
- Kanaler defineres, konfigureres og publiseres i Dynamics 365 Commerce headquarters.
- Områdebygger kan finne nettbutikkene som er konfigurert i Commerce Headquarters, og de kan tildeles et område.

Hvis du vil ha mer informasjon om kanaler, kan du se [Oversikt over kanaler](channels-overview.md). Hvis du vil ha mer informasjon om hvordan du konfigurerer en nettkanal, kan du se [Konfigurer en nettkanal](channel-setup-online.md).

#### <a name="locale"></a>Nasjonal innstilling

- Den nasjonale innstillingen brukes når du overleverer XML XLIFF-filer (Localization Interchange File Format) for lokalisering. Nasjonale innstillinger defineres og publiseres for hver kanal i Commerce Headquarters. Hvis du vil ha informasjon om hvordan du konfigurerer språk og kanaler i områdebyggeren, kan du se neste del.
- Den samme nasjonale innstillingen kan tildeles flere kanaler. På denne måten kan et felles språk tilbys på tvers av flere markeder.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Konfigurer språk og kanaler for netthandelsområdet

Som standard er alle Dynamics 365 Commerce-netthandelsområder konfigurert til å bruke én enkelt nettkanal og ett enkelt språk, uansett om du starter med Fabrikam-demoområdet eller oppretter et nytt område fra begynnelsen.

I denne konfigurasjonen utvikler kunder og partnere vanligvis alle anleggsmidler som skal brukes på tvers av land og språk. Disse ressursene omfatter maler, sider, fragmenter, innhold og medier. Alt områdeinnhold utvikles på det første språket du valgte for området, eller hvis du bruker Fabrikam-demoområdet, utvikles områdeinnholdet på engelsk.

![Standard Dynamics 365 Commerce-netthandelsområde](media/loc-guide-1.png)

> [!NOTE]
> Du kan konfigurere Fabrikam-demoområdet for et tilleggsspråk slik at innholdsutvikling kan gjøres på det språket. Hvis du vil ha mer informasjon om hvordan du legger til et nytt språk i et område og en kanal, kan du se delen [Konfigurer et tilleggsspråk for området](#configure-an-additional-language-for-your-site) senere i dette emnet.

Innholdsstyringssystemet (CMS) og sidemodellen for Dynamics 365 Commerce-netthandelsområder er imidlertid utformet for å gjøre det mulig å utvide til nye markeder og nasjonale innstillinger. Gjennom ett enkelt netthandelsområde kan du derfor styre ressursene for en nettbutikk som strekker seg over flere markeder og språk.

![Dynamics 365 Commerce-netthandelsområde som strekker seg over flere markeder og språk](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Konfigurer et tilleggsspråk for området

Prosessen med å konfigurere et nytt språk for et netthandelsområde har tre trinn.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Trinn 1: Legg til språket i kanalen (nettbutikken) i Commerce Headquarters

1. I Commerce Headquarters går du til kanalen der du vil legge til det nye språket. Hvis du vil finne listen over kanaler som du konfigurerte i Commerce headquarters, går du til **Retail og Commerce \> Kanaler \> Nettbutikker**.
1. Åpne nettbutikken som er tildelt området, ved å velge verdien for **Detaljhandelskanal-ID**. Du kan kontrollere nettbutikken som er tildelt området, ved å åpne innstillingssiden **Kanaler** i Commerce-områdebygger og se på navnet på nettbutikken i **Kanaler**-kolonnen. 
1. Velg **Legg til** på hurtigfanen **Språk**. I feltet **Språk** velger du koden for nasjonal innstilling for det nye språket. Velg deretter **Lagre**.
1. Gå til **Retail og Commerce \> IT for Retail og Commerce \> Distribusjonsplan** og kjører jobb **1070 kanalkonfigurasjon**. Når jobben er ferdig med å kjøre, kan du gå videre til trinn 2 og legge til språket i en kanal for området i områdebyggeren.

![Hurtigfanen Språk for en nettbutikk i Commerce Headquarters](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Trinn 2: Legg til språket i en kanal i områdebygger

Hvis du vil legge til et språk i en kanal i områdebygger, følger du disse trinnene.

1. Åpne området i Commerce-områdebygger, og åpne deretter **Kanaler**-siden i områdeinnstillinger.
1. Velg navnet på kanalen som du vil legge til språket i.
1. Velg **Legg til en nasjonal innstilling** i den høyre ruten.
1. I dialogboksen **Legg til en nasjonal innstilling** under **Legg til en nasjonal innstilling** velger du nasjonal innstilling for språket du tidligere la til i kanalen i Commerce Headquarters.
1. Velg domenet og banen som kundene ber om å vise området ditt på i denne kanalen og på dette språket.
1. Hvis du vil at språket skal være standardspråket for visning, oppretting og oppdatering av sider og fragmenter for områdebygger, merker du av for **Bruk som standardspråk for forfatterkanal**. 
    > [!NOTE]
    > Denne innstillingen påvirker bare områdebygger. Den påvirker ikke den publiserte områdeopplevelsen for kundene.
1. Velg **OK**.
1. Velg **Lagre og publiser**.

#### <a name="step-3-localize-your-site-content"></a>Trinn 3: Lokaliser områdeinnholdet

Når du går tilbake til **Sider**-visningen i Commerce-områdebygger, vil det nye språket være tilgjengelig i kanalen og i velgeren for nasjonal innstilling øverst til høyre. Du kan nå opprette lokaliserte versjoner av sider på originalspråket.

Prosessen for å lokalisere innholdet på sidene og fragmentene er dekket i delen [Lokaliser innhold på netthandelsområde](#localize-e-commerce-site-content) senere i dette emnet.

### <a name="configure-a-new-channel-for-your-site"></a>Konfigurer en ny kanal for området

Dynamics 365 Commerce-netthandelsområder kan betjene opplevelser som er definert på tvers av flere nettkanaler som er konfigurert i Commerce Headquarters. Et område bruker flere kanaler for å vise kunder en unik konfigurasjon av betalingsmåter, prisgrupper, produkthierarkier, sortimenter og et sett med produkter. En kanal brukes vanligvis til å konfigurere disse dimensjonene slik at de passer til kravene og innstillingene for opplevelsen som er knyttet til enkeltland. Denne fremgangsmåten er imidlertid en forretningsbeslutning som kunden tar. Det er ikke et krav.

Forutsetningene og oppgavene som er knyttet til oppsett av en kanal (nettbutikk) går utover dette dokumentets omfang. Hvis du vil ha mer informasjon om hvordan du konfigurerer en nettkanal i Commerce headquarters, kan du se [Grunnleggende om kanaloppsett](channels-overview.md#channel-setup-basics). Hvis du vil ha informasjon om trinn og krav som er spesifikke for nettkanaler, kan du se [Konfigurer en nettkanal](channel-setup-online.md).

Hvis du vil legge til en kanal i området i områdebygger, følger du disse trinnene.

1. Gå til **Områdeinnstillinger \> Kanaler** i Commerce-områdebygger. 
1. Velg **Legg til en kanal**.
1. Velg kanalen du vil legge til, under **Kanal** i dialogboksen **Legg til en kanal**. 
    > [!NOTE]
    > Du kan bare legge til kanaler som ikke allerede er lagt til på området.
1. Velg standard nasjonal innstilling for kanalen. Hvis du legger til nye språk i kanalen, kan du endre standardspråket til ett av dem.
1. Angi domenet og banen som skal utgjøre nettadressen som betjener innhold og opplevelser for denne kombinasjonen av en kanal og et språk.
1. Velg **OK**.
1. Velg **Lagre og publiser**.

## <a name="localize-e-commerce-site-content"></a>Lokaliser innhold på netthandelsområde

### <a name="xliff-basics"></a>Grunnleggende om XLIFF

XLIFF er et filformat i bransjestandard for å sende lokaliserbart innhold mellom innholdsstyringsverktøy. Commerce-områdebygger bruker XLIFF-filformatet til å eksportere metadatainnhold om side, fragment og bilde, slik at det kan lokaliseres og importeres på nytt.

Microsoft Dynamics-kunder arbeider vanligvis med lokaliseringsleverandører fra en tredjepart, for eksempel [Translated.com](https://translated.com/welcome) for å oversette XLIFF-filene til språkene de krever.

### <a name="localize-assets-in-site-builder"></a>Lokaliser ressurser i områdebygger

Følgende netthandelsområder kan lokaliseres i områdebygger:

- Sider
- Fragmenter
- Medieressurser
- Moduler

Alle nye sider, fragmenter og medieressurser opprettes i sammenheng med kanalen og språket som for øyeblikket er valgt i kanalen og i velgeren for nasjonal innstilling. Dette språket er vanligvis originalspråket, forutsatt at du ikke har konfigurert flere språk eller kanaler. På områder der flere kanaler og språk er konfigurert, defineres originalspråket av kanalen og den nasjonale innstillingen du har angitt som standard på siden **Kanaler** i områdeinnstillinger.

Trinnene for å lokalisere innhold for sider, fragmenter og medieressurser er like. Unntak og forskjeller blir påpekt i de følgende delene. Trinnene for å lokalisere modulinnhold er imidlertid forskjellig. Hvis du vil ha mer informasjon, kan du se delen [Lokaliser moduler](#localize-modules) senere i dette emnet.

#### <a name="step-1-export-an-xliff-file"></a>Trinn 1: Eksporter en XLIFF-fil

Hvis du vil eksportere en XLIFF-fil for en side, et fragment eller et bilde i områdebygger, følger du disse trinnene.

1. Åpne ressursen du vil eksportere innhold på originalspråk for, slik at den kan lokaliseres.
1. Velg **Lokalisering \> Eksporter XLIFF** på kommandolinjen.
    > [!NOTE]
    > Alternativet **Lokalisering** er bare synlig når ressursen er i **redigeringstilstand**.

En XLIFF-fil med navnet **\<assetname\>.xlf** blir lastet ned til nettleserens nedlastingsmappe. XLIFF-filen er spesifikk for ressursen du lokaliserer. Du eksporterer en XLIFF-fil for alle ressurser du vil lokalisere.

#### <a name="step-2-localize-the-xliff-file"></a>Trinn 2: Lokaliser XLIFF-filen

I de fleste tilfeller vil du arbeide med en lokaliseringsleverandør for å oversette XLIFF-filene. Hvis du imidlertid lokaliserer ressurser internt, eller hvis du bare vil teste lokaliseringsprosessen, må du gjøre følgende endringer i en XLIFF-fil:

- Legg til et målspråkattributt i elementet /xliff/file, og angi verdien til ID for nasjonal innstilling for språket du lokaliserer til. 
    > [!NOTE]
    > ID-en for nasjonal innstilling må samsvare med ID-en for nasjonal innstillinger fra siden **Kanaler** i områdeinnstillinger.
- Legg til et målelement for hvert //kilde-element der tekstverdien er den lokale versjonen av innholdet i kildeelementet.

Hvis du vil ha informasjon om skjemaet som styrer XLIFF-filer, kan du se [XLIFF 1.2-spesifikasjon](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Hvis du vil lokalisere en ressurs til flere språk, må du opprette en lokalisert XLIFF-fil for hvert av disse språkene.

#### <a name="step-3-import-the-localized-xliff-file"></a>Trinn 3: Importer den lokaliserte XLIFF-filen

Følg denne fremgangsmåten for å importere en XLIFF-fil for en ressurs.

1. Åpne ressursen du vil importere en XLIFF-fil for, i Commerce-områdebygger.
1. Velg kanalen og språket du importerer lokalisert innhold for, i kanalen og velgeren for nasjonal innstilling øverst til høyre.
1. Velg **Lokalisering \> Importer XLIFF** på kommandolinjen. Bla deretter til og velg den lokaliserte XLIFF-filen for valgt ressurs og språk.

Når XLIFF-filen er importert, opprettes det en variant av siden, fragmentet eller ressursen. Fra og med dette tidspunktet vil alle endringer som gjøres i den lokaliserte varianten, bare påvirke denne varianten. De påvirker ikke grunnressursen som varianten er avledet fra. På samme måte vil ikke endringer i grunnressursen varianten av denne ressursen. 

Når det gjelder sider, kan du imidlertid foreta endringer på tvers av varianter ved å endre malen eller oppsettet som disse sidene er bundet til. På samme måte vil endringer i et fragment påvirke alle sider som er avhengige av den varianten.

### <a name="images"></a>Bilder

Bilder kan bare gjengis i en side- eller modulvariant hvis innholdsmetadata som er tilknyttet disse bildene, er lokalisert. Følgende metadata i en medieressurs kan lokaliseres:

- Alternativ tekst
- Beskrivelse
- Tittel

For øyeblikket kan du ikke lokalisere binærfilen for en digital ressurs, for eksempel et bilde eller en video. Dynamics 365 Commerce-produktgruppen arbeider med denne funksjonen.

### <a name="localize-modules"></a>Lokaliser moduler

Strenger som gjengis som en del av selve modulen (for eksempel Forrige og Neste i en karusellmodul), lokaliseres separat fra modulinnhold. Hvis du vil ha instruksjoner , kan du se [Lokaliser en modul](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Ordliste for sidemodell](page-elements-overview.md)

[Deling på tvers av kanal](cross-channel-sharing.md)

[Lokaliser en modul](e-commerce-extensibility/localize-module.md)

[Moduldefinisjonsfil](e-commerce-extensibility/module-definition-file.md)

[Lokalisere utvidelsesressurser og etikettfiler for Commerce](dev-itpro/extension-resource-localization.md)

[Globaliser moduler ved hjelp av CultureInfoFormatter-klassen](e-commerce-extensibility/globalize-modules.md)

[Appinnstillinger: Temaer](e-commerce-extensibility/app-settings.md#themes-section)
