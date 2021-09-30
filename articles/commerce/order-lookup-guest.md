---
title: Aktivere ordreopslag for gæsteudbetaling
description: Dette emne beskriver, hvordan ordreopslag aktiveres i forbindelse med gæsteudbetaling i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 0368f567898210f122047a9f298bcb28b7540de1
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472584"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Aktivere ordreopslag for gæsteudbetaling

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emne beskriver, hvordan ordreopslag aktiveres i forbindelse med gæsteudbetaling i Microsoft Dynamics 365 Commerce.

Med ordreopslagsfunktionen til betaling ved kassen som gæst kan de kunder, der foretager køb, slå deres ordrer op. Ordreopslagsfunktionaliteten er nyttig, når kunder skal udføre handlinger, f.eks. kontrol af produkternes opfyldelsesstatus på en ordre, bekræftelse af den adresse, en ordre er afsendt til, bestilling af et produkt eller bekræftelse af den butik, som en ordre bliver afhentet fra.

Kunder, der placerer ordrer som registrerede brugere, kan se deres ordreoplysninger, når de er logget på, men det kan kunder, der bruger betaling ved kassen som gæst, ikke gøre. Når ordreopslagsfunktionen til betaling ved kassen er aktiveret, giver det dog kunder mulighed for at søge efter ordrer, som de har placeret som gæster. I denne form angiver kunder ordrebekræftelses-id'et og (valgfrit) den e-mail-adresse, de har angivet ved kassen.

Et link eller en knap, der fører kunden direkte til ordredetaljer om ordren, kan desuden medtages i ordrerelaterede transaktions-emails. Dette link eller denne knap fungerer for ordrer, der både placeres af registrerede brugere og af gæstebrugere.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Aktivere nødvendige funktioner i Commerce Headquarters

Hvis du vil aktivere ordreopslag for gæsteudbetaling, skal du aktivere følgende funktioner i **Arbejdsområder \> Funktionsadministration** i Commerce Headquarters.

| Funktion | Formål |
|---------|---------|
| Funktion til indstilling af anonyme ordredetaljer ved brugersøgning i Retail | Denne funktion viser brugergrænsefladen i Commerce-parametre, som giver dig mulighed for at aktivere API til ordreopslag for ikke-godkendte brugere og konfigurere, hvordan personlige data vises. |
| Aktivér generering af et stærkere kanalreference-id | Denne funktion genererer et mere sikkert kanalreference-id på 12 tegn (ordrebekræftelses-id), som kan overføres i forespørgselsstrengen, når en ordre ses op. |
| Generér et konsistent id-format for kanalreferencer på tværs af kanaler | Denne funktion genererer et sikkert kanalreference-id for ordrer, der placeres via et e-handelswebsted, POS (Retail POS) eller et callcenter. Før du kan aktivere denne funktion, skal funktionen **Aktivér generering af en stærkere kanalreference-id-funktion** være aktiveret. |

Når du har aktiveret funktionen **Retail anonyme brugere med ordredetaljermuligheder**, skal du aktivere den API, der understøtter opslag efter ikke-godkendte ordrer i Commerce Headquarters. Gå til **Retail og Commerce \> Konfiguration af hovedkontor \> Parametre \> Kundeordrer**. På siden **Debitorordrer** i oversigtspanelet **Ordresøgning** skal du angive indstillingen **Aktivér ikke-godkendte ordreopslag** til **Ja** som vist i følgende illustration.

## <a name="manage-the-display-of-personal-data"></a>Administrere visningen af personlige data

Oversigtspanelet **Ordresøgning** på siden **Kundeordrer** i Commerce Headquarters **indeholder et opslagsfelt med inkludering af personlige oplysninger i gæsteordrefeltet**, som giver dig mulighed for at styre, om private oplysninger vises for kunder. Disse personlige oplysninger omfatter kundens leveringsadresse og de sidste fire cifre i kundens kreditkortnummer. Personlige oplysninger vises som standard ikke til kunder, når opslag af ikke-godkendte ordrer er aktiveret. I følgende tabel beskrives tilgængelige indstillinger.

| Indstilling | Resultat |
|--------|--------|
| Aldrig | Standardværdien. Der vises ingen personlige oplysninger i ordreopslag. Når registrerede brugere, der er logget på, opslag efter en ordre, som de oprettede, mens de blev logget på, vil de kunne se deres personlige oplysninger. |
| Kun gæsteordrer | Private oplysninger vises i ordreopslag for ordrer, som debitorer har oprettet som gæster. Hvis en ordre er oprettet af en registreret bruger, skal den pågældende bruger logge på for at se deres personlige oplysninger. |
| Alle ordrer | Personlige oplysninger vises i alle ordreopslag. |

> [!NOTE]
> Disse indstillinger bestemmer, hvornår personlige data som f.eks. kundens adresse og de sidste fire cifre i kundens kreditkortnummer vises som anonyme gæstebrugere. For at hjælpe med at beskytte de registrerede kunders personlige oplysninger anbefales det, at du kun vælger indstillingen **Gæsteordrer**. Den mest sikre indstilling er dog **Aldrig**.

Når du har ændret værdien af opslagsfeltet **Medtag personlige data i gæsteordreopslagsfeltet**, skal du køre job 1070 (**Kanalkonfiguration**) i Commerce Headquarters ved at gå til **Retail og Commerce \> Retail og Commerce IT \> Distributionsplan**.

## <a name="configure-the-order-lookup-module"></a>Konfigurere ordreopslagsmodulet

Ordreopslagsmodulet i modulbiblioteket til handel bruges til at vise den form, som gæstebrugere bruger til at slå ordrer op. Ordreopslagsmodulet kan inkluderes i brødteksten på alle sider, der ikke kræver kunde-logon. Yderligere oplysninger om, hvordan du konfigurerer modulet, finder du i [modulet Ordreopslag](order-lookup-module.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Modulet Ordreopslag](order-lookup-module.md)

[Konfigurere en profil for mailbesked](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]