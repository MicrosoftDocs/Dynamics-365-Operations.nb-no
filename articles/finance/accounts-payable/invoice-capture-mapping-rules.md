---
title: Tildelingsregler for Invoice Capture-løsning
description: Denne artikkelen gir informasjon om oppsett av tilordningsregler i Invoice capture-løsningen.
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
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691236"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Tildelingsregler for Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tilordningsregler tar med grunnleggende hoveddata fra Microsoft Dynamics 365 Finance eller ERP-systemet (Enterprise Resource Planning). Når tilordningsregler er definert, hentes informasjonen som kreves for å opprette leverandørfakturaer i Finance. Når tilordningsregler brukes, vil AP-ekspeditøren kontrollere statusen i stedet for å fylle ut alle de manglende feltverdiene manuelt.

Det finnes fire typer tilordningsregler:

- Juridisk enhet
- Leverandørnummer
- Vare
- Utgiftstype

## <a name="manage-mapping-rules-by-using-the-app"></a>Administrere tilordningsregler ved hjelp av appen

Velg **Oppsett** for å administrere tilordningsregler ved hjelp av appen. Fanen **Tilordningsregeloppsett** har fire alternativer:

- Juridisk enhet 
- Leverandørnummer 
- Elementtilordning 
- Utgiftstype

Du velger for eksempel alternativet **Tilordningsregler for juridisk enhet**. Koden for den juridiske enheten vil bli identifisert ved hjelp av firmanavnet, adressen og avgiftsregistreringsnummeret. Hvis firmanavnet inneholder teksten Contoso Robotics USA for en regel som kalles **LE-USPM**, vil den juridiske enhetskoden være **USPM**.

Siden viser alle de aktive tilordningsreglene. Hvis du vil vise de inaktive tilordningsreglene, velger du regler for **Aktiv tilordning av regler for juridisk enhet** og **Inaktiv tilordning av regler for juridisk enhet**.

Følgende handlinger er tilgjengelige for tilordningsregler.

### <a name="create-a-mapping-rule"></a>Opprette en tilordningsregel

Du kan bruke to metoder for å opprette en tilordningsregel:

- Velg **Ny** for å opprette en ny tilordningsregel. Deretter angir du informasjonen for tilordningsregelen. Verdien **Regelnavn** må være unik for hver tilordningsregeltype.
- Hvis du velger en eksisterende tilordningsregel, blir **Kopier**-knappen tilgjengelig. Velg den, og velg deretter **OK** i dialogboksen som vises. En tilordningsregel opprettes ved å duplisere den valgte regelen.

### <a name="edit-a-mapping-rule"></a>Redigere en tilordningsregel

Hvis du vil redigere en tilordningsregel, velger du et felt og endrer verdien.

### <a name="activatedeactivate-mapping-rules"></a>Aktivere/deaktivere tilordningsregler

Hvis du vil deaktivere én eller flere tilordningsregler, kan du velge dem på siden **Aktive tilordningsregler**, og deretter velge **Deaktiver**. Reglene flyttes fra siden **Aktive tilordningsregler** til siden **Inaktive tilordningsregler**.

På samme måte, for å aktivere tilordningsregler, velger du dem på siden **Inaktive tilordningsregler**, og deretter velger du **Aktiver**.

### <a name="remove-mapping-rules"></a>Fjerne tilordningsregler

For å fjerne tilordningsregler velger du dem og deretter **Slett**.

### <a name="check-for-conflicts"></a>Se etter konflikter

Hvis to tilordningsregler har samme verdier for **Juridisk enhet** og **Leverandørkonto**, men forskjellige **Varenavn**-verdier, vil det oppdages en konflikt, og tilordningsregelen blir ikke opprettet eller oppdatert.

## <a name="importexport-mapping-rules-from-excel"></a>Importere/eksportere tilordningsregler fra Excel

Et Excel-tillegg kan brukes til å administrere regler i en bunke. Følgende alternativer er tilgjengelige:

- Last ned en Excel-mal.
- Eksporter til Excel.
- Importer fra Excel.

### <a name="download-an-excel-template"></a>Last ned en Excel-mal

Hvis du vil laste ned en Excel-mal, velger du **Last ned mal**. Deretter velger du feltene for å inkludere i malen.

### <a name="export-to-excel"></a>Eksporter til Excel

Du kan eksportere på to måter:

- Velg **Åpne i Excel Online** for å åpne filen i Excel. Du kan deretter redigere filen på nettet. Når du er ferdig, velg **Lagre**. Alle endringene lagres på **Tilordningsregel**-siden.
- Velg **Last ned regneark** for å laste ned en Excel-fil som inneholder tilordningsregler. Du kan deretter redigere filen. Når du er ferdig, velger du **Importer fra Excel** for å laste opp det oppdaterte regnearket.

### <a name="import-from-excel"></a>Importer fra Excel

1. Velg **Importer til Excel** for å importere data fra en XLSX-fil. Du kan også importere fra kommaseparerte verdier (CSV) eller XML-filer. Før du importerer, bør du avgjøre om duplikater er tillatt.
2. Velg **Se gjennom tilordning** for å gå gjennom attributttilordningen og finne ut om den er riktig. Du kan endre tilordningsrelasjonen.
3. Når du er ferdig, velger du **Avslutt import** for å starte importen.
4. Du kan velge **Spor prosess** for å spore fremdriften til importprosessen.

    Importstatusen oppdateres fra **Fullfør** til **Analyse**, og deretter til **Transformering** og til slutt til **Fullført**.

Når importprosessen er fullført, vises statistikk for fullførte, delvise feil, feil og totalt behandlet.
