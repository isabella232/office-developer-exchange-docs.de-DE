---
title: Steuern des Clientanwendungszugriffs auf EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: Erfahren Sie mehr zu den Optionen für die Verwaltung des Clientanwendungszugriffs auf EWS.
ms.openlocfilehash: 29a640178afc9814a0b2232225ae4307e49afed2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756822"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a><span data-ttu-id="3a0e5-103">Steuern des Clientanwendungszugriffs auf EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="3a0e5-103">Controlling client application access to EWS in Exchange</span></span>

<span data-ttu-id="3a0e5-104">Erfahren Sie mehr zu den Optionen für die Verwaltung des Clientanwendungszugriffs auf EWS.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-104">Learn about the options for managing client application access to EWS.</span></span>
  
<span data-ttu-id="3a0e5-p101">Jeder EWS-Clientanwendung, die Sie erstellen, muss Zugriff auf Exchange Online, Exchange Online als Teil von Office 365 oder eine Version von Exchange beginnend mit Exchange 2013, bevor diese EWS-Vorgänge aufrufen kann. Test- oder Produktionsserveradministratoren können die Exchange-Verwaltungsshell verwenden, um den Zugriff auf EWS entweder für alle Benutzer und Anwendungen, für einzelne Benutzer oder für einzelne Anwendungen zu beschränken. Die Zugriffssteuerung für EWS basiert auf Control EWS basiert auf Domänenkonten. Wenn eine Verbindung mit Anmeldeinformationen hergestellt wird, die von der lokalen Sicherheitsautorität authentifiziert wurden, gibt der Server einen Fehler zurück, der angibt, dass nur Domänenkonten eine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p101">Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations. Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications. Access control for EWS is based on domain accounts. When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect.</span></span> 
  
## <a name="access-control-for-ews-clients-and-users"></a><span data-ttu-id="3a0e5-109">Zugriffssteuerung für EWS-Clients und Benutzer</span><span class="sxs-lookup"><span data-stu-id="3a0e5-109">Access control for EWS clients and users</span></span>
<span data-ttu-id="3a0e5-110"><a name="bk_configure"> </a></span><span class="sxs-lookup"><span data-stu-id="3a0e5-110"></span></span>

<span data-ttu-id="3a0e5-111">Ihr Test- und Produktionsserveradministrator kann die Zugriffssteuerung für Clients, die eine Verbindung zu EWS herstellen, folgendermaßen konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="3a0e5-111">Your test or production server administrator can configure access control for clients that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="3a0e5-112">Indem für alle Clientanwendungen verhindert wird, dass eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-112">By blocking all client applications from connecting.</span></span>
    
- <span data-ttu-id="3a0e5-113">Indem nur bestimmten Clientanwendungen ermöglicht wird, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-113">By allowing specific client applications only to connect.</span></span>
    
- <span data-ttu-id="3a0e5-114">Indem allen Clientanwendungen ermöglicht wird, eine Verbindung herzustellen, mit Ausnahme derjenigen, die speziell blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-114">By allowing any client application to connect except those that are specifically blocked.</span></span>
    
- <span data-ttu-id="3a0e5-115">Indem allen Clientanwendungen ermöglicht wird, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-115">By allowing any client application to connect.</span></span>
    
<span data-ttu-id="3a0e5-116">Anwendungen werden von der Benutzer-Agent-Zeichenfolge identifiziert, die sie in der HTTP-Webanforderung senden.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-116">Applications are identified by the user agent string that they send in the HTTP web request.</span></span>
  
> [!SICHERHEITSHINWEIS]<span data-ttu-id="3a0e5-p102"> Das Blockieren auf Anwendungsebene ist kein Sicherheitsfeature. Die Benutzer-Agent-Zeichenfolge kann ganz einfach gefälscht werden. Wenn einer Anwendung Zugriff auf EWS gewährt wird, muss die Anwendung dennoch Anmeldeinformationen bereitstellen, die der Server authentifiziert, bevor die Anwendung eine Verbindung zu EWS herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p102"> Application-level blocking is not a security feature. The user agent string is easily spoofed. If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS.</span></span> 
  
<span data-ttu-id="3a0e5-120">Administratoren können über die folgenden Methoden die Zugriffssteuerung auch für Postfachbesitzer konfigurieren, die eine Verbindung zu EWS herstellen:</span><span class="sxs-lookup"><span data-stu-id="3a0e5-120">Administrators can also configure access control for mailbox owners that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="3a0e5-121">Durch Blockieren oder Zulassen ein ganzen Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-121">By blocking or allowing an entire organization.</span></span>
    
- <span data-ttu-id="3a0e5-122">Durch das Blockieren oder Zulassen einer Gruppe von Benutzern, die durch einen rollenbasierten Authentifizierungsbereich identifiziert werden, der Postfachbesitzer ein- oder ausschließt, die keinen Zugriff auf EWS haben.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-122">By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.</span></span>
    
- <span data-ttu-id="3a0e5-123">Durch Blockieren oder Zulassen eines einzelnen Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-123">By blocking or allowing an individual mailbox owner.</span></span>
    
<span data-ttu-id="3a0e5-p103">Bestimmte Zugriffssteuerungseinstellungen setzen allgemeine Zugriffssteuerungseinstellungen außer Kraft. Wenn eine Organisation beispielsweise EWS-Zugriff verweigert, einem einzelnen Postfachbesitzer jedoch Anwendungszugriff gewährt wird, hat die einzelne Einstellung Vorrang und der Zugriff wird gewährt.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p103">Specific access control settings override general access control settings. For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed.</span></span> 
  
