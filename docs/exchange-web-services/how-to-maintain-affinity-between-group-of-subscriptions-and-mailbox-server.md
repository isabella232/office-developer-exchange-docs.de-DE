---
title: Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Informieren Sie sich über die Beibehaltung der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver.
localization_priority: Priority
ms.openlocfilehash: 1618216cf69e08b2ae774264e0910856a59851af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455757"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a><span data-ttu-id="d6d13-103">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-103">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>

<span data-ttu-id="d6d13-104">Informieren Sie sich über die Beibehaltung der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="d6d13-104">Find out about maintaining the affinity between a group of subscriptions and the Mailbox server.</span></span>
  
<span data-ttu-id="d6d13-105">Affinität ist die Zuordnung einer Sequenz von Anforderungs-und Antwortnachrichten mit einem bestimmten Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="d6d13-105">Affinity is the association of a sequence of request and response messages with a particular Mailbox server.</span></span> <span data-ttu-id="d6d13-106">Für die meisten Funktionen in Exchange wird die Affinität vom Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d6d13-106">For most functionality in Exchange, affinity is handled by the server.</span></span> <span data-ttu-id="d6d13-107">Benachrichtigungen sind jedoch eine Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="d6d13-107">Notifications, however, are an exception.</span></span> <span data-ttu-id="d6d13-108">Der Client ist für die Beibehaltung der Affinität mit dem Postfachserver für Benachrichtigungsabonnements verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d6d13-108">The client is responsible for maintaining the affinity with the Mailbox server for notification subscriptions.</span></span> <span data-ttu-id="d6d13-109">Diese Affinität ermöglicht es dem Lastenausgleich und den Clientzugriffsservern zwischen dem Client und dem Server, Benachrichtigungsabonnements und zugehörige Anforderungen an den Postfachserver weiterzuleiten, der das Abonnement verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d6d13-109">This affinity enables the load balancer and Client Access servers between the client and the server to route notification subscriptions and related requests to the Mailbox server that maintains the subscription.</span></span> <span data-ttu-id="d6d13-110">Ohne Affinität wird die Anforderung möglicherweise an einen anderen Postfachserver weitergeleitet, der nicht die Abonnements des Clients enthält, was dazu führen kann, dass ein [ErrorSubscriptionNotFound](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-110">Without affinity, the request might get routed to a different Mailbox server that does not include the client's subscriptions, which can cause an [ErrorSubscriptionNotFound](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) error to be returned.</span></span> 
  
## <a name="how-is-affinity-maintained"></a><span data-ttu-id="d6d13-111">Wie wird Affinität beibehalten?</span><span class="sxs-lookup"><span data-stu-id="d6d13-111">How is affinity maintained?</span></span>
<span data-ttu-id="d6d13-112"><a name="bk_howmaintained"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d13-112"><a name="bk_howmaintained"> </a></span></span>

<span data-ttu-id="d6d13-113">Affinität in Exchange ist Cookie-basiert.</span><span class="sxs-lookup"><span data-stu-id="d6d13-113">Affinity in Exchange is cookie based.</span></span> <span data-ttu-id="d6d13-114">Der Client löst die Erstellung des Cookies durch einschließen bestimmter Kopfzeilen in der Abonnementanforderung aus, und die Abonnement Antwort enthält dann das Cookie.</span><span class="sxs-lookup"><span data-stu-id="d6d13-114">The client triggers the creation of the cookie by including specific headers in the subscription request, and then the subscription response contains the cookie.</span></span> <span data-ttu-id="d6d13-115">Der Client sendet dann dieses Cookie in nachfolgenden Anforderungen, um sicherzustellen, dass die Anforderung an den richtigen Postfachserver weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-115">The client then sends that cookie in subsequent requests to ensure that the request is routed to the right Mailbox server.</span></span>
  
<span data-ttu-id="d6d13-116">Konkret wird Affinität in Exchange wie folgt behandelt:</span><span class="sxs-lookup"><span data-stu-id="d6d13-116">More specifically, affinity in Exchange is handled by the following:</span></span> 
  
- <span data-ttu-id="d6d13-117">X-AnchorMailbox – ein HTTP-Header, der in der anfänglichen Abonnementanforderung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-117">X-AnchorMailbox — An HTTP header that is included in the initial subscription request.</span></span> <span data-ttu-id="d6d13-118">Er identifiziert das erste Postfach in einer Gruppe von Postfächern, die die Affinität mit dem gleichen Postfachserver gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-118">It identifies the first mailbox in a group of mailboxes that share affinity with the same Mailbox server.</span></span>
    
- <span data-ttu-id="d6d13-119">X-PreferServerAffinity – ein HTTP-Header, der in der anfänglichen Abonnementanforderung mit dem x-AnchorMailbox-Header enthalten ist und auf true festgelegt ist, um anzugeben, dass der Client die Beibehaltung der Affinität mit dem Postfachserver beantragt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-119">X-PreferServerAffinity — An HTTP header that is included in the initial subscription request with the X-AnchorMailbox header and is set to true to indicate that the client is requesting that affinity be maintained with the Mailbox server.</span></span>
    
