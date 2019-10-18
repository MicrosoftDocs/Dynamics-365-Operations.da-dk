---
title: Konfigurere mailindstillinger i Microsoft Dynamics 365 Talent - Attract
description: I dette emne forklares det, hvordan du kan konfigurere indstillinger for mail, der sendes af Microsoft Dynamcis 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008656"
---
# <a name="configure-email-settings"></a>Konfigurere mailindstillinger

[!include[banner](../includes/banner.md)]

Dit varemærke skaber tillid og hjælper dig med at opbygge en relation til kandidater, selv før de ansøger om dine stillinger. Positiv opfattelse af et brand tiltrækker de bedste talenter og øger eksisterende medarbejderes loyalitet. Microsoft Dynamics 365 Talent: Attract giver dig mulighed for at konfigurere mails, så de afspejler virksomhedens brand. Du kan derfor give jobkandidater en gennemført oplevelse, når de gennemgår ansøgningsprocessen.

Med Attract kan du udføre disse handlinger:

- Konfigurer mailindstillinger, så dit firmas Microsoft Exchange-mailtjenestekonto bruges. På denne måde ved ansøgere, at mails kommer fra dit firma. Du kan f.eks. konfigurere dine indstillinger, så kandidater modtager mails fra `recruiting@contoso.com` i stedet for `contoso@microsoft.com`.
- Opret en gennemført branding til al mailkommunikation ved at angive det globale sidehoved og den globale sidefod til alle mailskabeloner. 

> [!NOTE]
> Hvis du vil konfigurere Attract, så det bruger dit firmas mailtjenestekonto til at sende mail, skal du bruge tilføjelsesprogrammet Omfattende ansættelser.

## <a name="connect-an-email-service-account"></a>Forbinde en mailtjenestekonto

Ved at forbinde dit firmas mailtjenestekonto kan du oprette en brandet mailoplevelse for dine jobkandidater. Hvis du ikke tilslutter dit firmas konto, bruger Attract den Microsoft-brandede mailtjenestekonto.

1. Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.
2. Vælg **Tilslut en firmakonto** under **Mailtjenestekonti** under fanen **Mailindstillinger**.

    ![Tilslutte dit firmas mailtjenestekonto i Attract](./media/attract-admin-email-service-accounts.png)

    Du kan finde flere oplysninger om, hvordan du opretter en delt mailkonto, i [Delte postkasser i Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).

3. Log på ved hjælp af dine firmalegitimationsoplysninger i Microsoft-vinduet til logon.
4. Hvis du endnu ikke har oprettet en mailtjenestekonto, eller hvis du vil tilføje en ny, skal du vælge **Tilføj ny tjenestekonto** og derefter angive dine mailoplysninger. Hvis du allerede har konfigureret den mailtjenestekonto, du vil bruge, skal du vælge den.

Når din mailtjenestekonto er konfigureret korrekt, kan du se den på listen under **Mailtjenestekonti**.

## <a name="disconnect-an-email-service-account"></a>Frakoble en mailtjenestekonto

Hvis du ikke længere vil bruge dit firmas domæne i mailkommunikation via Attract, kan du frakoble en mailtjenestekonto.

1. Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.
2. Vælg knappen **Mere** (tre lodrette prikker) under **Mailtjenestekonti** under fanen **Mailindstillinger** ud for den mailtjenestekonto, du vil frakoble.
3. Vælg **Afbryd forbindelsen til mailkonto**.

    ![Frakobling af dit firmas mailtjenestekonto](./media/attract-admin-disconnect-email-account.png)

4. Når du bliver bedt om at bekræfte handlingen, skal du vælge **Afbryd forbindelsen**.

    ![Bekræftelse af frakobling af dit firmas mailtjenestekonto](./media/attract-admin-email-confirm-disconnect.png)

Hvis du ikke tilslutter en anden mailtjenestekonto, vil mails, der sendes fra Attract, bruge den Microsoft-brandede mailtjenestekonto.

## <a name="configure-email-template-settings"></a>Konfigurere mailskabelonindstillinger

Du kan uploade et billede af dit firmas logo og andre oplysninger som et brandet sidehoved til dine mails. Du kan også angive links til politikken for beskyttelse af personlige oplysninger og vilkår for anvendelse i mailsidefødder.

> [!NOTE]
> Du skal overholde alle gældende love i dit land eller område samt lovene i det land eller område, der er styrende for mailmodtageren. Disse love omfatter antispamregler.

1. Vælg **Indstillinger** (tandhjulssymbolet i øverste højre hjørne), og vælg dernæst **Administration**.
2. Træk det billede, du vil bruge som mailsidehoved, til billedfeltet under **Mailskabelonindstillinger** under fanen **Mailindstillinger**, eller klik i billedfeltet for at navigere til filen. Hvis du vil erstatte et eksisterende billede, skal du først vælge **Fjern** ud for det. Billedet skal være en JPEG-, JPG-, PNG-eller SVG-fil. Den anbefalede størrelse på billeder er mellem 25 og 800 pixelbredde og mellem 25 og 150 pixelhøje. Den maksimale filstørrelse for sidehovedet er 1 megabyte (MB).

    ![Tilføjelse af et billede til firmaets mailsidehoved](./media/attract-admin-email-header.png)

3. Under **Din politik om beskyttelse af personlige oplysninger for kommunikation** skal du angive et link til din virksomheds politik for beskyttelse af personlige oplysninger. Under **Dine Vilkår og betingelser for kommunikation** skal du angive et link til dit firmas vilkår for anvendelse.

    ![Tilføjelse af links til firmaets politik for beskyttelse af personlige oplysninger og vilkår for anvendelse i mailsidefod](./media/attract-admin-email-footer.png)

4. Vælg **Gem** for at gemme mailskabelonindstillingerne.
