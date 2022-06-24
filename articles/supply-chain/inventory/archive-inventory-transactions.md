---
title: Arkiver lagertransaksjoner
description: Denne artikkelen beskriver hvordan du arkiverer lagertransaksjonsdata for å forbedre systemytelsen.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c63cdee862e2e22649a3eb58ae37597741770e14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874108"
---
# <a name="archive-inventory-transactions"></a>Arkivere beholdningstransaksjoner

[!include [banner](../../includes/banner.md)]

Over tid vil lagertransaksjonstabellen (`InventTrans`) fortsette å vokse og bruke mer databaseplass. Spørringer som opprettes mot tabellen, vil derfor gradvis gå saktere. Denne artikkelen beskriver hvordan du kan bruke funksjonen *Arkiv for lagertransaksjoner* til å arkivere data om lagertransaksjoner for å forbedre systemytelsen.

> [!NOTE]
> Bare økonomisk oppdaterte lagertransaksjoner kan arkiveres i en valgt lukket finansperiode. Hvis du vil arkivere, må økonomisk oppdaterte utgående lagertransaksjoner ha avgangsstatusen *Solgt*, og innkommende lagertransaksjoner må ha tilgangsstatusen *Kjøpt*.

Når du arkiverer lagertransaksjoner, flyttes alle relaterte transaksjoner til tabellen `InventTransArchive`. Lageravgangstransaksjoner og lagermottakstransaksjoner arkiveres separat, basert på kombinasjonen av vare-IDen (`itemId`) og lagerdimensjons-ID (`inventDimId`), og de settes inn i den summerte avgangen og summerte mottakstransaksjoner.

Hvis en kombinasjon av `itemId` og `inventDimId` bare inneholder én mottaks- eller avgangstransaksjon, blir ikke transaksjonen arkivert.

## <a name="turn-on-the-feature-in-your-system"></a>Aktivere funksjonen i systemet

Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i denne artikkelen, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Arkiv for lagertransaksjoner*. Merk deg at denne funksjonen ikke kan deaktiveres når den først er aktivert.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Ting du bør vurdere før du arkiverer lagertransaksjoner

Før du arkiverer lagertransaksjoner, bør du vurdere følgende forretningsscenarioer, fordi de vil bli påvirket av operasjonen:

- Når du kontrollerer lagertransaksjoner fra tilknyttede dokumenter, for eksempel bestillingslinjer, vises de som arkivert. Hvis du vil gå gjennom de arkiverte transaksjonene, må du gå til **Lagerstyring \> Periodiske oppgaver \> Opprydding \> Arkiv for lagertransaksjoner**.
- Lagerlukking kan ikke avbrytes for arkiverte perioder. Før du kan avbryte en lagerlukking, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.
- Standard kostnadskonvertering kan ikke utføres for arkiverte perioder. Før du kan utføre standard kostnadskonvertering, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.
- Lagerrapporter som kommer fra lagertransaksjoner, vil påvirkes når du arkiverer lagertransaksjoner. Disse rapportene omfatter rapporten for aldersfordeling for lager og lagerverdirapporter.
- Lagerprognoser kan bli påvirket hvis de kjøres i løpet av arkiverte perioders tidshorisont.

## <a name="prerequisites"></a>Forutsetninger

Lagertransaksjoner kan bare arkiveres i perioder der følgende betingelser er oppfylt:

- Finansperioden må være avsluttet.
- Lagerlukking må kjøres på eller etter til-periodedatoen for arkivet.
- Perioden må være minst ett år før fra-periodedatoen til arkivet.
- Det må ikke finnes eksisterende lagerberegninger.

## <a name="archive-inventory-transactions"></a>Arkivere beholdningstransaksjoner

Hvis du vil arkivere lagertransaksjoner, følger du disse trinnene.

1. Gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding** \> **Arkiv for lagertransaksjon**.

    Siden **Arkiv for lagertransaksjoner** vises med en liste over arkiverte prosessposter.

    ![Siden Arkiv for lagertransaksjoner.](media/archive-inventory-empty.png "Siden Arkiv for lagertransaksjoner")

