---
title: Arbeide med funksjonsoppsett
description: Dette emnet beskriver hvordan du konfigurerer funksjoner for elektronisk fakturering.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41ffc9c7009291a55392e50c5e490d3288d122bc
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371627"
---
# <a name="work-with-feature-setups"></a>Arbeide med funksjonsoppsett

[!include [banner](../includes/banner.md)]

For å konfigurere genereringen av elektroniske filer og andre behandlingstrinn (for eksempel signere filer digitalt, sende dem til den offentlige nettjenesten og få et svar eller lagre dem) konfigurerer du datasamlebåndet for behandling, relevansregler og variabler for funksjoner for elektronisk fakturering.

Oppsettinformasjonen kombineres i konseptet *funksjonsoppsett* og kan opprettes, slettes og justeres. Informasjonen kan også vises for de ferdige versjonene av funksjoner for elektronisk fakturering.

Du kan opprette så mange elementer for funksjonsoppsett du trenger for å definere ulike scenarioer for generering, behandling og mottak av elektroniske filer. Selv om disse elementene for funksjonsoppsett har uavhengige behandlingshandlinger og -betingelser for kjøring, opprettes de som en del av én funksjon for elektronisk fakturering, og arver livssyklusen og utrullingsprosessen til den.

## <a name="add-a-feature-setup"></a>Legge til et funksjonsoppsett

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.
3. Velg en versjon av en funksjon for elektronisk fakturering som har statusen **Utkast**, på siden **Funksjoner for elektronisk fakturering**.
4. Velg **Legg til** i **Oppsett**-fanen.
5. Velg ett av følgende alternativer i feltgruppen **Ny** i rullegardinboksen **Opprett funksjonsoppsett**:
 
    - **Egendefinert oppsett** – Opprett et nytt funksjonsoppsett som har tomme kanaler, en tom datasamlebåndsliste for behandling, en tom del for relevansregler og et standardsett med variabler, avhengig av oppsettypen.
    - **Fra funksjonsoppsett** – Opprett en kopi av et annet funksjonsoppsett innenfor den gjeldende funksjonen for elektronisk fakturering.

6. Hvis du valgte alternativet **Egendefinert oppsett** i det forrige trinnet, angir du et navn og en beskrivelse for elementet for funksjonsoppsett, og deretter velger du ett av følgende alternativer i feltgruppen **Oppsettype**:

    - **Datasamlebånd for behandling** – Velg dette alternativet for å generere og behandle utgående elektroniske dokumenter. Når det gjelder denne oppsettypen, oppretter systemet en tom datasamlebåndsliste for behandling, en tom del for relevansregler og et standardsett med variabler. Du kan ikke arbeide med kanalene for inngående elektroniske dokumenter.
    - **Datakanal** – Velg dette alternativet for å konfigurere prosessen for mottak av inngående elektroniske dokumenter fra en av de definerte kanalene og sende dem direkte til Microsoft Dynamics 365 Finance eller Dynamics 365 Supply Chain Management uten flere handlinger. Når det gjelder denne oppsettypen, oppretter systemet en forhåndsdefinert liste over parametere for datakanalene, en tom del for relevansregler og et sett med standardvariabler. Du kan ikke legge til noen handlinger i datasamlebåndet for behandling.
    - **Datakanal og datasamlebånd for behandling** – Denne oppsettypen ligner på oppsettypen **Datakanal**. Før et inngående elektronisk dokument sendes til Finance eller Supply Chain Management, kan du imidlertid konfigurere ytterligere handlinger i datasamlebåndet for behandling.

7. Hvis du valgte alternativet **Datakanal** eller **Datakanal og datasamlebånd for behandling** i forrige trinn, må du velge kanalen som skal integreres med, i feltet **Velg datakanal**.
8. Velg **Opprett**.

Etter at et funksjonsoppsett er opprettet, kan du velge **Rediger** for å konfigurere det.

## <a name="edit-a-feature-setup"></a>Redigere et funksjonsoppsett

Avhengig av typen funksjonsoppsett du bruker, kan du konfigurere genereringen av utgående elektroniske filer og sende dem til eksterne kanaler eller motta inngående dokumenter og sende dem til programmet Finance eller Supply Chain Management.

### <a name="data-channel"></a>Datakanal

En *datakanal* tar den elektroniske filen og behandler eller sender den direkte til Finance eller Supply Chain Management. Dette alternativet er ikke tilgjengelig for funksjonsoppsett av typen **Datasamlebånd for behandling**.

Du kan definere en datakanal ved å angi navnet på kanalen. Deretter definerer du parameterne basert på den valgte kanaltypen. Identifikatoren for datakanal må referere til variabelen som opprettes spesifikt for å identifisere datakanalen. Den brukes som en referanse i Finance eller Supply Chain Management.