- <span data-ttu-id="d6d13-120">X-BackEndOverrideCookie – ein Cookie, das in der anfänglichen Abonnement Antwort enthalten ist und ein Cookie enthält, mit dem der Lastenausgleich und der Client Zugriffsserver nachfolgende Anforderungen an denselben Postfachserver weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-120">X-BackEndOverrideCookie — A cookie that is included in the initial subscription response and contains a cookie that the load balancer and Client Access server use to route subsequent requests to the same Mailbox server.</span></span>
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a><span data-ttu-id="d6d13-121">Wie kann ich die Affinität mit dem verwaltete EWS-API oder EWS beibehalten?</span><span class="sxs-lookup"><span data-stu-id="d6d13-121">How do I maintain affinity by using the EWS Managed API or EWS?</span></span>
<span data-ttu-id="d6d13-122"><a name="bk_howdoimaintain"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d13-122"><a name="bk_howdoimaintain"> </a></span></span>

<span data-ttu-id="d6d13-123">Sie können die gleichen Schritte verwenden, um die Affinität für mehrere Post Fach Abonnements und deren Postfachserver beizubehalten, unabhängig davon, ob Sie Streaming-, Pull-oder Push-Benachrichtigungen verwenden, und unabhängig davon, ob Sie auf einen lokalen Exchange-Server oder auf Exchange Online ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="d6d13-123">You can use the same steps to maintain affinity for multiple mailbox subscriptions and their Mailbox servers, regardless of whether you are using streaming, pull, or push notifications, and regardless of whether you're targeting an Exchange on-premises server or Exchange Online.</span></span>
  
