---
title: Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Hier erfahren Sie, wie Sie eine Gruppe von Kontakte zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: b3357f24e07a9c1b3b37ccb63b0f4f0d0a1d6fcf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756876"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste

Hier erfahren Sie, wie Sie eine Gruppe von Kontakte zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Sie können eine Gruppe von Kontakte, erstellen, die private [Verteilergruppe](distribution-groups-and-ews-in-exchange.md)mithilfe der EWS Managed API oder EWS ist. Wenn Kontaktgruppen erstellen möchten, verwenden Sie die Methoden in der [ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API-Klasse, oder verwenden Sie den [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgang. 
  
Beachten Sie, dass Sie die EWS Managed API oder EWS verwenden ist nicht möglich, um eine universelle Verteilergruppe oder Sicherheitsgruppe zu erstellen. Um eine universelle Verteilergruppe oder Sicherheitsgruppe erstellen, können Sie das [New-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx)[Exchange-Verwaltungsshell-Cmdlet](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)verwenden. 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>Erstellen Sie eine Gruppe von Kontakte mithilfe der EWS Managed API
<a name="bk_EWSMA"> </a>

So erstellen Sie eine Gruppe von Kontakte, Sie nur ein paar Informationen erforderlich: einen Namen für die Gruppe und die Mitglieder der Gruppe hinzu. Im folgenden Beispiel wird gezeigt, wie eine einfache Kontaktgruppe erstellen, die ein Paar von Gruppenmitgliedern enthält.
  
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

## <a name="create-a-contact-group-by-using-ews"></a>Erstellen Sie eine Gruppe von Kontakte mithilfe der Exchange-Webdienste
<a name="bk_EWSMA"> </a>

Es kann einigen Weitere Codezeilen dauern, aber Sie können eine Gruppe von Kontakte erstellen, mithilfe des [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgangs. Das folgende XML-Anforderung-Beispiel zeigt, wie Sie eine Gruppe von Kontakte erstellen können. Dies ist auch der XML-Anforderung, wenn gesendet wird, Sie [verwenden die EWS Managed API, um eine Gruppe von Kontakten zu erstellen](#bk_EWSMA).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

Es folgt ein Beispiel für eine erfolgreiche XML-Antwort auf die Anforderung. Beachten Sie, dass die zurückgegebenen Werte eine Element-ID für die neue Gruppe von Kontakten und einen Key ändern umfassen, dass Sie in einem anderen Code verwenden können, ändern die Gruppe von Kontakte oder erweitern die Gruppe, um die Mitglieder anzuzeigen. Die Element-ID wird zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
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
    
- [Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