## <a name="delegation-and-ews-access-management"></a><span data-ttu-id="3a0e5-126">Delegierung und EWS-Zugriffsverwaltung</span><span class="sxs-lookup"><span data-stu-id="3a0e5-126">Delegation and EWS access management</span></span>
<span data-ttu-id="3a0e5-127"><a name="bk_delegation"> </a></span><span class="sxs-lookup"><span data-stu-id="3a0e5-127"></span></span>

<span data-ttu-id="3a0e5-p104">Wenn stellvertretende Benutzer, die keinen Zugriff auf EWS haben, Ihre Clientanwendung verwenden, können sie mithilfe von EWS nicht auf das Postfach des Hauptbenutzers zugreifen, auch dann nicht, wenn der Hauptbenutzer Zugriff auf EWS hat. Wenn der stellvertretende Benutzer über EWS-Zugriff verfügt, kann der Stellvertreter Ihre EWS-Clientanwendung verwenden, um auf das Postfach des Hauptbenutzers zuzugreifen, auch wenn der Hauptbenutzer keinen Zugriff auf EWS hat.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p104">When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access. If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access.</span></span> 
  
## <a name="impersonation-and-ews-access-management"></a><span data-ttu-id="3a0e5-130">Identitätswechsel und EWS-Zugriffsverwaltung</span><span class="sxs-lookup"><span data-stu-id="3a0e5-130">Impersonation and EWS access management</span></span>
<span data-ttu-id="3a0e5-131"><a name="bk_impersonation"> </a></span><span class="sxs-lookup"><span data-stu-id="3a0e5-131"></span></span>

<span data-ttu-id="3a0e5-p105">Clientanwendungen, die im Auftrag von Postfachbesitzern eine Verbindung zu EWS herstellen, können die EWS-Einstellungen des Postfachbesitzers möglicherweise nicht verwenden. Angenommen, eine Anwendung, die E-Mails für ein Unternehmen archiviert, muss, unabhängig von den Einstellungen des Postfachbenutzers eine Verbindung zu EWS herstellen. Andere Programme, z. B. E-Mail-Clients, müssen die EWS-Einstellungen des Postfachbesitzers verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p105">Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner. For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are. Other applications, such as mail clients, do have to use the mailbox owner's EWS settings.</span></span> 
  
<span data-ttu-id="3a0e5-p106">Administratoren sollten ein Konto für den Identitätswechsel für jede Anwendung oder Anwendungsklasse erstellen, das bzw. die auf dem Server verwendet wird. Auf diese Weise kann der Administrator den rollenbasierten Zugriffssteuerungsbereich für alle Benutzer konfigurieren, die nicht über EWS-Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-p106">Administrators should create an impersonation account for each application or application class that they use on their server. This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions.</span></span> 
  
<span data-ttu-id="3a0e5-137">Um Identitätswechselkonten zu aktivieren, sollte der Test- oder Produktionsserveradministrator eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3a0e5-137">To enable impersonation accounts, your test or production server administrator should do one of the following:</span></span> 
  
- <span data-ttu-id="3a0e5-138">Hinzufügen der Gruppe der authentifizierten Benutzer zur Gruppe „Prä-Windows 2000 kompatibler Zugriff".</span><span class="sxs-lookup"><span data-stu-id="3a0e5-138">Add the Authenticated Users group to the Pre-Win2K Compatible Access Group.</span></span> 
    
- <span data-ttu-id="3a0e5-139">Hinzufügen der Exchange Server-Gruppe zur Windows-Autorisierungszugriffsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3a0e5-139">Add the Exchange Servers group to the Windows Authorization Access group.</span></span> 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a><span data-ttu-id="3a0e5-140">Cmdlets der Exchange-Verwaltungsshell für Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="3a0e5-140">Exchange Management Shell cmdlets for access management</span></span>
<span data-ttu-id="3a0e5-141"><a name="bk_cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="3a0e5-141"></span></span>

<span data-ttu-id="3a0e5-142">Administratoren verwenden die folgenden Cmdlets der Exchange-Verwaltungsshell, um die EWS-Zugriffssteuerung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="3a0e5-142">Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls:</span></span> 
  
- [<span data-ttu-id="3a0e5-143">Get-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="3a0e5-143">Get-CASMailbox</span></span>](http://technet.microsoft.com/de-de/library/bb124754.aspx)
    
- [<span data-ttu-id="3a0e5-144">Set-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="3a0e5-144">Set-CASMailbox</span></span>](http://technet.microsoft.com/de-de/library/bb125264.aspx)
    
- [<span data-ttu-id="3a0e5-145">Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e5-145">Get-OrganizationConfig</span></span>](http://technet.microsoft.com/de-de/library/aa997571.aspx)
    
- [<span data-ttu-id="3a0e5-146">Set-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e5-146">Set-OrganizationConfig</span></span>](http://technet.microsoft.com/de-de/library/aa997443.aspx)
    
## <a name="see-also"></a><span data-ttu-id="3a0e5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a0e5-147">See also</span></span>

- [<span data-ttu-id="3a0e5-148">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="3a0e5-148">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="3a0e5-149">Steuern des Zugriffs auf EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="3a0e5-149">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md)
- [<span data-ttu-id="3a0e5-150">Exchange Server-PowerShell (Exchange-Verwaltungsshell)</span><span class="sxs-lookup"><span data-stu-id="3a0e5-150">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/de-de/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [<span data-ttu-id="3a0e5-151">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a0e5-151">Windows PowerShell</span></span>](http://msdn.microsoft.com/de-de/library/dd835506%28v=vs.85%29.aspx)
    

