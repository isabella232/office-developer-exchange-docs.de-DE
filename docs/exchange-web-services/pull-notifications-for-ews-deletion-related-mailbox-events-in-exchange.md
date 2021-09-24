---
title: Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 83511eea-e0b5-4ef0-83b1-0c5434e6d3ab
description: Ermitteln Sie, welche Postfachereignisse ausgelöst werden, wenn Sie Elemente mithilfe von EWS in Exchange löschen.
ms.openlocfilehash: fa04d49f02cfec621f00a9b51b121cff22ca393b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510414"
---
# <a name="pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange"></a>Pullbenachrichtigungen in Exchange für Postfachereignisse im Zusammenhang mit Löschungen in EWS

Ermitteln Sie, welche Postfachereignisse ausgelöst werden, wenn Sie Elemente mithilfe von EWS in Exchange löschen.
  
Wenn Sie [Elemente und Ordner aus einem Postfach löschen,](deleting-items-by-using-ews-in-exchange.md)löst dies ein Postfachereignis aus. Unterschiedliche Versionen von Exchange als Reaktion auf Änderungen an Elementen und Ordnern in einem Postfach unterschiedliche Postfachereignisse zurückgeben. In der folgenden Tabelle sind die Postfachereignisse aufgeführt, die für Löschungen zurückgegeben werden, wenn Sie Pullbenachrichtigungen zum Abonnieren von Postfachereignissen verwenden. 
  
**Tabelle 1: Löschbezogene Postfachereignisse für Pullbenachrichtigungen**

|**Typ des Löschvorgangs und EWS-Vorgangs**|**Exchange 2010-Benachrichtigung, wenn Sie die einzelnen Ordnerbezeichner angeben**|**Exchange 2010-Benachrichtigung, wenn Sie alle Ordner angeben**|**Exchange Online und Exchange 2013-Benachrichtigung, wenn Sie die einzelnen Ordnerbezeichner angeben**|**Exchange Online und Exchange 2013, wenn Sie alle Ordner angeben**|
|:-----|:-----|:-----|:-----|:-----|
|Vorläufiges Löschen über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |MovedEvent für das Element. Dies gibt sowohl die alten als auch die neuen Bezeichner des übergeordneten Ordners an. Das Element wird in den Ordner für die gelöschten Elemente im Dumpster verschoben.   <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem Standardmäßigen Suchordner "AllItems".  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |
|Endgültiges Löschen über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |DeletedEvent für das Element.  <br/> DeletedEvent für das Element aus dem Standardmäßigen Suchordner "AllItems".  <br/> ModifiedEvent für den übergeordneten Ordner des Elements.  <br/> |
|Verschieben in den Ordner "Gelöschte Elemente" über den [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |MovedEvent für das Element. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für das Element. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für das Element. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Elements, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |DeletedEvent aus dem Standardmäßigen Suchordner "AllItems".  <br/> CreatedEvent für das Element im Ordner "AllItems".  <br/> ModifiedEvent für den ursprünglichen übergeordneten Ordner des Elements.  <br/> ModifiedEvent für den Ordner "Gelöschte Elemente".  <br/> |
|Vorläufiges Löschen über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |
|Endgültiges Löschen über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |DeletedEvent für den Ordner.  <br/> ModifiedEvent für den übergeordneten Ordner des Ordners.  <br/> |
|Verschieben in den Ordner "Gelöschte Elemente" über den [DeleteFolder-Vorgang](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |MovedEvent für den Ordner. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für den Ordner. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |MovedEvent für den Ordner. Dies gibt sowohl alte als auch neue bezeichner für übergeordnete Ordner an.  <br/> ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |ModifiedEvent für den alten übergeordneten Ordner des Ordners.  <br/> ModifiedEvent für den neuen übergeordneten Ordner des Ordners, bei dem es sich um den Ordner "Gelöschte Elemente" handelt.  <br/> |
   
## <a name="see-also"></a>Siehe auch


- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Umgang mit Fehlern in Exchange im Zusammenhang mit Löschungen in EWS](handling-deletion-related-errors-in-ews-in-exchange.md)
    

