---
title: Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: Hier erfahren Sie, wie Sie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in Ihrer verwalteten Exchange-Anwendung verwenden.
ms.openlocfilehash: c1b81356ab5dc288ab08287d47581871c36beb05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435702"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a><span data-ttu-id="94496-103">Verwenden der Antwort des Exchange-Verwaltungsshell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="94496-103">Use the Exchange Management Shell cmdlet response</span></span>

<span data-ttu-id="94496-104">Hier erfahren Sie, wie Sie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in Ihrer verwalteten Exchange-Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="94496-104">Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application.</span></span>
  
<span data-ttu-id="94496-105">**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365</span><span class="sxs-lookup"><span data-stu-id="94496-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="94496-106">Jedes Exchange-Verwaltungsshell-Cmdlet gibt eine oder mehrere [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) -Instanzen zurück, die eine konsistente Ansicht eines beliebigen Objekts in der Exchange-Verwaltungsshell-Umgebung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="94496-106">Each Exchange Management Shell cmdlet returns one or more [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) instances that provide a consistent view of any object in the Exchange Management Shell environment.</span></span> <span data-ttu-id="94496-107">Dieser Artikel enthält Informationen zum Verwenden der Eigenschaften einer **PSObject** -Instanz, um die Eigenschaftswerte des zugrunde liegenden Exchange Server 2013-API-Objekts zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="94496-107">This article provides information about how to use the properties of a **PSObject** instance to return the property values of the underlying Exchange Server 2013 API object.</span></span> 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a><span data-ttu-id="94496-108">Voraussetzungen für die Verwendung von Cmdlet-Antworten</span><span class="sxs-lookup"><span data-stu-id="94496-108">Prerequisites for using cmdlet responses</span></span>
<span data-ttu-id="94496-109"><a name="prerequisites_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="94496-109"><a name="prerequisites_bk"> </a></span></span>

<span data-ttu-id="94496-110">Um Cmdlet-Antworten verwenden zu können, benötigen Sie einen Verweis auf den **System. Automation. Management** -Namespace.</span><span class="sxs-lookup"><span data-stu-id="94496-110">To use cmdlet responses, you need a reference to the **System.Automation.Management** namespace.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="94496-111">Wenn Sie Visual Studio verwenden, um eine Anwendung zu erstellen, müssen Sie dem Projekt einen Verweis auf die Assembly System. Mangagement. Automation. dll hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="94496-111">When you are using Visual Studio to create an application, you must add a reference to the System.Mangagement.Automation.dll assembly to the project.</span></span> <span data-ttu-id="94496-112">Sie können die Assembly in einem der folgenden Speicherorte finden:</span><span class="sxs-lookup"><span data-stu-id="94496-112">You can find the assembly in one of the following locations:</span></span> 
> - <span data-ttu-id="94496-113">Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME)</span><span class="sxs-lookup"><span data-stu-id="94496-113">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span> 
> - <span data-ttu-id="94496-114">Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation</span><span class="sxs-lookup"><span data-stu-id="94496-114">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
## <a name="windows-powershell-remote-runspace"></a><span data-ttu-id="94496-115">Windows PowerShell Remote Remoterunspace</span><span class="sxs-lookup"><span data-stu-id="94496-115">Windows PowerShell remote runspace</span></span>
<span data-ttu-id="94496-116"><a name="usingremoterunspace_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="94496-116"><a name="usingremoterunspace_bk"> </a></span></span>

<span data-ttu-id="94496-117">Der Exchange-Verwaltungsshell verwendet Remote Windows PowerShell Funktionen für alle Befehle, sogar für Befehle, die auf dem lokalen Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="94496-117">The Exchange Management Shell uses remote Windows PowerShell features for all commands, even commands that are run on the local server.</span></span> <span data-ttu-id="94496-118">Daher werden alle Antworten von Exchange-Verwaltungsshell-Cmdlets serialisiert.</span><span class="sxs-lookup"><span data-stu-id="94496-118">As a result, all responses from Exchange Management Shell cmdlets are serialized XML.</span></span> <span data-ttu-id="94496-119">Dies bedeutet, dass das Response-Objekt nicht in den Exchange-Objekttyp umgewandelt werden kann, obwohl das Response-Objekt den Exchange-Objekttyp angibt, der zum Generieren der Antwort verwendet wurde. Stattdessen müssen Sie den Eigenschaftenbehälter verwenden, der vom Response-Objekt verfügbar gemacht wird, um die Werte aus dem Exchange-Objekttyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="94496-119">This means that although the response object indicates the Exchange object type that was used to generate the response, the response object cannot be cast to the Exchange object type; instead, you must use the property bag that is exposed by the response object to obtain the values from the Exchange object type.</span></span>
  
