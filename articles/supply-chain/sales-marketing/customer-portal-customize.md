---
title: Tilpasse og bruge kundeportalen
description: Denne artikel forklarer, hvordan du kan tilpasse debitorportalen, efter at den er føjet til systemet.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 85ec4beda2efe62ff5076a5ed694efbc47c6d87f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878868"
---
# <a name="customize-and-use-the-customer-portal"></a>Tilpasse og bruge kundeportalen

[!include [banner](../includes/banner.md)]


Denne artikel beskriver de forskellige sider, der er tilgængelige i debitorportalen lige fra starten. Her forklares, hvad siderne gør, og hvordan du kan tilpasse dem.

Debitorportalen indeholder nogle websider og handlinger lige fra starten. Følgende webstedkort giver et overblik over disse websider og handlinger samt de roller, der kan udføre handlingerne.

![Oversigt over kundeportalwebsted.](media/customer-portal-site-map.png "Oversigt over kundeportalwebsted")

## <a name="typical-customizations"></a>Typiske tilpasninger

I disse artikler kan du finde grundlæggende oplysninger om Power Apps-portaler og oplysninger om, hvordan du kan tilpasse portaler:

- [Arbejde med skabeloner](/powerapps/maker/portals/work-with-templates) – Denne artikel indeholder en generel oversigt over, hvordan Power Apps-portaler fungerer, og hvordan du kan foretage simple tilpasninger af portaler.
- [Administrere portalindhold](/dynamics365/portals/manage-portal-content) – Denne artikel forklarer, hvordan du kan administrere og tilpasse det indhold, der skal vises i din portal.
- [Redigere CSS](/powerapps/maker/portals/edit-css) – Denne artikel hjælper dig med at lave mere komplekse tilpasninger af portalens brugergrænseflade (UI).
- [Oprette et tema til din portal](/dynamics365/portals/create-theme) – Denne artikel hjælper dig med at oprette et brugergrænsefladetema til din portal.
- [Oprette og vise portalindhold nemt](/dynamics365/portals/create-expose-portal-content) – Denne artikel hjælper dig med at administrere de underliggende data og tabeller, du bruger til din portal.
- [Konfigurere en kontaktperson til brug i en portal](/powerapps/maker/portals/configure/configure-contacts) – Denne artikel forklarer, hvordan du opretter og tilpasser brugerroller, og hvordan sikkerhed og godkendelse fungerer i Power Apps-portaler.
- [Konfigurere noter til tabelformularer og webformularer på portaler](/powerapps/maker/portals/configure-notes) – Denne artikel forklarer, hvordan du kan føje dokumenter og yderligere lagerplads til din portal.
- [Fejlhåndtering for portalwebsted](/powerapps/maker/portals/admin/view-portal-error-log) – Denne artikel forklarer, hvordan du kan få vist logfilerne for portalfejl og gemme dem i din Microsoft Azure Blob-lagerkonto.

## <a name="customize-the-order-creation-process"></a>Tilpasse processen til oprettelse af ordrer

Når en bruger sender en ordre ved hjælp af debitorportalen, synkroniseres ordren automatisk til det relevante Dynamics 365 Supply Chain Management-miljø. Da brugeren er en ekstern kunde, er nogle af de påkrævede oplysninger bevidst skjult for ham eller hende. Disse oplysninger udfyldes automatisk, når formularen sendes.

I dette afsnit kan du se, hvordan du skal oprette kontaktpersoner for at undgå fejl. Her forklares de felter, der automatisk defineres, og hvordan du om nødvendigt kan ændre værdien i disse felter.

### <a name="the-out-of-box-order-creation-process"></a>Indbygget proces for oprettelse af ordrer

Her er standardtrinnene for afsendelse af en ordre fra debitorportalen.

