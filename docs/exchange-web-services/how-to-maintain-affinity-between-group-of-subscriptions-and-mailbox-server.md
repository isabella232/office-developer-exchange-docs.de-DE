---
title: Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Lernen Sie die Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver verwalten.
ms.openlocfilehash: 7cfbfb5cc19e092c37e3d48a7fcc4f27023516e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756914"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a><span data-ttu-id="fd3d3-103">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-103">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>

<span data-ttu-id="fd3d3-104">Lernen Sie die Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver verwalten.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-104">Find out about maintaining the affinity between a group of subscriptions and the Mailbox server.</span></span>
  
<span data-ttu-id="fd3d3-105">Affinität ist die Zuordnung einer Sequenz von Anforderung und Antwort-Nachrichten mit einem bestimmten Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-105">Affinity is the association of a sequence of request and response messages with a particular Mailbox server.</span></span> <span data-ttu-id="fd3d3-106">Die meisten Funktionen in Exchange wird vom Server Affinität behandelt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-106">For most functionality in Exchange, affinity is handled by the server.</span></span> <span data-ttu-id="fd3d3-107">Benachrichtigungen, sind jedoch eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-107">Notifications, however, are an exception.</span></span> <span data-ttu-id="fd3d3-108">Der Client ist verantwortlich für die Verwaltung von der Affinität für Benachrichtigungsabonnements mit dem Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-108">The client is responsible for maintaining the affinity with the Mailbox server for notification subscriptions.</span></span> <span data-ttu-id="fd3d3-109">Diese Affinität ermöglicht das System zum Lastenausgleich und Clientzugriffs-Servern zwischen dem Client und dem Server Route Benachrichtigung Abonnements und verwandte Anforderungen an den Postfachserver, der das Abonnement verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-109">This affinity enables the load balancer and Client Access servers between the client and the server to route notification subscriptions and related requests to the Mailbox server that maintains the subscription.</span></span> <span data-ttu-id="fd3d3-110">Ohne Affinität kann die Anforderung an einem anderen Postfachserver geleitet erhalten möchten, die nicht der Client-Abonnements, die was dazu einen [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Fehler zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-110">Without affinity, the request might get routed to a different Mailbox server that does not include the client's subscriptions, which can cause an [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) error to be returned.</span></span> 
  
## <a name="how-is-affinity-maintained"></a><span data-ttu-id="fd3d3-111">Wie wird die Affinität verwaltet?</span><span class="sxs-lookup"><span data-stu-id="fd3d3-111">How is affinity maintained?</span></span>
<span data-ttu-id="fd3d3-112"><a name="bk_howmaintained"> </a></span><span class="sxs-lookup"><span data-stu-id="fd3d3-112"></span></span>

<span data-ttu-id="fd3d3-113">Affinität in Exchange ist Cookie-basierte.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-113">Affinity in Exchange is cookie based.</span></span> <span data-ttu-id="fd3d3-114">Der Client löst die Erstellung des Cookies durch das Einbeziehen von bestimmter Kopfzeilen in der Anforderung Abonnement, und klicken Sie dann die Abonnement-Antwort enthält das Cookie.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-114">The client triggers the creation of the cookie by including specific headers in the subscription request, and then the subscription response contains the cookie.</span></span> <span data-ttu-id="fd3d3-115">Der Client sendet anschließend das Cookie in nachfolgenden Anforderungen, um sicherzustellen, dass die Anforderung an den richtigen Postfachserver geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-115">The client then sends that cookie in subsequent requests to ensure that the request is routed to the right Mailbox server.</span></span>
  
<span data-ttu-id="fd3d3-116">Genauer gesagt ist Affinität in Exchange durch Folgendes behandelt:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-116">More specifically, affinity in Exchange is handled by the following:</span></span> 
  
- <span data-ttu-id="fd3d3-117">X-AnchorMailbox – Ein HTTP-Header, die in der anfänglichen Abonnement Anforderung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-117">X-AnchorMailbox — An HTTP header that is included in the initial subscription request.</span></span> <span data-ttu-id="fd3d3-118">Das erste Postfach in einer Gruppe von Postfächern, die mit dem gleichen Postfachserver Affinität freigeben identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-118">It identifies the first mailbox in a group of mailboxes that share affinity with the same Mailbox server.</span></span>
    
- <span data-ttu-id="fd3d3-119">X-PreferServerAffinity – Ein HTTP-Header, die in der anfänglichen Abonnement-Anforderung mit dem X-AnchorMailbox-Header enthalten ist, und festgelegt ist auf "true", um anzugeben, dass der Client anfordert, dass mit dem Postfachserver Affinität verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-119">X-PreferServerAffinity — An HTTP header that is included in the initial subscription request with the X-AnchorMailbox header and is set to true to indicate that the client is requesting that affinity be maintained with the Mailbox server.</span></span>
    
