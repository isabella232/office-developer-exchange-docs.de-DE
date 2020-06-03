---
title: Erstellen von Exchange-Verwaltungsshell Tools
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46e4812f-37a8-449f-bd37-bc4a94605db9
description: Hier finden Sie Informationen zu den ersten Schritten beim Erstellen von Exchange-Verwaltungsshell Tools für Exchange.
ms.openlocfilehash: c6e11fa5b55aa514b12f4f52bc9346ac213d3781
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463727"
---
# <a name="create-exchange-management-shell-tools"></a><span data-ttu-id="02585-103">Erstellen von Exchange-Verwaltungsshell Tools</span><span class="sxs-lookup"><span data-stu-id="02585-103">Create Exchange Management Shell tools</span></span>

<span data-ttu-id="02585-104">Hier finden Sie Informationen zu den ersten Schritten beim Erstellen von Exchange-Verwaltungsshell Tools für Exchange.</span><span class="sxs-lookup"><span data-stu-id="02585-104">Find information to get started creating Exchange Management Shell tools for Exchange.</span></span>

<span data-ttu-id="02585-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="02585-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="02585-106">Das Exchange-Verwaltungsshell bietet eine umfangreiche Reihe von Befehlen auf der Grundlage der Windows PowerShell Plattform zum Verwalten von Exchange Online, Exchange Online im Rahmen von Office 365 oder einer lokalen Exchange-Version, die mit Exchange 2013 beginnt.</span><span class="sxs-lookup"><span data-stu-id="02585-106">The Exchange Management Shell provides a rich set of commands, based on the Windows PowerShell platform, for managing Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange starting with Exchange 2013.</span></span> <span data-ttu-id="02585-107">Sie können Exchange-Verwaltungsshell Befehle verwenden, um die Verwaltung eines Servers zu automatisieren, indem Sie die Befehle direkt ausführen oder Befehlsskripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="02585-107">You can use Exchange Management Shell commands to automate the administration of a server by directly executing the commands, or by using command scripts.</span></span>
  
<span data-ttu-id="02585-108">Wenn Sie Exchange-Verwaltungsshell Befehle aus einer Hostanwendung wie einer Verwaltungsanwendung, die auf dem Desktop des Administrators oder über eine webbasierte Anwendung läuft, verwenden möchten, können Sie Exchange-Verwaltungsshell-Cmdlets in der Visual Basic-oder C#-Anwendung aufrufen, um einen Exchange-Server zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="02585-108">If you need to use Exchange Management Shell commands from within a hosting application, such as an administrative application that is running on the administrator's desktop or through a web-based application, you can call Exchange Management Shell cmdlets from within your Visual Basic or C# application to manage an Exchange server.</span></span>
  
## <a name="get-started-with-exchange-management-shell-tools"></a><span data-ttu-id="02585-109">Erste Schritte mit Exchange-Verwaltungsshell Tools</span><span class="sxs-lookup"><span data-stu-id="02585-109">Get started with Exchange Management Shell tools</span></span>
<span data-ttu-id="02585-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span><span class="sxs-lookup"><span data-stu-id="02585-110"><a name="SP15GettingStartedTemplate_WhatDoYouNeed"> </a></span></span>

<span data-ttu-id="02585-111">Wenn Sie mit dem Erstellen Windows PowerShell Hostanwendungen vertraut sind und ein Beispiel sehen möchten, das zeigt, wie die Exchange-Verwaltungsshell-Cmdlets aus einer Anwendung aufgerufen werden, oder um ein Beispiel für die Typen von Anwendungen anzuzeigen, die Sie mithilfe der Exchange-Verwaltungsshell-Cmdlets erstellen können, lesen Sie [Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="02585-111">If you are familiar with creating Windows PowerShell host applications and want to see an example that shows how to call the Exchange Management Shell cmdlets from an application, or to see an example of the types of applications that you can create by using the Exchange Management Shell cmdlets, see [Get a list of mail users by using the Exchange Management Shell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md).</span></span>
  
<span data-ttu-id="02585-112">Die Exchange-Verwaltungsshell-Cmdlets sind Erweiterungen für Windows PowerShell, eine aufgabenbasierte Befehlszeilen-Shell und Skriptsprache, die speziell für die Systemverwaltung entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="02585-112">The Exchange Management Shell cmdlets are extensions to Windows PowerShell, a task-based command-line shell and scripting language that is designed specifically for system administration.</span></span> <span data-ttu-id="02585-113">Windows PowerShell baut auf dem .NET Framework auf und stellt eine objektorientierte API für Cmdlet-, Anbieter-und Host Anwendungsentwickler bereit.</span><span class="sxs-lookup"><span data-stu-id="02585-113">Windows PowerShell is built on the .NET Framework, and provides an object-oriented API for cmdlet, provider, and host application developers.</span></span> <span data-ttu-id="02585-114">Weitere Informationen zur Windows PowerShell Programmierung finden Sie im [Windows PowerShell SDK](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="02585-114">To learn about Windows PowerShell programming, see the [Windows PowerShell SDK](https://msdn.microsoft.com/library/dd835506%28VS.85%29.aspx).</span></span>
  
<span data-ttu-id="02585-115">Die Exchange-Verwaltungsshell-Cmdlets akzeptieren und geben Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="02585-115">The Exchange Management Shell cmdlets accept and return objects.</span></span> <span data-ttu-id="02585-116">Eine Liste der Cmdlets der Exchange-Verwaltungsshell und deren Eingabe-und Ausgabetypen finden Sie unter [Exchange-Verwaltungsshell Cmdlet Input and Output Types](exchange-management-shell-cmdlet-input-and-output-types.md).</span><span class="sxs-lookup"><span data-stu-id="02585-116">For a list of Exchange management shell cmdlets and their input and output types, see [Exchange Management Shell cmdlet input and output types](exchange-management-shell-cmdlet-input-and-output-types.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="02585-117">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="02585-117">In this section</span></span>

- [<span data-ttu-id="02585-118">Neue und aktualisierte Exchange-Verwaltungsshell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="02585-118">New and updated Exchange Management Shell cmdlets</span></span>](new-and-updated-exchange-management-shell-cmdlets.md)  
- [<span data-ttu-id="02585-119">Eingabe- und Ausgabetypen für Cmdlets der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="02585-119">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
- [<span data-ttu-id="02585-120">Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="02585-120">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
- [<span data-ttu-id="02585-121">Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="02585-121">Use the Exchange Management Shell cmdlet response</span></span>](how-to-use-the-exchange-management-shell-cmdlet-response.md)


## <a name="see-also"></a><span data-ttu-id="02585-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02585-122">See also</span></span>

- [<span data-ttu-id="02585-123">Exchange-Verwaltungsshell Namespaces</span><span class="sxs-lookup"><span data-stu-id="02585-123">Exchange Management Shell namespaces</span></span>](exchange-management-shell-namespaces.md)  
- [<span data-ttu-id="02585-124">Exchange Server-PowerShell (Exchange-Verwaltungsshell)</span><span class="sxs-lookup"><span data-stu-id="02585-124">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)  
- [<span data-ttu-id="02585-125">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="02585-125">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

