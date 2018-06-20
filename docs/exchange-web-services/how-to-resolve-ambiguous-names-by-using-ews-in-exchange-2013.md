---
title: Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Erfahren Sie, wie die EWS Managed API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie die erste möglicher Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder eines Kontaktordners im Postfach des Benutzers.
ms.openlocfilehash: 05a88043083a27d2e6d445cd71e5f3919c5a775d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756989"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a><span data-ttu-id="1be47-103">Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="1be47-103">Resolve ambiguous names by using EWS in Exchange 2013</span></span>

<span data-ttu-id="1be47-104">Erfahren Sie, wie die EWS Managed API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie die erste möglicher Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder eines Kontaktordners im Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1be47-104">Learn how to use the EWS Managed API or EWS to resolve ambiguous names by getting possible matches from Active Directory Domain Services (AD DS) or a contacts folder in your user's mailbox.</span></span>
  
<span data-ttu-id="1be47-105">Ein Benutzer in Ihrer Organisation erhält eine handgeschriebenen Liste der Namen und Adressen für Mitarbeiter, die eine Schulung teilnahmen.</span><span class="sxs-lookup"><span data-stu-id="1be47-105">A user in your organization is given a hand-written list of names and addresses for employees that attended a training session.</span></span> <span data-ttu-id="1be47-106">Sie eine e-Mail mit einige zusätzliche Informationen an Personen in der Liste senden möchten, aber sie alle e-Mail-Adresse können nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1be47-106">They want to send an email with some additional information to people on the list, but they can't read everyone's email address.</span></span> <span data-ttu-id="1be47-107">Wenn Sie für Ihre Benutzer in Ihrer Anwendung dieses Problem zu beheben möchten, können EWS helfen.</span><span class="sxs-lookup"><span data-stu-id="1be47-107">If you want to solve this problem for your users in your application, EWS can help.</span></span> <span data-ttu-id="1be47-108">Sie können die [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgang verwenden, um eine Liste der möglichen Übereinstimmungen für eine Auswahl von Text, z. B. Teil eines Nachnamens zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1be47-108">You can use the [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API method or the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to return a list of potential matches for a selection of text, such as part of a last name.</span></span> <span data-ttu-id="1be47-109">Die zurückgegebenen Elemente möglicherweise öffentliche Benutzerpostfächer, Verteilergruppen und Kontakte.</span><span class="sxs-lookup"><span data-stu-id="1be47-109">The returned items can be public user mailboxes, distribution groups, and contacts.</span></span> 
  
<span data-ttu-id="1be47-110">Beachten Sie, dass Exchange e-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, in einem mehrwertigen Array speichert.</span><span class="sxs-lookup"><span data-stu-id="1be47-110">Note that Exchange saves email addresses with prefixed routing types, such as smtp or sip, in a multivalue array.</span></span> <span data-ttu-id="1be47-111">Die **ResolveName** -Methode und der **ResolveNames** Vorgang ausführen eine teilweise Übereinstimmung mit jeder Wert eines Arrays beim Hinzufügen der Routingtyp am Anfang der aufgelöste Name, beispielsweise "Sip: User1".</span><span class="sxs-lookup"><span data-stu-id="1be47-111">The **ResolveName** method and the **ResolveNames** operation perform a partial match against each value of that array when you add the routing type at the beginning of the unresolved name, such as "sip:User1".</span></span> <span data-ttu-id="1be47-112">Wenn Sie eine Routingtyp nicht angeben, wird die Methode oder der Vorgang standardmäßig auf smtp, ihm eine primäre SMTP-Adresseneigenschaft zuordnen und nicht durchsucht das mehrwertige Array.</span><span class="sxs-lookup"><span data-stu-id="1be47-112">If you don't specify a routing type, the method or operation will default to smtp, match it to a primary smtp address property, and not search the multivalue array.</span></span> <span data-ttu-id="1be47-113">Beispielsweise wenn Sie nach ' User1 suchen ' und nicht das Präfix "Sip" einschließen, erhalten Sie keine sip:User1@Contoso.com vorkommen, selbst wenn, die ein gültiges Postfach wird.</span><span class="sxs-lookup"><span data-stu-id="1be47-113">For example, if you search for User1 and do not include the sip prefix, you will not receive sip:User1@Contoso.com as a result, even if that is a valid mailbox.</span></span> 
  
<span data-ttu-id="1be47-114">Sie können nur eine mehrdeutigen Name in einer einzelnen Anforderung angeben.</span><span class="sxs-lookup"><span data-stu-id="1be47-114">You can only specify one ambiguous name in a single request.</span></span> <span data-ttu-id="1be47-115">Wenn Sie eine Liste von mehrdeutige Namen aufgelöst haben, müssen Sie die Liste durchlaufen, und rufen Sie die Methode oder der Vorgang für jeden Eintrag.</span><span class="sxs-lookup"><span data-stu-id="1be47-115">If you have a list of ambiguous names to resolve, you will need to loop through the list and call the method or operation for each entry.</span></span> <span data-ttu-id="1be47-116">Kandidaten aus eines Benutzers Kontakteordner müssen einen Wert ungleich Null-Element-ID, die dann in einem Aufruf der [Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) -Methode oder [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) Operation Anforderung verwendet werden kann, um zusätzliche Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1be47-116">Candidates from a user's Contacts folder will have a non-null item ID value, which can then be used in a [Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) method call or [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request to retrieve additional information.</span></span> <span data-ttu-id="1be47-117">Wenn der Kandidaten eine Verteilergruppe ist, können Sie die [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API-Methode oder [der ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS-Vorgangs zum Abrufen der Liste der Elemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="1be47-117">If the candidate is a distribution group, you can use the [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS operation to get the list of members.</span></span> <span data-ttu-id="1be47-118">Wenn der Parameter _ReturnContactDetails_ oder das **ReturnFullContactData** EWS-Attribut auf "true" Active Directory-Einträge, die über eine **ResolveName** -Methode zurückgegeben, festgelegt ist oder **ResolveNames** Vorgang zusätzliche Eigenschaften enthält Beschreiben des Kontakts.</span><span class="sxs-lookup"><span data-stu-id="1be47-118">If the  _returnContactDetails_ parameter or the **ReturnFullContactData** EWS attribute is set to true, Active Directory entries returned via a **ResolveName** method or **ResolveNames** operation will include additional properties that describe the contact.</span></span> <span data-ttu-id="1be47-119">Der Parameter _ReturnContactDetails_ oder das **ReturnFullContactData** -Attribut nicht Einfluss auf die Daten, die für Kontakte zurückgegeben wird und Kontaktgruppen.</span><span class="sxs-lookup"><span data-stu-id="1be47-119">The  _returnContactDetails_ parameter or the **ReturnFullContactData** attribute does not affect the data that is returned for contacts and contact groups.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a><span data-ttu-id="1be47-120">Lösen Sie mehrdeutige Namen auf, mithilfe von EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="1be47-120">Resolve ambiguous names by using EWS Managed API</span></span>
<span data-ttu-id="1be47-121"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="1be47-121"></span></span>

<span data-ttu-id="1be47-122">Die [ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) -Methode können Sie die um Kandidaten zu finden, die den mehrdeutigen Name entsprechen, den Sie weitergeben.</span><span class="sxs-lookup"><span data-stu-id="1be47-122">You can use the [ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) method to find candidates that match the ambiguous name you pass.</span></span> <span data-ttu-id="1be47-123">Überladungen der **ResolveName** -Methode können Sie die Kandidaten in fünf verschiedenen Arten gesucht.</span><span class="sxs-lookup"><span data-stu-id="1be47-123">You can use overloads of the **ResolveName** method to search for candidates in five different ways.</span></span> 
  
<span data-ttu-id="1be47-124">**In Tabelle 1. Überladene ResolveName-Methoden**</span><span class="sxs-lookup"><span data-stu-id="1be47-124">**Table 1. Overloaded ResolveName methods**</span></span>

|<span data-ttu-id="1be47-125">**Methode**</span><span class="sxs-lookup"><span data-stu-id="1be47-125">**Method**</span></span>|<span data-ttu-id="1be47-126">**Funktionsweise**</span><span class="sxs-lookup"><span data-stu-id="1be47-126">**How it works**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1be47-127">ResolveName(String)</span><span class="sxs-lookup"><span data-stu-id="1be47-127">ResolveName(String)</span></span>](http://msdn.microsoft.com/en-us/library/dd635548%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="1be47-128">Sucht Kontakte im Kontakteordner der Benutzer und der globalen Adressliste (GAL) – in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1be47-128">Finds contacts in the user's Contacts folder and the Global Address List (GAL) — in that order.</span></span> <span data-ttu-id="1be47-129">String-Variable ist die mehrdeutiger Name, den Sie zu beheben versuchen.</span><span class="sxs-lookup"><span data-stu-id="1be47-129">The string variable is the ambiguous name you are trying to resolve.</span></span>  <br/> |
|[<span data-ttu-id="1be47-130">ResolveName (Zeichenfolge, ResolveNameSearchLocation, Boolesch)</span><span class="sxs-lookup"><span data-stu-id="1be47-130">ResolveName(String, ResolveNameSearchLocation, Boolean)</span></span>](http://msdn.microsoft.com/en-us/library/dd634595%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="1be47-131">Sucht nach Kontakten in den Standardordner Kontakte und/oder der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="1be47-131">Finds contacts in the default Contacts folder and/or the Global Address List (GAL).</span></span> <span data-ttu-id="1be47-132">String-Wert ist der mehrdeutiger Name, der Speicherort der gibt den Ordner Kontakte und/oder der globalen Adressliste und der boolesche Wert gibt an, ob die vollständigen Kontaktinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1be47-132">The string value is the ambiguous name, the search location specifies the Contacts folder and/or the GAL, and the Boolean value indicates whether to return the full contact information.</span></span>  <br/> |
|[<span data-ttu-id="1be47-133">ResolveName (Zeichenfolge, ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="1be47-133">ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](http://msdn.microsoft.com/en-us/library/hh532803%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="1be47-134">Sucht nach Kontakten in den Standardordner Kontakte und/oder der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="1be47-134">Finds contacts in the default Contacts folder and/or Global Address List (GAL).</span></span> <span data-ttu-id="1be47-135">Mit dieser Methode können Sie die Eigenschaften festlegen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1be47-135">This method enables you to set the properties that are returned.</span></span>  <br/> |
|[<span data-ttu-id="1be47-136">ResolveName (String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)</span><span class="sxs-lookup"><span data-stu-id="1be47-136">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)</span></span>](http://msdn.microsoft.com/en-us/library/dd636014%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="1be47-137">Sucht nach Kontakten in angegebenen Kontaktordner und/oder der globalen Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="1be47-137">Finds contacts in specified contact folders and/or the Global Address List (GAL).</span></span> <span data-ttu-id="1be47-138">Mit dieser Methode können Sie um eine Auflistung von Ordner für die Suche zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="1be47-138">You can use this method to pass a collection of folders to search.</span></span> <span data-ttu-id="1be47-139">So können Sie Kontaktordner als den Standardordner Kontakte durchsucht.</span><span class="sxs-lookup"><span data-stu-id="1be47-139">This enables you to look in contact folders other than the default Contacts folder.</span></span>  <br/> |
|[<span data-ttu-id="1be47-140">ResolveName (String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)</span><span class="sxs-lookup"><span data-stu-id="1be47-140">ResolveName(String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)</span></span>](http://msdn.microsoft.com/en-us/library/hh532581%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="1be47-141">Sucht nach Kontakten in der globalen Adressliste (GAL) und/oder in bestimmten Ordnern Kontakt.</span><span class="sxs-lookup"><span data-stu-id="1be47-141">Finds contacts in the Global Address List (GAL) and/or in specific contact folders.</span></span> <span data-ttu-id="1be47-142">Mit dieser Methode können Sie die Eigenschaften festlegen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1be47-142">This method enables you to set the properties that are returned.</span></span>  <br/> |
   
<span data-ttu-id="1be47-143">Wir beginnen mit ein einfaches Beispiel.</span><span class="sxs-lookup"><span data-stu-id="1be47-143">Let's start with a simple example.</span></span> <span data-ttu-id="1be47-144">Im folgenden Beispiel wird veranschaulicht, wie die Zeichenfolge "Dan" auflösen und Ausgabe der Name und e-Mail-Adresse des einzelnen Candidate gefunden.</span><span class="sxs-lookup"><span data-stu-id="1be47-144">The following example shows how to resolve the text string "dan" and output the name and email address of each candidate found.</span></span> <span data-ttu-id="1be47-145">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1be47-145">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="1be47-146">Die Antwort gibt maximal 100 Kandidaten, obwohl möglicherweise mehr als 100 potenzielle Kandidaten zurück.</span><span class="sxs-lookup"><span data-stu-id="1be47-146">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates.</span></span> <span data-ttu-id="1be47-147">Um zu bestimmen, ob nur die ersten 100 Kandidaten für eine größere Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert des [IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) im [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1be47-147">To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of [IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) in the [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="1be47-148">Wenn der Wert true ist, sind keine weiteren mögliche Kandidaten; Wenn der Wert false ist, zurückgegeben, die-Methode nur die ersten 100 für eine größere Anzahl von potenziellen Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="1be47-148">If the value is true, there are no more possible candidates; if the value is false, the method only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="1be47-149">Wenn Sie in einer großen Organisation arbeiten, ist es wahrscheinlich, dass ein Namen wie "Dan" die maximale Anzahl von 100 Kandidaten zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1be47-149">If you work in a large organization, it's likely that a name like "dan" will return the maximum number of 100 candidates.</span></span> <span data-ttu-id="1be47-150">Um die Anzahl der zurückgegebenen Kandidaten zu reduzieren, einschränken Sie, in dem Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="1be47-150">To reduce the number of candidates returned, limit where you search.</span></span> <span data-ttu-id="1be47-151">Das nächste Beispiel verwendet die [ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) -Aufzählung, um anzugeben, wo Sie suchen, um den mehrdeutige Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="1be47-151">The next example uses the [ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) enumeration to specify where to search to resolve the ambiguous name.</span></span> 
  
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

<span data-ttu-id="1be47-152">Wenn Sie Ihre Kontakte in einem anderen Ordner als den bekannten Kontakteordner speichern, verwenden Sie eine der überladenen Methoden um wo Kandidaten gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="1be47-152">If you store your contacts in a folder other than the well-known Contacts folder, use one of the overloaded methods to specify where to look for candidates.</span></span> <span data-ttu-id="1be47-153">Das folgende Beispiel erstellt eine Ordnerliste für die **ResolveName** -Methode basierend auf den Ordner-ID.</span><span class="sxs-lookup"><span data-stu-id="1be47-153">The following example creates a folder list for the **ResolveName** method based on the folder ID.</span></span> <span data-ttu-id="1be47-154">Die **FolderId** wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="1be47-154">The **FolderId** has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="1be47-155">Wenn Sie Filter anwenden und keine Kandidaten zurückgegeben werden, wird die [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) NULL Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="1be47-155">If you apply filters and no candidates are returned, the [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) will contain zero entries.</span></span> <span data-ttu-id="1be47-156">Sie können dies überprüfen, indem Sie die [Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) -Eigenschaft der Auflistung ansehen.</span><span class="sxs-lookup"><span data-stu-id="1be47-156">You can verify this by looking at the [Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) property of the collection.</span></span> 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a><span data-ttu-id="1be47-157">Lösen Sie mehrdeutige Namen auf, mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="1be47-157">Resolve ambiguous names by using EWS</span></span>
<span data-ttu-id="1be47-158"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="1be47-158"></span></span>

<span data-ttu-id="1be47-159">[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgangs können Sie um mögliche Kandidaten für ein mehrdeutiger Name zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1be47-159">You can use the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS operation to identify possible candidates for an ambiguous name.</span></span> <span data-ttu-id="1be47-160">Das [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) -Element enthält den mehrdeutigen Name, den Sie zu beheben möchten.</span><span class="sxs-lookup"><span data-stu-id="1be47-160">The [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) element contains the ambiguous name you want to resolve.</span></span> <span data-ttu-id="1be47-161">Im folgenden Beispiel wird gezeigt, wie den Namen Sadie aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="1be47-161">The following example shows how to resolve the name Sadie.</span></span> <span data-ttu-id="1be47-162">Dies ist auch die XML-Anfrage, die die EWS Managed API verwendet, wenn Sie die [Verwendung der ResolveName-Methode](#bk_EWSMA), außer dass sie einen anderen Namen für Beispiele gültiger verwendet.</span><span class="sxs-lookup"><span data-stu-id="1be47-162">This is also the XML request that the EWS Managed API uses when you [use the ResolveName method](#bk_EWSMA), except that it uses a different name for valid output examples.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="1be47-163">Die Antwort zurückgegeben maximal 100 Kandidaten, obwohl möglicherweise mehr als 100 potenzielle Kandidaten zu bestimmen, ob nur die ersten 100 Kandidaten für eine größere Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert der [IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) -Attribut des [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) -Elements.</span><span class="sxs-lookup"><span data-stu-id="1be47-163">The response returns a maximum of 100 candidates, although there might be more than 100 potential candidates To determine whether only the first 100 candidates of a larger number of candidates were returned, check the value of the [IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) attribute of the [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="1be47-164">Wenn der Wert true ist, sind keine weiteren mögliche Kandidaten; Wenn der Wert false ist, zurückgegeben, der Vorgang nur die ersten 100 für eine größere Anzahl von potenziellen Kandidaten.</span><span class="sxs-lookup"><span data-stu-id="1be47-164">If the value is true, there are no more possible candidates; if the value is false, the operation only returned the first 100 of a larger number of potential candidates.</span></span> 
  
<span data-ttu-id="1be47-165">Das folgende Beispiel zeigt die XML-Antwort, wenn eine in Frage kommende gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1be47-165">The following example shows the XML response when one candidate is found.</span></span> <span data-ttu-id="1be47-166">Beachten Sie, dass die [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) bis zu 100 Kandidaten, jeweils, die durch die [Lösung](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) -Element und dessen untergeordnete Elemente enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="1be47-166">Remember, the [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) can contain up to 100 candidates, each one represented by the [Resolution](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) element and its child elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="1be47-167">Sie nun nicht immer mit Kandidaten für Ihre mehrdeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="1be47-167">You're not always going to come up with candidates for your ambiguous name.</span></span> <span data-ttu-id="1be47-168">Das folgende Beispiel zeigt die XML-Antwort als Fehler, wenn keine Kandidaten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1be47-168">The following example shows the XML response, as an error, when no candidates are found.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="see-also"></a><span data-ttu-id="1be47-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1be47-169">See also</span></span>


- [<span data-ttu-id="1be47-170">Benutzer und Kontakte in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="1be47-170">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="1be47-171">Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="1be47-171">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

