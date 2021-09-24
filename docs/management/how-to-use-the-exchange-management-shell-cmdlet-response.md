---
title: Verwenden der Cmdlet-Antwort Exchange Verwaltungsshell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: In diesem Artikel erfahren Sie, wie Sie die Antwort eines Cmdlets Exchange Verwaltungsshell in Ihrer Exchange verwalteten Anwendung verwenden.
ms.openlocfilehash: be66be31e435be1553eba16d8f367a79317618f2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520963"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>Verwenden der Cmdlet-Antwort Exchange Verwaltungsshell

In diesem Artikel erfahren Sie, wie Sie die Antwort eines Cmdlets Exchange Verwaltungsshell in Ihrer Exchange verwalteten Anwendung verwenden.
  
**Gilt für:** Exchange Online | Exchange Server 2013 | Office 365
  
Jedes Cmdlet der Exchange Verwaltungsshell gibt eine oder mehrere [PSObject-Instanzen](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) zurück, die eine konsistente Ansicht aller Objekte in der Exchange Verwaltungsshell-Umgebung bereitstellen. Dieser Artikel enthält Informationen zum Verwenden der Eigenschaften einer **PSObject-Instanz,** um die Eigenschaftswerte des zugrunde liegenden Exchange Server 2013-API-Objekts zurückzugeben. 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>Voraussetzungen für die Verwendung von Cmdlet-Antworten
<a name="prerequisites_bk"> </a>

Um Cmdlet-Antworten zu verwenden, benötigen Sie einen Verweis auf den **System.Automation.Management-Namespace.** 
  
> [!NOTE]
>  Wenn Sie Visual Studio zum Erstellen einer Anwendung verwenden, müssen Sie dem Projekt einen Verweis auf die System.Mangagement.Automation.dll assembly hinzufügen. Sie finden die Assembly an einem der folgenden Speicherorte: 
> - Für die Betriebssysteme Windows XP und Windows Vista im Windows PowerShell-Installationsverzeichnis ($PSHOME) 
> - Für die Betriebssysteme Windows 7 und Windows 8 im folgenden Ordner: Windows\assembly\GAC_MSIL\System.Management.Automation 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell Remoterunspace
<a name="usingremoterunspace_bk"> </a>

Die Exchange Verwaltungsshell verwendet Remote-Windows PowerShell-Features für alle Befehle, auch für Befehle, die auf dem lokalen Server ausgeführt werden. Daher werden alle Antworten von Exchange Verwaltungsshell-Cmdlets in XML serialisiert. Dies bedeutet, dass das Antwortobjekt zwar den Exchange Objekttyp angibt, der zum Generieren der Antwort verwendet wurde, das Antwortobjekt jedoch nicht in den Exchange Objekttyp umgewandelt werden kann. Stattdessen müssen Sie den Eigenschaftenbehälter verwenden, der vom Antwortobjekt verfügbar gemacht wird, um die Werte aus dem Exchange Objekttyp abzurufen.
  
Der Eigenschaftenbehälter im Antwortobjekt enthält ein Schlüssel-Wert-Paar für jede öffentliche Eigenschaft oder Methode im Exchange Objekttyp. Das Antwortobjekt enthält den Namen des zugrunde liegenden Exchange Objekttyps; Sie können diesen Namen verwenden, um den Exchange Objekttyp zu bestimmen, der durch das Antwortobjekt dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können. Jeder Wert im Eigenschaftenbehälter enthält auch Typinformationen, sodass Sie den Eigenschaftswert in den entsprechenden verwalteten Typ umwandeln können.
  
## <a name="use-the-cmdlet-response"></a>Verwenden der Cmdlet-Antwort
<a name="usingPSObject_bk"> </a>

Die [PSObject-Klasse](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx) macht die folgenden drei öffentlichen Eigenschaften verfügbar, die die Werte des zugrunde liegenden Exchange 2013-API-Objekts enthalten: [Eigenschaften,](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx) [Methoden](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)und [Member.](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx) Jede Eigenschaft, die vom Exchange 2013-API-Objekt verfügbar gemacht wird, weist ein entsprechendes Schlüssel-Wert-Paar in den Eigenschaften **"Properties"** und **"Members"** auf. Ihre Anwendung kann die **Properties-Auflistung** anhand des Namens einer Eigenschaft indizieren, um den Wert der Eigenschaft abzurufen. 
  
Mit der **TypeNames-Eigenschaft** der **PSObject-Instanz** können Sie den Typ des zugrunde liegenden Exchange objekts bestimmen, das von der **PSObject-Instanz** gekapselt wird. Die **TypeNames-Eigenschaft** ist eine Auflistung von Zeichenfolgen, die die Objekthierarchie des dargestellten Typs enthält. Sie können diese Namen verwenden, um das Objekt zu bestimmen, das von der **PSObject-Instanz** dargestellt wird, sodass Sie die entsprechende Eigenschaft extrahieren können. 
  
Im folgenden Codebeispiel wird die Cmdlet-Antwort verwendet, um den Inhalt der **Properties-Auflistung** einer **PSObject-Instanz** auf der Konsole zu drucken. Das Codebeispiel erfordert einen Verweis auf den **System.Automation.Management-Namespace.** 
  
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

- [Erstellen von Exchange-Verwaltungsshell-Tools](create-exchange-management-shell-tools.md)   
- [Abrufen einer Liste von E-Mail-Benutzern mithilfe der Exchange-Verwaltungsshell](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

