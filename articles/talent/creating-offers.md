---
title: Opprette, godkjenne og signere tilbud
description: Dette emnet beskriver hvordan du kan opprette, godkjenne og registrere et tilbud for en kandidat ved hjelp av Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8c5f95f1d3be22a73cc42cb3667b793490f2a136
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739639"
---
# <a name="create-approve-and-sign-offers"></a>Opprette, godkjenne og signere tilbud

[!include[banner](../includes/banner.md)]

I mange tilfeller må klargjøring av en tilbudspakke for en kandidat være en svært rask prosess.
Bruk av malene som er definert av Attract-administratoren, vil redusere tiden og innsatsen som kreves for å forberede og sende tilbud til en kandidat.

## <a name="create-an-offer"></a>Opprette et tilbud

Når Offer Management-appen er aktivert, kan alle brukere som har rollen ansettelsesansvarlig eller rekrutterer, forberede en tilbudspakke for kandidaten. Hvis du vil forberede tilbudet, kan du gjøre følgende.

1.  Gå til jobben og kandidatsøknaden du oppretter tilbudet for.

1.  Gå til **Tilbudsstadium**, og klikk **Klargjør tilbud**.

    Du omdirigeres til tilbudsappen der du kan se kandidaten med statusen **Ny**. Du kan også se andre tilbud som du bidrar til, som oppretter eller godkjenner.

1.  Klikk **Klargjør tilbud**. 
    
    Det vises en rekke tilbudspakker som er gjort tilgjengelige av systemansvarlig.

1.  Velg en pakke, og klikk **Ferdig** for å starte klargjøring av tilbudet.

    Tilbudspakkemalen lastes inn med den tilsvarende jobben, og med detaljer om kandidaten fylt ut i tilbudet.

1.  Alle tilbudsdataplassholderne som er en del av tilbudspakken, er synlige på målsiden. Du kan fylle ut alle verdier på tvers av pakken på denne siden.

    På målsiden kan du også se alle tilbudsdokumentmalene som er en del av tilbudspakken.

1.  Du kan kanskje nå redigere innholdet i tilbudet, avhengig av hvordan malen ble konfigurert av administratoren.

1.  Hvis du må fjerne dokumenter som er merket som ikke nødvendige, kan du gjøre dette.

1. Når alle tilbudsdataplassholdere er fylt ut, klikker du **Lagre** for å lagre en kladd av tilbudet.

>[!NOTE]
> Når du har lagret en kladd, kan du slette utkastversjonen av tilbudet eller velge en ny mal for pakken, om nødvendig.


## <a name="approve-an-offer"></a>Godkjenne et tilbud

De fleste tilbud må gå gjennom en godkjenningsprosess for å kontrollere at tilbudet oppfyller de nødvendige standardene. Hvis et tilbud ikke overholder standardene, for eksempel hvis personen som opprettet tilbudet, ikke fulgte tilbudsdatareglene og overstyrte verdiene i tilbudet, vil godkjenningsprosessen være obligatorisk. Hvis du vil sende et tilbud til godkjenning, kan du gjøre følgende.

1.  Når tilbudet er i kladdemodus, legger du til godkjennerne på **godkjennerpanelet**. 
    >[!NOTE]
    > Ansettelsesansvarlige legges til som godkjenner som standard. Du kan velge enhver bruker fra organisasjonen som en godkjenner for tilbudet.

1.  Hvis du trenger, kan du tilordne godkjennere i en sekvensiell godkjenningsmetode eller en metode for parallell godkjenning. Dette alternativet er bare tilgjengelig hvis det ble konfigurert slik av administratoren.
    >[!NOTE]
    > Hvis godkjenningsprosessen er sekvensiell, kan du redigere rekkefølgen av godkjennere om nødvendig.

1.  Når du er ferdig med å definere godkjenningsrekken, kan du redigere innholdet i e-posten for godkjenning og deretter sende meldingen til godkjennerne. Klikk **Send til godkjennere**.
    >[!NOTE]
    > Hvis tilbudet ikke var standard, må du angi en begrunnelse.

1.  Hvis personen som opprettet tilbudet, velger å hoppe over en godkjenner, kan de skrive inn en merknad og gå til neste godkjenner.

Godkjennere mottar en e-post som ber dem godkjenne tilbudet. De kan klikke koblingen i e-postmeldingen for å åpne tilbudet, gå gjennom hele tilbudspakken, og enten godkjenne det eller sende det tilbake til personen som opprettet tilbudet. Tilbudsgodkjennere må legge til flere notater hvis de forkaster tilbudspakken for ytterligere endringer. 

I tilfeller der det er en ny versjon av tilbudet blir opprettet før du godkjenneren handler, kan ikke godkjenneren godkjenne eller avvise tilbudet.

## <a name="offer-versioning"></a>Versjonskontroll av tilbud 

Når tilbudet er godkjent eller sendt tilbake for ytterligere endringer, kan du velge alternativet **Aktiverer redigering** for å opprette en ny versjon av tilbudet. Den nye versjonen av tilbudsversjonen har alle tilbudsdataverdiene og listen over godkjennere som er overført fra den siste versjonen. 

