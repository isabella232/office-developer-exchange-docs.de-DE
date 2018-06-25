---
title: Generieren Sie eine Liste von Endpunkten für die AutoErmittlung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: Erfahren Sie, wie Sie eine Priorität für die AutoErmittlung Endpunkte erstellen.
ms.openlocfilehash: ccecacc9c8beef464727efbc9d1fced7a81f9b7c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756900"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="a8a2c-103">Generieren Sie eine Liste von Endpunkten für die AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="a8a2c-103">Generate a list of Autodiscover endpoints</span></span>

<span data-ttu-id="a8a2c-104">Erfahren Sie, wie Sie eine Priorität für die AutoErmittlung Endpunkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-104">Find out how to generate a prioritized list of Autodiscover endpoints.</span></span>
  
<span data-ttu-id="a8a2c-105">Die erste Aufgabe in der [AutoErmittlung-Prozesses](autodiscover-for-exchange.md) wird zum Erstellen der Liste der AutoErmittlung-Endpunkte für die Anwendung zu testen.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-105">The first task in the [Autodiscover process](autodiscover-for-exchange.md) is to generate a list of Autodiscover endpoints for your application to try.</span></span> <span data-ttu-id="a8a2c-106">Diese Endpunkte AutoErmittlung können stammen aus einer [SCP-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) oder die e-Mail-Adresse des Benutzers abgeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-106">These Autodiscover endpoints can come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) or can be derived from the user's email address.</span></span> <span data-ttu-id="a8a2c-107">Schließlich können Sie eine große Anzahl von Endpunkten am Ende.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-107">In the end, you can end up with a large number of endpoints.</span></span> <span data-ttu-id="a8a2c-108">Sehen wir uns an, wie Sie sie nach Priorität sortieren können.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-108">Let's take a look at how you can organize them by priority.</span></span> 
  
## <a name="start-with-scp-lookup"></a><span data-ttu-id="a8a2c-109">Beginnen Sie mit SCP-Suche</span><span class="sxs-lookup"><span data-stu-id="a8a2c-109">Start with SCP lookup</span></span>
<span data-ttu-id="a8a2c-110"><a name="bk_StartWithScp"> </a></span><span class="sxs-lookup"><span data-stu-id="a8a2c-110"></span></span>

<span data-ttu-id="a8a2c-111">AutoErmittlung-Endpunkte, die keinen [SCP-Suche](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) stammen sollte die höchste Priorität in der Liste verfügen.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-111">Autodiscover endpoints that come from an [SCP lookup](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) should have top priority in your list.</span></span> <span data-ttu-id="a8a2c-112">Administratoren können konfigurieren SCP-Objekten so, dass Ihr Client an den Endpunkt engsten oder am effizientesten AutoErmittlung weitergeleitet, daher es ratsam ist, diese Endpunkte zu starten.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-112">Administrators can configure SCP objects to route your client to the closest or most efficient Autodiscover endpoint, so it is a good idea to start with these endpoints.</span></span> <span data-ttu-id="a8a2c-113">Da die SCP-Suchprozess Priorisierung Schema verfügt, sind die Ergebnisse der SCP-Suche bereits, wie folgt priorisiert:</span><span class="sxs-lookup"><span data-stu-id="a8a2c-113">Because the SCP lookup process has its own prioritization scheme, the results of an SCP lookup are already prioritized, as follows:</span></span> 
  
1. <span data-ttu-id="a8a2c-114">AutoErmittlung-Endpunkten von SCP-Objekten, die mit einem Bereich für die Active Directory-Standort, zu dem der Client-Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-114">Autodiscover endpoints from SCP objects scoped to the Active Directory site that the client computer belongs to.</span></span>
    
2. <span data-ttu-id="a8a2c-115">AutoErmittlung-Endpunkten von SCP-Objekten, die nicht mit einem Bereich für alle Active Directory-Standort.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-115">Autodiscover endpoints from SCP objects not scoped to any Active Directory site.</span></span>
    
3. <span data-ttu-id="a8a2c-116">AutoErmittlung-Endpunkten von SCP-Objekten bezogen auf einem anderen Active Directory-Standort als die Website, der der Clientcomputer gehört.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-116">Autodiscover endpoints from SCP objects scoped to a different Active Directory site than the site that the client computer belongs to.</span></span>
    
