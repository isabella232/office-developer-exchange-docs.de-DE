---
title: Archivierung in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: Informationen Sie zu Archivierung in EWS in Exchange.
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756813"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="379b3-103">Archivierung in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="379b3-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="379b3-104">Informationen Sie zu Archivierung in EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="379b3-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="379b3-105">Archivpostfächer sind sekundäre Postfächer, die einem Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="379b3-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="379b3-106">Archivpostfächer sind in der Regel zum Verwalten von Speichergrenzen für e-Mail verwendet.</span><span class="sxs-lookup"><span data-stu-id="379b3-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="379b3-107">Beispielsweise könnte der älteren e-Mail-Elemente in regelmäßigen Abständen aus dem Posteingang in das Archivpostfach verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="379b3-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="379b3-108">Exchange Online, Exchange Online als Teil von Office 365 und Exchange Server 2013 eine Einführung in zwei neue Exchange-Webdienste (EWS)-Vorgänge, die Sie verwenden können, um eine Reihe von e-Mail-Elementen aus einem primären Postfach archivieren.</span><span class="sxs-lookup"><span data-stu-id="379b3-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="379b3-109">Archivierung von Elementen im Posteingang auf diese Weise wird die Hierarchie der Ordner Elemente beibehalten.</span><span class="sxs-lookup"><span data-stu-id="379b3-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="379b3-110">Darüber hinaus können archivpostfächer jetzt gespeichert werden, entweder lokal auf einem Client oder Remote, in eine Möglichkeit, die mit einem Ordnerpfad auf den Inhalt des Archivs zeigen hauptsächlich an einen Benutzer nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="379b3-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="379b3-111">Archivierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="379b3-111">Archiving operations in EWS</span></span>

<span data-ttu-id="379b3-112">Die folgende Tabelle enthält die Archivierung Vorgänge, die in Exchange 2013 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="379b3-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="379b3-113">**Name des Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="379b3-113">**Operation name**</span></span>|<span data-ttu-id="379b3-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="379b3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="379b3-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="379b3-115">ArchiveItem</span></span>](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="379b3-116">Verschiebt ein Element aus dem Hauptpostfach in das Archivpostfach.</span><span class="sxs-lookup"><span data-stu-id="379b3-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="379b3-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="379b3-117">CreateFolderPath</span></span>](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="379b3-118">Erstellt einen URI, der auf den Speicherort für das Archivpostfach verweist.</span><span class="sxs-lookup"><span data-stu-id="379b3-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="379b3-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="379b3-119">See also</span></span>

- [<span data-ttu-id="379b3-120">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="379b3-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="379b3-121">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="379b3-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="379b3-122">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="379b3-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