Godkjennere kan bytte mellom ulike tilbuddversjoner hvis versjonene var delt med dem for godkjenning. En godkjenner eller tilbudsoppretter kan også velge å slette en bestemt utkasttilbudsversjon for å gå tilbake til den forrige tilstanden.


## <a name="send-an-offer-to-a-candidate"></a>Send et tilbud til en kandidat 

Når tilbudet er lagret, godkjent og klar til å bli sendt til kandidaten, klikker du **Send til kandidat**.

Det finnes flere handlinger du kan utføre før du sender tilbudet til kandidaten.
-  Du kan vise listen over dokumenter som er en del av tilbudspakken som skal sendes til kandidaten.

-  Du kan angi en utløpsdato for tilbudet. Kandidater forventes å godta eller avvise tilbudet før utløpsdatoen.  Kandidaten sendes en påminnelse 48 timer før tilbudet utløper.

-  Det kan være du vil inkludere flere dokumenter i tilbudsgodkjenningsprosessen. Du vil ha muligheten til å vise dokumenttypen som kreves.

- Alternativet for e-signatur: Det er to måter å koble til en valgt e-signaturleverandør. Gå til **Brukerinnstillinger** i **Tilbud**, og under **Tilkoblinger** kobler du til **Adobe Sign** eller **DocuSign**. Du kan eventuelt bli bedt om å koble **Send tilbud til kandidat**-siden hvis tilkoblingen ikke allerede ble opprettet basert på brukerinnstillingene. E-signaturkontoen må bare være koblet én gang. Den samme brukerlisensen brukes for alle fremtidige tilbudspakker som sendes ut av samme bruker. 

### <a name="adobe-sign"></a>Adobe Sign
Hvis Adobe Sign ble valgt som foretrukket e-signeringsmetode, må tilbudsopprettere koble til Adobe Sign-lisensen i dette trinnet. 

### <a name="docusign"></a>DocuSign
Hvis DocuSign ble valgt som foretrukket e-signeringsmetode, må tilbudsopprettere koble til DocuSign-lisensen. Når du er logget på, kobles standardkontoen og tillatelsene som er tilknyttet brukerens DocuSign-profil, til Talent Attract. 

-  Du kan vise og redigere e-postmalen etter behov.

Når tilbudet er klart, og du klikker **Send til kandidat**, vil kandidaten motta en e-post om at et tilbud venter på gjennomgang.

>[!NOTE]
> Hvis du bruker Adobe Sign eller DocuSign og du støter på en feil under sending av tilbudet til kandidaten, prøv å koble fra og koble e-signaturbrukerkontoen til igjen fra **Brukerinnstillinger**. Hvis problemet vedvarer, kan du kontakte vår brukerstøtte ved hjelp av **Rapporter et problem**-koblingen.

## <a name="candidates-actions-after-receiving-an-offer"></a>Kandidatens handlinger etter å ha mottatt et tilbud

Etter at kandidaten har fått melding om at et tilbud er delt med dem, kan de klikke koblingen i e-posten for å gå til søknadsinstrumentbordet og vise tilbudet. Instrumentbordet viser kandidaten eventuelle aktiviteter som de fortsatt må fullføre.

1.  For å se tilbudet og alle relaterte dokumenter må kandidaten klikke **Vis tilbud**.

    Kandidater kan også laste ned tilbudspakken i et ZIP-format.

1.  For å godta tilbudet må kandidatene klikke **Gå til signatur** for hvert dokument som er en del av tilbudspakken.

1.  Når alle dokumentene er individuelt signert og godkjent, må kandidaten velge å fullføre godkjenningsprosessen ved å klikke **Godta tilbud** øverst på siden.

1.  For å avvise tilbudet må klikke kandidaten **Avvis tilbudet** øverst på siden, velge en passende årsak, legge til en kommentar om nødvendig, og deretter klikke **Avslå**.

1.  Etter at de har godtatt eller avslått tilbudet, kan kandidatene fortsette å vise tilbudet eller gå tilbake til søknadsinstrumentbordet.

1.  Hvis andre dokumenter ble forespurt som en del av tilbudsgodkjenningsprosessen, bør kandidaten velge å laste opp dokumenter etter behov og merke dem til den forespurte dokumenttypen.

1.  Personen som opprettet tilbudet, vil bli varslet når alle dokumentene har blitt lastet opp, og tilbudspakken er signert.


## <a name="withdrawing-an-offer"></a>Trekke tilbake et tilbud

Et tilbud kan trekkes tilbake fra en kandidat når som helst av ulike årsaker. 
1.  Trekk tilbake tilbudet ved å klikke ellipseknappen (**...**) og deretter **Trekk tilbake tilbudet**. 

2. Det vises en melding der kandidaten blir spurt om han har blitt kontaktet om endringen i status. Hvis kandidaten ikke har blitt kontaktet ennå, får du muligheten til å sende en e-post til kandidaten og informere om flere handlinger. 

   Tilbudet vil ikke lenger være tilgjengelig for kandidaten.


## <a name="closing-an-offer"></a>Lukke et tilbud 

Når et tilbud har blitt godtatt, avslått eller trukket tilbake uten behov for flere handlinger, kan du lukke tilbudet slik at ingen flere endringer kan gjøres i denne tilbudpakken.
