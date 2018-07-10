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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756876"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a><span data-ttu-id="8bde4-103">Erstellen von Kontaktgruppen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="8bde4-103">Create contact groups by using EWS in Exchange</span></span>

<span data-ttu-id="8bde4-104">Hier erfahren Sie, wie Sie eine Gruppe von Kontakte zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="8bde4-104">Learn how to create a contact group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8bde4-105">Sie können eine Gruppe von Kontakte, erstellen, die private [Verteilergruppe](distribution-groups-and-ews-in-exchange.md)mithilfe der EWS Managed API oder EWS ist.</span><span class="sxs-lookup"><span data-stu-id="8bde4-105">You can create a contact group, which is a private [distribution group](distribution-groups-and-ews-in-exchange.md), by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="8bde4-106">Wenn Kontaktgruppen erstellen möchten, verwenden Sie die Methoden in der [ContactGroup](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API-Klasse, oder verwenden Sie den [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8bde4-106">To create contact groups, use the methods in the [ContactGroup](http://msdn.microsoft.com/de-de/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API class, or use the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="8bde4-107">Beachten Sie, dass Sie die EWS Managed API oder EWS verwenden ist nicht möglich, um eine universelle Verteilergruppe oder Sicherheitsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8bde4-107">Note that you can't use the EWS Managed API or EWS to create a universal distribution group or security group.</span></span> <span data-ttu-id="8bde4-108">Um eine universelle Verteilergruppe oder Sicherheitsgruppe erstellen, können Sie das [New-DistributionGroup](http://technet.microsoft.com/de-de/library/aa998856%28v=exchg.150%29.aspx)[Exchange-Verwaltungsshell-Cmdlet](http://msdn.microsoft.com/de-de/library/ff326159%28v=exchg.140%29.aspx)verwenden.</span><span class="sxs-lookup"><span data-stu-id="8bde4-108">To create a universal distribution group or security group, you can use the [New-DistributionGroup](http://technet.microsoft.com/de-de/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](http://msdn.microsoft.com/de-de/library/ff326159%28v=exchg.140%29.aspx).</span></span> 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a><span data-ttu-id="8bde4-109">Erstellen Sie eine Gruppe von Kontakte mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="8bde4-109">Create a contact group by using the EWS Managed API</span></span>
<span data-ttu-id="8bde4-110"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8bde4-110"></span></span>

<span data-ttu-id="8bde4-111">So erstellen Sie eine Gruppe von Kontakte, Sie nur ein paar Informationen erforderlich: einen Namen für die Gruppe und die Mitglieder der Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="8bde4-111">To create a contact group, you just need a couple pieces of information: a name for the group, and the members to add to the group.</span></span> <span data-ttu-id="8bde4-112">Im folgenden Beispiel wird gezeigt, wie eine einfache Kontaktgruppe erstellen, die ein Paar von Gruppenmitgliedern enthält.</span><span class="sxs-lookup"><span data-stu-id="8bde4-112">The following example shows how to create a simple contact group that contains a couple of group members.</span></span>
  
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

## <a name="create-a-contact-group-by-using-ews"></a><span data-ttu-id="8bde4-113">Erstellen Sie eine Gruppe von Kontakte mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="8bde4-113">Create a contact group by using EWS</span></span>
<span data-ttu-id="8bde4-114"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8bde4-114"></span></span>

<span data-ttu-id="8bde4-115">Es kann einigen Weitere Codezeilen dauern, aber Sie können eine Gruppe von Kontakte erstellen, mithilfe des [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8bde4-115">It might take a few more lines of code, but you can create a contact group by using the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="8bde4-116">Das folgende XML-Anforderung-Beispiel zeigt, wie Sie eine Gruppe von Kontakte erstellen können.</span><span class="sxs-lookup"><span data-stu-id="8bde4-116">The following XML request example shows how you can create a contact group.</span></span> <span data-ttu-id="8bde4-117">Dies ist auch der XML-Anforderung, wenn gesendet wird, Sie [verwenden die EWS Managed API, um eine Gruppe von Kontakten zu erstellen](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="8bde4-117">This is also the XML request that is sent when you [use the EWS Managed API to create a contact group](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="8bde4-118">Es folgt ein Beispiel für eine erfolgreiche XML-Antwort auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="8bde4-118">The following is an example of a successful XML response to the request.</span></span> <span data-ttu-id="8bde4-119">Beachten Sie, dass die zurückgegebenen Werte eine Element-ID für die neue Gruppe von Kontakten und einen Key ändern umfassen, dass Sie in einem anderen Code verwenden können, ändern die Gruppe von Kontakte oder erweitern die Gruppe, um die Mitglieder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8bde4-119">Notice that the values returned include an item ID for the new contact group and a change key that you can use in other code to modify the contact group or expand the group to see the members.</span></span> <span data-ttu-id="8bde4-120">Die Element-ID wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8bde4-120">The item ID is shortened for readability.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8bde4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bde4-121">See also</span></span>


- [<span data-ttu-id="8bde4-122">Verteilergruppen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8bde4-122">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8bde4-123">Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8bde4-123">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

