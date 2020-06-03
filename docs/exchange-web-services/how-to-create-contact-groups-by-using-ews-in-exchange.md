---
title: Erstellen von Kontaktgruppen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Erfahren Sie, wie Sie eine Kontaktgruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen.
ms.openlocfilehash: 1da876bbda72f5bea08fd9855aa3f554135d54aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528139"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>Erstellen von Kontaktgruppen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie eine Kontaktgruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen.
  
Sie können eine Kontaktgruppe, bei der es sich um eine private [Verteilergruppe](distribution-groups-and-ews-in-exchange.md)handelt, mithilfe der verwaltete EWS-API oder EWS erstellen. Verwenden Sie zum Erstellen von Kontaktgruppen die Methoden in der [Contactgroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) -verwaltete EWS-API-Klasse, oder verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgang. 
  
Beachten Sie, dass Sie die verwaltete EWS-API oder EWS nicht zum Erstellen einer universellen Verteilergruppe oder Sicherheitsgruppe verwenden können. Zum Erstellen einer universellen Verteilergruppe oder Sicherheitsgruppe können Sie das Cmdlet [New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange-Verwaltungsshell](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)verwenden. 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>Erstellen Sie eine Kontaktgruppe mithilfe der verwaltete EWS-API
<a name="bk_EWSMA"> </a>

Um eine Kontaktgruppe zu erstellen, benötigen Sie nur einige Informationen: einen Namen für die Gruppe und die Mitglieder, die der Gruppe hinzugefügt werden sollen. Das folgende Beispiel zeigt, wie Sie eine einfache Kontaktgruppe erstellen, die ein paar Gruppenmitglieder enthält.
  
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

Es kann einige weitere Codezeilen benötigen, aber Sie können eine Kontaktgruppe mithilfe der [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Operation erstellen. Das folgende XML-Anforderungs Beispiel zeigt, wie Sie eine Kontaktgruppe erstellen können. Dies ist auch die XML-Anforderung, die gesendet wird, wenn Sie [die verwaltete EWS-API verwenden, um eine Kontaktgruppe zu erstellen](#bk_EWSMA).
  
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

Im folgenden finden Sie ein Beispiel für eine erfolgreiche XML-Antwort auf die Anforderung. Beachten Sie, dass die zurückgegebenen Werte eine Element-ID für die neue Kontaktgruppe und einen Änderungsschlüssel enthalten, den Sie in anderem Code zum Ändern der Kontaktgruppe oder zum Erweitern der Gruppe verwenden können, um die Mitglieder anzuzeigen. Die Element-ID wird zur Lesbarkeit gekürzt.
  
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
    