1. Velg **Arkiv for lagertransaksjoner** på handlingssiden for å opprette et arkiv for lagertransaksjoner.
1. I dialogboksen **Arkiv for lagertransaksjoner** angir du følgende feilt i hurtigfanen **Parametere**:

    - **Fra-dato i lukket finansperiode** – Velg den tidligste transaksjonsdatoen som skal tas med i arkivet.
    - **Til-dato i lukket finansperiode** – Velg den seneste transaksjonsdatoen som skal tas med i arkivet.

    ![Dialgoboksen Arkiv for lagertransaksjoner.](media/archive-inventory-dates.png "Dialgoboksen Arkiv for lagertransaksjoner")

    > [!NOTE]
    > Bare perioder som oppfyller [forutsetningene](#prerequisites), vil være tilgjengelige for valg.

1. Definer detaljer for satsvis behandling i hurtigfanen **Kjør i bakgrunnen** etter behov. Følg de vanlige trinnene for satsvise jobber i Microsoft Dynamics 365 Supply Chain Management.
1. Velg **OK**.
1. Du får en melding som ber deg om å bekrefte at du ønsker å fortsette. Les meldingen nøye, og velg deretter **Ja** hvis du vil fortsette.

    Du mottar en melding som angir at arkivjobben for lagertransaksjoner er lagt til i den satsvise køen. Jobben vil nå begynne å arkivere lagertransaksjoner fra den valgte perioden.

## <a name="view-archived-inventory-transactions"></a>Vis arkiverte lagertransaksjoner

Siden **Arkiv for lagertransaksjoner** viser din fullstendige arkiveringshistorikk. Hver rad i rutenettet viser informasjon som datoen da arkivet ble opprettet, brukeren som opprettet den og statusen den ble opprettet på.

![Arkivere historikk på siden Arkiv for lagertransaksjoner.](media/archive-inventory-full.png "Arkivere historikk på siden Arkiv for lagertransaksjoner")

I rullegardinlisten øverst på siden velger du en av følgende verdier for å filtrere arkivene som vises i rutenettet:

- **Aktive** – Vis bare aktive arkiver, ikke tilbakeførte arkiver.
- **Alle** – Vis alle arkiver, både aktive og tilbakeførte.

Følgende informasjon vises for hvert arkiv i rutenettet:

- **Aktive** – En hake angir at arkivet er aktivt.
- **Fra-dato** – Datoen for den eldste transaksjonen som kan tas med i arkivet.
- **Til-dato** – Datoen for den yngste transaksjonen som kan tas med i arkivet.
- **Planlagt av** – Brukerkontoen som opprettet arkivet.
- **Utført** – Datoen da arkivet ble opprettet.
- **Tilbakeført** – En hake angir at arkivet er tilbakeført.
- **Stopp gjeldende oppdatering** – En hake angir at arkivering pågår, men at den er stoppet midlertidig.
- **Tilstand** – Behandlingsstatusen til arkivet. De mulige verdiene er *Venter*, *Pågår* og *Avsluttet*.

Verktøylinjen over rutenettet inneholder følgende knapper som du kan bruke til å arbeide med et valgt arkiv:

- **Arkiverte transaksjoner** – Vis alle detaljene i det valgte arkivet. Siden **Arkiverte transaksjoner** vises med alle transaksjonene i arkivet.

    ![Siden Arkiverte transaksjoner.](media/archive-inventory-transactions.png "Siden Arkiverte transaksjoner")

    Hvis du vil vise mer informasjon om en bestemt transaksjon på siden **Arkiverte transaksjoner**, kan du velge den i rutenettet og deretter velge **Arkiverte transaksjonsdetaljer** i handlingsruten. Detaljsiden **Arkiverte transaksjoner** som vises, viser informasjon som finanspostering, relaterte underregnskapsreferanser og finansdimensjoner.

- **Stanse arkivering midlertidig** – Stans et valgt arkiv midlertidig som behandles. Den midlertidige stansen aktiveres bare etter at arkiveringsoppgaven er generert. Det kan derfor ta litt tid før den midlertidige stansen trer i kraft. Hvis et arkiv er stoppet midlertidig, vises det en hake i feltet **Stopp gjeldende oppdatering**.
- **Fortsett arkivering** – Fortsett behandling for et valgt arkiv som midlertidig er stanset.
- **Tilbakefør** – Tilbakefør det valgte arkivet. Du kan bare tilbakeføre et arkiv hvis feltet **Tilstand** er satt til *Avsluttet*. Hvis et arkiv er tilbakeført, vises det en hake i feltet **Tilbakefør**.

## <a name="extend-your-code-to-support-custom-fields"></a>Utvide koden for å støtte egendefinerte felter

Hvis tabellen `InventTrans` inneholder ett eller flere egendefinerte felter, kan det hende at du må utvide koden for å støtte dem, avhengig av hva de kalles.

- Hvis de egendefinerte feltene fra tabellen `InventTrans` har de samme feltnavnene som i tabellen `InventtransArchive`, betyr det at de har en 1:1-tilordning. Derfor kan du bare plassere de egendefinerte feltene i feltgruppen `InventoryArchiveFields` i tabellen `inventTrans`.
- Hvis de egendefinerte feltnavnene i tabellen `InventTrans` ikke samsvarer med feltnavnene i tabellen `InventtransArchive`, må du legge til kode for å tilordne dem. Hvis du for eksempel har et systemfelt kalt `InventTrans.CreatedDateTime`, må du opprette et felt i tabellen `InventTransArchive` med et annet navn (for eksempel `InventtransArchive.InventTransCreatedDateTime`) og legge til utvidelser i klassene `InventTransArchiveProcessTask` og `InventTransArchiveSqlStatementHelper`, som vist i eksempelkoden nedenfor.

Følgende eksempelkode viser et eksempel på hvordan du legger til den nødvendige utvidelsen i klassen `InventTransArchiveProcessTask`.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Følgende eksempelkode viser et eksempel på hvordan du legger til den nødvendige utvidelsen i klassen `InventTransArchiveSqlStatementHelper`.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
