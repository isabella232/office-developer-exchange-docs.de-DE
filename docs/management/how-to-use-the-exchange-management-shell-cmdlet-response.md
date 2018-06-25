---
title: Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Erfahren Sie, wie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in der verwalteten Exchange-Anwendung verwenden.
ms.openlocfilehash: 5edf75afd556f67e815bc519c87586f2f62f057b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757136"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a><span data-ttu-id="d171d-103">Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort</span><span class="sxs-lookup"><span data-stu-id="d171d-103">Use the Exchange Management Shell cmdlet response</span></span>

<span data-ttu-id="d171d-104">Erfahren Sie, wie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in der verwalteten Exchange-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d171d-104">Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application.</span></span>
  
<span data-ttu-id="d171d-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="d171d-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="d171d-106">Jede Exchange-Verwaltungsshell-Cmdlet gibt eine oder mehrere [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) -Instanzen, die eine konsistente Ansicht eines Objekts in der Exchange-Verwaltungsshell-Umgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d171d-106">Each Exchange Management Shell cmdlet returns one or more [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) instances that provide a consistent view of any object in the Exchange Management Shell environment.</span></span> <span data-ttu-id="d171d-107">Dieser Artikel enthält Informationen dazu, wie Sie die Eigenschaften einer Instanz **PSObject** verwenden, um die Eigenschaftswerte des zugrunde liegenden Exchange Server 2013-API-Objekts zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d171d-107">This article provides information about how to use the properties of a **PSObject** instance to return the property values of the underlying Exchange Server 2013 API object.</span></span> 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a><span data-ttu-id="d171d-108">Voraussetzung für die Verwendung von Cmdlets Antworten</span><span class="sxs-lookup"><span data-stu-id="d171d-108">Prerequisites for using cmdlet responses</span></span>
<span data-ttu-id="d171d-109"><a name="prerequisites_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d171d-109"></span></span>

<span data-ttu-id="d171d-110">Um Cmdlet Antworten zu verwenden, benötigen Sie einen Verweis auf den **System.Automation.Management** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="d171d-110">To use cmdlet responses, you need a reference to the **System.Automation.Management** namespace.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="d171d-111">Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die Assembly System.Mangagement.Automation.dll hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d171d-111">When you are using Visual Studio to create an application, you must add a reference to the System.Mangagement.Automation.dll assembly to the project.</span></span> <span data-ttu-id="d171d-112">Die Assembly finden Sie in einem der folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="d171d-112">You can find the assembly in one of the following locations:</span></span> 
> - <span data-ttu-id="d171d-113">Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME)</span><span class="sxs-lookup"><span data-stu-id="d171d-113">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span> 
> - <span data-ttu-id="d171d-114">Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation</span><span class="sxs-lookup"><span data-stu-id="d171d-114">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
## <a name="windows-powershell-remote-runspace"></a><span data-ttu-id="d171d-115">Remote Windows PowerShell-runspace</span><span class="sxs-lookup"><span data-stu-id="d171d-115">Windows PowerShell remote runspace</span></span>
<span data-ttu-id="d171d-116"><a name="usingremoterunspace_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d171d-116"></span></span>

<span data-ttu-id="d171d-117">Die Exchange-Verwaltungsshell verwendet remote Windows PowerShell-Features für alle Befehle, sogar, die auf dem lokalen Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d171d-117">The Exchange Management Shell uses remote Windows PowerShell features for all commands, even commands that are run on the local server.</span></span> <span data-ttu-id="d171d-118">Infolgedessen serialisiert alle Antworten von den Exchange-Verwaltungsshell-Cmdlets sind XML.</span><span class="sxs-lookup"><span data-stu-id="d171d-118">As a result, all responses from Exchange Management Shell cmdlets are serialized XML.</span></span> <span data-ttu-id="d171d-119">Dies bedeutet, dass zwar das Antwortobjekt den Exchange-Objekttyp, der zum Generieren der Antwort verwendet wurde angibt, im Response-Objekt in der Exchange-Objekttyp umgewandelt werden kann. Stattdessen müssen Sie den Eigenschaftenbehälter verwenden, der von der Response-Objekt zum Abrufen der Werte aus den Exchange-Objekttyp verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d171d-119">This means that although the response object indicates the Exchange object type that was used to generate the response, the response object cannot be cast to the Exchange object type; instead, you must use the property bag that is exposed by the response object to obtain the values from the Exchange object type.</span></span>
  