<span data-ttu-id="a8a2c-117">Nachdem Sie die Ergebnisse der SCP-Suchprozess haben, können Sie Endpunkte hinzufügen, die von e-Mail-Adresse des Benutzers abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-117">After you have the results of the SCP lookup process, you can add endpoints that derive from the user's email address.</span></span> <span data-ttu-id="a8a2c-118">Diese können dienen als eine standardmäßige Endpunkte und Fallback festgelegt, falls es keine Ergebnisse SCP gibt oder die Endpunkte von SCP-Suche zurückgegebenen nicht ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-118">These can serve as a default set of endpoints and a fallback in case there are no SCP results or the endpoints returned from the SCP lookup are not sufficient.</span></span>
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a><span data-ttu-id="a8a2c-119">Hinzufügen von e-Mail-Adresse des Benutzers abgeleitete Endpunkte</span><span class="sxs-lookup"><span data-stu-id="a8a2c-119">Add endpoints derived from the user's email address</span></span>
<span data-ttu-id="a8a2c-120"><a name="bk_AddDerivedEndpoints"> </a></span><span class="sxs-lookup"><span data-stu-id="a8a2c-120"></span></span>

<span data-ttu-id="a8a2c-121">Wenn SCP-Suche funktioniert nicht oder nicht die SCP-Suche zurückgegebenen Endpunkte eine erfolgreiche Antwort zurückzugeben, können die e-Mail-Adresse des Benutzers einen Satz von AutoErmittlung Standardendpunkte abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-121">When SCP lookup doesn't work, or the endpoints returned by the SCP lookup don't return a successful response, you can derive a set of default Autodiscover endpoints from the user's email address.</span></span> <span data-ttu-id="a8a2c-122">Diese Endpunkte sollte eine niedrigere Priorität als die SCP-Suche stammen, jedoch möglicherweise benötigt werden, wenn die SCP-Suche nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-122">These endpoints should be a lower priority than any that come from an SCP lookup, but you might need them if the SCP lookup was not successful.</span></span>
  
### <a name="to-derive-autodiscover-endpoints"></a><span data-ttu-id="a8a2c-123">AutoErmittlung Endpunkte abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-123">To derive Autodiscover endpoints</span></span>

1. <span data-ttu-id="a8a2c-124">Extrahieren Sie den Domänennamen aus e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-124">Extract the domain name from the user's email address.</span></span> <span data-ttu-id="a8a2c-125">Angenommen, wenn die e-Mail-Adresse des Benutzers Sadie.Daniels@contoso.com ist, wäre der Domänennamen "contoso.com".</span><span class="sxs-lookup"><span data-stu-id="a8a2c-125">For example, if the user's email address is Sadie.Daniels@contoso.com, the domain name would be contoso.com.</span></span>
    
2. <span data-ttu-id="a8a2c-126">Endpunkt-URLs ohne Dateierweiterungen in den folgenden Formaten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="a8a2c-126">Construct endpoint URLs without file extensions in the following formats:</span></span>
    
  - <span data-ttu-id="a8a2c-127">"https://" + Domäne + "/ Autodiscover/AutoErmittlung"</span><span class="sxs-lookup"><span data-stu-id="a8a2c-127">"https://" + domain + "/autodiscover/autodiscover"</span></span>
    
  - <span data-ttu-id="a8a2c-128">"https://autodiscover."</span><span class="sxs-lookup"><span data-stu-id="a8a2c-128"></span></span> <span data-ttu-id="a8a2c-129">+ Domäne + "/ Autodiscover/AutoErmittlung"</span><span class="sxs-lookup"><span data-stu-id="a8a2c-129">+ domain + "/autodiscover/autodiscover"</span></span>
    
