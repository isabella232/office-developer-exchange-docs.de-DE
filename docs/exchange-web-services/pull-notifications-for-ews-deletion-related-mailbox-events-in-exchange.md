---
title: Ziehen Sie Benachrichtigungen für EWS Postfach löschen-bezogenen Ereignisse in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Erfahren Sie, welche Postfach Ereignisse ausgelöst werden, wenn Elemente im Exchange mithilfe der Exchange-Webdienste zu löschen.
ms.openlocfilehash: b12d6a16cc539f36b6b4dcd7274529e9def3c247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757122"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Ziehen Sie Benachrichtigungen für EWS Postfach löschen-bezogenen Ereignisse in Exchange

Erfahren Sie, welche Postfach Ereignisse ausgelöst werden, wenn Elemente im Exchange mithilfe der Exchange-Webdienste zu löschen.
  
Wenn Sie die [Elemente und Ordner von einem Postfach löschen](deleting-items-by-using-ews-in-exchange.md), dadurch wird ein Postfach-Ereignis. Verschiedene Versionen von Exchange zurückgeben anderes Postfach Ereignisse Reaktion auf Änderungen auf Elemente und Ordner in einem Postfach. Die folgende Tabelle zeigt die Postfach-Ereignisse, die für Löschvorgänge zurückgegeben werden, wenn Sie Pull Benachrichtigungen zum Abonnieren von Ereignissen Postfach verwenden. 
  
**Tabelle 1: Postfach löschen-bezogenen Ereignisse für Pull-Benachrichtigungen**

|**Typ der Löschvorgang und die EWS-Vorgang**|**Exchange 2010-Benachrichtigung, wenn Sie angeben, dass jeder Ordner-ID**|**Exchange 2010-Benachrichtigung, wenn Sie alle Ordner angeben**|**Exchange Online und Exchange 2013-Benachrichtigung, wenn Sie angeben, dass jeder Ordner-ID**|**Exchange Online und Exchange 2013, wenn Sie alle Ordner angeben**|
|:-----|:-----|:-----|:-----|:-----|
|Über den [Vorgang DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) vorläufiges löschen <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |MovedEvent für das Element. Dies gibt an, die alte und neue übergeordnete Ordner Bezeichner. Das Element wird in den Ordner Löschvorgänge verschoben die Dumpster.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem Standardordner Suche alle Artikel.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |
|Über den [Vorgang DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) schwerer löschen <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem Standardordner Suche alle Artikel.  <br/> ModifiedEvent für das Element übergeordneten Ordner.  <br/> |
|Verschieben Sie in den Ordner Gelöschte Objekte über den [DeleteItem-Vorgang](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent für das Element. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für das Element alten übergeordneten Ordner.  <br/> ModifiedEvent für das Element neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |MovedEvent für das Element. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für das Element alten übergeordneten Ordner.  <br/> ModifiedEvent für das Element neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |MovedEvent für das Element. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für das Element alten übergeordneten Ordner.  <br/> ModifiedEvent für das Element neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |DeletedEvent aus dem Standardordner Suche alle Artikel.  <br/> CreatedEvent für das Element im Ordner alle Artikel.  <br/> ModifiedEvent für das Element ursprünglichen übergeordneten Ordner.  <br/> ModifiedEvent für den Ordner Gelöschte Objekte.  <br/> |
|Vorläufiges löschen über den [DeleteFolder-Vorgang](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |
|Über den [Vorgang DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) schwerer löschen <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den Ordner übergeordneten Ordner.  <br/> |
|Verschieben Sie in den Ordner Gelöschte Objekte über der [DeleteFolder-Vorgang](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent für den Ordner. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für den Ordner alten übergeordneten Ordner.  <br/> ModifiedEvent für den Ordner neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |MovedEvent für den Ordner. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für den Ordner alten übergeordneten Ordner.  <br/> ModifiedEvent für den Ordner neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |MovedEvent für den Ordner. Hiermit wird sowohl das alte und neue übergeordnete Ordner Bezeichner.  <br/> ModifiedEvent für den Ordner alten übergeordneten Ordner.  <br/> ModifiedEvent für den Ordner neue übergeordnete Ordner, der den Ordner Gelöschte Objekte ist.  <br/> |ModifiedEvent für den Ordner alten übergeordneten Ordner.  <br/> ModifiedEvent für den neuen übergeordneten Ordners, der den Ordner Gelöschte Objekte ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Fehlerbehandlung Löschung-bezogene in EWS in Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    