1. På startsiden skal du vælge **Opret ordre** for at åbne guiden **Oprette ordre**.
1. På siden **Ordreoplysninger** skal du angive følgende felter:

    - **Ønsket modtagelsesdato** – Angiv leveringsdatoen.
    - **Leveringsadresse** – Angiv den adresse, som ordren skal leveres til.
    - **Firma** – Vælg navnet på debitorfirmaet. Dette felt udfyldes automatisk for brugere, der ikke er administratorer.
    - **Rekvisitionsnummer** – Angiv ordrens rekvisitionsnummer. Dette felt er valgfrit.
    - **Levér til land/område** – Angiv det land eller det område, som varerne skal leveres til. Dette felt udfyldes automatisk for brugere, der ikke er administratorer.

    ![Siden Ordreoplysninger.](media/customer-portal-order-information.png "Siden Ordreoplysninger")

1. Vælg **Næste**.
1. På siden **Varer** skal du vælge **Tilføj vare**.

    ![Siden varer.](media/customer-portal-items.png "Siden varer")

1. I dialogboksen **Vareoplysninger** indstilles følgende felter:

    - **Produktnavn** – Find og vælg et produkt, der skal føjes til ordren.
    - **Antal** – Angiv antal af det valgte produkt.
    - **Enhed** – Angiv måleenheden (f.eks **ea**, **kg** eller **kasse**).
    - **Forkalkuleret nettobeløb** – Værdien beregnes som den forkalkulerede pris for varen × antallet for den valgte enhed.

    ![Dialogboksen Vareoplysninger.](media/customer-portal-item-information.png "Dialogboksen Vareoplysninger")

1. Vælg **Send** for at føje varen til ordren.
1. Gentag trin 4 til 6, indtil du har tilføjet alle de varer, du vil bestille.
1. Vælg **Næste** på siden **Varer**, når du er færdig med at tilføje varer.
1. Siden **Ordreoplysninger** viser en oversigt over ordren. Gennemse ordreindholdet og leveringsoplysningerne. Hvis alt ser korrekt ud, skal du vælge **Send** for at sende ordren.

    ![Siden Fuldførte ordreoplysninger.](media/customer-portal-order-submit.png "Siden Fuldførte ordreoplysninger")

### <a name="standard-data-setup"></a>Opsætning af standarddata

For at hjælpe med at sikre en problemfri brugeroplevelse udfylder debitorportalen automatisk værdier for flere obligatoriske felter. Disse værdier er baseret på oplysningerne i kontaktpersonposten for den kunde, der skal sende ordren.

For hver [kontaktrække](/powerapps/maker/portals/configure/configure-contacts), der tilhører en kunde, som skal bruge kundeportalen til at sende ordrer, skal der angives værdier for følgende obligatoriske felter. Ellers opstår der fejl.

- **Firma** – Den juridiske enhed, som ordren tilhører
- **Potentiel kunde** – Den kundekonto, der er tilknyttet ordren
- **Prisliste** – Tilpasset prisliste til kunden
- **Valuta** – Valutaen for prisen
- **Levér til land/område** – Det land eller det område, som varerne skal leveres til

Følgende felter angives automatisk for salgsordretabellen:

- **Sprog** – Ordrens sprog (som standard hentes værdien fra kontaktpersonposten).
- **Levér til land/område** – Det land eller område, som varerne vil blive leveret til (som standard hentes værdien fra kontaktpersonposten).
- **Kontaktperson** – Den bruger, der kan kontaktes for at få oplysninger om ordren (som standard hentes værdien fra kontaktpersonposten).
- **Firma** – Den juridiske enhed, som ordren tilhører (som standard hentes værdien fra kontaktpersonposten).
- **Potentiel kunde** – Den debitorkonto, der er tilknyttet ordren (som standard hentes værdien fra kontaktpersonposten).
- **Fakturakunde** – Odrens faktureringskonto (standardværdien er den potentielle kunde fra kontaktpersonposten).
- **Salgsordrenavn** – Navnet på salgsordren (standardværdien er **salgsordre**).
- **Valuta** – Valutaen for prisen (som standard hentes værdien fra kontaktpersonposten).
- **Prisliste** – Den tilpassede prisliste til kunden (som standard hentes værdien fra kontaktpersonposten).
- **Beskrivelse af leveringsadresse** – Salgsordrens leveringsadresse (standardværdien er **beskrivelse af leveringsadressen**).

