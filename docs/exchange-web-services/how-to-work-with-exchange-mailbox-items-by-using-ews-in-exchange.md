---
title: Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: Erfahren Sie, wie Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.
ms.openlocfilehash: a40cd7ae682c1fb0a8d2f9cfcb10d99d4ab08052
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353966"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a><span data-ttu-id="34b66-103">Arbeiten mit Exchange-Postfachelementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="34b66-103">How to: Work with Exchange mailbox items by using EWS in Exchange</span></span>

<span data-ttu-id="34b66-104">Erfahren Sie, wie Elemente mithilfe der verwalteten EWS-API oder EWS in Exchange erstellt, abgerufen, aktualisiert und gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="34b66-104">Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="34b66-105">Zum Arbeiten mit Elementen in einem Postfach können Sie mit der verwalteten EWS-API oder EWS arbeiten.</span><span class="sxs-lookup"><span data-stu-id="34b66-105">You can use the EWS Managed API or EWS to work with items in a mailbox.</span></span> <span data-ttu-id="34b66-106">Sie können generische Elemente - verwaltete EWS-API-[Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Objekte oder EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx)-Typen verwenden, um einige Operationen (Abrufen eines Elements oder Löschen eines Elements mithilfe des Bezeichners des Elements) auszuführen; den Großteil der Zeit müssen Sie jedoch ein [stark typisiertes Element](folders-and-items-in-ews-in-exchange.md#bk_item) verwenden, um eine Abruf- oder Aktualisierungsoperation auszuführen, da Sie Zugriff auf die Eigenschaften benötigen, die spezifisch für das stark typisierte Element sind.</span><span class="sxs-lookup"><span data-stu-id="34b66-106">You can use generic items — EWS Managed API [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) objects or EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) types — to perform some operations (getting an item or deleting an item by using the item's identifier); however, most of the time you'll have to use a [strongly typed item](folders-and-items-in-ews-in-exchange.md#bk_item) to perform a get or update operation because you'll need access to the properties that are specific to the strongly typed item.</span></span> 

<span data-ttu-id="34b66-107">Sie können beispielsweise kein generisches Element zum Abrufen eines Elements verwenden, das ein Start- und Enddatum aufweist - dazu benötigen Sie ein verwaltetes EWS-API- [Appointment](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)-Objekt oder einen EWS-[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)-Typen.</span><span class="sxs-lookup"><span data-stu-id="34b66-107">For example, you can't use a generic item to retrieve an item that contains a start and end date - you need an EWS Managed API [Appointment](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or an EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) type to do that.</span></span> <span data-ttu-id="34b66-108">Und wenn Sie die verwaltete EWS-API verwenden, müssen Sie immer stark typisierte Elemente erstellen, da die generische **Item** -Klasse keinen Konstruktor aufweist.</span><span class="sxs-lookup"><span data-stu-id="34b66-108">And if you're using the EWS Managed API, you always have to create strongly typed items, because the generic **Item** class does not have a constructor.</span></span> <span data-ttu-id="34b66-109">Wenn Sie mit einem nicht stark typisierten Element arbeiten, können Sie immer die einfache **Item** -Klasse zum Arbeiten mit dem Element verwenden.</span><span class="sxs-lookup"><span data-stu-id="34b66-109">If you're working with an item that is not strongly typed, you can always use the base **Item** class to work with the item.</span></span> 
  
<span data-ttu-id="34b66-110">**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Operationen für das Arbeiten mit Elementen**</span><span class="sxs-lookup"><span data-stu-id="34b66-110">**Table 1. EWS Managed API methods and EWS operations for working with items**</span></span>

|<span data-ttu-id="34b66-111">**Gewünschte Aktion**</span><span class="sxs-lookup"><span data-stu-id="34b66-111">**In order to…**</span></span>|<span data-ttu-id="34b66-112">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="34b66-112">**EWS Managed API method**</span></span>|<span data-ttu-id="34b66-113">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="34b66-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34b66-114">Erstellen eines generischen Elements</span><span class="sxs-lookup"><span data-stu-id="34b66-114">Create a generic item</span></span>  <br/> |<span data-ttu-id="34b66-p103">Keine. Sie können nur mit der verwalteten EWS-API bestimmte Elementtypen erstellen; Sie können keine generischen Elemente erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b66-p103">None. You can only create specific item types by using the EWS Managed API; you cannot create generic items.</span></span>  <br/> |[<span data-ttu-id="34b66-117">CreateItem</span><span class="sxs-lookup"><span data-stu-id="34b66-117">CreateItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="34b66-118">Abrufen eines Elements</span><span class="sxs-lookup"><span data-stu-id="34b66-118">Get an item</span></span>  <br/> |[<span data-ttu-id="34b66-119">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="34b66-119">Item.Bind</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="34b66-120">GetItem</span><span class="sxs-lookup"><span data-stu-id="34b66-120">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="34b66-121">Aktualisieren eines Elements</span><span class="sxs-lookup"><span data-stu-id="34b66-121">Update an item</span></span>  <br/> |[<span data-ttu-id="34b66-122">Item.Update</span><span class="sxs-lookup"><span data-stu-id="34b66-122">Item.Update</span></span>](http://msdn.microsoft.com/de-DE/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="34b66-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="34b66-123">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="34b66-124">Löschen eines Elements</span><span class="sxs-lookup"><span data-stu-id="34b66-124">Delete an item</span></span>  <br/> |[<span data-ttu-id="34b66-125">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="34b66-125">Item.Delete</span></span>](http://msdn.microsoft.com/de-DE/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="34b66-126">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="34b66-126">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="34b66-p104">In diesem Artikel erfahren Sie, wann Sie die generische Basisklasse verwenden können und wann Sie zum Abschließen der Aufgabe ein stark typisiertes Element benötigen. In den Codebeispielen wird die Verwendung der Basisklasse veranschaulicht, und was Sie tun müssen, wenn Sie die Basisklasse nicht verwenden können oder Sie nicht Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="34b66-p104">In this article, you'll learn when you can use the generic base class and when you need to use a strongly typed item to complete your task. The code examples will show you how to use the base class, and what to do when you can't use the base class or it doesn't fit your needs.</span></span>
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="34b66-129">Erstellen eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="34b66-129">Create an item by using the EWS Managed API</span></span>
<span data-ttu-id="34b66-130"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-130"></span></span>

<span data-ttu-id="34b66-p105">Die verwaltete EWS-API weist keinen öffentlich verfügbaren Konstruktur für die [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Klasse auf, Sie müssen den Konstruktor für den spezifischen Elementtypen verwenden, den Sie erstellen möchten, um ein Element zu erstellen. Verwenden Sie beispielsweise den [EmailMessage-Klassenkonstruktor](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) zum Erstellen einer neuen E-Mail-Nachricht, und den [Contact-Klassenkonstruktor](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx), um einen neuen Kontakt zu erstellen. Gleichermaßen gibt der Server niemals generische **Item** -Objekte in Antworten zurück; alle generischen Elemente werden als **EmailMessage** -Objekte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b66-p105">The EWS Managed API does not have a publicly available constructor for the [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) class, so you must use the constructor for the specific item type you want to create in order to create an item. For example, use the [EmailMessage class constructor](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create a new email message, and the [Contact class constructor](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) to create a new contact. Likewise, the server never returns generic **Item** objects in responses; all generic items are returned as **EmailMessage** objects.</span></span> 
  
<span data-ttu-id="34b66-p106">Wenn Sie den zu erstellenden Elementtypen kennen, können Sie die Aufgabe in wenigen Schritten abschließen. Diese Schritte ähneln sich für alle Elementtypen:</span><span class="sxs-lookup"><span data-stu-id="34b66-p106">When you know the type of item to create, you can complete the task in just a few steps. The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="34b66-136">Initialisieren Sie eine neue Instanz einer der [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Klassen mit dem [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt als Parameter.</span><span class="sxs-lookup"><span data-stu-id="34b66-136">Initialize a new instance of one of the [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) classes with the [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object as a parameter.</span></span> 
    
2. <span data-ttu-id="34b66-p107">Legen Sie die Eigenschaften des Elements fest. Die Schemas für jeden Elementtyp unterscheiden sich, es sind also unterschiedliche Eigenschaften für die verschiedenen Elemente verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34b66-p107">Set properties on the item. The schemas are different for each item type, so different properties are available for different items.</span></span>
    
3. <span data-ttu-id="34b66-139">Speichern Sie das Element oder speichern und senden Sie das Element.</span><span class="sxs-lookup"><span data-stu-id="34b66-139">Save the item, or save and send the item.</span></span>
    
<span data-ttu-id="34b66-140">Sie können beispielsweise ein [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt erstellen, die [Subject](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)-, [Body](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)- und [ToRecipients](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx)-Eigenschaften festlegen und es dann mithilfe der [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode senden.</span><span class="sxs-lookup"><span data-stu-id="34b66-140">For example, you can create an [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object, set the [Subject](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx), and [ToRecipients](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) properties, and then send it by using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

<span data-ttu-id="34b66-141">Weitere Informationen zum Erstellen eines Besprechungs- oder Terminelements mithilfe der verwalteten EWS-API finden Sie unter [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-141">To learn how to create a meeting or appointment item by using the EWS Managed API, see [How to: Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="create-an-item-by-using-ews"></a><span data-ttu-id="34b66-142">Erstellen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="34b66-142">Create an item by using EWS</span></span>
<span data-ttu-id="34b66-143"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-143"></span></span>

<span data-ttu-id="34b66-p108">Sie können ein generische Element oder ein stark typisierte Element mithilfe von EWS erstellen. Die Schritte sind für alle Elementtypen ähnlich:</span><span class="sxs-lookup"><span data-stu-id="34b66-p108">You can create a generic item or a strongly typed item by using EWS. The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="34b66-146">Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)-Operation, um ein Element im Exchange-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b66-146">Use the [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to create an item in the Exchange store.</span></span> 
    
2. <span data-ttu-id="34b66-147">Verwenden Sie das [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx)-Element, um ein oder mehrere zu erstellende Elemente aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="34b66-147">Use the [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) element to contain one or more items to create.</span></span> 
    
3. <span data-ttu-id="34b66-148">Legen Sie die Eigenschaften des Elements fest.</span><span class="sxs-lookup"><span data-stu-id="34b66-148">Set properties on the item.</span></span>
    
<span data-ttu-id="34b66-p109">Sie können beispielsweise eine E-Mail-Nachricht erstellen und senden, indem Sie den Code aus dem folgenden Beispiel verwenden. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="34b66-p109">For example, you can create an email message and send it by using the code in the following example. This is also the XML request that the EWS Managed API sends when you call the [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="34b66-151">Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="34b66-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="34b66-152">Weitere Informationen zum Erstellen eines Besprechungs- oder Terminelements mithilfe von EWS finden Sie unter [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-152">To learn how to create a meeting or appointment item by using EWS, see [How to: Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="34b66-153">Abrufen eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="34b66-153">Get an item by using the EWS Managed API</span></span>
<span data-ttu-id="34b66-154"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-154"></span></span>

<span data-ttu-id="34b66-p110">Um ein Element mithilfe der verwalteten EWS-API abzurufen, wenn Sie die [Item.Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des abzurufenden Elements kennen, können Sie bei dem Element einfach eine der [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methoden aufrufen, sodass das Element abgerufen wird. Als bewährte Vorgehensweise empfehlen wir die zurückgegebenen Eigenschaften nur auf erforderlichen zu begrenzen. In diesem Beispiel wird die **Id** -Eigenschaft des Elements und die **Subject** -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="34b66-p110">To use the EWS Managed API to get an item if you know the [Item.Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to retrieve, you simply call one of the [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) methods on the item, and the item is retrieved. As a best practice, we recommend that you limit the properties returned to only those that are required. This example returns the item **Id** property and the **Subject** property.</span></span> 
  
<span data-ttu-id="34b66-p111">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisieren Elements.</span><span class="sxs-lookup"><span data-stu-id="34b66-p111">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

<span data-ttu-id="34b66-160">Wenn Sie ein Element suchen, das bestimmte Kriterien erfüllt, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="34b66-160">If you're searching for an item that meets specific criteria, do the following:</span></span>
  
1. <span data-ttu-id="34b66-161">Erstellen Sie eine Bindung für den Ordner, der die abzurufenden Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="34b66-161">Bind to the folder that contains the items to get.</span></span>
    
2. <span data-ttu-id="34b66-162">Instanziieren Sie ein [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) oder ein [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx), um die zurückzugebenden Elemente zu filtern.</span><span class="sxs-lookup"><span data-stu-id="34b66-162">Instantiate a [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) or a [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to filter the items to return.</span></span> 
    
3. <span data-ttu-id="34b66-163">Instanziieren Sie ein [ItemView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx)- oder [CalendarView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx)-Objekt, um die Anzahl der zurückzugebenden Elemente anzugeben.</span><span class="sxs-lookup"><span data-stu-id="34b66-163">Instantiate an [ItemView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object to specify the number of items to return.</span></span> 
    
4. <span data-ttu-id="34b66-164">Rufen Sie die [ExchangeService.FindItems](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)- oder [ExchangeService.FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="34b66-164">Call the [ExchangeService.FindItems](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [ExchangeService.FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="34b66-p112">Wenn Sie beispielsweise ungelesene E-Mail-Nachrichten im Postfach abrufen möchten, verwenden Sie den Code aus dem folgenden Beispiel. In diesem Beispiel wird eine **SearchFilterCollection** zum Begrenzen der Ergebnisse der **FindItems** -Methode für ungelesene Nachrichten verwendet, außerdem wird die **ItemView** eingeschränkt, damit die Ergebnisse auf ein Element begrenzt. Dieser bestimmte Code funktioniert nur mit [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekten, da der [EmailMessageSchema.IsRead](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx)-Wert Teil des **SearchFilter** ist.</span><span class="sxs-lookup"><span data-stu-id="34b66-p112">For example, if you want to retrieve unread email messages in the Inbox, use the code in the following example. This example uses a **SearchFilterCollection** to limit the results of the **FindItems** method to unread messages, and limits the **ItemView** to limit results to one item. This particular code only works on [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects because the [EmailMessageSchema.IsRead](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) value is part of the **SearchFilter**.</span></span> 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

<span data-ttu-id="34b66-p113">Alternativ können Sie ein [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) verwenden, um die Ergebnisse der Suche einzuschränken, siehe folgendes Codebeispiel. In diesem Beispiel wird die [FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode verwendet, um bis zu fünf Termine abzurufen, die in den nächsten 30 Tagen anstehen. Dieser Code funktioniert natürlich nur bei Kalenderelementen.</span><span class="sxs-lookup"><span data-stu-id="34b66-p113">Alternatively, you can use a [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) to limit the results of the search as shown in the following code example. This example uses the [FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve up to five appointments that occur in the next 30 days. This code of course only works on calendar items.</span></span> 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

<span data-ttu-id="34b66-p114">Beachten Sie, dass sich die vom Server in der **Bind** -Methodenantwort zurückgegebenen Informationen von denen unterscheiden, die der Server für eine **FindItem** - oder **FindAppointment** -Methodenantwort zurückgibt. Die **Bind** -Methode kann alle schematisierten Eigenschaften zurückgeben, wohingegen die **FindItem** - und **FindAppointment** -Methoden nicht alle schematisierten Eigenschaften zurückgibt. Wenn Sie also vollständigen Zugriff auf das Element benötigen, müssen Sie die **Bind** -Methode verwenden. Wenn Sie das Element **Id** des abzurufenden Elements nicht haben, verwenden Sie die **FindItem** - oder **FindAppointment** -Methoden zum Abrufen der ID, und verwenden Sie dann die **Bind** -Methode, um die erforderlichen Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="34b66-p114">Note that the information the server returns in the **Bind** method response is different than the information that the server returns for a **FindItem** or **FindAppointment** method response. The **Bind** method can return all the schematized properties, whereas the **FindItem** and **FindAppointment** methods do not return all the schematized properties. So if you need full access to the item, you'll have to use the **Bind** method. If you don't have the item **Id** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** methods to retrieve the Id, and then use the **Bind** method to retrieve the properties you need.</span></span> 
  
<span data-ttu-id="34b66-175">Weitere Informationen zum Abrufen eines Besprechungs- oder Terminelements mithilfe der verwalteten EWS-API finden Sie unter [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-175">To learn how to get a meeting or appointment item by using the EWS Managed API, see [How to: Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="get-an-item-by-using-ews"></a><span data-ttu-id="34b66-176">Abrufen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="34b66-176">Get an item by using EWS</span></span>
<span data-ttu-id="34b66-177"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-177"></span></span>

<span data-ttu-id="34b66-178">Wenn Sie die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) des abzurufenden Elements kennen, können Sie das Element mithilfe der [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-Operation abrufen.</span><span class="sxs-lookup"><span data-stu-id="34b66-178">If you know the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the item to retrieve, you can get the item by using the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation.</span></span> 
  
<span data-ttu-id="34b66-p115">Im folgenden Beispiel wird die XML-Anforderung zum Abrufen des [Betreffs](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) eines Elements mit einer bestimmten **ItemId** veranschaulicht. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API beim Aufrufen der [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode zu einer **ItemId** sendet. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="34b66-p115">The following example shows the XML request to get the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of an item with a specific **ItemId**. This is also the XML request that the EWS Managed API sends when calling the [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method on an **ItemId**. The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="34b66-p116">Im folgenden Beispiel wird die XML-Antwort veranschaulicht, die der Server zurückgibt, nachdem er die **GetItem**-Operation verarbeitet. Die Antwort gibt an, dass das Element erfolgreich abgerufen wurde. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="34b66-p116">The following example shows the XML response that the server returns after it processes the **GetItem** operation. The response indicates the item was retrieved successfully. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="34b66-p117">Wenn Sie die **ItemId** des abzurufenden Elements nicht kennen, können Sie die [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)-Operation verwenden, um das Element zu suchen. Um die **FindItem**-Operation verwenden zu können, müssen Sie zunächst den Ordner identifizieren, den Sie suchen. Sie können den Ordner identifizieren, indem Sie den **DistinguinguishedFolderName** oder die [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) verwenden. Zum Abrufen der erforderlichen [FolderId](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) können Sie die [FindFolder](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)- oder **SyncFolderHierarchy**-Operationen verwenden. Verwenden Sie anschließend die **FindItem**-Operation, um den Ordner nach Ergebnissen zu durchsuchen, die mit dem Suchfilter übereinstimmen. Im Gegensatz zur verwalteten EWS-API bietet EWS keine separate Suchoperation für Termine. Die **FindItem**-Operation ruft Elemente aller Typen ab.</span><span class="sxs-lookup"><span data-stu-id="34b66-p117">If you do not know the **ItemId** of the item you want to retrieve, you can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find the item. In order to use the **FindItem** operation, you must first identify the folder that you're searching. You can identify the folder by using its **DistinguinguishedFolderName** or by using the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx). You can use either the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) or [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operations to get the **FolderId** you need. Then use the **FindItem** operation to search that folder for results that match the search filter. Unlike the EWS Managed API, EWS does not provide a separate find operation for appointments. The **FindItem** operation retrieves items of all types.</span></span> 
  
<span data-ttu-id="34b66-p118">Im folgenden Beispiel wird die XML- **FindItem**-Operationsanforderung veranschaulicht, die an den Server gesendet wird, um Termine im Kalenderordner zu suchen, die in den nächsten 30 Tagen anstehen. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="34b66-p118">The following example shows the XML **FindItem** operation request that is sent to the server to find appointments in the Calendar folder that occur in the next 30 days. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="34b66-p119">Der Server antwortet auf die **FindItem**-Anforderung mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert von **NoError** umfasst, der angibt, dass die Operation erfolgreich abgeschlossen wurde. Falls Kalenderelemente die Filterkriterien erfüllen, sind sie in der Antwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="34b66-p119">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the operation completed successfully. If any calendar items meet the filtering criteria, they are included in the response.</span></span>
  
<span data-ttu-id="34b66-p120">Beachten Sie, dass sich die vom Server in der **GetItem**-Operationsantwort zurückgegebenen Informationen von denen unterscheiden, die der Server in einer **FindItem**- oder **FindAppointment**-Operationsantwort zurückgibt. Die **GetItem**-Operation kann alle schematisierten Eigenschaften zurückgeben, wohingegen die **FindItem**- und **FindAppointment**-Operationen nicht alle schematisierten Eigenschaften zurückgeben. Wenn Sie also vollständigen Zugriff auf das Element benötigen, müssen Sie die **GetItem**-Operation verwenden. Wenn Sie die **ItemId** des abzurufenden Elements nicht haben, verwenden Sie die **FindItem**- oder **FindAppointment**-Operationen, um die **ItemId** abzurufen und verwenden Sie anschließend die **GetItem**-Operation zum Abrufen der erforderlichen Elemente.</span><span class="sxs-lookup"><span data-stu-id="34b66-p120">Note that the information the server returns in the **GetItem** operation response is different than the information the server returns in a **FindItem** or **FindAppointment** operation response. The **GetItem** operation can return all the schematized properties, whereas the **FindItem** and **FindAppointment** operations do not return all the schematized properties. So if you need full access to the item, you'll have to use the **GetItem** operation. If you don't have the **ItemId** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** operations to retrieve the **ItemId**, and then use the **GetItem** operation to retrieve the elements you need.</span></span> 
  
<span data-ttu-id="34b66-200">Weitere Informationen zum Abrufen eines Besprechungs- oder Terminelements mithilfe von EWS finden Sie unter [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-200">To learn how to get a meeting or appointment item by using EWS, see [How to: Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="34b66-201">Aktualisieren eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="34b66-201">Update an item by using the EWS Managed API</span></span>
<span data-ttu-id="34b66-202"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-202"></span></span>

<span data-ttu-id="34b66-p121">Die Schritte zum Aktualisieren eines Elements mithilfe der verwalteten EWS-API ähneln sich für alle Elementtypen; die Elementeigenschaften für die einzelnen Elementtypen unterscheiden sich jedoch und bei der [Update](http://msdn.microsoft.com/de-DE/library/office/dd635915%28v=exchg.80%29.aspx)-Methode stehen viele überladene Methoden zur Auswahl. So aktualisieren Sie ein Element:</span><span class="sxs-lookup"><span data-stu-id="34b66-p121">The steps to update an item by using the EWS Managed API are similar for all item types; however, the item properties are different for each item type, and the [Update](http://msdn.microsoft.com/de-DE/library/office/dd635915%28v=exchg.80%29.aspx) method has many overloaded methods to choose from. To update an item:</span></span> 
  
1. <span data-ttu-id="34b66-p122">Verwenden Sie die [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)-Methode zum Abrufen der aktuellsten Version des Elements, sofern Sie sie nicht bereits haben. Um die Eigenschaften eines bestimmten stark typisierten Elements zu aktualisieren, müssen Sie eine Bindung zu diesem Elementtyp erstellen. Zum Aktualisieren der für einen generischen Elementtyp verfügbaren Eigenschaften können Sie eine Bindung zum [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b66-p122">Use the [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get the latest version of the item, unless you already have it. To update properties specific to a strongly typed item, you'll have to bind to that item type. To update properties available on the generic item type, you can bind to the [Item](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object.</span></span> 
    
2. <span data-ttu-id="34b66-208">Aktualisieren Sie die Eigenschaften des Elements.</span><span class="sxs-lookup"><span data-stu-id="34b66-208">Update the properties on the item.</span></span>
    
3. <span data-ttu-id="34b66-209">Rufen Sie die **Update** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="34b66-209">Call the **Update** method.</span></span> 
    
<span data-ttu-id="34b66-210">Sie können beispielsweise den Betreff einer E-Mail mithilfe des generischen Elementtyps aktualisieren, wie im Code des folgenden Beispiels dargestellt.</span><span class="sxs-lookup"><span data-stu-id="34b66-210">For example, you can update the subject of an email by using the generic item type, as shown in the code in the following example.</span></span>
  
<span data-ttu-id="34b66-p123">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisierenden Elements.</span><span class="sxs-lookup"><span data-stu-id="34b66-p123">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

<span data-ttu-id="34b66-213">Weitere Informationen zum Aktualisieren eines Besprechungs- oder Terminelements mithilfe der verwalteten EWS-API finden Sie unter [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-213">To learn how to update a meeting or appointment item by using the EWS Managed API, see [How to: Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-ews"></a><span data-ttu-id="34b66-214">Aktualisieren eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="34b66-214">Update an item by using EWS</span></span>
<span data-ttu-id="34b66-215"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-215"></span></span>

<span data-ttu-id="34b66-216">Gehen Sie zum Aktualisieren eines Elements mithilfe von EWS folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="34b66-216">To update an item by using EWS, do the following:</span></span>
  
1. <span data-ttu-id="34b66-217">Verwenden Sie die [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)-Operation zum Abrufen der aktuellsten Version des Elements, sofern Sie sie nicht bereits haben.</span><span class="sxs-lookup"><span data-stu-id="34b66-217">Use the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to get the latest version of the item, unless you already have it.</span></span> 
    
2. <span data-ttu-id="34b66-218">Verwenden Sie die [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)-Operation, um die zu aktualisierenden Felder anzugeben und weisen Sie diesen Feldern neue Werte zu.</span><span class="sxs-lookup"><span data-stu-id="34b66-218">Use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to specify fields to update and assign new values to those fields.</span></span> 
    
<span data-ttu-id="34b66-p124">Im folgenden Beispiel wird die XML- **UpdateItem**-Operationsanforderung veranschaulicht, die an den Server gesendet wird, um den [Betreff](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx)-Wert der E-Mail-Nachricht zu aktualisieren. Die Werte für einige Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="34b66-p124">The following example shows the XML **UpdateItem** operation request that is sent to the server to update the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) value of the email message. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="34b66-221">Der Server antwortet auf die **UpdateItem**-Anforderung mit einer [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** umfasst, der angibt, dass die Elementaktualisierung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="34b66-221">The server responds to the **UpdateItem** request with a [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item update was successful.</span></span>
  
<span data-ttu-id="34b66-222">Weitere Informationen zum Aktualisieren eines Besprechungs- oder Terminelements mithilfe von EWS finden Sie unter [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-222">To learn how to update a meeting or appointment item by using EWS, see [How to: Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="34b66-223">Löschen eines Elements mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="34b66-223">Delete an item by using the EWS Managed API</span></span>
<span data-ttu-id="34b66-224"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-224"></span></span>

<span data-ttu-id="34b66-p125">Sie können Elemente löschen, indem Sie sie in den Ordner „Gelöschte Elemente" oder den Papierkorb verschieben. Wenn Sie die [ItemId](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu löschenden Elements kennen, rufen Sie bei dem Element einfach die [Delete](http://msdn.microsoft.com/de-DE/library/office/dd635072%28v=exchg.80%29.aspx)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="34b66-p125">You can delete items by moving them to the Deleted Items folder or to the dumpster. If you know the [ItemId](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to delete, just call the [Delete](http://msdn.microsoft.com/de-DE/library/office/dd635072%28v=exchg.80%29.aspx) method on the item.</span></span> 
  
<span data-ttu-id="34b66-227">Gehen Sie folgendermaßen vor, wenn Sie das Element suchen müssen, bevor Sie es löschen:</span><span class="sxs-lookup"><span data-stu-id="34b66-227">If you need to find the item before deleting it, do the following:</span></span>
  
1. <span data-ttu-id="34b66-228">Rufen Sie die [FindItems](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)- oder [FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)-Methode, um nach dem zu löschenden Element zu suchen.</span><span class="sxs-lookup"><span data-stu-id="34b66-228">Call the [FindItems](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [FindAppointments](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to find the item to delete.</span></span> 
    
1. <span data-ttu-id="34b66-229">Instanziieren Sie ein [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) und begrenzen Sie es auf die zurückzugebenden Eigenschaften oder verwenden Sie eine [SearchFilterCollection](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx), um nach bestimmten Elementen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="34b66-229">Instantiate a [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) and limit it to the properties to return, or use a [SearchFilterCollection](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) to find specific items.</span></span> 
    
2. <span data-ttu-id="34b66-230">Instanziieren Sie eine [ItemView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) oder [CalendarView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx), um die Anzahl der zurückzugebenden Elemente anzugeben.</span><span class="sxs-lookup"><span data-stu-id="34b66-230">Instantiate an [ItemView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) to specify the number of items to return.</span></span> 
    
2. <span data-ttu-id="34b66-231">Rufen Sie die [Delete](http://msdn.microsoft.com/de-DE/library/office/dd635072%28v=exchg.80%29.aspx)-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="34b66-231">Call the [Delete](http://msdn.microsoft.com/de-DE/library/office/dd635072%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="34b66-232">Im folgenden Code wird beispielsweise veranschaulicht, wie eine E-Mail-Nachricht in den Ordner „Gelöschte Elemente“ verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="34b66-232">For example, the following code shows how to move an email message to the Deleted Items folder.</span></span>
  
<span data-ttu-id="34b66-p126">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer an einem Exchange-Server authentifiziert wurde. Die lokale Variable  *itemId*  ist die [ID](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des zu aktualisierenden Elements.</span><span class="sxs-lookup"><span data-stu-id="34b66-p126">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

<span data-ttu-id="34b66-235">Weitere Informationen zum Löschen von Elementen finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-235">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="34b66-236">Weitere Informationen zum Löschen eines Besprechungs- oder Terminelements mithilfe der verwalteten EWS-API finden Sie unter [Löschen von Terminen und Abbrechen an Besprechungen mit EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-236">To learn how to delete a meeting or appointment item by using the EWS Managed API, see [How to: Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-ews"></a><span data-ttu-id="34b66-237">Löschen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="34b66-237">Delete an item by using EWS</span></span>
<span data-ttu-id="34b66-238"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-238"></span></span>

<span data-ttu-id="34b66-239">Sie können ein Element mithilfe der [DeleteItem](../web-service-reference/deleteitem-operation.md)-Operation löschen.</span><span class="sxs-lookup"><span data-stu-id="34b66-239">You can delete an item by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) operation.</span></span> 
  
<span data-ttu-id="34b66-p128">Im folgenden Beispiel wird die XML-Anforderung veranschaulicht, die an den Server gesendet wird, um die E-Mail-Nachricht in den Ordner „Gelöschte Elemente“ zu verschieben. Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="34b66-p128">The following example shows the XML request that is sent to the server to move the email message to the Deleted Items folder. The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="34b66-242">Der Server antwortet auf die **DeleteItem**-Anforderung mit einer [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx)-Wert von **NoError** umfasst, der angibt, dass der Löschvorgang des Elements erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="34b66-242">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item deletion was successful.</span></span>
  
<span data-ttu-id="34b66-243">Weitere Informationen zum Löschen von Elementen finden Sie unter [Löschen von Elementen mithilfe von EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-243">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="34b66-244">Weitere Informationen zum Löschen eines Besprechungs- oder Terminelements mithilfe von EWS finden Sie unter [Löschen von Terminen und Abbrechen an Besprechungen mit EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-244">To learn how to delete a meeting or appointment item by using EWS, see [How to: Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="move-or-copy-items-to-another-mailbox"></a><span data-ttu-id="34b66-245">Verschieben oder Kopieren von Elementen in ein anderes Postfach</span><span class="sxs-lookup"><span data-stu-id="34b66-245">Move or copy items to another mailbox</span></span>
<span data-ttu-id="34b66-246"><a name="bk_movecopybtnmailboxes"> </a></span><span class="sxs-lookup"><span data-stu-id="34b66-246"></span></span>

<span data-ttu-id="34b66-p130">Sie können Elemente mithilfe der [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx)- und [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx)-Operationen zwischen Postfächern verschieben oder kopieren. Weitere Informationen dazu finden Sie unter [Exportieren und Importieren von Elementen mit EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="34b66-p130">You can move or copy items between mailboxes by using the [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) and [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) operations. To learn more, see [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34b66-249">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34b66-249">See also</span></span>

- [<span data-ttu-id="34b66-250">Ordner und Elemente in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="34b66-250">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="34b66-251">Arbeiten mit Ordnern unter Verwendung von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="34b66-251">How to: Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="34b66-252">Löschen von Elementen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="34b66-252">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    

