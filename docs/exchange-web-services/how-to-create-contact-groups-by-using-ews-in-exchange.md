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
# <a name="create-contact-groups-by-using-ews-in-exchange"></a><span data-ttu-id="74ae5-103">Erstellen von Kontaktgruppen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="74ae5-103">Create contact groups by using EWS in Exchange</span></span>

<span data-ttu-id="74ae5-104">Erfahren Sie, wie Sie eine Kontaktgruppe mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen.</span><span class="sxs-lookup"><span data-stu-id="74ae5-104">Learn how to create a contact group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="74ae5-105">Sie können eine Kontaktgruppe, bei der es sich um eine private [Verteilergruppe](distribution-groups-and-ews-in-exchange.md)handelt, mithilfe der verwaltete EWS-API oder EWS erstellen.</span><span class="sxs-lookup"><span data-stu-id="74ae5-105">You can create a contact group, which is a private [distribution group](distribution-groups-and-ews-in-exchange.md), by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="74ae5-106">Verwenden Sie zum Erstellen von Kontaktgruppen die Methoden in der [Contactgroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) -verwaltete EWS-API-Klasse, oder verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="74ae5-106">To create contact groups, use the methods in the [ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API class, or use the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="74ae5-107">Beachten Sie, dass Sie die verwaltete EWS-API oder EWS nicht zum Erstellen einer universellen Verteilergruppe oder Sicherheitsgruppe verwenden können.</span><span class="sxs-lookup"><span data-stu-id="74ae5-107">Note that you can't use the EWS Managed API or EWS to create a universal distribution group or security group.</span></span> <span data-ttu-id="74ae5-108">Zum Erstellen einer universellen Verteilergruppe oder Sicherheitsgruppe können Sie das Cmdlet [New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange-Verwaltungsshell](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)verwenden.</span><span class="sxs-lookup"><span data-stu-id="74ae5-108">To create a universal distribution group or security group, you can use the [New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx).</span></span> 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a><span data-ttu-id="74ae5-109">Erstellen Sie eine Kontaktgruppe mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="74ae5-109">Create a contact group by using the EWS Managed API</span></span>
<span data-ttu-id="74ae5-110"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="74ae5-110"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="74ae5-111">Um eine Kontaktgruppe zu erstellen, benötigen Sie nur einige Informationen: einen Namen für die Gruppe und die Mitglieder, die der Gruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="74ae5-111">To create a contact group, you just need a couple pieces of information: a name for the group, and the members to add to the group.</span></span> <span data-ttu-id="74ae5-112">Das folgende Beispiel zeigt, wie Sie eine einfache Kontaktgruppe erstellen, die ein paar Gruppenmitglieder enthält.</span><span class="sxs-lookup"><span data-stu-id="74ae5-112">The following example shows how to create a simple contact group that contains a couple of group members.</span></span>
  
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

## <a name="create-a-contact-group-by-using-ews"></a><span data-ttu-id="74ae5-113">Erstellen einer Kontaktgruppe mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="74ae5-113">Create a contact group by using EWS</span></span>
<span data-ttu-id="74ae5-114"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="74ae5-114"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="74ae5-115">Es kann einige weitere Codezeilen benötigen, aber Sie können eine Kontaktgruppe mithilfe der [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) -EWS-Operation erstellen.</span><span class="sxs-lookup"><span data-stu-id="74ae5-115">It might take a few more lines of code, but you can create a contact group by using the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="74ae5-116">Das folgende XML-Anforderungs Beispiel zeigt, wie Sie eine Kontaktgruppe erstellen können.</span><span class="sxs-lookup"><span data-stu-id="74ae5-116">The following XML request example shows how you can create a contact group.</span></span> <span data-ttu-id="74ae5-117">Dies ist auch die XML-Anforderung, die gesendet wird, wenn Sie [die verwaltete EWS-API verwenden, um eine Kontaktgruppe zu erstellen](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="74ae5-117">This is also the XML request that is sent when you [use the EWS Managed API to create a contact group](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="74ae5-118">Im folgenden finden Sie ein Beispiel für eine erfolgreiche XML-Antwort auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="74ae5-118">The following is an example of a successful XML response to the request.</span></span> <span data-ttu-id="74ae5-119">Beachten Sie, dass die zurückgegebenen Werte eine Element-ID für die neue Kontaktgruppe und einen Änderungsschlüssel enthalten, den Sie in anderem Code zum Ändern der Kontaktgruppe oder zum Erweitern der Gruppe verwenden können, um die Mitglieder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="74ae5-119">Notice that the values returned include an item ID for the new contact group and a change key that you can use in other code to modify the contact group or expand the group to see the members.</span></span> <span data-ttu-id="74ae5-120">Die Element-ID wird zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="74ae5-120">The item ID is shortened for readability.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="74ae5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ae5-121">See also</span></span>


- [<span data-ttu-id="74ae5-122">Verteilergruppen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="74ae5-122">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="74ae5-123">Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="74ae5-123">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