- <span data-ttu-id="fd3d3-120">X-BackEndOverrideCookie – Ein Cookie, das in der anfänglichen Abonnement Antwort enthalten ist, und enthält eine Cookie, die das System zum Lastenausgleich und Clientzugriffsserver verwenden, um nachfolgende Anforderungen an den gleichen Postfachserver weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-120">X-BackEndOverrideCookie — A cookie that is included in the initial subscription response and contains a cookie that the load balancer and Client Access server use to route subsequent requests to the same Mailbox server.</span></span>
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a><span data-ttu-id="fd3d3-121">Wie behalten ich Affinität mithilfe des EWS Managed API oder EWS?</span><span class="sxs-lookup"><span data-stu-id="fd3d3-121">How do I maintain affinity by using the EWS Managed API or EWS?</span></span>
<span data-ttu-id="fd3d3-122"><a name="bk_howdoimaintain"> </a></span><span class="sxs-lookup"><span data-stu-id="fd3d3-122"></span></span>

<span data-ttu-id="fd3d3-123">Sie können die gleichen Schritte zum Aufrechterhalten der Affinität für mehrere Postfach-Abonnements und ihren Postfachservern, unabhängig davon, ob Sie streaming, Pull oder Push-Benachrichtigungen, verwenden und unabhängig davon, ob Sie vorgesehenen eine lokale Exchange-Server oder Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-123">You can use the same steps to maintain affinity for multiple mailbox subscriptions and their Mailbox servers, regardless of whether you are using streaming, pull, or push notifications, and regardless of whether you're targeting an Exchange on-premises server or Exchange Online.</span></span>
  
