---
title: Steuern des Zugriffs auf EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: Erfahren Sie, wie der Zugriff auf EWS für Benutzer, Anwendungen oder die gesamte Organisation gesteuert wird.
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756870"
---
# <a name="control-access-to-ews-in-exchange"></a><span data-ttu-id="7168b-103">Steuern des Zugriffs auf EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7168b-103">How to: Control access to EWS in Exchange</span></span>

<span data-ttu-id="7168b-104">Erfahren Sie, wie der Zugriff auf EWS für Benutzer, Anwendungen oder die gesamte Organisation gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7168b-104">Find out how to control access to EWS for users, applications, or the entire organization.</span></span>
  
<span data-ttu-id="7168b-p101">Unabhängig davon, ob Sie die verwaltete EWS-API oder EWS direkt in Ihrer Anwendung verwenden, können Sie den Zugriff auf Exchange-Webdienste (EWS) steuern. Wenn Sie über Administratorrechte auf Ihrem Exchange-Server verfügen, können Sie den Zugriff auf EWS mithilfe der Exchange-Verwaltungsshell verwalten und den Zugriff global, für jeden Benutzer und für jede Anwendung steuern.</span><span class="sxs-lookup"><span data-stu-id="7168b-p101">Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS). If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.</span></span>
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a><span data-ttu-id="7168b-107">Cmdlets der Exchange-Verwaltungsshell zum Konfigurieren der Zugriffssteuerung</span><span class="sxs-lookup"><span data-stu-id="7168b-107">Exchange Management Shell cmdlets for configuring access control</span></span>
<span data-ttu-id="7168b-108"><a name="bk_Cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="7168b-108"></span></span>

<span data-ttu-id="7168b-109">Mit den folgenden Cmdlets der Exchange-Verwaltungsshell können Sie die aktuelle Zugriffskonfiguration anzeigen und EWS-Zugriffssteuerungen festlegen:</span><span class="sxs-lookup"><span data-stu-id="7168b-109">You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:</span></span>
  