Du bør definere et sett med filtre i fanen **Vedleggsfilter** for å hente bestemte filer fra kanalen. Du kan opprette flere linjer hvis du forventer at filene kommer til å ha ulike filtyper, eller hvis filer må behandles ulikt avhengig av filnavnet. Her er hovedparameterne:

- **Navn** – Angi navnet på filen som systemet skal referere til under behandling. I programmene Finance og Supply Chain Management kan du se filene i innsendingsloggen.
- **Filter** – Definer filteret for å velge filer.
- **Valgfritt** – Hvis det ikke er merket av for dette alternativet, kreves filen. I dette tilfellet viser systemet en feilmelding hvis kanalene ikke inneholder filer som tilsvarer filteret. Denne parameteren gjelder for e-postmeldinger.

Hvis kanalen er en postboks og en innkommende e-postmelding inneholder flere vedlegg, kan du konfigurere regler for å definere hvordan tjenesten skal håndtere vedlegg. Tjenesten kan behandle hvert vedlegg som en egen elektronisk faktura, eller den kan behandle ett vedlegg som en hovedfaktura og alle andre vedlegg som tillegg.

### <a name="processing-pipeline"></a>Behandlingspipeline

Et *datasamlebånd for behandling* er et sett med *handlinger* som kjøres sekvensielt til de er fullført. Du kan bruke et datasamlebånd for behandling til å konfigurere prosessen for generering av elektroniske filer og utføre andre trinn (for eksempel signere filer digitalt, sende dem til eksterne nettjenester og analysere svaret og motta og behandle inngående dokumenter).

Listen over handlinger er forhåndsdefinert. Du kan bruke knappene **Ny** og **Slett** til å angi kombinasjonen av handlinger som logisk definerer den nødvendige prosessen for å sende inn eller motta dokumenter.

Handlingsrekkefølgen er viktig. Du kan justere rekkefølgen ved å bruke **Opp**- og **Ned**-knappene.

Hver handling har et sett med parametere du kan konfigurere eller justere. Det bestemte settet med parametere avhenger av handlingstypen.

- **Handling** – Velg handlingstypen.
- **Handlingsnavn** – Angi navnet på handlingen. Dette navnet vises i innsendingslogger og i meldinger i programmene Finance og Supply Chain Management.
- **Beskrivelse** – Gir mer informasjon om formålet med handlingen i prosessen.
- **Aktiver nytt forsøk** – Hvis du merker av for dette alternativet, kan du velge en handling i feltet **Prøv handling på nytt** og konfigurere ytterligere parametere i fanen **Parametere for nytt forsøk**.

    Funksjonalitet for nytt forsøk lar deg konfigurere tjenestens virkemåte hvis en bestemt handling ikke kan kjøres. Hvis den eksterne nettjenesten du prøver å koble til, for eksempel ikke svarer, kan du angi hvor mange ganger systemet skal prøve å koble til på nytt, med hvilket intervall og fra hvilken handling i datasamlebåndet for behandling.

- **Eksporter resultater** – Du kan merke av for dette alternativet for *én* handling i datasamlebåndet for behandling. Den elektroniske filen som handlingen produserer i programmet Finance eller Supply Chain Management, kan deretter eksporteres fra siden **Innsendingslogg for elektroniske dokumenter**.

### <a name="applicability-rules"></a>Relevansregler

*Relevansregler* er konfigurerbare setninger som gir en kontekst for kjøring av funksjoner for elektronisk fakturering via funksjonssettet for elektronisk fakturering.
Forretningsdokumenter som sendes inn fra Finance eller Supply Chain Management til elektronisk fakturering, har ikke en eksplisitt referanse som gjør at funksjonssettet for elektronisk fakturering kan kalle opp en bestemt versjon av en funksjon for elektronisk fakturering og et bestemt element for funksjonsoppsett, for å behandle innsendingen. Når et forretningsdokument imidlertid er riktig konfigurert, inneholder det de nødvendige elementene som gjør at elektronisk fakturering kan fastsette hvilken versjon av en funksjon for elektronisk fakturering og hvilket datasamlebånd for behandling som må velges og kjøres.

Med relevansregler kan den elektroniske faktureringstjenesten finne funksjonene for elektroniske fakturering som må brukes til å behandle en innsending. **Kontekst**-feltene i det innsendte forretningsdokumentet sammenlignes med setninger fra relevansregler for å finne de riktige funksjonene.

Du kan arbeide med relevansregler på følgende måter:

