---
title: Konfigurere Invoice Capture-løsningen
description: Denne artikkelen beskriver hvordan du konfigurerer Invoice Capture-løsningen.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691182"
---
# <a name="configure-the-invoice-capture-solution"></a>Konfigurere Invoice Capture-løsningen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når Invoice Capture-løsningen er installert, må du konfigurere miljøet. Prosessen består av følgende grunnleggende trinn.

1. **Nødvendig:** Synkroniser juridiske enheter fra Microsoft Dynamics 365 Finance. Dette trinnet brukes til å definere organisasjonsstrukturen i Microsoft Power Platform.
2. **Nødvendig:** Konfigurer kanalene for import av fakturabilder. Løsningen støtter følgende kanaler:

    - Office 365 Outlook (standard)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valgfritt:** Definer flere konfigurasjonsgrupper for OCR-tjenesten, optisk tegngjenkjenning.
4. **Valgfritt:** Definer tilordningsregler for den juridiske enheten, leverandørkontoen, varen og innkjøpstypen.

Denne artikkelen fokuserer på de to trinnene som kreves for prosessen. Hvis du vil ha mer informasjon om konfigurasjonsgrupper, kan du se [Konfigurasjonsgrupper for Invoice Capture-løsning](invoice-capture-config-group.md). Hvis du vil ha mer informasjon om tilordningsregler, kan du se [Tildelingsregler for Invoice Capture-løsning](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Administrere juridiske enheter

Finance definerer juridiske enheter som organisasjoner som identifiseres via registrering hos juridiske myndigheter. Forretningsaktiviteter utføres og registreres i separate juridiske enheter. I Microsoft Power Platform-forretningsenheter er sikkerhetsroller og brukere koblet sammen på en måte som følger den rollebaserte sikkerhetsmodellen.

Forretningsenheter brukes sammen med sikkerhetsroller for å kontrollere datatilgang. Brukerne ser bare informasjonen de trenger for å kunne gjøre jobben sin. Invoice capture-løsningen gir et konfigurasjonsområde der du kan laste inn grunnleggende informasjon fra eksisterende juridiske enheter i Finance og administrere de enhetene som opprettes manuelt. De juridiske enhetene brukes på leverandørfakturaer og i sikkerhetskontroll.

Når en juridisk enhet opprettes og vises i listevisningen, opprettes det automatisk en standard forretningsenhet med samme navn. Teamet tildeles sikkerhetsrollen **AP-assistent**. Når juridiske enheter importeres, importeres grunnleggende hoveddata fra Finance. Varene som ikke finnes, vil bli identifisert av juridisk enhet, og vil legge dem til i Invoice capture-løsningen. Standard konfigurasjonsgruppe tilordnes til nye juridiske enheter.

### <a name="sync-legal-entities"></a>Synkronisere juridiske enheter

Du kan ikke opprette juridiske enheter direkte. Du kan imidlertid synkronisere juridiske enheter fra Finance. Følg denne fremgangsmåten for å synkronisere juridiske enheter.

1. Gå til **Oppsett \>Systemoppsett \> Behandle juridiske enheter**.
2. Velg **Synkroniser juridiske enheter**, og velg deretter **OK** i bekreftelsesdialogboksen.

Når synkroniseringen er fullført, vises antall nye juridiske enheter. De nye juridiske enhetene vises i listevisningen. Standard konfigurasjonsgruppe tilordnes til de nye juridiske enhetene.

## <a name="configure-invoice-import-channels"></a>Konfigurere fakturaimportkanaler

Leverandører sender fakturaer fra ulike kanaler (e-post, arbeidsområde for filer eller fakturaportal) via ulike formater (papir eller bilde). Invoice capture-løsningen kan håndtere ulike kanaler og formater. Følgende typer støttes:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Når en kanal opprettes for en bestemt konto, bygges det opp en automatisert flyt som har en forhåndsdefinert mal, for å overvåke innkommende e-postmeldinger eller filer i innboksen eller på området. Alle filer som har en gyldig faktura, kan gjenkjennes og sendes til fakturaområdet for å vente på behandling av Accounts payable-assistenten. Vedlegget må være i PDF-format eller bildeformat. Fakturaer kan lastes inn i Invoice capture-løsningen i henhold til kanalkonfigurasjonen.

### <a name="create-a-channel"></a>Opprette en kanal

Hvis du har importert tilleggsløsningspakken (Dynamics 365 Invoice capture – Installasjonsverktøy), er standardtilkoblingen for Office 365 Outlook klar til å brukes. Hvis du vil opprette flere tilkoblinger for ulike e-postkontoer eller andre kanaltyper, kan du se [Opprette flere tilkoblinger for kanaler](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Hvis du vil opprette en kanal, følger du trinnene nedenfor.

1. Gå til **Oppsett \> Systemoppsett \> Konfigurasjonskanaler**.
2. Velg **Ny**.
3. Angi følgende felter:

    - Kanalnavn
    - Beskrivelse
    - Type
    - Tilkobling

Bare e-postmeldinger eller filer som samsvarer med de følgende kriteriene, kan importeres til løsningen.

| Type               | Konfigurasjon  | Mer informasjon |
|--------------------|----------------|------------------|
| Office 365 Outlook | Mappe         | E-postmappen må være under rotkatalogen. Som standard brukes innboksmappen. En undermappe støttes ikke. |
|                    | Emnefilter | (Valgfritt) En delstreng som skal tas med i emnet. |
|                    | Fra           | (Valgfritt) E-postadressen til avsender/avsdere. Hvis du angir flere avsenderadresser, bruker du semikolon (;) som skilletegn. |
| SharePoint         | Adresse til webområde   | URLen til områdeadressen. |
|                    | Mappe         | Mappen i områdeadressen. |

### <a name="activate-the-channel"></a>Aktivere kanalen

Når en flyt lagres, viser feltene statusen til kanalen og tidspunktet da den ble opprettet. I starten settes **Status**-feltet til **Inaktiv**. **Statusårsak**-feltet angir at kanalen er initialisert og klar til å aktiveres.

Velg **Aktiver** for å aktivere kanalen. Feltene **Status** og **Statusårsak** oppdateres.

Hvis en kanal ikke er nødvendig, kan du deaktivere den. Velg **Deaktiver** for å deaktivere en kanal. Feltene **Status** og **Statusårsak** oppdateres.

### <a name="manage-flows-in-flow-management"></a>Administrere flyter i flytadministrasjon

Du kan vise en kanal på sidne **Konfigurasjonskanaler** eller i flytadministrasjon.

Hvis du vil vise flere detaljer, kan du gå til **Administrasjonssystem \> Standardløsning \> Skyflyter**, og velg målflyten. Detaljene som vises, omfatter koblede koblinger, eiere og historikker for kjøring.

Hvis du vil synkronisere statusen, velger du **Kontroll** for å bekrefte at statusen til kanalen stemmer overens med statusen til flyten.

Noen tilfeller av unntakshåndtering vises i **Statusårsak**-feltet:

- **Manglende Dataverse-tilkobling** – Gjeldende bruker har ikke opprettet minst én **Microsoft Dataverse**-tilkoblingsreferanse.
- **Finner ikke** – Flyten som er koblet til kanalen, er slettet i flytadministrasjon. Kanalen må lagres på nytt for å opprette en ny kanal.
- **Deaktiveres i flytstyring** – Flyten er deaktivert i flytadministrasjon, og statusen til kanalen er forskjellig fra flytens status.
- **Aktivert i flytadministrasjon** – Flyten er aktivert i flytadministrasjon, og statusen til kanalen er forskjellig fra flytens status.
- **Det oppstod en uventet feil** – Brukeren må bekrefte at området er et Kommunikasjonsområde, og at mappen er et Dokumentbibliotek.