<span data-ttu-id="a8a2c-130">Nachdem Sie die Liste der Endpunkt-URLs kompiliert werden, die von SCP-Suche und die e-Mail-Adresse des Benutzers abgeleitet werden sollen, müssen Sie möglicherweise überarbeiten Dateinamenerweiterungen in diesen URLs, je nachdem, ob Sie die [AutoErmittlung SOAP-Webdienst](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) oder die [POX verwenden AutoErmittlung-Webdienst](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8a2c-130">After you compile the list of endpoint URLs that derive from both SCP lookup and the user's email address, you might need to revise file name extensions in those URLs, depending on whether you're using the [SOAP Autodiscover web service](http://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx) or the [POX Autodiscover web service](http://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx).</span></span>
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a><span data-ttu-id="a8a2c-131">Fügen Sie hinzu oder Ersetzen Sie Dateinamenerweiterungen Endpunkt-URLs</span><span class="sxs-lookup"><span data-stu-id="a8a2c-131">Add or replace file name extensions in endpoint URLs</span></span>
<span data-ttu-id="a8a2c-132"><a name="bk_FileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="a8a2c-132"></span></span>

<span data-ttu-id="a8a2c-133">Sie können den AutoErmittlungsdienst mithilfe der AutoErmittlung SOAP-Webdienst oder den Webdienst POX AutoErmittlung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-133">You can access the Autodiscover service by using either the SOAP Autodiscover web service or the POX Autodiscover web service.</span></span> <span data-ttu-id="a8a2c-134">Jeder Dienst verwendet ähnliche Endpunkt-URLs mit der einzige Unterschied ist, die Dateinamenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-134">Each service uses similar endpoint URLs, with the only difference being the file name extension.</span></span> <span data-ttu-id="a8a2c-135">Der AutoErmittlung SOAP-Webdienst verwendet die Erweiterung "svc" und der Webdienst POX AutoErmittlung verwendet die Erweiterung ".xml".</span><span class="sxs-lookup"><span data-stu-id="a8a2c-135">The SOAP Autodiscover web service uses the ".svc" file name extension, and the POX Autodiscover web service uses the ".xml" file name extension.</span></span>
  
<span data-ttu-id="a8a2c-136">Standardmäßig sind der AutoErmittlung-Endpunkt-URLs von SCP-Suche zurückgegeben POX URLs.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-136">By default, the Autodiscover endpoint URLs returned from an SCP lookup are POX URLs.</span></span> <span data-ttu-id="a8a2c-137">Jedoch bei Verwendung von SOAP-AutoErmittlung können einfach die Dateinamenerweiterung aus ".xml" an "svc" ändern und versuchen Sie es eine SOAP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-137">However, if you are using SOAP Autodiscover, you can simply change the file name extension from ".xml" to ".svc" and try a SOAP request.</span></span>
  
<span data-ttu-id="a8a2c-138">Für die abgeleiteten AutoErmittlung-Endpunkt-URLs die Erweiterung fehlt.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-138">For the derived Autodiscover endpoint URLs, the file extension is omitted.</span></span> <span data-ttu-id="a8a2c-139">Fügen Sie die entsprechende Erweiterung für die AutoErmittlung-Webdienst, den Sie arbeiten, bevor Sie versuchen, die URL hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-139">Add the appropriate file extension for the Autodiscover web service you are using prior to trying the URL.</span></span>
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a><span data-ttu-id="a8a2c-140">Beispiel: Erstellen einer Liste von AutoErmittlung-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="a8a2c-140">Example: Generating a list of Autodiscover endpoints</span></span>
<span data-ttu-id="a8a2c-141"><a name="bk_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="a8a2c-141"></span></span>

<span data-ttu-id="a8a2c-142">Sehen wir uns an einem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-142">Let's take a look at an example.</span></span> <span data-ttu-id="a8a2c-143">Sadie Daniels (Sadie.Daniels@contoso.com) ist eine Exchange-Webdienste (EWS)-Anwendung zum ersten Mal verwendet.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-143">Sadie Daniels (Sadie.Daniels@contoso.com) is using an Exchange Web Services (EWS) application for the first time.</span></span> <span data-ttu-id="a8a2c-144">Die Anwendung verwendet für die AutoErmittlung selbst konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-144">The application uses Autodiscover to configure itself.</span></span> <span data-ttu-id="a8a2c-145">Sadies Computers ausführt, wird die Domäne "contoso.com" und "Redmond" Active Directory-Standort ist.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-145">Sadie's computer is joined to the contoso.com domain and is in the Redmond Active Directory site.</span></span> <span data-ttu-id="a8a2c-146">Die Anwendung generiert eine Liste der AutoErmittlung-Endpunkte, die in Abbildung 1 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-146">The application generates the list of Autodiscover endpoints shown in Figure 1.</span></span>
  
<span data-ttu-id="a8a2c-147">**Abbildung 1: Beispielliste AutoErmittlung**</span><span class="sxs-lookup"><span data-stu-id="a8a2c-147">**Figure 1: Sample list of Autodiscover endpoints**</span></span>

![Eine Beispielliste mit Endpunkten für die AutoErmittlung, in der über die SCP-Suche abgerufene Endpunkte mit einer höheren Priorität angezeigt werden als abgeleitete Endpunkte](media/Ex15_Autodiscover_GenerateList_Example.png)
  
<span data-ttu-id="a8a2c-149">Die EWS-Anwendung in diesem Beispiel bevorzugt den AutoErmittlung für SOAP-Webdienst, damit es die Dateinamenerweiterung für die SCP-Ergebnisse "svc" geändert, vor dem Senden von SOAP-Anforderungen für diese.</span><span class="sxs-lookup"><span data-stu-id="a8a2c-149">The EWS application in this example prefers the SOAP Autodiscover web service, so it changes the file name extension for the SCP results to ".svc" before sending SOAP requests to them.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="a8a2c-150">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a8a2c-150">Next steps</span></span>
<span data-ttu-id="a8a2c-151"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a8a2c-151"></span></span>

<span data-ttu-id="a8a2c-152">Nachdem Sie eine Liste von Endpunkten AutoErmittlung generiert haben, testen Sie sie durch [Senden von Anforderungen an die Endpunkte](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span><span class="sxs-lookup"><span data-stu-id="a8a2c-152">After you generate a list of Autodiscover endpoints, try them by [sending requests to those endpoints](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8a2c-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8a2c-153">See also</span></span>


- [<span data-ttu-id="a8a2c-154">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="a8a2c-154">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="a8a2c-155">Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8a2c-155">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="a8a2c-156">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="a8a2c-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    