1. <span data-ttu-id="fd3d3-124">Für jedes Postfach, [für die AutoErmittlung aufrufen](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) und die Werten "groupinginformation" und "externalewsurl" benutzereinstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-124">For each mailbox, [call Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and get the GroupingInformation and ExternalEwsUrl user settings.</span></span> <span data-ttu-id="fd3d3-125">Für die SOAP-AutoErmittlung Sie verwenden im [Setting](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) -Element, und für die AutoErmittlung POX, verwenden Sie das [Werten "groupinginformation"](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) -Element.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-125">For SOAP Autodiscover, you use the [Setting](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element, and for POX Autodiscover, you use the [GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) element.</span></span> 
    
2. <span data-ttu-id="fd3d3-126">Mit den Werten "groupinginformation" und "externalewsurl" Einstellungen der AutoErmittlung-Antworten Place Postfächer mit der gleichen Werten "groupinginformation" und "externalewsurl" verkettet Wert in der gleichen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-126">Using the GroupingInformation and ExternalEwsUrl settings from the Autodiscover responses, place mailboxes with the same ExternalEwsUrl and GroupingInformation concatenated value in the same group.</span></span> <span data-ttu-id="fd3d3-127">Wenn alle Gruppen mehr als 200 Postfächer verfügen, zerlegen Sie die Gruppen weitere, sodass jede Gruppe nicht mehr als 200 Postfächer verfügt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-127">If any groups have more than 200 mailboxes, break the groups down further so that each group has no more than 200 mailboxes.</span></span>
    
3. <span data-ttu-id="fd3d3-128">Erstellen und Verwenden von einem [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) -Objekt für den Rest der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-128">Create and use one [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) object for the rest of the procedure.</span></span> <span data-ttu-id="fd3d3-129">Sie verwenden, werden automatisch die gleichen **ExchangeService** -Objekt, Cookies und Header (klicken Sie nach festlegen) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-129">When you use the same **ExchangeService** object, cookies and headers (when they are set) are automatically maintained.</span></span> <span data-ttu-id="fd3d3-130">Beachten Sie, dass wenn Sie die Gruppe streaming-Abonnements in eine einzelne Verbindung nicht möchten, erstellen Sie ein anderes **ExchangeService** -Objekt für jeden angenommener Benutzer frei.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-130">Note that if you do not intend to group streaming subscriptions into a single connection, you are free to create a different **ExchangeService** object for each impersonated user.</span></span> 
    
4. <span data-ttu-id="fd3d3-131">[Senden Sie ein Abonnement](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) -Anforderung für den Benutzer, dessen Benutzername wird zuerst angezeigt, wenn alle Benutzer in der Gruppe alphabetisch sortiert sind (werden zusammenfassend an diesen Benutzer als den Anker Postfachbenutzer).</span><span class="sxs-lookup"><span data-stu-id="fd3d3-131">[Send a subscription](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) request for the user whose user name appears first when all users in the group are sorted alphabetically (we'll refer to this user as the anchor mailbox user).</span></span> <span data-ttu-id="fd3d3-132">Die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-132">Do the following:</span></span> 
    
  - <span data-ttu-id="fd3d3-133">Fügen Sie den X-AnchorMailbox-Header mit einem Wert, der an die SMTP-Adresse des Postfachbenutzers Anker festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-133">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user.</span></span>
    
  - <span data-ttu-id="fd3d3-134">Fügen Sie den X-PreferServerAffinity-Header mit einem Wert auf True festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-134">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="fd3d3-135">Verwenden Sie die Rolle ["ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) " (der Typ ["ExchangeImpersonation"](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="fd3d3-135">Use the [ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
5. <span data-ttu-id="fd3d3-136">Rufen Sie in der Antwort Abonnement des X-BackEndOverrideCookie-Werts.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-136">In the subscription response, get the X-BackEndOverrideCookie value.</span></span> <span data-ttu-id="fd3d3-137">Dieser Wert wird in jede nachfolgende Abonnement Anforderung für Benutzer in dieser Gruppe einschließen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-137">Include this value in each of the subsequent subscription requests for users in this group.</span></span>
    
6. <span data-ttu-id="fd3d3-138">Senden Sie für jeden zusätzlichen Benutzer in der Gruppe eine Anforderung Abonnement und die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-138">For each additional user in the group, send a subscription request and do the following:</span></span>
    
  - <span data-ttu-id="fd3d3-139">Fügen Sie den X-AnchorMailbox-Header mit einem Wert, der an die SMTP-Adresse des Postfachbenutzers Anker für die Gruppe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-139">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user for the group.</span></span>
    
  - <span data-ttu-id="fd3d3-140">Fügen Sie den X-PreferServerAffinity-Header mit einem Wert auf True festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-140">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="fd3d3-141">Enthalten Sie die X-BackEndOverrideCookie, die in den Anker Postfachbenutzer Abonnement Antwort zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-141">Include the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response.</span></span>
    
  - <span data-ttu-id="fd3d3-142">Verwenden Sie die Rolle ["ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) " (der Typ ["ExchangeImpersonation"](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="fd3d3-142">Use the [ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
    <span data-ttu-id="fd3d3-143">Beachten Sie, dass der Server die Werte X PreferServerAffinity und X BackendOverrideCookie zusammen verwendet, um das routing an den Postfachserver ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-143">Note that the server uses the X-PreferServerAffinity and X-BackendOverrideCookie values together to perform the routing to the mailbox server.</span></span> <span data-ttu-id="fd3d3-144">Die X-AnchorMailbox Kopfzeile ist auch erforderlich, aber wird vom Server ignoriert, wenn die anderen beiden Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-144">The X-AnchorMailbox header is also required, but is ignored by the server if the other two values are valid.</span></span> <span data-ttu-id="fd3d3-145">Wenn X AnchorMailbox und X-PreferServerAffinity befinden sich in einer Anforderung und X BackendOverrideCookie ist nicht mit inbegriffen, wird der Wert X AnchorMailbox verwendet, um die Anforderungen weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-145">If X-AnchorMailbox and X-PreferServerAffinity are in a request and X-BackendOverrideCookie is not included, the X-AnchorMailbox value is used to route the requests.</span></span>
    
    <span data-ttu-id="fd3d3-146">Da die X-PreferServerAffinity und X BackendOverrideCookie Werte führen Sie das routing, wenn das Postfach Anker jemals zu einer anderen Gruppe oder Server verschoben wird, ändert die Logik nicht, da die X-BackendOverrideCookie die Anforderung an den richtigen Server weitergeleitet wird für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-146">Because the X-PreferServerAffinity and X-BackendOverrideCookie values perform the routing, if the anchor mailbox ever moves to another group or server, the logic does not change because the X-BackendOverrideCookie will route the request to the correct server for the group.</span></span>
    
7. <span data-ttu-id="fd3d3-147">Senden Sie eine einzelne [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) oder [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) Anforderungen für die Gruppe, und gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-147">Send a single [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) requests for the group, and do the following:</span></span> 
    
  - <span data-ttu-id="fd3d3-148">Enthalten Sie in jeder der einzelnen Abonnement Antworten für Postfächer in der Gruppe zurückgegebenen Werte sind [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fd3d3-148">Include the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values returned in each of the individual subscription responses for mailboxes in the group.</span></span> 
    
  - <span data-ttu-id="fd3d3-149">Wenn mehr als 200 Abonnements für die Gruppe vorhanden ist, erstellen Sie mehrere Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-149">If more than 200 subscriptions exist for the group, create multiple requests.</span></span> <span data-ttu-id="fd3d3-150">Die maximale Anzahl von [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) Werte, die in einer Anforderung ist 200.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-150">The maximum number of [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values to include in a request is 200.</span></span> 
    
  - <span data-ttu-id="fd3d3-151">Wenn Sie weitere Verbindungen als der Zielpostfach verfügbar sind, verwenden Sie das Dienstkonto zum Identitätswechsel für das Anker-Postfach für die Gruppe; andernfalls Identitätswechsel nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-151">If you need more connections than are available to the target mailbox, use the service account to impersonate the anchor mailbox for the group; otherwise, do not use impersonation.</span></span> <span data-ttu-id="fd3d3-152">Idealerweise sollten Sie ein eindeutiges Postfach pro Anforderung [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) oder [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) anzunehmen, so dass nie Drosselung Grenzwerte auftreten.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-152">Ideally, you want to impersonate a unique mailbox per [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) request so that you never encounter throttling limits.</span></span> 
    
  - <span data-ttu-id="fd3d3-153">Verwenden Sie ApplicationImpersonation, wenn Sie [Weitere Verbindungen als der Zielpostfach verfügbar sind benötigen](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling). andernfalls ApplicationImpersonation nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-153">Use ApplicationImpersonation if you need [more connections than are available to the target mailbox](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); otherwise, do not use ApplicationImpersonation.</span></span>
    
  - <span data-ttu-id="fd3d3-154">Fügen Sie den X-PreferServerAffinity-Header, und legen Sie es auf "true".</span><span class="sxs-lookup"><span data-stu-id="fd3d3-154">Include the X-PreferServerAffinity header and set it to true.</span></span> <span data-ttu-id="fd3d3-155">Dieser Wert wird automatisch enthalten, wenn Sie das **ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-155">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
  - <span data-ttu-id="fd3d3-156">Enthalten Sie die X-BackEndOverrideCookie für die Gruppe (die X-BackEndOverrideCookie, die in den Anker Postfachbenutzer Abonnement Antwort zurückgegeben wurden).</span><span class="sxs-lookup"><span data-stu-id="fd3d3-156">Include the X-BackEndOverrideCookie for the group (the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response).</span></span> <span data-ttu-id="fd3d3-157">Dieser Wert wird automatisch enthalten, wenn Sie das **ExchangeService** -Objekt verwenden, das Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-157">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
8. <span data-ttu-id="fd3d3-158">Übergeben Sie die zurückgegebenen Ereignisse auf einem getrennten Thread für die Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-158">Pass the returned events to a separate thread for processing.</span></span>
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a><span data-ttu-id="fd3d3-159">Welche Drosselung Werte muss ich berücksichtigen?</span><span class="sxs-lookup"><span data-stu-id="fd3d3-159">What throttling values do I need to take into consideration?</span></span>
<span data-ttu-id="fd3d3-160"><a name="bk_throttling"> </a></span><span class="sxs-lookup"><span data-stu-id="fd3d3-160"></span></span>

<span data-ttu-id="fd3d3-161">Wenn Sie Ihre Benachrichtigung Implementierung planen, möchten Sie zwei Werte berücksichtigt werden: die Anzahl der Verbindungen und die Anzahl der Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-161">As you plan your notification implementation, you'll want to take two values into consideration: the number of connections, and the number of subscriptions.</span></span> <span data-ttu-id="fd3d3-162">Die folgende Tabelle enthält die Standardwerte für jede Einstellung [Drosselung](ews-throttling-in-exchange.md) und wie die Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-162">The following table lists the default values for each [throttling](ews-throttling-in-exchange.md) setting and how the settings are used.</span></span> <span data-ttu-id="fd3d3-163">Das Budget ist für jeden Wert der Zielpostfach zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-163">For each value, the budget is allocated to the target mailbox.</span></span> <span data-ttu-id="fd3d3-164">Aus diesem Grund ist Verwenden des Identitätswechsels, um zusätzliche Verbindungen zu erhalten ein erforderlicher Schritt in vielen Szenarien aus.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-164">For this reason, using impersonation to gain additional connections is a required step in many scenarios.</span></span> 
  
<span data-ttu-id="fd3d3-165">**In Tabelle 1. Drosselung Standardwerte**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-165">**Table 1. Default throttling values**</span></span>

|<span data-ttu-id="fd3d3-166">**Bereich von Belang**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-166">**Area of consideration**</span></span>|<span data-ttu-id="fd3d3-167">**Drosselung Einstellung**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-167">**Throttling setting**</span></span>|<span data-ttu-id="fd3d3-168">**Standardwert**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-168">**Default value**</span></span>|<span data-ttu-id="fd3d3-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-169">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd3d3-170">Streaming Verbindungen</span><span class="sxs-lookup"><span data-stu-id="fd3d3-170">Streaming connections</span></span>  <br/> |<span data-ttu-id="fd3d3-171">Hängenden Verbindungslimit Standard</span><span class="sxs-lookup"><span data-stu-id="fd3d3-171">Default hanging connection limit</span></span>  <br/> |<span data-ttu-id="fd3d3-172">10 für Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fd3d3-172">10 for Exchange Online</span></span>  <br/> <span data-ttu-id="fd3d3-173">3 für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="fd3d3-173">3 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="fd3d3-174">Die maximale Anzahl von gleichzeitigen streaming Verbindungen, die über ein Konto verfügen, kann gleichzeitig auf dem Server geöffnet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-174">The maximum number of concurrent streaming connections that an account can have open on the server at one time.</span></span> <span data-ttu-id="fd3d3-175">Arbeiten innerhalb dieser Grenzwert, verwenden Sie ein Dienstkonto mit der Rolle "ApplicationImpersonation" für die Ziel-Postfächer zugewiesen und Identitätswechsel für den ersten Benutzer in den einzelnen Gruppen der Abonnement-ID, wenn Ereignisse gestreamt abrufen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-175">To work within this limit, use a service account with the ApplicationImpersonation role assigned for the target mailboxes, and impersonate the first user in each subscription ID group when getting streamed events.</span></span>  <br/> |
|<span data-ttu-id="fd3d3-176">Pull oder Push-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="fd3d3-176">Pull or push connections</span></span>  <br/> |<span data-ttu-id="fd3d3-177">EWSMaxConcurrency</span><span class="sxs-lookup"><span data-stu-id="fd3d3-177">EWSMaxConcurrency</span></span>  <br/> |<span data-ttu-id="fd3d3-178">27</span><span class="sxs-lookup"><span data-stu-id="fd3d3-178">27</span></span>  <br/> |<span data-ttu-id="fd3d3-179">Die maximale Anzahl von gleichzeitigen Pull oder Push-Verbindungen (Anforderungen, die geliefert, aber noch nicht beantwortet wurden), dass ein Konto öffnen auf dem Server gleichzeitig durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-179">The maximum number of concurrent pull or push connections (requests that have been received but not yet responded to) that an account can have open on the server at one time.</span></span>  <br/> |
|<span data-ttu-id="fd3d3-180">Abonnements</span><span class="sxs-lookup"><span data-stu-id="fd3d3-180">Subscriptions</span></span>  <br/> |<span data-ttu-id="fd3d3-181">EWSMaxSubscriptions</span><span class="sxs-lookup"><span data-stu-id="fd3d3-181">EWSMaxSubscriptions</span></span>  <br/> |<span data-ttu-id="fd3d3-182">20 für Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fd3d3-182">20 for Exchange Online</span></span>  <br/> <span data-ttu-id="fd3d3-183">5000 für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="fd3d3-183">5000 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="fd3d3-184">Die maximale Anzahl von nonexpired Abonnements, die ein Konto gleichzeitig durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-184">The maximum number of nonexpired subscriptions that an account can have at one time.</span></span> <span data-ttu-id="fd3d3-185">Dieser Wert wird verringert, wenn das Abonnement auf dem Server erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-185">This value is decremented when the subscription is created on the server.</span></span>  <br/> |
   
<span data-ttu-id="fd3d3-186">Das folgende Beispiel zeigt, wie Budgets behandelt werden zwischen alle Zielpostfach und das Dienstkonto, das der Rolle ["ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) " für die Ziel-Postfächer zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-186">The following example shows how budgets are handled between any target mailbox and the service account that has the [ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx) role assigned for the target mailboxes.</span></span> 
  
- <span data-ttu-id="fd3d3-187">ServiceAccount1 (sa1) Identität viele Benutzer (m1, m2, m3 usw.) und Abonnements für jedes Postfach erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-187">ServiceAccount1 (sa1) impersonates many users (m1, m2, m3, and so on) and creates subscriptions for each mailbox.</span></span> <span data-ttu-id="fd3d3-188">Beachten Sie, dass bei der Erstellung von Abonnements von Ihrem Besitzer sa1, damit beim Öffnen sa1 einer Verbindungs mit der Abonnements, EWS erzwingt, dass die Abonnements sa1 gehören.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-188">Note that when the subscriptions are created, the subscription owner is sa1, so when sa1 opens a connection with the subscriptions, EWS enforces that the subscriptions are owned by sa1.</span></span>
    
- <span data-ttu-id="fd3d3-189">Sa1 können die Verbindung wie folgt öffnen:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-189">Sa1 can open the connection in the following ways:</span></span>
    
1. <span data-ttu-id="fd3d3-190">Ohne Identitätswechsel sodass die Verbindung gegen sa1 aufgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-190">Without impersonation, so the connection is charged against sa1.</span></span>
    
2. <span data-ttu-id="fd3d3-191">Durch Benutzer annehmen der Identität – beispielsweise m1 –, damit die Verbindung mit einer Kopie der m1 Budget berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-191">By impersonating any of the users — m1 for example — so that the connection is charged against a copy of m1's budget.</span></span> <span data-ttu-id="fd3d3-192">(M1 selbst kann öffnen zehn Verbindungen mit Exchange Online und alle Dienstkonten Identitätswechsel bei m1 können zehn Verbindungen mithilfe des kopierten Budgets.)</span><span class="sxs-lookup"><span data-stu-id="fd3d3-192">(M1 itself can open ten connections by using Exchange Online, and all service accounts impersonating m1 can open ten connections by using the copied budget.)</span></span>
    
- <span data-ttu-id="fd3d3-193">Wenn das Verbindungslimit erreicht ist, stehen die folgenden problemumgehungen:</span><span class="sxs-lookup"><span data-stu-id="fd3d3-193">If the connection limit is hit, the following workarounds are available:</span></span>
    
  - <span data-ttu-id="fd3d3-194">Wenn die Option 1 verwendet wird, kann der Administrator mehrere Dienstkonten zum Identitätswechsel für weitere Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-194">If option 1 is used, the administrator can create multiple service accounts to impersonate additional users.</span></span>
    
  - <span data-ttu-id="fd3d3-195">Wenn die Option 2 verwendet wird, kann der Code eines anderen Benutzers imitieren – beispielsweise m2.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-195">If option 2 is used, the code can impersonate another user — m2 for example.</span></span>
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a><span data-ttu-id="fd3d3-196">Beispiel: Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver</span><span class="sxs-lookup"><span data-stu-id="fd3d3-196">Example: Maintaining affinity between a group of subscriptions and the Mailbox server</span></span>
<span data-ttu-id="fd3d3-197"><a name="bk_ce"> </a></span><span class="sxs-lookup"><span data-stu-id="fd3d3-197"></span></span>

<span data-ttu-id="fd3d3-198">Okay, in der Praxis sehen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-198">Okay, let's see it in action.</span></span> <span data-ttu-id="fd3d3-199">Das folgende Codebeispiel zeigt, wie Benutzer gruppieren und verwenden Sie die X-AnchorMailbox und X PreferServerAffinity Header und das Cookie X BackendOverrideCookie zum Aufrechterhalten der Affinität mit dem Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-199">The following code example shows you how to group users and use the X-AnchorMailbox and X-PreferServerAffinity headers and the X-BackendOverrideCookie cookie to maintain affinity with the Mailbox server.</span></span> <span data-ttu-id="fd3d3-200">Da die Kopf- und das Cookie von großer Wichtigkeit im Textabschnitt Affinität sind, konzentriert sich auf die EWS XML-Anforderungen und Antworten in diesem Beispiel wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-200">Because the headers and the cookie are of primary importance in the affinity story, this example focuses on the EWS XML requests and responses.</span></span> <span data-ttu-id="fd3d3-201">Um die EWS Managed API verwenden, um den Hauptteil der Abonnement-Anforderungen und-Antworten erstellen, finden Sie unter [Stream-Benachrichtigungen bezüglich Postfach Ereignisse im Exchange mithilfe der Exchange-Webdienste](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) , und [ziehen Sie Benachrichtigungen über Postfach Ereignisse mithilfe von EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="fd3d3-201">To use the EWS Managed API to create the body of the subscription requests and responses, see [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="fd3d3-202">Dieser Abschnitt enthält zusätzliche Schritte spezielle zur Wartung Affinität und die Kopfzeilen auf Ihre Anfragen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-202">This section includes additional steps particular to maintaining affinity and adding the headers to your requests.</span></span>
  
<span data-ttu-id="fd3d3-203">Dieses Beispiel besteht aus vier Benutzer: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com und sadie@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-203">This example has four users: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com, and sadie@contoso.com.</span></span> <span data-ttu-id="fd3d3-204">Die folgende Abbildung zeigt den Werten "groupinginformation" und "externalewsurl" [für die AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) für die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-204">The following figure shows the GroupingInformation and ExternalEwsUrl [Autodiscover settings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) for the users.</span></span> 
  
<span data-ttu-id="fd3d3-205">**Abbildung 1. Für die AutoErmittlung verwendet, um die Gruppenpostfächer**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-205">**Figure 1. Autodiscover settings used to group mailboxes**</span></span>

![Tabelle mit den Werten "GroupingInformation" und "ExternalEwsUrl" für jeden Benutzer.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
<span data-ttu-id="fd3d3-207">Verwenden die Einstellungen der AutoErmittlung-Antworten, werden die Postfächer nach den verketteten Wert von den Werten "groupinginformation" und "externalewsurl" Einstellungen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-207">Using the settings from the Autodiscover responses, the mailboxes are grouped by the concatenated value of the GroupingInformation and ExternalEwsUrl settings.</span></span> <span data-ttu-id="fd3d3-208">In diesem Beispiel Alfred und Sadie die gleichen Werte aufweisen, damit sie in einer Gruppe sind, und Alisa und Ronnie dieselben Werte wie, freigeben, damit sie in einer anderen Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-208">In this example, Alfred and Sadie have the same values, so they are in one group, and Alisa and Ronnie share the same values, so they are in another group.</span></span>
  
<span data-ttu-id="fd3d3-209">**Abbildung 2. Erstellen von postfachgruppen**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-209">**Figure 2. Creating mailbox groups**</span></span>

![Tabelle, die zeigt, wie Postfachgruppen mithilfe von AutoErmittlungseinstellungen erstellt werden.](media/Exchange2013_NotificationAffinityGrouping.png)
  
<span data-ttu-id="fd3d3-211">In diesem Beispiel wird konzentrieren wir uns auf Gruppe a Wir würden verwenden Sie dieselben Schritte für die Gruppe B, aber Sie können einen anderen Wert für die X-AnchorMailbox für diese Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-211">For the purpose of this example, we'll focus on Group A. We would use the same steps for group B, but use a different X-AnchorMailbox value for that group.</span></span>
  
<span data-ttu-id="fd3d3-212">[ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx), erstellen Sie die Abonnement-Anforderung für das Postfach Anker (alfred@contoso.com), mit dem X-AnchorMailbox-Header zu der die e-Mail-Adresse und eine X-PreferServerAffinity-Header-Wert "true".</span><span class="sxs-lookup"><span data-stu-id="fd3d3-212">Using [ApplicationImpersonation](http://technet.microsoft.com/de-de/library/dd776119%28v=exchg.150%29.aspx), create the subscription request for the anchor mailbox (alfred@contoso.com), with the X-AnchorMailbox header set to the their email address and an X-PreferServerAffinity header value of true.</span></span> <span data-ttu-id="fd3d3-213">Den Server zum Erstellen einer X-BackEndOverrideCookie für die Antwort wird ausgelöst, wenn diese Headerwerte zwei wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-213">Setting these two header values will trigger the server to create an X-BackEndOverrideCookie for the response.</span></span>
  
<span data-ttu-id="fd3d3-214">Wenn Sie die EWS Managed API verwenden, verwenden Sie die [Wertpaare](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)-[Add](http://msdn.microsoft.com/de-de/library/cy7xta5e) -Methode zwei Header auf Ihre Anforderung Abonnement hinzufügen, wie dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-214">If you're using the EWS Managed API, use the [HttpHeaders](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](http://msdn.microsoft.com/de-de/library/cy7xta5e) method to add the two headers to your subscription request, as shown.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

<span data-ttu-id="fd3d3-215">So sieht Alfreds Abonnement Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-215">So Alfred's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="fd3d3-216">Die folgende XML-Meldung wird die Antwort auf Alfreds Abonnements an, und die X-BackEndOverrideCookie enthält.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-216">The following XML message is the response to Alfred's subscription request, and it includes the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="fd3d3-217">Senden Sie dieses Cookie für alle nachfolgenden Anforderungen für Benutzer in dieser Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-217">Resend this cookie for all subsequent requests for users in this group.</span></span> <span data-ttu-id="fd3d3-218">Beachten Sie, dass die Antwort auch zusätzliche Cookies, wie das Exchangecookie Cookie von Exchange 2010 verwendet enthält.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-218">Notice that the response also contains additional cookies, such as the exchangecookie cookie used by Exchange 2010.</span></span> <span data-ttu-id="fd3d3-219">Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2013-Versionen ignorieren Exchangecookie, wenn es in den nachfolgenden Abonnement Anfragen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-219">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013, ignore exchangecookie if it is included in subsequent subscription requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="fd3d3-220">Verwenden die X-BackEndOverrideCookie aus Alfreds Antwort und der X-AnchorMailbox-Header wird die Abonnement-Anforderung für Sadie erstellt, das Mitglied Gruppe A. Sadie Abonnement Anforderung sieht folgendermaßen aus.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-220">Using the X-BackEndOverrideCookie from Alfred's response and the X-AnchorMailbox header, the subscription request is created for Sadie, the other member of Group A. Sadie's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@consoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@consoso.com </t:SmtpAddress>
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

<span data-ttu-id="fd3d3-221">Sadies Abonnements Antwort sieht folgendermaßen aus.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-221">Sadie's subscription response looks like this.</span></span> <span data-ttu-id="fd3d3-222">Beachten Sie, dass es nicht in der X-BackEndOverrideCookie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-222">Note that it does not include the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="fd3d3-223">Der Client ist verantwortlich für das Zwischenspeichern dieses Werts für zukünftige Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-223">The client is responsible for caching that value for future requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="fd3d3-224">Verwenden die [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) Werte aus den Abonnement Antworten, wurde die Anforderung einer [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) -Operation für alle Abonnements in der Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-224">Using the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values from the subscription responses, a [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) operation request was created for all the subscriptions in the group.</span></span> <span data-ttu-id="fd3d3-225">Da weniger als 200 Abonnements in dieser Gruppe vorhanden sind, werden alle in einer Anforderung gesendet.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-225">Because there are less than 200 subscriptions in this group, they are all sent in one request.</span></span> <span data-ttu-id="fd3d3-226">Die X-PreferServerAffinity Kopfzeile festgelegt ist auf "true" und die X-BackEndOverrideCookie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-226">The X-PreferServerAffinity header is set to true and the X-BackEndOverrideCookie is included.</span></span> 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="fd3d3-227">Die zurückgegebene Ereignisse werden auf einem getrennten Thread zur Verarbeitung übergeben.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-227">The returned events are then passed to a separate thread for processing.</span></span>
  
## <a name="how-has-affinity-changed"></a><span data-ttu-id="fd3d3-228">Wie hat sich Affinität geändert?</span><span class="sxs-lookup"><span data-stu-id="fd3d3-228">How has affinity changed?</span></span>
<span data-ttu-id="fd3d3-229"><a name="bk_howchanged"> </a></span><span class="sxs-lookup"><span data-stu-id="fd3d3-229"></span></span>

<span data-ttu-id="fd3d3-230">In Exchange 2010-Abonnements auf dem Clientzugriffsserver bleiben wie in Abbildung 3 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-230">In Exchange 2010, subscriptions are maintained on the Client Access server, as shown in Figure 3.</span></span> <span data-ttu-id="fd3d3-231">In Versionen von Exchange spätestens Exchange 2010 werden Abonnements auf dem Postfachserver verwaltet, wie in Abbildung 4 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-231">In versions of Exchange later than Exchange 2010, subscriptions are maintained on the Mailbox server, as shown in Figure 4.</span></span>
  
<span data-ttu-id="fd3d3-232">**Abbildung 3. Prozess für die Verwaltung der Affinität in Exchange 2010**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-232">**Figure 3. Process for maintaining affinity in Exchange 2010**</span></span>

![Abbildung, die zeigt, wie die Tabelle aktiver Abonnements auf dem Clientzugriffsserver in Exchange 2010 verwaltet wird.](media/Exchange2013_NoficationAffinity2010.png)
  
<span data-ttu-id="fd3d3-234">**Abbildung 4. Prozess für die Verwaltung der Affinität in Exchange Online und Exchange 2013**</span><span class="sxs-lookup"><span data-stu-id="fd3d3-234">**Figure 4. Process for maintaining affinity in Exchange Online and Exchange 2013**</span></span>

![Abbildung, die zeigt, wie der Lastenausgleich und Clientzugriffsserver Anforderungen an den Postfachserver leiten, der die Tabelle aktiver Abonnements in Exchange Server und Exchange Online verwaltet.](media/Exchange2013_NoficationAffinity2013.png)
  
<span data-ttu-id="fd3d3-236">In Exchange 2010, der Client nur kennt die Adresse des Systems zum Lastenausgleich und die Exchangecookie, die vom Server zurückgegeben wird sichergestellt, dass die Anforderung an den richtigen Client Access Server weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-236">In Exchange 2010, the client only knows the address of the load balancer, and the exchangecookie that is returned by the server ensures that the request is routed to the right Client Access server.</span></span> <span data-ttu-id="fd3d3-237">In späteren Versionen, die das System zum Lastenausgleich und die Clientzugriffs-Serverrollen müssen beide jedoch die Anforderungen entsprechend weitergeleitet werden, bevor sie an den Postfachserver gelangen.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-237">However, in later versions, the load balancer and the Client Access server roles both have to route the requests appropriately before they get to the Mailbox server.</span></span> <span data-ttu-id="fd3d3-238">Dazu, dass zusätzliche Informationen erforderlich ist, ist der Grund, warum der neue Kopf- und Cookie eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-238">To do that, additional information is required, which is why the new headers and cookie were introduced.</span></span> <span data-ttu-id="fd3d3-239">Der Artikel [Benachrichtigung Abonnements, Postfach-Ereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) wird erläutert, wie Abonnements in Exchange 2013 verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-239">The article [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explains how subscriptions are maintained in Exchange 2013.</span></span> 
  
<span data-ttu-id="fd3d3-240">Sie möglicherweise feststellen, dass die Exchangecookie, die Exchange 2010 verwendet weiterhin von späteren Versionen zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-240">You might notice that the exchangecookie that Exchange 2010 uses is still returned by later versions.</span></span> <span data-ttu-id="fd3d3-241">Es ist keine Beschädigungen in dieses Cookie in Anforderungen einschließlich, aber höhere Versionen von Exchange ignorieren.</span><span class="sxs-lookup"><span data-stu-id="fd3d3-241">There's no harm in including this cookie in requests, but later versions of Exchange ignore it.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd3d3-242">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd3d3-242">See also</span></span>

- [<span data-ttu-id="fd3d3-243">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-243">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="fd3d3-244">Stream-Benachrichtigungen bezüglich Postfach Ereignisse mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-244">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="fd3d3-245">Ziehen Sie Benachrichtigungen über Ereignisse Postfach mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-245">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="fd3d3-246">Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-246">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
- [<span data-ttu-id="fd3d3-247">Änderungen bei der Verwaltung von Affinität für EWS-Abonnements...</span><span class="sxs-lookup"><span data-stu-id="fd3d3-247">Changes in Managing Affinity for EWS Subscriptions…</span></span>](http://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [<span data-ttu-id="fd3d3-248">EWS-Einschränkung in Exchange</span><span class="sxs-lookup"><span data-stu-id="fd3d3-248">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