- <span data-ttu-id="7168b-110">[Get-CASMailbox](http://technet.microsoft.com/de-DE/library/bb124754.aspx): Zeigt an, welche Parameter für ein bestimmtes Postfach festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7168b-110">[Get-CASMailbox](http://technet.microsoft.com/de-DE/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.</span></span>   
- <span data-ttu-id="7168b-111">[Set-CASMailbox](http://technet.microsoft.com/de-DE/library/bb125264.aspx): Legt Parameter für ein bestimmtes Postfach fest.</span><span class="sxs-lookup"><span data-stu-id="7168b-111">[Set-CASMailbox](http://technet.microsoft.com/de-DE/library/bb125264.aspx) - Sets parameters for a particular mailbox.</span></span>    
- <span data-ttu-id="7168b-112">[Get-OrganizationConfig](http://technet.microsoft.com/de-DE/library/aa997571.aspx): Zeigt die Parameter für die gesamte Organisation an.</span><span class="sxs-lookup"><span data-stu-id="7168b-112">[Get-OrganizationConfig](http://technet.microsoft.com/de-DE/library/aa997571.aspx) - Shows you the parameters for the entire organization.</span></span>    
- <span data-ttu-id="7168b-113">[Set-OrganizationConfig](http://technet.microsoft.com/de-DE/library/aa997443.aspx): Legt die Parameter für die gesamte Organisation fest.</span><span class="sxs-lookup"><span data-stu-id="7168b-113">[Set-OrganizationConfig](http://technet.microsoft.com/de-DE/library/aa997443.aspx) - Sets the parameters for the entire organization.</span></span> 

<span data-ttu-id="7168b-114"><a name="bk_Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="7168b-114"></span></span>

## <a name="examples-controlling-access-to-ews"></a><span data-ttu-id="7168b-115">Beispiele: Steuern des Zugriffs auf Konferenzen</span><span class="sxs-lookup"><span data-stu-id="7168b-115">Examples: Controlling access to EWS</span></span>

<span data-ttu-id="7168b-116">Werfen wir einen Blick auf einige Szenarien, in denen gezeigt wird, wie Sie den Zugriff auf Ihre Anwendung steuern können.</span><span class="sxs-lookup"><span data-stu-id="7168b-116">Let's take a look at a few scenarios that show you how you can control access to your application.</span></span>
  
<span data-ttu-id="7168b-117">**Tabelle 1. Befehle zum Steuern des Zugriffs auf EWS**</span><span class="sxs-lookup"><span data-stu-id="7168b-117">**Table 1. Commands for controlling access to EWS**</span></span>

|<span data-ttu-id="7168b-118">Zweck</span><span class="sxs-lookup"><span data-stu-id="7168b-118">If you want to</span></span> |<span data-ttu-id="7168b-119">Verwenden Sie den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="7168b-119">Use this command</span></span>|
|:-----|:-----|
|<span data-ttu-id="7168b-120">Verhindern, dass Clientanwendungen EWS verwenden.</span><span class="sxs-lookup"><span data-stu-id="7168b-120">Block all client applications from using EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/><span data-ttu-id="7168b-p102">Damit können in der AllowList aufgeführte Anwendungen eine Verbindung herstellen. In diesem Beispiel sind keine Anwendungen in der AllowList enthalten, was bedeutet, dass keine Anwendungen EWS verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7168b-p102">This allows applications listed in the AllowList to connect. In this example, no applications are included in the AllowList, so no applications can use EWS.</span></span> |
|<span data-ttu-id="7168b-123">Zulassen, dass eine Liste von Clientanwendungen EWS verwendet.</span><span class="sxs-lookup"><span data-stu-id="7168b-123">Allow a list of client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/><span data-ttu-id="7168b-p103">Damit können bestimmte Anwendungen EWS verwenden. In diesem Beispiel wird der Zugriff für jede Anwendung gewährt, deren Zeichenfolge des Benutzer-Agenten mit „OWA/" beginnt.  </span><span class="sxs-lookup"><span data-stu-id="7168b-p103">This allows specific applications to use EWS. In this example, any application that has a user agent string that starts with "OWA/" is allowed access.</span></span> |
|<span data-ttu-id="7168b-126">Zulassen, dass alle Clientanwendungen EWS verwenden, mit Ausnahme derjenigen, die blockiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7168b-126">Allow all client applications to use EWS except those that are specifically blocked.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/><span data-ttu-id="7168b-127">In diesem Beispiel werden nur Anwendungen blockiert, die eine Zeichenfolge des Benutzer-Agenten aufweisen, die mit „OWA/“ beginnt.</span><span class="sxs-lookup"><span data-stu-id="7168b-127">This example only blocks applications from using EWS that have a user agent string that starts with "OWA/".</span></span> |
|<span data-ttu-id="7168b-128">Zulassen, dass alle Clientanwendungen EWS verwenden.</span><span class="sxs-lookup"><span data-stu-id="7168b-128">Allow all client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> <span data-ttu-id="7168b-129">Da keine BlockList angegeben ist, können alle Anwendungen EWS verwenden.</span><span class="sxs-lookup"><span data-stu-id="7168b-129">Because no BlockList is specified, all applications can use EWS.</span></span> |
|<span data-ttu-id="7168b-130">Blockieren der Verwendung von EWS für die gesamte Organisation</span><span class="sxs-lookup"><span data-stu-id="7168b-130">Block the entire organization from using EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$false` |
|<span data-ttu-id="7168b-131">Zulassen der Verwendung von EWS für die gesamte Organisation</span><span class="sxs-lookup"><span data-stu-id="7168b-131">Allow the entire organization to use EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$true`|
|<span data-ttu-id="7168b-132">Blockieren der Verwendung von EWS für ein einzelnes Postfach</span><span class="sxs-lookup"><span data-stu-id="7168b-132">Block an individual mailbox from using EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|<span data-ttu-id="7168b-133">Zulassen, dass ein einzelnes Postfach EWS verwendet.</span><span class="sxs-lookup"><span data-stu-id="7168b-133">Allow an individual mailbox to use EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a><span data-ttu-id="7168b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7168b-134">See also</span></span>

- [<span data-ttu-id="7168b-135">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="7168b-135">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="7168b-136">Steuern des Clientanwendungszugriffs auf EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7168b-136">Controlling client application access to EWS in Exchange</span></span>](controlling-client-application-access-to-ews-in-exchange.md)   
- <span data-ttu-id="7168b-137">
  [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)</span><span class="sxs-lookup"><span data-stu-id="7168b-137">[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)</span></span> 
- [<span data-ttu-id="7168b-138">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7168b-138">Windows PowerShell</span></span>](http://msdn.microsoft.com/de-DE/library/dd835506%28v=vs.85%29.aspx)
    

