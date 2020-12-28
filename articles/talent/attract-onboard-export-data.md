---
title: Eksportere data fra Attract og Onboard
description: Eksportere data fra Dynamics 365 Talent - Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460631"
---
# <a name="export-data-from-attract-and-onboard"></a>Eksportere data fra Attract og Onboard

[!include [banner](includes/banner.md)]

Som annonceret i [Tilbagetrækningen af Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) tilbagetrækker vi Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard d. 1. februar 2022. Begge apps kan nu tilbyde funktioner til dataeksport for at hjælpe med migreringen til et andet produkt.

## <a name="export-data-from-attract"></a>Eksportér data fra Attract

Du kan eksportere dine data uden at begrænse adgangen til dit miljø. Det kan være en god ide at gøre dette med henblik på test eller for at forstå vores datastruktur. Når du er klar til at overføre, skal du begrænse adgangen til dit Attract-miljø vha. instruktionerne efter denne procedure. Sørg for at eksportere dataene igen. 

1. Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Vælg **Anmod om en dataeksport** under **Dataeksport**.

   ![[Anmode om en dataeksport fra Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Når meddelelsen **Din anmodning behandles**, skal du klikke på **OK**. Dataeksporten kan vare op til 20 minutter, afhængigt af eksportens størrelsen.

4. Når eksporten er fuldført, skal du vælge knappen **Download** ud for den. 

   >[!NOTE]
   >Alle dataeksporter er tilgængelige i syv dage, hvorefter linket **Download** udløber.</br>
   
Downloaden indeholder en .zip-fil med dine Attract-data, herunder følgende mapper:

| Mappenavn | Beskrivelse |
| --- | --- |
| Administratorindstillinger | Konfigurationer af Attract-administrationscenter. |
| Kandidater | Alle kandidater, der er føjet til job eller talentpuljer. |
| Mailskabeloner | Alle mailskabeloner, der er konfigureret for miljøet. |
| Skabeloner til jobtilbudspakker | Alle job tilbyder pakkeskabeloner, der er oprettet, plus de tilknyttede konfigurationer. |
| Job, der tilbyder regelsæt |  Alle filer med regelsæt, der er uploadet til tilbudsstyring. |
| Skabeloner til jobtilbud | Alle jobtilbudsdokumentskabeloner, der er oprettet for miljøet. |
| Jobtilbud | Alle oprettede job. Slettede job eksporteres ikke. Undermapperne indeholder kandidatansøgninger med undermapper til vedhæftninger af kandidatansøgninger og tilbyder evt. pakker. |
| Skabeloner til jobtilbud | Skabeloner til jobtilbud, der er konfigureret i miljøet. |
| Talentpuljer | Alle oprettede talentpuljer, deres bidragyderelister og kandidatlister til talentgrupperne. |
| Arbejdere | Liste over alle de arbejdere, der findes i miljøet, plus deres roller. |
| (rodmappe) | En JSON-skemafil, der beskriver datastrukturfelterne. |

### <a name="restrict-access-to-attract"></a>Begræns adgangen til Attract

Når du er klar til at overføre, skal du begrænse ikke-administratorer i at få adgang til dit Attract-miljø og eksportere dataene.

>[!IMPORTANT]
>Begrænsning af adgangen til dit Attract-miljø er permanent og kan ikke fortrydes. Hvis brugere uden administratorrettigheder fortsat skal have adgang til dit miljø, kan du springe dette trin over.

1. Gå til [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Hvis du vil forhindre, at ikke-administratorer får adgang til dit Attract-miljø, skal du vælge **Begræns adgang nu** under **Begræns adgang nu til denne app**. Hvis du begrænser adgangen, medfører det også, at aktive job, der er bogført, ikke bogføres.

   ![[Begræns ikke-administratoradgang til Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Når advarslen **Dette er en permanent ændringe** vises, skal du vælge **Begræns adgang** for permanent at begrænse brugere, der ikke er administratorer, ud af dette miljø. Vælg **Annuller**, hvis du ikke er klar til at fuldføre dette trin.

   ![[Advarsel om, at begrænsende adgang er en permanent ændring](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administratorer kan fortsætte med at få adgang til dataeksport- og personrapportsiderne, når du har begrænset adgangen til Attract-miljøet.

## <a name="export-data-from-onboard"></a>Eksportér data fra Onboard

Når du er klar, kan du downloade skabeloner, guider og kandidatdata fra Onboard.

1. Gå til [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Vælg **Anmod om en dataeksport** under **Dataeksport**. 

   ![[Anmode om en dataeksport fra Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Når meddelelsen **Din anmodning behandles**, skal du klikke på **OK**. Dataeksporten kan vare op til 20 minutter, afhængigt af eksportens størrelsen.

4. Når eksporten er fuldført, skal du vælge knappen **Download** ud for den. 

   ![[Download data, som er eksporteret fra Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Dataeksporten er tilgængelig i syv dage. Efter syv dage udløber linket **Download**, og du skal anmode om en ny eksport, hvis du har brug for at downloade dataene igen. Når du starter en ny dataeksport, udløber eventuelle eksisterende downloads, efter at den nye eksport er fuldført.

Downloaden er en .zip-fil, der indeholder:

- En **Skabelon** mappe, der indeholder dine indbyggede Onboard-skabeloner i Word-dokumentformat.

- En **Guides** mappe, der indeholder dine indbyggede Onboard-guides i Word-dokumentformat.

## <a name="see-also"></a>Se også

[Tilbagetrækning af Dynamics 365 Talent: Attract- og Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)