### <a name="modify-the-order-creation-process"></a>Tilpasning af processen til oprettelse af ordrer

Du kan frit ændre udseendet og brugergrænsefladen for debitorportalen, hvis du ikke ændrer grundprocessen for oprettelse af ordrer. Hvis du vil ændre processen for ordreoprettelse, er der nogle få punkter, som du skal huske.

Du må ikke fjerne følgende kolonner fra salgsordretabellen i Microsoft Dataverse, da de skal bruges til at oprette en salgsordre med to skrivninger:

- **Firma** – Den juridiske enhed, som ordren tilhører
- **Navn** – Navnet på salgsordren
- **Valuta** – Valutaen for prisen
- **Prisliste** – Tilpasset prisliste til kunden
- **Levér til land/område** – Det land eller det område, som varerne skal leveres til
- **Potentiel kunde** – Den kundekonto, der er tilknyttet ordren
- **Sprog** – Ordresproget (typisk er dette sprog den potentielle kundes sprog).
- **Beskrivelse af leveringsadresse** – Salgsordrens leveringsadresse

Følgende kolonner er påkrævet for varer:

- **Produkt** – Det produkt, der skal bestilles
- **Antal** – Antallet af det valgte produkt
- **Enhed** – Måleenheden (f.eks **ea**, **kg** eller **kasse**)
- **Levér til land/område** – Leveringsland eller -område
- **Beskrivelse af leveringsadresse** – Ordrens leveringsadresse

Du skal sikre dig, at debitorportalen kan sende værdier for alle disse kolonner.

Hvis du vil føje kolonner til siden eller fjerne kolonner, kan du finde flere oplysninger under [Oprette eller redigere formularer til hurtig oprettelse for en strømlinet dataindtastningsoplevelse](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Hvis du vil ændre, hvordan kolonner forudindstilles, og hvordan værdier angives, når siden gemmes, skal du se følgende oplysninger i dokumentationen for Power Apps-portalerne:

- [Udfyldning af felt på forhånd](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Angive værdi ved lagring](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Tilpasse startsiden

Alle kontrolelementer i debitorportalen er indbyggede kontrolelementer i Power Apps-portalerne. Du kan tilpasse dem ved at følge trinnene i [Oprette en side](/powerapps/maker/portals/compose-page) i dokumentationen for Power Apps- portaler.

Det eneste brugerdefinerede kontrolelement, der er medtaget i debitorportalskabelonen, bruges til at oprette felterne på startsiden.

![Felter på startsiden.](media/customer-portal-home-page-tiles.png "Felter på startsiden")

Følg disse trin for at ændre felterne.

1. Åbn [Portal Management-appen](/powerapps/maker/portals/configure/configure-portal).
1. Vælg **Sideskabeloner** i navigationsruden til venstre.

    ![Navigationsruden Portalstyring.](media/customer-portal-nav.png "Navigationsruden Portalstyring")

1. Vælg den sideskabelon, der hedder **Start**.
1. I feltet **Webskabelon** skal du vælge linket **Start** for at åbne kildekoden for denne side.

    ![Feltet Webskabelon.](media/customer-portal-web-template.png "Feltet Webskabelon")

1. Du kan nu se hele kildekoden for startsiden og ændre den efter behov.

## <a name="resources"></a>Ressourcer

Yderligere oplysninger om, hvordan du kan konfigurere og tilpasse debitorportalen, finder du i følgende ressourcer:

- [Power Apps-dokumentationen til portaler](/powerapps/maker/portals/overview)
- [Dokumentationen til dobbeltskrivning](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Om portalens livscyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Opgradering af en portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Overflytning af portalkonfiguration](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 for Customer Engagement-apps](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]