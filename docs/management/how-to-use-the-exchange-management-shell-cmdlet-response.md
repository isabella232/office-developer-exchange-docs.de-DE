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
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Verwenden Sie die Exchange-Verwaltungsshell-Cmdlet-Antwort

Erfahren Sie, wie die Antwort von einem Exchange-Verwaltungsshell-Cmdlet in der verwalteten Exchange-Anwendung verwenden.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Jede Exchange-Verwaltungsshell-Cmdlet gibt eine oder mehrere [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) -Instanzen, die eine konsistente Ansicht eines Objekts in der Exchange-Verwaltungsshell-Umgebung bereitstellen. Dieser Artikel enthält Informationen dazu, wie Sie die Eigenschaften einer Instanz **PSObject** verwenden, um die Eigenschaftswerte des zugrunde liegenden Exchange Server 2013-API-Objekts zurückzugeben. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Voraussetzung für die Verwendung von Cmdlets Antworten
<a name="prerequisites_bk"> </a>

Um Cmdlet Antworten zu verwenden, benötigen Sie einen Verweis auf den **System.Automation.Management** -Namespace. 
  
> [!NOTE]
>  Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die Assembly System.Mangagement.Automation.dll hinzufügen. Die Assembly finden Sie in einem der folgenden Speicherorte: 
> - Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME) 
> - Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation 
  
## <a name="windows-powershell-remote-runspace"></a>Remote Windows PowerShell-runspace
<a name="usingremoterunspace_bk"> </a>

Die Exchange-Verwaltungsshell verwendet remote Windows PowerShell-Features für alle Befehle, sogar, die auf dem lokalen Server ausgeführt werden. Infolgedessen serialisiert alle Antworten von den Exchange-Verwaltungsshell-Cmdlets sind XML. Dies bedeutet, dass zwar das Antwortobjekt den Exchange-Objekttyp, der zum Generieren der Antwort verwendet wurde angibt, im Response-Objekt in der Exchange-Objekttyp umgewandelt werden kann. Stattdessen müssen Sie den Eigenschaftenbehälter verwenden, der von der Response-Objekt zum Abrufen der Werte aus den Exchange-Objekttyp verfügbar gemacht wird.
  
Die Eigenschaftensammlung im Response-Objekt enthält Schlüssel/Wert-Paar für jeden öffentliche Eigenschaft oder Methode in der Exchange-Objekttyp an. Response-Objekt enthält den Namen des zugrunde liegenden Exchange Objekttyps; Dieser Name können Sie um den Exchange-Objekttyp zu bestimmen, der durch das Response-Objekt dargestellt wird, damit Sie die entsprechende Eigenschaft extrahieren können. Jeder Wert in der Eigenschaftensammlung enthält auch Typinformationen, sodass der Wert der Eigenschaft in den entsprechenden verwalteten Typ umgewandelt werden kann.
  
## <a name="use-the-cmdlet-response"></a>Verwenden Sie die Cmdlet-Antwort
<a name="usingPSObject_bk"> </a>

Die [PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx) -Klasse bietet die folgenden drei öffentlichen Eigenschaften mit den Werten des zugrunde liegenden Objekts Exchange 2013-API: [Eigenschaften](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methoden](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.methods%28VS.85%29.aspx)und [Mitglieder](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.members%28VS.85%29.aspx). Jede Eigenschaft, die durch das Exchange 2013-API-Objekt verfügbar gemacht wird hat einen entsprechenden Schlüssel/Wert-Paar in den Eigenschaften **Eigenschaften** und **Mitglieder** an. Die Anwendung kann die **Properties** -Auflistung durch den Namen einer Eigenschaft zum Abrufen des Werts der Eigenschaft indizieren. 
  
Die **TypeNames** -Eigenschaft der Instanz **PSObject** können Sie um den Typ des zugrunde liegenden Exchange-Objekts zu ermitteln, die von der Instanz **PSObject** gekapselte ist. Die **TypeNames** -Eigenschaft ist eine Auflistung von Zeichenfolgen, die die Objekthierarchie des dargestellte Typs enthält. Diese Namen können Sie um das Objekt zu bestimmen, das von der Instanz **PSObject** dargestellt wird, damit Sie die entsprechende Eigenschaft extrahieren können. 
  
Im folgenden Codebeispiel wird die Cmdlet-Antwort zum Drucken des Inhalts der **Properties** -Auflistung einer **PSObject** -Instanz in der Konsole verwendet. Das Codebeispiel erfordert einen Verweis auf den **System.Automation.Management** -Namespace. 
  
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

## <a name="see-also"></a>Siehe auch

- [Erstellen von Exchange-Verwaltungsshell-tools](create-exchange-management-shell-tools.md)   
- [Abrufen einer Liste von e-Mail-Benutzer mithilfe der Exchange-Verwaltungsshell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

