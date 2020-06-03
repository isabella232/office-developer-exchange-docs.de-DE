---
title: Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: In diesem Artikel erfahren Sie, wie Sie mit dem verwaltete EWS-API oder EWS eindeutige Namen auflösen können, indem Sie mögliche Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder aus einem Kontaktordner im Postfach des Benutzers erhalten.
ms.openlocfilehash: 5e30e268f54e6ca257e188592e49d168e64332ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527747"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a><span data-ttu-id="bb7b3-103">Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bb7b3-103">Resolve ambiguous names by using EWS in Exchange 2013</span></span>

<span data-ttu-id="bb7b3-104">In diesem Artikel erfahren Sie, wie Sie mit dem verwaltete EWS-API oder EWS eindeutige Namen auflösen können, indem Sie mögliche Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder aus einem Kontaktordner im Postfach des Benutzers erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-104">Learn how to use the EWS Managed API or EWS to resolve ambiguous names by getting possible matches from Active Directory Domain Services (AD DS) or a contacts folder in your user's mailbox.</span></span>
  
<span data-ttu-id="bb7b3-105">Ein Benutzer in Ihrer Organisation erhält eine handschriftliche Liste mit Namen und Adressen für Mitarbeiter, die an einer Schulungssitzung teilgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-105">A user in your organization is given a hand-written list of names and addresses for employees that attended a training session.</span></span> <span data-ttu-id="bb7b3-106">Sie möchten eine e-Mail mit einigen zusätzlichen Informationen an Personen in der Liste senden, aber Sie können nicht alle e-Mail-Adressen lesen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-106">They want to send an email with some additional information to people on the list, but they can't read everyone's email address.</span></span> <span data-ttu-id="bb7b3-107">Wenn Sie dieses Problem für Ihre Benutzer in Ihrer Anwendung lösen möchten, kann EWS helfen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-107">If you want to solve this problem for your users in your application, EWS can help.</span></span> <span data-ttu-id="bb7b3-108">Sie können die [Datei "ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine Liste möglicher Übereinstimmungen für eine Textauswahl zurückzugeben, beispielsweise einen Teil eines Nachnamens.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-108">You can use the [ExchangeService.ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API method or the [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to return a list of potential matches for a selection of text, such as part of a last name.</span></span> <span data-ttu-id="bb7b3-109">Bei den zurückgegebenen Elementen kann es sich um öffentliche Benutzerpostfächer, Verteilergruppen und Kontakte handeln.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-109">The returned items can be public user mailboxes, distribution groups, and contacts.</span></span> 
  
<span data-ttu-id="bb7b3-110">Beachten Sie, dass Exchange e-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP in einem mehrwertigen Array speichert.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-110">Note that Exchange saves email addresses with prefixed routing types, such as smtp or sip, in a multivalue array.</span></span> <span data-ttu-id="bb7b3-111">Die **ResolveName** -Methode und der **ResolveNames** -Vorgang führen eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens wie "SIP: user1" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-111">The **ResolveName** method and the **ResolveNames** operation perform a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1".</span></span> <span data-ttu-id="bb7b3-112">Wenn Sie keinen Routingtyp angeben, wird die Methode oder der Vorgang standardmäßig auf SMTP festgelegt, mit einer primären SMTP-Adress Eigenschaft abgeglichen und nicht mit dem mehrwertigen Array durchsucht.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-112">If you don't specify a routing type, the method or operation will default to smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> <span data-ttu-id="bb7b3-113">Wenn Sie beispielsweise nach user1 suchen und das SIP-Präfix nicht einschließen, erhalten Sie SIP:user1@contoso.com nicht als Ergebnis, selbst wenn es sich um ein gültiges Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-113">For example, if you search for User1 and do not include the sip prefix, you will not receive sip:User1@Contoso.com as a result, even if that is a valid mailbox.</span></span> 
  