<span data-ttu-id="94496-120">Der Eigenschaftenbehälter im Response-Objekt enthält ein Schlüssel/Wert-Paar für jede öffentliche Eigenschaft oder Methode im Exchange-Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="94496-120">The property bag in the response object contains a key/value pair for each public property or method in the Exchange object type.</span></span> <span data-ttu-id="94496-121">Das Response-Objekt enthält den Namen des zugrunde liegenden Exchange-Objekttyps; Sie können diesen Namen verwenden, um den Exchange-Objekttyp zu ermitteln, der durch das Response-Objekt dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können.</span><span class="sxs-lookup"><span data-stu-id="94496-121">The response object contains the name of the underlying Exchange object type; you can use this name to determine the Exchange object type that is represented by the response object so that you can extract the appropriate property.</span></span> <span data-ttu-id="94496-122">Jeder Wert im Eigenschaftenbehälter enthält auch Typinformationen, sodass Sie den Eigenschaftswert in den entsprechenden verwalteten Typ umwandeln können.</span><span class="sxs-lookup"><span data-stu-id="94496-122">Each value in the property bag also includes type information so that you can cast the property value to the appropriate managed type.</span></span>
  
## <a name="use-the-cmdlet-response"></a><span data-ttu-id="94496-123">Verwenden der Cmdlet-Antwort</span><span class="sxs-lookup"><span data-stu-id="94496-123">Use the cmdlet response</span></span>
<span data-ttu-id="94496-124"><a name="usingPSObject_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="94496-124"><a name="usingPSObject_bk"> </a></span></span>

<span data-ttu-id="94496-125">Die [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) -Klasse macht die folgenden drei öffentlichen Eigenschaften verfügbar, die die Werte des zugrunde liegenden Exchange 2013-API-Objekts enthalten: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)und [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="94496-125">The [PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) class exposes the following three public properties that contain the values of the underlying Exchange 2013 API object: [Properties](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx), and [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span></span> <span data-ttu-id="94496-126">Jede Eigenschaft, die vom Exchange 2013-API-Objekt verfügbar gemacht wird, verfügt über ein entsprechendes Schlüssel/Wert-Paar in den Eigenschaften **Properties** und **Members** .</span><span class="sxs-lookup"><span data-stu-id="94496-126">Each property that is exposed by the Exchange 2013 API object has a corresponding key/value pair in the **Properties** and **Members** properties.</span></span> <span data-ttu-id="94496-127">Ihre Anwendung kann die **Properties** -Auflistung nach dem Namen einer Eigenschaft indizieren, um den Wert der Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94496-127">Your application can index the **Properties** collection by the name of a property to retrieve the value of the property.</span></span> 
  
<span data-ttu-id="94496-128">Sie können die **typeNames** -Eigenschaft der **PSObject** -Instanz verwenden, um den Typ des zugrunde liegenden Exchange-Objekts zu ermitteln, das von der **PSObject** -Instanz gekapselt wird.</span><span class="sxs-lookup"><span data-stu-id="94496-128">You can use the **TypeNames** property of the **PSObject** instance to determine the type of the underlying Exchange object that is encapsulated by the **PSObject** instance.</span></span> <span data-ttu-id="94496-129">Die **typeNames** -Eigenschaft ist eine Auflistung von Zeichenfolgen, die die Objekthierarchie des dargestellten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="94496-129">The **TypeNames** property is a collection of strings that contains the object hierarchy of the represented type.</span></span> <span data-ttu-id="94496-130">Sie können diese Namen verwenden, um das Objekt zu bestimmen, das durch die **PSObject** -Instanz dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können.</span><span class="sxs-lookup"><span data-stu-id="94496-130">You can use these names to determine the object that is represented by the **PSObject** instance so that you can extract the appropriate property.</span></span> 
  
<span data-ttu-id="94496-131">Im folgenden Codebeispiel wird die Cmdlet-Antwort verwendet, um den Inhalt der **Properties** -Auflistung einer **PSObject** -Instanz in der Konsole zu drucken.</span><span class="sxs-lookup"><span data-stu-id="94496-131">The following code example uses the cmdlet response to print the contents of the **Properties** collection of a **PSObject** instance on the console.</span></span> <span data-ttu-id="94496-132">Für das Codebeispiel ist ein Verweis auf den **System. Automation. Management** -Namespace erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94496-132">The code example requires a reference to the **System.Automation.Management** namespace.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="94496-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94496-133">See also</span></span>

- [<span data-ttu-id="94496-134">Erstellen von Exchange-Verwaltungsshell Tools</span><span class="sxs-lookup"><span data-stu-id="94496-134">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="94496-135">Abrufen einer Liste von e-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="94496-135">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

