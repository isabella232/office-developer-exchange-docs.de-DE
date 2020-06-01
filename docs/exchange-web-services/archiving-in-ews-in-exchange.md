---
title: Archivierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Erfahren Sie mehr über die Archivierung in EWS in Exchange.
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456213"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="d814d-103">Archivierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d814d-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="d814d-104">Erfahren Sie mehr über die Archivierung in EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="d814d-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="d814d-105">Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d814d-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="d814d-106">Archivpostfächer werden in der Regel zum Verwalten von e-Mail-Speichergrenzwerten verwendet.</span><span class="sxs-lookup"><span data-stu-id="d814d-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="d814d-107">Beispielsweise können ältere e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d814d-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="d814d-108">Exchange Online, Exchange Online im Rahmen von Office 365 und Exchange Server 2013 Einführung zweier neuer Exchange-Webdienste Vorgänge, die Sie zum Archivieren einer Gruppe von e-Mail-Elementen aus einem primären Postfach verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d814d-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="d814d-109">Wenn Sie Posteingangs Elemente auf diese Weise archivieren, wird die Ordnerhierarchie der Elemente beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d814d-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="d814d-110">Darüber hinaus können Archivpostfächer nun entweder lokal auf einem Client oder Remote in einer für einen Benutzer undurchsichtigen Weise gespeichert werden, indem ein Ordnerpfad verwendet wird, um auf den Inhalt des Archivs zu deuten.</span><span class="sxs-lookup"><span data-stu-id="d814d-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="d814d-111">Archivierungsvorgänge in EWS</span><span class="sxs-lookup"><span data-stu-id="d814d-111">Archiving operations in EWS</span></span>

<span data-ttu-id="d814d-112">In der folgenden Tabelle sind die in Exchange 2013 eingeführten Archivierungsvorgänge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d814d-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="d814d-113">**Name des Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="d814d-113">**Operation name**</span></span>|<span data-ttu-id="d814d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d814d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d814d-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="d814d-115">ArchiveItem</span></span>](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="d814d-116">Verschiebt ein Element aus dem primären Postfach in das Archivpostfach.</span><span class="sxs-lookup"><span data-stu-id="d814d-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="d814d-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="d814d-117">CreateFolderPath</span></span>](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="d814d-118">Erstellt einen URI, der auf den Speicherort für das Archivpostfach zeigt.</span><span class="sxs-lookup"><span data-stu-id="d814d-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d814d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d814d-119">See also</span></span>

- [<span data-ttu-id="d814d-120">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="d814d-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="d814d-121">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="d814d-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="d814d-122">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="d814d-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