<span data-ttu-id="d171d-120">Die Eigenschaftensammlung im Response-Objekt enthält Schlüssel/Wert-Paar für jeden öffentliche Eigenschaft oder Methode in der Exchange-Objekttyp an.</span><span class="sxs-lookup"><span data-stu-id="d171d-120">The property bag in the response object contains a key/value pair for each public property or method in the Exchange object type.</span></span> <span data-ttu-id="d171d-121">Response-Objekt enthält den Namen des zugrunde liegenden Exchange Objekttyps; Dieser Name können Sie um den Exchange-Objekttyp zu bestimmen, der durch das Response-Objekt dargestellt wird, damit Sie die entsprechende Eigenschaft extrahieren können.</span><span class="sxs-lookup"><span data-stu-id="d171d-121">The response object contains the name of the underlying Exchange object type; you can use this name to determine the Exchange object type that is represented by the response object so that you can extract the appropriate property.</span></span> <span data-ttu-id="d171d-122">Jeder Wert in der Eigenschaftensammlung enthält auch Typinformationen, sodass der Wert der Eigenschaft in den entsprechenden verwalteten Typ umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d171d-122">Each value in the property bag also includes type information so that you can cast the property value to the appropriate managed type.</span></span>
  
## <a name="use-the-cmdlet-response"></a><span data-ttu-id="d171d-123">Verwenden Sie die Cmdlet-Antwort</span><span class="sxs-lookup"><span data-stu-id="d171d-123">Use the cmdlet response</span></span>
<span data-ttu-id="d171d-124"><a name="usingPSObject_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="d171d-124"></span></span>

<span data-ttu-id="d171d-125">Die [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) -Klasse bietet die folgenden drei öffentlichen Eigenschaften mit den Werten des zugrunde liegenden Objekts Exchange 2013-API: [Eigenschaften](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methoden](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.methods%28VS.85%29.aspx)und [Mitglieder](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d171d-125">The [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) class exposes the following three public properties that contain the values of the underlying Exchange 2013 API object: [Properties](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.methods%28VS.85%29.aspx), and [Members](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span></span> <span data-ttu-id="d171d-126">Jede Eigenschaft, die durch das Exchange 2013-API-Objekt verfügbar gemacht wird hat einen entsprechenden Schlüssel/Wert-Paar in den Eigenschaften **Eigenschaften** und **Mitglieder** an.</span><span class="sxs-lookup"><span data-stu-id="d171d-126">Each property that is exposed by the Exchange 2013 API object has a corresponding key/value pair in the **Properties** and **Members** properties.</span></span> <span data-ttu-id="d171d-127">Die Anwendung kann die **Properties** -Auflistung durch den Namen einer Eigenschaft zum Abrufen des Werts der Eigenschaft indizieren.</span><span class="sxs-lookup"><span data-stu-id="d171d-127">Your application can index the **Properties** collection by the name of a property to retrieve the value of the property.</span></span> 
  
<span data-ttu-id="d171d-128">Die **TypeNames** -Eigenschaft der Instanz **PSObject** können Sie um den Typ des zugrunde liegenden Exchange-Objekts zu ermitteln, die von der Instanz **PSObject** gekapselte ist.</span><span class="sxs-lookup"><span data-stu-id="d171d-128">You can use the **TypeNames** property of the **PSObject** instance to determine the type of the underlying Exchange object that is encapsulated by the **PSObject** instance.</span></span> <span data-ttu-id="d171d-129">Die **TypeNames** -Eigenschaft ist eine Auflistung von Zeichenfolgen, die die Objekthierarchie des dargestellte Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="d171d-129">The **TypeNames** property is a collection of strings that contains the object hierarchy of the represented type.</span></span> <span data-ttu-id="d171d-130">Diese Namen können Sie um das Objekt zu bestimmen, das von der Instanz **PSObject** dargestellt wird, damit Sie die entsprechende Eigenschaft extrahieren können.</span><span class="sxs-lookup"><span data-stu-id="d171d-130">You can use these names to determine the object that is represented by the **PSObject** instance so that you can extract the appropriate property.</span></span> 
  
<span data-ttu-id="d171d-131">Im folgenden Codebeispiel wird die Cmdlet-Antwort zum Drucken des Inhalts der **Properties** -Auflistung einer **PSObject** -Instanz in der Konsole verwendet.</span><span class="sxs-lookup"><span data-stu-id="d171d-131">The following code example uses the cmdlet response to print the contents of the **Properties** collection of a **PSObject** instance on the console.</span></span> <span data-ttu-id="d171d-132">Das Codebeispiel erfordert einen Verweis auf den **System.Automation.Management** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="d171d-132">The code example requires a reference to the **System.Automation.Management** namespace.</span></span> 
  
```cs
foreach (PSPropertyInfo propertyInfo in psObject.Properties)
{
    Console.WriteLine(string.Format("{0}: {1}",
        propertyInfo.Name, propertyInfo.Value);
}
```

<br/>

```vb
For Each PropertyInfo As PSProperty In ObjectInfo.Properties
    Console.WriteLine(String.Format("{0}: {1}", PropertyInfo.Name, PropertyInfo.Value))
Next

```

## <a name="see-also"></a><span data-ttu-id="d171d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d171d-133">See also</span></span>

- [<span data-ttu-id="d171d-134">Erstellen von Exchange-Verwaltungsshell-tools</span><span class="sxs-lookup"><span data-stu-id="d171d-134">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="d171d-135">Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="d171d-135">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

