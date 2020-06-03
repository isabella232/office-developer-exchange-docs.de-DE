---
title: UpdateItem-Vorgang (Vorgang)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: b0a7f114-d040-40eb-a8f3-05ea6489e472
description: Der UpdateItem-Vorgang wird zum Aktualisieren von Aufgabenelementeigenschaften in der Exchange-Informationsspeicher verwendet.
ms.openlocfilehash: 0041af114d11fd9577037dd154e40b84e8483c35
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459805"
---
# <a name="updateitem-operation-task"></a>UpdateItem-Vorgang (Vorgang)

Der UpdateItem-Vorgang wird zum Aktualisieren von Aufgabenelementeigenschaften in der Exchange-Informationsspeicher verwendet.
  
## <a name="remarks"></a>Bemerkungen

Sie können keine Aufgabenanforderungen mithilfe von Exchange Webdienste senden. Exchange Webdienste kann Aufgabenanforderungen zurückgeben, die von MicrosoftOfficeOutlook erstellt werden. Wenn bereits eine Aufgabenanfrage gesendet wurde, gibt eine Anforderung zum Aktualisieren der Aufgabe einen Fehler zurück.
  
## <a name="updating-the-current-occurrence-of-a-recurring-task"></a>Aktualisieren des aktuellen Vorkommens einer wiederkehrenden Aufgabe

Das Ergebnis einer UpdateItem-Operation bei wiederkehrenden Vorgängen unterscheidet sich vom Ergebnis des UpdateItem-Vorgangs für einen einzelnen, nicht wiederkehrenden Vorgang. Änderungen an einem Vorkommen einer wiederkehrenden Aufgabe führen dazu, dass einmalige Vorgänge generiert werden, wenn die folgenden Updates vorgenommen werden:
  
1. Die Status-Eigenschaft eines regenerierenden oder nonregenerating wiederkehrenden Tasks wird auf **Completed**festgelegt.
    
2. Das Startdatum oder das Enddatum eines wiederkehrenden nonregenerating-Vorgangs wird geändert.
    
Wenn beispielsweise eine **UpdateItem** -Anforderung den completed-Wert einer wiederkehrenden Aufgabe auf **true**festgelegt wird, enthält die **UpdateItemResponse** eine neue ID und ChangeKey, die eine neu erstellte einmalige Aufgabe darstellen. Die in der Anforderung enthaltene ID ist weiterhin gültig, und die wiederkehrende Aufgabe, die durch diese ID dargestellt wird, wurde aktualisiert und stellt das nächste Vorkommen dar. Die in der Anforderung enthaltene ChangeKey ist nicht mehr gültig, da die wiederkehrende Aufgabe aktualisiert wurde. 
  
Sie können den [GetItem-Vorgang](getitem-operation.md) verwenden, um die neuesten **ChangeKey** für den wiederkehrenden Vorgang abzurufen. 
  
Bei nicht wiederkehrenden Vorgängen oder beim letzten Auftreten einer wiederkehrenden Aufgabe gibt die UpdateItem-Antwort dieselbe **ID** zurück, die an Sie übergeben wurde, und gibt die zugeordnete aktualisierte **ChangeKey**zurück.
  
## <a name="see-also"></a>Siehe auch



[UpdateItem-Vorgang](updateitem-operation.md)

