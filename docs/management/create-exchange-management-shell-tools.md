---
title: Erstellen von Exchange-Verwaltungsshell-tools
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: Hier finden Sie Informationen zu ersten Schritten beim Erstellen der Exchange-Verwaltungsshell-Tools für Exchange.
ms.openlocfilehash: e8414460007f333e50c9d596bf977792977b1e4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757132"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="5e323-103">Erstellen von Exchange-Verwaltungsshell-tools</span><span class="sxs-lookup"><span data-stu-id="5e323-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="5e323-104">Hier finden Sie Informationen zu ersten Schritten beim Erstellen der Exchange-Verwaltungsshell-Tools für Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e323-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="5e323-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="5e323-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="5e323-106">Die Exchange-Verwaltungsshell bietet einen umfassenden Satz von Befehlen, basierend auf der Windows PowerShell-Plattform für die Verwaltung von Exchange Online, Exchange Online als Teil von Office 365 oder eine lokale Version von Exchange, beginnend mit Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="5e323-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="5e323-107">Exchange-Verwaltungsshell-Befehlen können Sie die Verwaltung eines Servers durch die Befehle direkt ausgeführt oder mithilfe von Befehlsskripts automatisieren.</span><span class="sxs-lookup"><span data-stu-id="5e323-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="5e323-108">Wenn Sie Exchange-Verwaltungsshell-Befehle in einer hosting-Anwendung, wie eine administrative Anwendung verwenden, die der Administrator Desktop oder über eine webbasierte Anwendung ausgeführt wird, können Sie Exchange-Verwaltungsshell-Cmdlets von Anrufen in der Visual Basic oder C#-Anwendung zum Verwalten von eines Exchange-Servers.</span><span class="sxs-lookup"><span data-stu-id="5e323-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="5e323-109">Erste Schritte mit Exchange-Verwaltungsshell-tools</span><span class="sxs-lookup"><span data-stu-id="5e323-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="5e323-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="5e323-110"></span></span>

<span data-ttu-id="5e323-111">Wenn Sie mit der Erstellung von Windows PowerShell-hostanwendungen vertraut sind, und sehen Sie ein Beispiel, das zeigt, wie der Exchange-Verwaltungsshell-Cmdlets aus einer Anwendung aufzurufen, oder sehen Sie ein Beispiel für die Typen von Anwendungen, die Sie erstellen können, über die Exchange möchten -Verwaltungsshell-Cmdlets finden Sie unter [Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="5e323-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="5e323-112">Die Exchange-Verwaltungsshell-Cmdlets sind Erweiterungen für Windows PowerShell, eine vorgangsbasierte Befehlszeilenshell und Skriptsprache, die speziell für die Systemadministration konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="5e323-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="5e323-113">Windows PowerShell basiert auf .NET Framework und bietet eine objektorientierte-API für das Cmdlet Anbieter und Host-Anwendungsentwickler.</span><span class="sxs-lookup"><span data-stu-id="5e323-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="5e323-114">Weitere Informationen zu den Windows PowerShell-Programmierung finden Sie in der [Windows PowerShell-SDK](http://msdn.microsoft.com/de-de/library/dd835506%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5e323-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](http://msdn.microsoft.com/de-de/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="5e323-115">Die Exchange-Verwaltungsshell-Cmdlets annehmen und Zurückgeben von Objekten.</span><span class="sxs-lookup"><span data-stu-id="5e323-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="5e323-116">Eine Liste der Exchange-Verwaltungsshell-Cmdlets und ihre Eingabe- und Typen finden Sie unter [Exchange-Verwaltungsshell-Cmdlet ein- und Ausgabe Typen](exchange-management-shell-cmdlet-input-and-output-types.md).</span><span class="sxs-lookup"><span data-stu-id="5e323-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5e323-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="5e323-117">In this section</span></span>

- [<span data-ttu-id="5e323-118">Neue und aktualisierte Exchange-Verwaltungsshell-cmdlets</span><span class="sxs-lookup"><span data-stu-id="5e323-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="5e323-119">Exchange-Verwaltungsshell Eingabe- und Ausgabedateien Typen</span><span class="sxs-lookup"><span data-stu-id="5e323-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="5e323-120">Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="5e323-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="5e323-121">Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort</span><span class="sxs-lookup"><span data-stu-id="5e323-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="5e323-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e323-122">See also</span></span>

- [<span data-ttu-id="5e323-123">Exchange-Verwaltungsshell-namespaces</span><span class="sxs-lookup"><span data-stu-id="5e323-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="5e323-124">Exchange Server-PowerShell (Exchange-Verwaltungsshell)</span><span class="sxs-lookup"><span data-stu-id="5e323-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/de-de/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="5e323-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5e323-125">Windows PowerShell</span></span>](http://msdn.microsoft.com/de-de/library/dd835506%28v=vs.85%29.aspx)
    