1. <span data-ttu-id="d6d13-124">Rufen Sie für jedes Postfach die [AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) auf, und rufen Sie die Benutzereinstellungen GroupingInformation und ExternalEwsUrl ab.</span><span class="sxs-lookup"><span data-stu-id="d6d13-124">For each mailbox, [call Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and get the GroupingInformation and ExternalEwsUrl user settings.</span></span> <span data-ttu-id="d6d13-125">Für die SOAP-AutoErmittlung verwenden Sie das [Setting](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) -Element, und für POX AutoErmittlung verwenden Sie das [GroupingInformation](https://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="d6d13-125">For SOAP Autodiscover, you use the [Setting](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element, and for POX Autodiscover, you use the [GroupingInformation](https://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) element.</span></span> 
    
2. <span data-ttu-id="d6d13-126">Platzieren Sie mithilfe der GroupingInformation-und ExternalEwsUrl-Einstellungen aus den Antworten der AutoErmittlung Postfächer mit dem gleichen ExternalEwsUrl-und GroupingInformation-verketteten Wert in derselben Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d6d13-126">Using the GroupingInformation and ExternalEwsUrl settings from the Autodiscover responses, place mailboxes with the same ExternalEwsUrl and GroupingInformation concatenated value in the same group.</span></span> <span data-ttu-id="d6d13-127">Wenn Gruppen über mehr als 200 Postfächer verfügen, unterbrechen Sie die Gruppen weiter, sodass jede Gruppe nicht mehr als 200 Postfächer aufweist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-127">If any groups have more than 200 mailboxes, break the groups down further so that each group has no more than 200 mailboxes.</span></span>
    
3. <span data-ttu-id="d6d13-128">Erstellen Sie und verwenden Sie ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) -Objekt für den Rest der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d6d13-128">Create and use one [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) object for the rest of the procedure.</span></span> <span data-ttu-id="d6d13-129">Wenn Sie dasselbe **Datei "ExchangeService** -Objekt verwenden, werden Cookies und Kopfzeilen (wenn Sie festgelegt sind) automatisch verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d6d13-129">When you use the same **ExchangeService** object, cookies and headers (when they are set) are automatically maintained.</span></span> <span data-ttu-id="d6d13-130">Beachten Sie, dass Sie, wenn Sie nicht beabsichtigen, Streaming-Abonnements in einer einzelnen Verbindung zu gruppieren, ein anderes **Datei "ExchangeService** -Objekt für jeden imitierten Benutzer erstellen können.</span><span class="sxs-lookup"><span data-stu-id="d6d13-130">Note that if you do not intend to group streaming subscriptions into a single connection, you are free to create a different **ExchangeService** object for each impersonated user.</span></span> 
    
4. <span data-ttu-id="d6d13-131">[Senden Sie eine Abonnement](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) Anforderung für den Benutzer, dessen Benutzername zuerst angezeigt wird, wenn alle Benutzer in der Gruppe alphabetisch sortiert sind (dieser Benutzer wird als Anker Postfachbenutzer bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="d6d13-131">[Send a subscription](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) request for the user whose user name appears first when all users in the group are sorted alphabetically (we'll refer to this user as the anchor mailbox user).</span></span> <span data-ttu-id="d6d13-132">Gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="d6d13-132">Do the following:</span></span> 
    
  - <span data-ttu-id="d6d13-133">Fügen Sie den X-AnchorMailbox-Header mit einem Wert ein, der auf die SMTP-Adresse des Anker Postfachbenutzers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-133">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user.</span></span>
    
  - <span data-ttu-id="d6d13-134">Fügen Sie den X-PreferServerAffinity-Header hinzu, wobei der Wert auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-134">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="d6d13-135">Verwenden Sie die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle (der [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) -Typ).</span><span class="sxs-lookup"><span data-stu-id="d6d13-135">Use the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
5. <span data-ttu-id="d6d13-136">Rufen Sie in der Abonnement Antwort den X-BackEndOverrideCookie-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="d6d13-136">In the subscription response, get the X-BackEndOverrideCookie value.</span></span> <span data-ttu-id="d6d13-137">Fügen Sie diesen Wert in jede der nachfolgenden Abonnementanforderungen für Benutzer in dieser Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="d6d13-137">Include this value in each of the subsequent subscription requests for users in this group.</span></span>
    
6. <span data-ttu-id="d6d13-138">Senden Sie für jeden weiteren Benutzer in der Gruppe eine Abonnementanforderung, und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d6d13-138">For each additional user in the group, send a subscription request and do the following:</span></span>
    
  - <span data-ttu-id="d6d13-139">Fügen Sie den X-AnchorMailbox-Header mit einem Wert ein, der auf die SMTP-Adresse des Anker Postfachbenutzers für die Gruppe festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-139">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user for the group.</span></span>
    
  - <span data-ttu-id="d6d13-140">Fügen Sie den X-PreferServerAffinity-Header hinzu, wobei der Wert auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-140">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="d6d13-141">Schließen Sie die X-BackEndOverrideCookie ein, die in der Abonnement Antwort des Anchor-Postfachbenutzers zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d6d13-141">Include the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response.</span></span>
    
  - <span data-ttu-id="d6d13-142">Verwenden Sie die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle (der [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) -Typ).</span><span class="sxs-lookup"><span data-stu-id="d6d13-142">Use the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](https://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
    <span data-ttu-id="d6d13-143">Beachten Sie, dass der Server die Werte x-PreferServerAffinity und x-BackendOverrideCookie zusammen verwendet, um das Routing an den Postfachserver durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-143">Note that the server uses the X-PreferServerAffinity and X-BackendOverrideCookie values together to perform the routing to the mailbox server.</span></span> <span data-ttu-id="d6d13-144">Der X-AnchorMailbox-Header ist ebenfalls erforderlich, wird vom Server jedoch ignoriert, wenn die beiden anderen Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="d6d13-144">The X-AnchorMailbox header is also required, but is ignored by the server if the other two values are valid.</span></span> <span data-ttu-id="d6d13-145">Wenn sich x-AnchorMailbox und x-PreferServerAffinity in einer Anforderung befinden und x-BackendOverrideCookie nicht enthalten ist, wird der x-AnchorMailbox-Wert verwendet, um die Anforderungen weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-145">If X-AnchorMailbox and X-PreferServerAffinity are in a request and X-BackendOverrideCookie is not included, the X-AnchorMailbox value is used to route the requests.</span></span>
    
    <span data-ttu-id="d6d13-146">Da die x-PreferServerAffinity-und x-BackendOverrideCookie-Werte das Routing durchführen, ändert sich die Logik nicht, wenn das Anker Postfach jemals auf eine andere Gruppe oder einen anderen Server verschoben wird, da die x-BackendOverrideCookie die Anforderung an den richtigen Server für die Gruppe weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="d6d13-146">Because the X-PreferServerAffinity and X-BackendOverrideCookie values perform the routing, if the anchor mailbox ever moves to another group or server, the logic does not change because the X-BackendOverrideCookie will route the request to the correct server for the group.</span></span>
    
7. <span data-ttu-id="d6d13-147">Senden Sie eine einzelne [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -oder [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) -Anforderung für die Gruppe, und führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d6d13-147">Send a single [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) requests for the group, and do the following:</span></span> 
    
  - <span data-ttu-id="d6d13-148">Fügen Sie die in jeder einzelnen Abonnement Antwort für Postfächer in der Gruppe zurückgegebenen [Subscription](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -Wert-Werte ein.</span><span class="sxs-lookup"><span data-stu-id="d6d13-148">Include the [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values returned in each of the individual subscription responses for mailboxes in the group.</span></span> 
    
  - <span data-ttu-id="d6d13-149">Wenn mehr als 200 Abonnements für die Gruppe vorhanden sind, erstellen Sie mehrere Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-149">If more than 200 subscriptions exist for the group, create multiple requests.</span></span> <span data-ttu-id="d6d13-150">Die maximale Anzahl von [Subskriptions](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -ID-Werten, die in eine Anforderung eingeschlossen werden sollen, lautet 200.</span><span class="sxs-lookup"><span data-stu-id="d6d13-150">The maximum number of [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values to include in a request is 200.</span></span> 
    
  - <span data-ttu-id="d6d13-151">Wenn Sie mehr Verbindungen benötigen, als für das Zielpostfach zur Verfügung stehen, verwenden Sie das Dienstkonto, um die Identität des Anker Postfachs für die Gruppe zu imitieren. Verwenden Sie andernfalls keinen Identitätswechsel.</span><span class="sxs-lookup"><span data-stu-id="d6d13-151">If you need more connections than are available to the target mailbox, use the service account to impersonate the anchor mailbox for the group; otherwise, do not use impersonation.</span></span> <span data-ttu-id="d6d13-152">Idealerweise möchten Sie die Identität eines eindeutigen Postfachs pro [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -oder [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) -Anforderung annehmen, damit keine Einschränkungs Grenzwerte auftreten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-152">Ideally, you want to impersonate a unique mailbox per [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](https://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) request so that you never encounter throttling limits.</span></span> 
    
  - <span data-ttu-id="d6d13-153">Verwenden Sie ApplicationImpersonation, wenn Sie [mehr Verbindungen benötigen, als für das Zielpostfach verfügbar sind](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling). Verwenden Sie andernfalls nicht ApplicationImpersonation.</span><span class="sxs-lookup"><span data-stu-id="d6d13-153">Use ApplicationImpersonation if you need [more connections than are available to the target mailbox](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); otherwise, do not use ApplicationImpersonation.</span></span>
    
  - <span data-ttu-id="d6d13-154">Fügen Sie den X-PreferServerAffinity-Header hinzu, und legen Sie ihn auf true fest.</span><span class="sxs-lookup"><span data-stu-id="d6d13-154">Include the X-PreferServerAffinity header and set it to true.</span></span> <span data-ttu-id="d6d13-155">Dieser Wert wird automatisch einbezogen, wenn Sie das **Datei "ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d6d13-155">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
  - <span data-ttu-id="d6d13-156">Schließen Sie die x-BackEndOverrideCookie für die Gruppe ein (die x-BackEndOverrideCookie, die in der Abonnement Antwort des Anchor-Postfachbenutzers zurückgegeben wurde).</span><span class="sxs-lookup"><span data-stu-id="d6d13-156">Include the X-BackEndOverrideCookie for the group (the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response).</span></span> <span data-ttu-id="d6d13-157">Dieser Wert wird automatisch einbezogen, wenn Sie das **Datei "ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d6d13-157">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
8. <span data-ttu-id="d6d13-158">Übergeben Sie die zurückgegebenen Ereignisse zur Verarbeitung an einen separaten Thread.</span><span class="sxs-lookup"><span data-stu-id="d6d13-158">Pass the returned events to a separate thread for processing.</span></span>
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a><span data-ttu-id="d6d13-159">Welche Drosselungswerte muss ich berücksichtigen?</span><span class="sxs-lookup"><span data-stu-id="d6d13-159">What throttling values do I need to take into consideration?</span></span>
<span data-ttu-id="d6d13-160"><a name="bk_throttling"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d13-160"><a name="bk_throttling"> </a></span></span>

<span data-ttu-id="d6d13-161">Während Sie Ihre Benachrichtigungs Implementierung planen, sollten Sie zwei Werte berücksichtigen: die Anzahl der Verbindungen und die Anzahl der Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d6d13-161">As you plan your notification implementation, you'll want to take two values into consideration: the number of connections, and the number of subscriptions.</span></span> <span data-ttu-id="d6d13-162">In der folgenden Tabelle sind die Standardwerte für jede [Einschränkungs](ews-throttling-in-exchange.md) Einstellung und die Verwendung der Einstellungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-162">The following table lists the default values for each [throttling](ews-throttling-in-exchange.md) setting and how the settings are used.</span></span> <span data-ttu-id="d6d13-163">Für jeden Wert wird das Budget dem Zielpostfach zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-163">For each value, the budget is allocated to the target mailbox.</span></span> <span data-ttu-id="d6d13-164">Aus diesem Grund ist die Verwendung eines Identitätswechsels zur Gewinnung zusätzlicher Verbindungen ein erforderlicher Schritt in vielen Szenarien.</span><span class="sxs-lookup"><span data-stu-id="d6d13-164">For this reason, using impersonation to gain additional connections is a required step in many scenarios.</span></span> 
  
<span data-ttu-id="d6d13-165">**Tabelle 1. Standardmäßige Drosselungswerte**</span><span class="sxs-lookup"><span data-stu-id="d6d13-165">**Table 1. Default throttling values**</span></span>

|<span data-ttu-id="d6d13-166">**Beachtung des Bereichs**</span><span class="sxs-lookup"><span data-stu-id="d6d13-166">**Area of consideration**</span></span>|<span data-ttu-id="d6d13-167">**Einschränkungseinstellung**</span><span class="sxs-lookup"><span data-stu-id="d6d13-167">**Throttling setting**</span></span>|<span data-ttu-id="d6d13-168">**Standardwert**</span><span class="sxs-lookup"><span data-stu-id="d6d13-168">**Default value**</span></span>|<span data-ttu-id="d6d13-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6d13-169">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d6d13-170">Streaming-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="d6d13-170">Streaming connections</span></span>  <br/> |<span data-ttu-id="d6d13-171">Grenzwert für die standardmäßige hängende Verbindung</span><span class="sxs-lookup"><span data-stu-id="d6d13-171">Default hanging connection limit</span></span>  <br/> |<span data-ttu-id="d6d13-172">10 für Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d6d13-172">10 for Exchange Online</span></span>  <br/> <span data-ttu-id="d6d13-173">3 für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d6d13-173">3 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="d6d13-174">Die maximale Anzahl gleichzeitiger Streaming-Verbindungen, die ein Konto auf dem Server gleichzeitig geöffnet haben kann.</span><span class="sxs-lookup"><span data-stu-id="d6d13-174">The maximum number of concurrent streaming connections that an account can have open on the server at one time.</span></span> <span data-ttu-id="d6d13-175">Wenn Sie innerhalb dieses Grenzwerts arbeiten möchten, verwenden Sie ein Dienstkonto mit der ApplicationImpersonation-Rolle, die für die Zielpostfächer zugewiesen ist, und imitieren Sie den ersten Benutzer in jeder Abonnement-ID-Gruppe, wenn Sie Streaming-Ereignisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-175">To work within this limit, use a service account with the ApplicationImpersonation role assigned for the target mailboxes, and impersonate the first user in each subscription ID group when getting streamed events.</span></span>  <br/> |
|<span data-ttu-id="d6d13-176">Pull-oder Push-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="d6d13-176">Pull or push connections</span></span>  <br/> |<span data-ttu-id="d6d13-177">EWSMaxConcurrency</span><span class="sxs-lookup"><span data-stu-id="d6d13-177">EWSMaxConcurrency</span></span>  <br/> |<span data-ttu-id="d6d13-178">27</span><span class="sxs-lookup"><span data-stu-id="d6d13-178">27</span></span>  <br/> |<span data-ttu-id="d6d13-179">Die maximale Anzahl gleichzeitiger Pull-oder Push-Verbindungen (Anforderungen, die empfangen wurden, aber noch nicht beantwortet wurden), die ein Konto auf dem Server gleichzeitig öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="d6d13-179">The maximum number of concurrent pull or push connections (requests that have been received but not yet responded to) that an account can have open on the server at one time.</span></span>  <br/> |
|<span data-ttu-id="d6d13-180">Abonnements</span><span class="sxs-lookup"><span data-stu-id="d6d13-180">Subscriptions</span></span>  <br/> |<span data-ttu-id="d6d13-181">EWSMaxSubscriptions</span><span class="sxs-lookup"><span data-stu-id="d6d13-181">EWSMaxSubscriptions</span></span>  <br/> |<span data-ttu-id="d6d13-182">20 für Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d6d13-182">20 for Exchange Online</span></span>  <br/> <span data-ttu-id="d6d13-183">5000 für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d6d13-183">5000 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="d6d13-184">Die maximale Anzahl von nicht abgelaufenen Abonnements, die ein Konto auf einmal haben kann.</span><span class="sxs-lookup"><span data-stu-id="d6d13-184">The maximum number of nonexpired subscriptions that an account can have at one time.</span></span> <span data-ttu-id="d6d13-185">Dieser Wert wird dekrementiert, wenn das Abonnement auf dem Server erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-185">This value is decremented when the subscription is created on the server.</span></span>  <br/> |
   
<span data-ttu-id="d6d13-186">Im folgenden Beispiel wird gezeigt, wie die Budgets zwischen einem beliebigen Zielpostfach und dem Dienstkonto verarbeitet werden, dem die [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) -Rolle für die Zielpostfächer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-186">The following example shows how budgets are handled between any target mailbox and the service account that has the [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx) role assigned for the target mailboxes.</span></span> 
  
- <span data-ttu-id="d6d13-187">Dienstkonto1 (SA1) imitiert viele Benutzer (M1, m2, M3 usw.) und erstellt Abonnements für jedes Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6d13-187">ServiceAccount1 (sa1) impersonates many users (m1, m2, m3, and so on) and creates subscriptions for each mailbox.</span></span> <span data-ttu-id="d6d13-188">Beachten Sie Folgendes: Wenn die Abonnements erstellt werden, ist der Abonnementbesitzer SA1, wenn SA1 also eine Verbindung mit den Abonnements öffnet, erzwingt EWS, dass die Abonnements Eigentum von SA1 sind.</span><span class="sxs-lookup"><span data-stu-id="d6d13-188">Note that when the subscriptions are created, the subscription owner is sa1, so when sa1 opens a connection with the subscriptions, EWS enforces that the subscriptions are owned by sa1.</span></span>
    
- <span data-ttu-id="d6d13-189">Sa1 kann die Verbindung wie folgt öffnen:</span><span class="sxs-lookup"><span data-stu-id="d6d13-189">Sa1 can open the connection in the following ways:</span></span>
    
1. <span data-ttu-id="d6d13-190">Ohne Identitätswechsel, sodass die Verbindung mit SA1 aufgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-190">Without impersonation, so the connection is charged against sa1.</span></span>
    
2. <span data-ttu-id="d6d13-191">Durch die Identität eines beliebigen Benutzers, beispielsweise M1, damit die Verbindung mit einer Kopie des m1's-Budgets belastet wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-191">By impersonating any of the users — m1 for example — so that the connection is charged against a copy of m1's budget.</span></span> <span data-ttu-id="d6d13-192">(M1 selbst kann zehn Verbindungen mit Exchange Online öffnen, und alle Dienstkonten, die die Identität M1 annehmen, können zehn Verbindungen mit dem kopierten Budget öffnen.)</span><span class="sxs-lookup"><span data-stu-id="d6d13-192">(M1 itself can open ten connections by using Exchange Online, and all service accounts impersonating m1 can open ten connections by using the copied budget.)</span></span>
    
- <span data-ttu-id="d6d13-193">Wenn der Verbindungsgrenzwert erreicht ist, stehen die folgenden Problemumgehungen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="d6d13-193">If the connection limit is hit, the following workarounds are available:</span></span>
    
  - <span data-ttu-id="d6d13-194">Wenn Option 1 verwendet wird, kann der Administrator mehrere Dienstkonten erstellen, um die Identität weiterer Benutzer zu imitieren.</span><span class="sxs-lookup"><span data-stu-id="d6d13-194">If option 1 is used, the administrator can create multiple service accounts to impersonate additional users.</span></span>
    
  - <span data-ttu-id="d6d13-195">Wenn Option 2 verwendet wird, kann der Code die Identität eines anderen Benutzers annehmen-beispielsweise m2.</span><span class="sxs-lookup"><span data-stu-id="d6d13-195">If option 2 is used, the code can impersonate another user — m2 for example.</span></span>
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a><span data-ttu-id="d6d13-196">Beispiel: beibehalten der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver</span><span class="sxs-lookup"><span data-stu-id="d6d13-196">Example: Maintaining affinity between a group of subscriptions and the Mailbox server</span></span>
<span data-ttu-id="d6d13-197"><a name="bk_ce"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d13-197"><a name="bk_ce"> </a></span></span>

<span data-ttu-id="d6d13-198">Okay, lassen Sie es uns in Aktion sehen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-198">Okay, let's see it in action.</span></span> <span data-ttu-id="d6d13-199">Im folgenden Codebeispiel wird veranschaulicht, wie Sie Benutzer gruppieren und die x-AnchorMailbox-und x-PreferServerAffinity-Header und das x-BackendOverrideCookie-Cookie verwenden, um die Affinität mit dem Postfachserver beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-199">The following code example shows you how to group users and use the X-AnchorMailbox and X-PreferServerAffinity headers and the X-BackendOverrideCookie cookie to maintain affinity with the Mailbox server.</span></span> <span data-ttu-id="d6d13-200">Da die Header und das Cookie im Affinitäts Text von größter Wichtigkeit sind, konzentriert sich dieses Beispiel auf die EWS-XML-Anforderungen und-Antworten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-200">Because the headers and the cookie are of primary importance in the affinity story, this example focuses on the EWS XML requests and responses.</span></span> <span data-ttu-id="d6d13-201">Informationen zum Erstellen des Textkörpers der Abonnementanforderungen und-Antworten mithilfe der verwaltete EWS-API finden Sie unter [Stream notifications about Mailbox Events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about Mailbox Events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="d6d13-201">To use the EWS Managed API to create the body of the subscription requests and responses, see [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="d6d13-202">Dieser Abschnitt enthält zusätzliche Schritte für die Beibehaltung der Affinität und das Hinzufügen der Kopfzeilen zu Ihren Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-202">This section includes additional steps particular to maintaining affinity and adding the headers to your requests.</span></span>
  
<span data-ttu-id="d6d13-203">Dieses Beispiel besteht aus vier Benutzern: Alfred@contoso.com, Alisa@contoso.com, Ronnie@contoso.com und Sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="d6d13-203">This example has four users: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com, and sadie@contoso.com.</span></span> <span data-ttu-id="d6d13-204">In der folgenden Abbildung sind die GroupingInformation-und ExternalEwsUrl- [AutoErmittlungseinstellungen](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) für die Benutzer dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-204">The following figure shows the GroupingInformation and ExternalEwsUrl [Autodiscover settings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) for the users.</span></span> 
  
<span data-ttu-id="d6d13-205">**Abbildung 1. Zum Gruppieren von Postfächern verwendete AutoErmittlungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="d6d13-205">**Figure 1. Autodiscover settings used to group mailboxes**</span></span>

![Tabelle mit den Werten "GroupingInformation" und "ExternalEwsUrl" für jeden Benutzer.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
<span data-ttu-id="d6d13-207">Mithilfe der Einstellungen der Auto Ermittlungs Antworten werden die Postfächer nach dem verketteten Wert der GroupingInformation-und ExternalEwsUrl-Einstellungen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="d6d13-207">Using the settings from the Autodiscover responses, the mailboxes are grouped by the concatenated value of the GroupingInformation and ExternalEwsUrl settings.</span></span> <span data-ttu-id="d6d13-208">In diesem Beispiel haben Alfred und Sadie die gleichen Werte, also sind Sie in einer Gruppe, und Alisa und Ronnie teilen die gleichen Werte, sodass Sie sich in einer anderen Gruppe befinden.</span><span class="sxs-lookup"><span data-stu-id="d6d13-208">In this example, Alfred and Sadie have the same values, so they are in one group, and Alisa and Ronnie share the same values, so they are in another group.</span></span>
  
<span data-ttu-id="d6d13-209">**Abbildung 2. Erstellen von Post Fachgruppen**</span><span class="sxs-lookup"><span data-stu-id="d6d13-209">**Figure 2. Creating mailbox groups**</span></span>

![Tabelle, die zeigt, wie Postfachgruppen mithilfe von AutoErmittlungseinstellungen erstellt werden.](media/Exchange2013_NotificationAffinityGrouping.png)
  
<span data-ttu-id="d6d13-211">Im Rahmen dieses Beispiels konzentrieren wir uns auf Gruppe A. Wir würden die gleichen Schritte für Gruppe B verwenden, verwenden jedoch einen anderen X-AnchorMailbox-Wert für diese Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d6d13-211">For the purpose of this example, we'll focus on Group A. We would use the same steps for group B, but use a different X-AnchorMailbox value for that group.</span></span>
  
<span data-ttu-id="d6d13-212">Erstellen Sie mithilfe von [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)die Abonnementanforderung für das Anker Postfach (Alfred@contoso.com), wobei der x-AnchorMailbox-Header auf die e-Mail-Adresse und den x-PreferServerAffinity-Headerwert true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-212">Using [ApplicationImpersonation](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx), create the subscription request for the anchor mailbox (alfred@contoso.com), with the X-AnchorMailbox header set to the their email address and an X-PreferServerAffinity header value of true.</span></span> <span data-ttu-id="d6d13-213">Durch Festlegen dieser beiden Headerwerte wird der Server ausgelöst, um eine X-BackEndOverrideCookie für die Antwort zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-213">Setting these two header values will trigger the server to create an X-BackEndOverrideCookie for the response.</span></span>
  
<span data-ttu-id="d6d13-214">Wenn Sie die verwaltete EWS-API verwenden, fügen Sie die beiden Kopfzeilen mithilfe der [httpheaders-](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)-[Add](https://msdn.microsoft.com/library/cy7xta5e) -Methode wie dargestellt zu ihrer Abonnementanforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d6d13-214">If you're using the EWS Managed API, use the [HttpHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](https://msdn.microsoft.com/library/cy7xta5e) method to add the two headers to your subscription request, as shown.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

<span data-ttu-id="d6d13-215">Alfreds Abonnement-Anforderung sieht also so aus.</span><span class="sxs-lookup"><span data-stu-id="d6d13-215">So Alfred's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d6d13-216">Die folgende XML-Nachricht ist die Antwort auf die Abonnementanforderung von Alfred und enthält die X-BackEndOverrideCookie.</span><span class="sxs-lookup"><span data-stu-id="d6d13-216">The following XML message is the response to Alfred's subscription request, and it includes the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="d6d13-217">Senden Sie dieses Cookie erneut für alle nachfolgenden Anforderungen für Benutzer in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d6d13-217">Resend this cookie for all subsequent requests for users in this group.</span></span> <span data-ttu-id="d6d13-218">Beachten Sie, dass die Antwort auch zusätzliche Cookies enthält, beispielsweise das von Exchange 2010 verwendete exchangecookie-Cookie.</span><span class="sxs-lookup"><span data-stu-id="d6d13-218">Notice that the response also contains additional cookies, such as the exchangecookie cookie used by Exchange 2010.</span></span> <span data-ttu-id="d6d13-219">Exchange Online, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2013 beginnen, ignorieren Sie exchangecookie, wenn Sie in nachfolgenden Abonnementanforderungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d6d13-219">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013, ignore exchangecookie if it is included in subsequent subscription requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="d6d13-220">Wenn Sie die x-BackEndOverrideCookie von Alfreds Antwort und den x-AnchorMailbox-Header verwenden, wird die Abonnementanforderung für Sadie erstellt, das andere Mitglied der Abonnementanforderung der Gruppe A. Sadie sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="d6d13-220">Using the X-BackEndOverrideCookie from Alfred's response and the X-AnchorMailbox header, the subscription request is created for Sadie, the other member of Group A. Sadie's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com </t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="d6d13-221">Sadies Abonnement Antwort sieht wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="d6d13-221">Sadie's subscription response looks like this.</span></span> <span data-ttu-id="d6d13-222">Beachten Sie, dass die X-BackEndOverrideCookie nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d6d13-222">Note that it does not include the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="d6d13-223">Der Client ist für die Zwischenspeicherung dieses Werts für zukünftige Anforderungen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d6d13-223">The client is responsible for caching that value for future requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="d6d13-224">Mithilfe der [Subscription](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) -Werte aus den Abonnement Antworten wurde eine [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -Vorgangsanforderung für alle Abonnements in der Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-224">Using the [SubscriptionId](https://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values from the subscription responses, a [GetStreamingEvents](https://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) operation request was created for all the subscriptions in the group.</span></span> <span data-ttu-id="d6d13-225">Da in dieser Gruppe weniger als 200 Abonnements vorhanden sind, werden Sie alle in einer einzigen Anforderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="d6d13-225">Because there are less than 200 subscriptions in this group, they are all sent in one request.</span></span> <span data-ttu-id="d6d13-226">Der x-PreferServerAffinity-Header ist auf true festgelegt, und die x-BackEndOverrideCookie ist enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6d13-226">The X-PreferServerAffinity header is set to true and the X-BackEndOverrideCookie is included.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</t:SubscriptionId>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>10</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d6d13-227">Die zurückgegebenen Ereignisse werden dann zur Verarbeitung an einen separaten Thread übergeben.</span><span class="sxs-lookup"><span data-stu-id="d6d13-227">The returned events are then passed to a separate thread for processing.</span></span>
  
## <a name="how-has-affinity-changed"></a><span data-ttu-id="d6d13-228">Wie wurde die Affinität geändert?</span><span class="sxs-lookup"><span data-stu-id="d6d13-228">How has affinity changed?</span></span>
<span data-ttu-id="d6d13-229"><a name="bk_howchanged"> </a></span><span class="sxs-lookup"><span data-stu-id="d6d13-229"><a name="bk_howchanged"> </a></span></span>

<span data-ttu-id="d6d13-230">In Exchange 2010 werden Abonnements auf dem Client Zugriffsserver verwaltet, wie in Abbildung 3 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-230">In Exchange 2010, subscriptions are maintained on the Client Access server, as shown in Figure 3.</span></span> <span data-ttu-id="d6d13-231">In Versionen von Exchange später als Exchange 2010 werden Abonnements auf dem Postfachserver verwaltet, wie in Abbildung 4 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d6d13-231">In versions of Exchange later than Exchange 2010, subscriptions are maintained on the Mailbox server, as shown in Figure 4.</span></span>
  
<span data-ttu-id="d6d13-232">**Abbildung 3. Prozess zum Beibehalten der Affinität in Exchange 2010**</span><span class="sxs-lookup"><span data-stu-id="d6d13-232">**Figure 3. Process for maintaining affinity in Exchange 2010**</span></span>

![Abbildung, die zeigt, wie die Tabelle aktiver Abonnements auf dem Clientzugriffsserver in Exchange 2010 verwaltet wird.](media/Exchange2013_NoficationAffinity2010.png)
  
<span data-ttu-id="d6d13-234">**Abbildung 4. Prozess zum Beibehalten der Affinität in Exchange Online und Exchange 2013**</span><span class="sxs-lookup"><span data-stu-id="d6d13-234">**Figure 4. Process for maintaining affinity in Exchange Online and Exchange 2013**</span></span>

![Abbildung, die zeigt, wie der Lastenausgleich und Clientzugriffsserver Anforderungen an den Postfachserver leiten, der die Tabelle aktiver Abonnements in Exchange Server und Exchange Online verwaltet.](media/Exchange2013_NoficationAffinity2013.png)
  
<span data-ttu-id="d6d13-236">In Exchange 2010 kennt der Client nur die Adresse des Lastenausgleichsmoduls, und die vom Server zurückgegebene exchangecookie stellt sicher, dass die Anforderung an den richtigen Clientzugriffsserver weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="d6d13-236">In Exchange 2010, the client only knows the address of the load balancer, and the exchangecookie that is returned by the server ensures that the request is routed to the right Client Access server.</span></span> <span data-ttu-id="d6d13-237">In höheren Versionen müssen das Lastenausgleichsmodul und die Client Zugriffs-Serverrollen beide Anforderungen jedoch entsprechend weiterleiten, bevor Sie zum Postfachserver gelangen.</span><span class="sxs-lookup"><span data-stu-id="d6d13-237">However, in later versions, the load balancer and the Client Access server roles both have to route the requests appropriately before they get to the Mailbox server.</span></span> <span data-ttu-id="d6d13-238">Dafür sind zusätzliche Informationen erforderlich, weshalb die neuen Header und Cookies eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="d6d13-238">To do that, additional information is required, which is why the new headers and cookie were introduced.</span></span> <span data-ttu-id="d6d13-239">In den Artikeln [Benachrichtigungsabonnements, Post Fach Ereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) wird erklärt, wie Abonnements in Exchange 2013 verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="d6d13-239">The article [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explains how subscriptions are maintained in Exchange 2013.</span></span> 
  
<span data-ttu-id="d6d13-240">Möglicherweise wird feststellen, dass die exchangecookie, die von Exchange 2010 verwendet werden, noch von höheren Versionen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d6d13-240">You might notice that the exchangecookie that Exchange 2010 uses is still returned by later versions.</span></span> <span data-ttu-id="d6d13-241">Es schadet nicht, dieses Cookie in Anforderungen einzubinden, aber spätere Versionen von Exchange ignorieren es.</span><span class="sxs-lookup"><span data-stu-id="d6d13-241">There's no harm in including this cookie in requests, but later versions of Exchange ignore it.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6d13-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6d13-242">See also</span></span>

- [<span data-ttu-id="d6d13-243">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-243">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="d6d13-244">Streambenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-244">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="d6d13-245">Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-245">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="d6d13-246">Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-246">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
- [<span data-ttu-id="d6d13-247">Änderungen beim Verwalten der Affinität für EWS-Abonnements...</span><span class="sxs-lookup"><span data-stu-id="d6d13-247">Changes in Managing Affinity for EWS Subscriptions…</span></span>](https://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [<span data-ttu-id="d6d13-248">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6d13-248">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

