---
title: Erstellen von Kontaktgruppen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Erfahren Sie, wie Sie eine Kontaktgruppe mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
ms.openlocfilehash: ade7fa68b00b055268cd5f0c34a75e0abbdb18ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513220"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>Erstellen von Kontaktgruppen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie eine Kontaktgruppe mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
  
Mithilfe der verwalteten EWS-API oder EWS können Sie eine Kontaktgruppe erstellen, bei der es sich um eine private [Verteilergruppe](distribution-groups-and-ews-in-exchange.md)handelt. Verwenden Sie zum Erstellen von Kontaktgruppen die Methoden in der verwalteten [ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS-API-Klasse, oder verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS-Vorgang. 
  
Beachten Sie, dass Sie die verwaltete EWS-API oder EWS nicht verwenden können, um eine universelle Verteiler- oder Sicherheitsgruppe zu erstellen. Zum Erstellen einer universellen Verteiler- oder Sicherheitsgruppe können Sie das Cmdlet ["New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell"](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)verwenden. 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>Erstellen einer Kontaktgruppe mithilfe der verwalteten EWS-API
<a name="bk_EWSMA"> </a>

Zum Erstellen einer Kontaktgruppe benötigen Sie nur ein paar Informationen: einen Namen für die Gruppe und die Mitglieder, die der Gruppe hinzugefügt werden sollen. Das folgende Beispiel zeigt, wie Sie eine einfache Kontaktgruppe erstellen, die ein paar Gruppenmitglieder enthält.
  
```cs
// Create a new contact group object.
ContactGroup myContactGroup = new ContactGroup(service);
// Give the group a name.
myContactGroup.DisplayName = "My Contact Group";
// Add some members to the group.
myContactGroup.Members.Add(new GroupMember("sadie@contoso.com"));
myContactGroup.Members.Add(new GroupMember("alfred@contoso.com"));
// Save the group.
myContactGroup.Save();

```

## <a name="create-a-contact-group-by-using-ews"></a>Erstellen einer Kontaktgruppe mithilfe von EWS
<a name="bk_EWSMA"> </a>

Es kann einige weitere Codezeilen dauern, aber Sie können eine Kontaktgruppe mithilfe des [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS-Vorgangs erstellen. Das folgende XML-Anforderungsbeispiel zeigt, wie Sie eine Kontaktgruppe erstellen können. Dies ist auch die XML-Anforderung, die gesendet wird, wenn Sie [die verwaltete EWS-API zum Erstellen einer Kontaktgruppe verwenden.](#bk_EWSMA)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

Es folgt ein Beispiel für eine erfolgreiche XML-Antwort auf die Anforderung. Beachten Sie, dass die zurückgegebenen Werte eine Element-ID für die neue Kontaktgruppe und einen Änderungsschlüssel enthalten, den Sie in anderem Code verwenden können, um die Kontaktgruppe zu ändern oder die Gruppe zu erweitern, um die Mitglieder anzuzeigen. Die Element-ID wird zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                          Id="AAMkADBlY…" 
                          ChangeKey="EgAAABYAAAAD7hO1SJPWTbICFWZ4U3NMAABXzQiK" />
               </DistributionList>
            </Items>
         </CreateItemResponseMessage>
      </ResponseMessages>
   </CreateItemResponse>
```

## <a name="see-also"></a>Siehe auch


- [Verteilergruppen und EWS in Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