- Velg **Ny** for å legge til en ny setning i et sett med relevansregler.
- Velg **Slett** for å slette en setning.
- Velg flere poster, og bruk knappen **Grupper** eller **Løs opp gruppe** til å opprette en kombinasjon av elementer eller logiske setninger. Velg for eksempel linjene du vil gruppere, og velg deretter **Grupper setning**. Når setninger grupperes, legges det til en ny kolonne i rutenettet. Denne kolonnen angir den logiske operatoren for den grupperte setningen. Følgende operatortyper støttes:

    - Equal
    - Not equal
    - Større enn / Mindre enn
    - Større enn eller lik / Mindre enn eller lik
    - Contains
    - Begynner med

    > [!NOTE]
    > Når du opphever gruppering av en setning, må du alltid starte fra det innerste grupperingsnivået.

### <a name="variables"></a>Variabler

*Variabler* gir deg større fleksibilitet når du konfigurerer et datasamlebånd for behandling og dataflyten blant handlingene. Du kan referere til en variabel i noen handlingsparametere for å lagre data eller elektroniske filer midlertidig. Noen variabler brukes til å sende data mellom programmet Finance eller Supply Chain Management og tjenesten for elektronisk fakturering.

Systemet oppretter noen variabler som standard. Variabelen **BusinessDocumentDataModel** inneholder for eksempel forretningsdata i en JSON-struktur (JavaScript Object Notation) som kommer i oppkallet fra det tilkoblede programmet under innsendingen.

Følgende variabeltyper er tilgjengelige:

- **Konstant** – En beholder for lagring av midlertidige data som brukes i behandling av datasamlebåndshandlinger.
- **Fra klient** – Innholdet i variabelen hentes fra Dynamics 365-klienten når innsendingen kjøres.
- **Til klient** – Innholdet i variabelen gjøres tilgjengelig for import av Dynamics 365-klienten når innsendingen kjøres.
- **Datatype** – Velg datatypen for informasjonen som er lagret i variabelen.

### <a name="parameters"></a>Parametere

Alternativet **Deaktiver reduksjon av forretningsdata** brukes til å optimalisere strukturen til forretningsdatanyttelasten som kommer fra programmet Finance eller Supply Chain Management under innsending av elektronisk dokument. Optimaliseringen bidrar til å redusere dataene som går inn i tjenesten for elektronisk fakturering, for videre transformasjon til den nødvendige elektroniske filen. Standardverdien er **Nei**.

- **Ja** – Finance eller Supply Chain Management sender en JSON-fil av strukturen **Fakturamodell** eller **Regnskapsmodell** (for Brasil) som er definert i modulen **Elektronisk fakturering**. Alle elementene i modellen er fylt med forretningsdata på programsiden, uavhengig av den endelige elektroniske filstrukturen. Modeller inneholder vanligvis mer forretningsdata enn målfilstrukturen krever, og det kan ta mer tid å generere disse dataene i programmet. Verdien **Ja** for dette alternativet kreves i de sjeldne tilfellene der du vil generere ulike utdatafiler i én funksjon for elektronisk fakturering og funksjonsoppsett. Verdien **Ja** er nyttig når du feilsøker scenarioene, strukturen til de elektroniske filene og fullstendigheten til forretningsdataene.
- **Nei** – Finance eller Supply Chain Management foretar det første oppkallet til tjenesten uten forretningsdata. Formålet med dette oppkallet er å hente informasjon om ER-konfigurasjon (Electronic Reporting) som skal brukes til transformasjon av elektronisk fil i datasamlebåndet for behandling. Denne informasjonen returneres til programmet, som bruker den til å fastsette delsettet med forretningsdata som skal tas med i JSON-filen av strukturen **Fakturamodell** eller **Regnskapsmodell** (for Brasil). Verdien **Nei** for dette alternativet bidrar til å redusere mengden forretningsdata som programmet sender inn til tjenesten, fordi programmet bare kan sende inn forretningsdataene som kreves for å kunne generere en elektronisk fil.

### <a name="validate-a-feature-setup"></a>Validere et funksjonsoppsett

Du kan kjøre validering for å kontrollere konsekvensen for hele konfigurasjonen. Hvis en obligatorisk parameter for en handling for eksempel er tom, oppdager valideringen denne inkonsekvensen, og du får en advarsel.

- I handlingsruten på siden **Funksjonsversjonsoppsett** velger du **Valider**.

## <a name="delete-a-feature-setup"></a>Slette et funksjonsoppsett

1. Velg en versjon av en funksjon for elektronisk fakturering som har statusen **Utkast**, på siden **Funksjoner for elektronisk fakturering**.
2. Velg **Slett** i **Oppsett**-fanen.
3. Velg **Ja** i meldingsboksen som vises, for å bekrefte at du vil slette funksjonsoppsettet.
