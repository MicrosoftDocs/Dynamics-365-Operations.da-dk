---
title: Konfigurere løsningen Invoice Capture
description: I denne artikel forklares det, hvordan du kan konfigurere løsningen Invoice Capture.
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
ms.contentlocale: da-DK
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691133"
---
# <a name="configure-the-invoice-capture-solution"></a>Konfigurere løsningen Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Når løsningen Invoice Capture er installeret, skal du konfigurere miljøet. Processen består af følgende basistrin.

1. **Påkrævet:** Synkroniser de juridiske enheder fra Microsoft Dynamics 365 Finance. Dette trin bruges til at konfigurere organisationsstrukturen i Microsoft Power Platform.
2. **Påkrævet:** Konfigurer kanalerne til import af fakturabilleder. Løsningen understøtter følgende kanaler:

    - Office 365 Outlook (standard)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **Valgfrit:** Definer flere variantgrupper for OCR-tjenesten (Optical Character Recognition - optisk tegngenkendelse).
4. **Valgfrit:** Definer tilknytningsregler for den juridiske enhed, kreditorkontoen, varen og indkøbstypen.

Denne artikel er fokuseret på de to nødvendige trin i processen. Du kan finde flere oplysninger om variantgrupper i [Variantgrupper til løsningen Invoice Capture](invoice-capture-config-group.md). Du kan finde flere oplysninger om tilknytningsregler i [Tilknytningsregler for løsningen Invoice Capture](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Administrere juridiske enheder

Finance definerer en juridisk enhed som en organisation, der er identificeret via registrering hos en juridisk myndighed. Forretningsaktiviteter udføres og registreres i separate juridiske enheder. I Microsoft Power Platform er afdelinger, sikkerhedsroller og brugere knyttet sammen på en måde, der passer til den rollebaserede sikkerhedsmodel.

Afdelinger bruges sammen med sikkerhedsroller til at styre dataadgang. Brugere kan kun se de oplysninger, de har brug for til at udføre deres job. Løsningen Invoice Capture indeholder et konfigurationsområde, hvor du kan indlæse grundlæggende oplysninger fra eksisterende juridiske enheder i Finance og administrere de enheder, der oprettes manuelt. De juridiske enheder bruges på kreditorfakturaer og i sikkerhedskontrol.

Når en juridisk enhed oprettes og vises i listevisningen, oprettes der automatisk en standardafdeling med samme navn. Teamet tildeles sikkerhedsrollen **Kreditorassistent**. Når juridiske enheder importeres, importeres grundlæggende masterdata fra Finance. De ikke-eksisterende elementer identificeres af den juridiske enhed og føjer dem til løsningen Invoice Capture. Standardvariantgruppen tildeles nye juridiske enheder.

### <a name="sync-legal-entities"></a>Synkronisere juridiske enheder

Du kan ikke oprette juridiske enheder direkte. Du kan dog synkronisere juridiske enheder fra Finance. Benyt følgende fremgangsmåde for at synkronisere juridiske enheder.

1. Gå til **Opsætning \> Systemopsætning \> Administrer juridiske enheder**.
2. Vælg **Synkroniser juridiske enheder**, og vælg derefter **OK** i bekræftelsesdialogboksen.

Når synkroniseringen er fuldført, vises antallet af nye juridiske enheder. De nye juridiske enheder vises i listevisningen. Standardvariantgruppen tildeles de nye juridiske enheder.

## <a name="configure-invoice-import-channels"></a>Konfigurere fakturaimportkanaler

Leverandører sender fakturaer fra forskellige kanaler (mail, filarbejdsområde eller fakturaportal) via forskellige formater (papir eller billede). Løsningen Invoice Capture kan håndtere forskellige kanaler og formater. Følgende typer understøttes:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Når der oprettes en kanal til en bestemt konto, oprettes der et automatisk flow med en foruddefineret skabelon, der kan overvåge indgående mails eller filer i indbakken eller filområdet. Alle filer, der indeholder en gyldig faktura, kan genkendes og sendes til fakturaområdet for at afvente behandling af kreditorassistenten. Den vedhæftede fil skal være i PDF- eller billedformat. Fakturaer kan indlæses i løsningen Invoice Capture i overensstemmelse med kanalkonfigurationen.

### <a name="create-a-channel"></a>Oprette en kanal

Hvis du har importeret den ekstra løsningspakke (Dynamics 365 Invoice Capture – installationsværktøjer), er standardforbindelsen til Office 365 Outlook klar til brug. Hvis du vil oprette flere forbindelser til forskellige mailkonti eller andre kanaltyper, skal du se [Oprette flere forbindelser til kanaler](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Følg disse trin for at oprette en kanal.

1. Gå til **Opsætning \> Systemopsætning \> Konfigurer kanaler**.
2. Vælg **Ny**.
3. Angiv følgende felter:

    - Kanalnavn
    - Beskrivende tekst
    - Type
    - Forbindelse

Det er kun mails eller filer, der opfylder følgende kriterier, som kan importeres til løsningen.

| Type               | Konfiguration  | Flere oplysninger |
|--------------------|----------------|------------------|
| Office 365 Outlook | Mappe         | Mailmappen skal være under rodmappen. Som standard bruges mappen Indbakke. En undermappe understøttes ikke. |
|                    | Emnefilter | (Valgfrit) En understring, der skal medtages i emnet. |
|                    | Fra           | (Valgfri) Afsenders mailadresse. Hvis du vil angive flere adresser, skal du bruge semikolon (;) som separator. |
| SharePoint         | Webstedets adresse   | URL-adressen til webstedet. |
|                    | Mappe         | Mappen i adressen på webstedet. |

### <a name="activate-the-channel"></a>Aktivere kanalen

Når et flow gemmes, viser felterne status for kanalen og tidspunktet for oprettelse af den. Feltet **Status** er først angivet til **Inaktiv**. Feltet **Statusårsag** angiver, at kanalen er blevet initialiseret og er klar til at blive aktiveret.

For at aktivere kanalen skal du vælge **Aktivér**. Felterne **Status** og **Statusårsag** opdateres.

Hvis det ikke er nødvendigt med en kanal, kan du deaktivere den. For at deaktivere kanalen skal du vælge **Deaktiver**. Felterne **Status** og **Statusårsag** opdateres.

### <a name="manage-flows-in-flow-management"></a>Administrere flow i flowstyring

Du kan få vist en kanal på siden **Konfigurer kanaler** eller i flowstyring.

Hvis du vil have vist flere detaljer, skal du gå til **Administrationssystem \> Standardløsning \> Cloudflow** og vælge målflowet. De oplysninger, der vises, omfatter sammenkædede forbindelser, ejere og kørselshistorik.

Hvis du vil synkronisere statussen, skal du vælge **Tjek** for at bekræfte, at kanalens status svarer til status for flowet.

Nogle tilfælde af undtagelseshåndtering vises i feltet **Statusårsag**:

- **Manglende Dataverse-forbindelse** – Den aktuelle bruger har ikke oprettet mindst én **Microsoft Dataverse**-forbindelsesreference.
- **Ikke fundet** – Det flow, der er kædet sammen med kanalen, er blevet slettet i flowstyringen. Kanalen skal gemmes igen for at oprette en ny kanal.
- **Deaktiveret i flowstyring** – Flowet er deaktiveret i flowstyring, og kanalens status afviger fra status for flowet.
- **Aktiveret i flowstyring** – Flowet er aktiveret i flowstyring, og kanalens status afviger fra status for flowet.
- **Der opstod en uventet fejl** – Brugeren skal bekræfte, at webstedet er et "Kommunikationswebsted", og at mappen er "Dokumentbibliotek".