<span data-ttu-id="bb7b3-114">Sie können nur einen eindeutigen Namen in einer einzelnen Anforderung angeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-114">You can only specify one ambiguous name in a single request.</span></span> <span data-ttu-id="bb7b3-115">Wenn Sie eine Liste mit uneindeutigen Namen auflösen müssen, müssen Sie die Liste durchlaufen und die Methode oder den Vorgang für jeden Eintrag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-115">If you have a list of ambiguous names to resolve, you will need to loop through the list and call the method or operation for each entry.</span></span> <span data-ttu-id="bb7b3-116">Kandidaten aus dem Ordner Kontakte eines Benutzers verfügen über einen Element-ID-Wert ungleich NULL, der dann in einem [Contact. Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) -Methodenaufruf oder einer [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Vorgangsanforderung zum Abrufen zusätzlicher Informationen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-116">Candidates from a user's Contacts folder will have a non-null item ID value, which can then be used in a [Contact.Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) method call or [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request to retrieve additional information.</span></span> <span data-ttu-id="bb7b3-117">Wenn es sich bei dem Kandidaten um eine Verteilergruppe handelt, können Sie die verwaltete EWS-API-Methode von [expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) oder den EWS-Vorgang [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) verwenden, um die Liste der Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-117">If the candidate is a distribution group, you can use the [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS operation to get the list of members.</span></span> <span data-ttu-id="bb7b3-118">Wenn der Parameter _returnContactDetails_ oder das **ReturnFullContactData** -EWS-Attribut auf true festgelegt ist, enthalten Active Directory Einträge, die über eine **ResolveName** -Methode oder einen **ResolveNames** -Vorgang zurückgegeben werden, zusätzliche Eigenschaften, die den Kontakt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-118">If the  _returnContactDetails_ parameter or the **ReturnFullContactData** EWS attribute is set to true, Active Directory entries returned via a **ResolveName** method or **ResolveNames** operation will include additional properties that describe the contact.</span></span> <span data-ttu-id="bb7b3-119">Der _returnContactDetails_ -Parameter oder das **ReturnFullContactData** -Attribut wirkt sich nicht auf die Daten aus, die für Kontakte und Kontaktgruppen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-119">The  _returnContactDetails_ parameter or the **ReturnFullContactData** attribute does not affect the data that is returned for contacts and contact groups.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a><span data-ttu-id="bb7b3-120">Auflösen von nicht eindeutigen Namen mithilfe von verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="bb7b3-120">Resolve ambiguous names by using EWS Managed API</span></span>
<span data-ttu-id="bb7b3-121"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="bb7b3-121"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="bb7b3-122">Sie können die [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) -Methode verwenden, um Kandidaten zu finden, die mit dem nicht eindeutigen Namen übereinstimmen, den Sie übergeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-122">You can use the [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) method to find candidates that match the ambiguous name you pass.</span></span> <span data-ttu-id="bb7b3-123">Sie können Überladungen der **ResolveName** -Methode verwenden, um auf fünf verschiedene Arten nach Kandidaten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-123">You can use overloads of the **ResolveName** method to search for candidates in five different ways.</span></span> 
  
<span data-ttu-id="bb7b3-124">**Tabelle 1. Überladene ResolveName-Methoden**</span><span class="sxs-lookup"><span data-stu-id="bb7b3-124">**Table 1. Overloaded ResolveName methods**</span></span>

|<span data-ttu-id="bb7b3-125">**Methode**</span><span class="sxs-lookup"><span data-stu-id="bb7b3-125">**Method**</span></span>|<span data-ttu-id="bb7b3-126">**Funktionsweise**</span><span class="sxs-lookup"><span data-stu-id="bb7b3-126">**How it works**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb7b3-127">ResolveName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="bb7b3-127">ResolveName(String)</span></span>](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="bb7b3-128">Findet Kontakte im Kontakteordner des Benutzers und in der globalen Adressliste (GAL) – in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-128">Finds contacts in the user's Contacts folder and the Global Address List (GAL) — in that order.</span></span> <span data-ttu-id="bb7b3-129">Die Zeichenfolgenvariable ist der eindeutige Name, den Sie auflösen möchten.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-129">The string variable is the ambiguous name you are trying to resolve.</span></span>  <br/> |
|[<span data-ttu-id="bb7b3-130">ResolveName (String, ResolveNameSearchLocation, Boolean)</span><span class="sxs-lookup"><span data-stu-id="bb7b3-130">ResolveName(String, ResolveNameSearchLocation, Boolean)</span></span>](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="bb7b3-131">Sucht nach Kontakten im Standardordner "Kontakte" und/oder in der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="bb7b3-131">Finds contacts in the default Contacts folder and/or the Global Address List (GAL).</span></span> <span data-ttu-id="bb7b3-132">Der Zeichenfolgenwert ist der nicht eindeutiger Name, der Such Speicherort gibt den Kontakteordner und/oder die GAL an, und der boolesche Wert gibt an, ob die vollständigen Kontaktinformationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-132">The string value is the ambiguous name, the search location specifies the Contacts folder and/or the GAL, and the Boolean value indicates whether to return the full contact information.</span></span>  <br/> |
|[<span data-ttu-id="bb7b3-133">ResolveName (String, ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="bb7b3-133">ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="bb7b3-134">Sucht nach Kontakten im standardmäßigen Kontakteordner und/oder der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="bb7b3-134">Finds contacts in the default Contacts folder and/or Global Address List (GAL).</span></span> <span data-ttu-id="bb7b3-135">Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-135">This method enables you to set the properties that are returned.</span></span>  <br/> |
|[<span data-ttu-id="bb7b3-136">ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)</span><span class="sxs-lookup"><span data-stu-id="bb7b3-136">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)</span></span>](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="bb7b3-137">Sucht nach Kontakten in angegebenen Kontaktordnern und/oder der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="bb7b3-137">Finds contacts in specified contact folders and/or the Global Address List (GAL).</span></span> <span data-ttu-id="bb7b3-138">Sie können diese Methode verwenden, um eine Sammlung von Ordnern an die Suche zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-138">You can use this method to pass a collection of folders to search.</span></span> <span data-ttu-id="bb7b3-139">Auf diese Weise können Sie in anderen Kontaktordnern als dem Standardordner Kontakte suchen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-139">This enables you to look in contact folders other than the default Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="bb7b3-140">ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="bb7b3-140">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="bb7b3-141">Sucht Kontakte in der globalen Adressliste (GAL) und/oder in bestimmten Kontaktordnern.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-141">Finds contacts in the Global Address List (GAL) and/or in specific contact folders.</span></span> <span data-ttu-id="bb7b3-142">Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-142">This method enables you to set the properties that are returned.</span></span>  <br/> |
   
<span data-ttu-id="bb7b3-143">Lassen Sie uns mit einem einfachen Beispiel beginnen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-143">Let's start with a simple example.</span></span> <span data-ttu-id="bb7b3-144">Das folgende Beispiel zeigt, wie Sie die Textzeichenfolge "Dan" auflösen und den Namen und die e-Mail-Adresse jedes gefundenen Kandidaten ausgeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-144">The following example shows how to resolve the text string "dan" and output the name and email address of each candidate found.</span></span> <span data-ttu-id="bb7b3-145">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-145">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="bb7b3-146">Die Antwort gibt maximal 100 Kandidaten zurück, allerdings gibt es möglicherweise mehr als 100 potenzielle Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-146">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates.</span></span> <span data-ttu-id="bb7b3-147">Überprüfen Sie den Wert von [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) im [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) -Objekt, um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-147">To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) in the [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="bb7b3-148">Wenn der Wert true ist, gibt es keine weiteren möglichen Kandidaten; Wenn der Wert auf false festgelegt ist, hat die Methode nur den ersten 100 einer größeren Anzahl potenzieller Kandidaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-148">If the value is true, there are no more possible candidates; if the value is false, the method only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="bb7b3-149">Wenn Sie in einer großen Organisation arbeiten, ist es wahrscheinlich, dass ein Name wie "Dan" die maximale Anzahl von 100 Kandidaten zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-149">If you work in a large organization, it's likely that a name like "dan" will return the maximum number of 100 candidates.</span></span> <span data-ttu-id="bb7b3-150">Wenn Sie die Anzahl der zurückgegebenen Kandidaten reduzieren möchten, beschränken Sie die Suchfunktion.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-150">To reduce the number of candidates returned, limit where you search.</span></span> <span data-ttu-id="bb7b3-151">Im nächsten Beispiel wird die [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) -Aufzählung verwendet, um anzugeben, wo gesucht werden soll, um den nicht eindeutigen Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-151">The next example uses the [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) enumeration to specify where to search to resolve the ambiguous name.</span></span> 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="bb7b3-152">Wenn Sie Ihre Kontakte in einem anderen Ordner als dem bekannten Ordner Kontakte speichern, verwenden Sie eine der überladenen Methoden, um anzugeben, wo nach Kandidaten gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-152">If you store your contacts in a folder other than the well-known Contacts folder, use one of the overloaded methods to specify where to look for candidates.</span></span> <span data-ttu-id="bb7b3-153">Im folgenden Beispiel wird eine Ordnerliste für die **ResolveName** -Methode basierend auf der Ordner-ID erstellt.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-153">The following example creates a folder list for the **ResolveName** method based on the folder ID.</span></span> <span data-ttu-id="bb7b3-154">Die **Ordner** -Nr wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-154">The **FolderId** has been shortened for readability.</span></span> 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

<span data-ttu-id="bb7b3-155">Wenn Sie Filter anwenden und keine Kandidaten zurückgegeben werden, enthält die [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) NULL Einträge.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-155">If you apply filters and no candidates are returned, the [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) will contain zero entries.</span></span> <span data-ttu-id="bb7b3-156">Sie können dies überprüfen, indem Sie die [count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) -Eigenschaft der Auflistung betrachten.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-156">You can verify this by looking at the [Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) property of the collection.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a><span data-ttu-id="bb7b3-157">Auflösen von nicht eindeutigen Namen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="bb7b3-157">Resolve ambiguous names by using EWS</span></span>
<span data-ttu-id="bb7b3-158"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="bb7b3-158"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="bb7b3-159">Sie können den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) -EWS-Vorgang verwenden, um mögliche Kandidaten für einen nicht eindeutigen Namen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-159">You can use the [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to identify possible candidates for an ambiguous name.</span></span> <span data-ttu-id="bb7b3-160">Das [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) -Element enthält den eindeutigen Namen, den Sie auflösen möchten.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-160">The [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) element contains the ambiguous name you want to resolve.</span></span> <span data-ttu-id="bb7b3-161">Im folgenden Beispiel wird gezeigt, wie der Name Sadie aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-161">The following example shows how to resolve the name Sadie.</span></span> <span data-ttu-id="bb7b3-162">Dies ist auch die XML-Anforderung, die der verwaltete EWS-API verwendet, wenn Sie [die ResolveName-Methode verwenden](#bk_EWSMA), mit dem Unterschied, dass für gültige Ausgabe Beispiele ein anderer Name verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-162">This is also the XML request that the EWS Managed API uses when you [use the ResolveName method](#bk_EWSMA), except that it uses a different name for valid output examples.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="bb7b3-163">Die Antwort gibt maximal 100 Kandidaten zurück, obwohl es möglicherweise mehr als 100 potenzielle Kandidaten gibt, um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert des [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) -Attributs des [resolutionset](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) -Elements.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-163">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of the [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) attribute of the [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="bb7b3-164">Wenn der Wert true ist, gibt es keine weiteren möglichen Kandidaten; Wenn der Wert auf false festgelegt ist, hat der Vorgang nur den ersten 100 einer größeren Anzahl potenzieller Kandidaten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-164">If the value is true, there are no more possible candidates; if the value is false, the operation only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="bb7b3-165">Das folgende Beispiel zeigt die XML-Antwort, wenn ein Kandidat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-165">The following example shows the XML response when one candidate is found.</span></span> <span data-ttu-id="bb7b3-166">Denken Sie daran, dass das [resolutionset](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) bis zu 100 Kandidaten enthalten kann, wobei jedes durch das [Auflösungs](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) Element und dessen untergeordnete Elemente dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-166">Remember, the [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) can contain up to 100 candidates, each one represented by the [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) element and its child elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="bb7b3-167">Sie werden nicht immer mit Kandidaten für Ihren eindeutigen Namen kommen.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-167">You're not always going to come up with candidates for your ambiguous name.</span></span> <span data-ttu-id="bb7b3-168">Im folgenden Beispiel wird die XML-Antwort als Fehler angezeigt, wenn keine Kandidaten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="bb7b3-168">The following example shows the XML response, as an error, when no candidates are found.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="bb7b3-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb7b3-169">See also</span></span>


- [<span data-ttu-id="bb7b3-170">Personen und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="bb7b3-170">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="bb7b3-171">Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="bb7b3-171">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

