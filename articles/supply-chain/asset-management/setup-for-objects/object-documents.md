---
title: Aktivdokumenter
description: I dette emne beskrives aktivdokumenter i Styring af aktiver.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5b791fd3e060c4f4ecdb1ca599a6041d421db74
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024517"
---
# <a name="asset-documents"></a><span data-ttu-id="36db9-103">Aktivdokumenter</span><span class="sxs-lookup"><span data-stu-id="36db9-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="36db9-104">I dette emne beskrives aktivdokumenter i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="36db9-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="36db9-105">I Styring af aktiver kan du oprette dokumenter, så de automatisk relateres til f.eks. jobtyper, aktivproducenter, aktivtyper eller aktiver.</span><span class="sxs-lookup"><span data-stu-id="36db9-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="36db9-106">Denne funktion er nyttig, når opdaterede dokumentversioner udgives.</span><span class="sxs-lookup"><span data-stu-id="36db9-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="36db9-107">I så fald skal du bare placere det opdaterede dokument på den standardplacering, du bruger til dine Finance and Operations-dokumenter, og vedhæfte dokumentet til den dokumentposten for det aktiv, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="36db9-107">In that case, you just have to put the updated document in the standard location that you use for your Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="36db9-108">Du kan derefter få adgang til det opdaterede dokument fra menupunkterne **Alle aktiver**, **Aktive aktiver**, **Mine aktive aktiver**, **Alle arbejdsordrer** og **Aktive arbejdsordrejobs**.</span><span class="sxs-lookup"><span data-stu-id="36db9-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="36db9-109">Processen til tilknytning af dokumenter til en aktivdokumentpost bruger det dokumenthåndteringssystem, der er angivet som standard.</span><span class="sxs-lookup"><span data-stu-id="36db9-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="36db9-110">**Eksempel 1:** et dokument, der er relateret til en jobtype, kan beskrive en procedure for den pågældende jobtype.</span><span class="sxs-lookup"><span data-stu-id="36db9-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="36db9-111">**Eksempel 2:** et dokument, der er relateret til en kombination af en aktivtype, en producent og en model, kan være standardmanualen for den valgte aktivproducentmodel.</span><span class="sxs-lookup"><span data-stu-id="36db9-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="36db9-112">Opret aktivdokumentrelation</span><span class="sxs-lookup"><span data-stu-id="36db9-112">Create asset document relation</span></span>

1. <span data-ttu-id="36db9-113">Vælg **Styring af aktiver** \> **Opsætning** \> **Aktivdokumenter**.</span><span class="sxs-lookup"><span data-stu-id="36db9-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="36db9-114">Vælg **Ny** for at oprette en aktivdokumentpost.</span><span class="sxs-lookup"><span data-stu-id="36db9-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="36db9-115">Afhængigt af det hvor detaljeret, du ønsker, at dokumentrelationen skal være, skal du foretage relevante valg i et eller flere af følgende felter: **Aktivtype**, **Producent**, **Model**, **Aktiv**, **Jobtypekategori**, **Jobtype**, **Jobtypevariant** og **Jobkrav**.</span><span class="sxs-lookup"><span data-stu-id="36db9-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="36db9-116">De indstillinger, der er tilgængelige i felterne **Jobtypevariant** og **Jobkrav**, afhænger af dit valg i feltet **Jobtype**.</span><span class="sxs-lookup"><span data-stu-id="36db9-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36db9-117">Når systemet søger efter dokumenter, der skal relateres til et aktiv eller en arbejdsordre, gennemgår Styring af aktiver alle aktivdokumentposter for at søge efter et potentielt match.</span><span class="sxs-lookup"><span data-stu-id="36db9-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="36db9-118">Den kontrollerer altid den mest specifikke kombination først.</span><span class="sxs-lookup"><span data-stu-id="36db9-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="36db9-119">Med andre ord kontrollerer Styring af aktiver først, om der er et match for feltet **Jobkrav**.</span><span class="sxs-lookup"><span data-stu-id="36db9-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="36db9-120">Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Jobtypevariant**.</span><span class="sxs-lookup"><span data-stu-id="36db9-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="36db9-121">Hvis der ikke findes et match, kontrolleres det, om der er et match for feltet **Jobtype** osv.</span><span class="sxs-lookup"><span data-stu-id="36db9-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="36db9-122">Som du kan se i layoutet for siden **Styring af aktiver**, betyder denne adfærd, at Styring af aktiver kontrollerer hver enkelt post fra højre mod venstre for et match for at finde den mest specifikke kombination.</span><span class="sxs-lookup"><span data-stu-id="36db9-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="36db9-123">Flere dokumenter kan være relateret til et aktiv eller en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="36db9-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="36db9-124">Du kan redigere serviceniveauet på en reparationsanmodning eller en arbejdsordre efter behov.</span><span class="sxs-lookup"><span data-stu-id="36db9-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="36db9-125">Vælg **Vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="36db9-125">Select **Attachments**.</span></span> <span data-ttu-id="36db9-126">Standardsiden **Dokumentoversigt** vises.</span><span class="sxs-lookup"><span data-stu-id="36db9-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="36db9-127">Konfigurer de dokumenter eller notater, der skal knyttes til aktivets dokumentpost.</span><span class="sxs-lookup"><span data-stu-id="36db9-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="36db9-128">Når du har vedhæftet dokumenter, viser feltet **Vedhæftede filer** det antal dokumenter, der er relateret til posten.</span><span class="sxs-lookup"><span data-stu-id="36db9-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
