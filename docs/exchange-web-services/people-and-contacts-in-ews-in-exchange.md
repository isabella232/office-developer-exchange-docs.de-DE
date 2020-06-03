---
title: Personen und Kontakte in EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 043c33be-a0d1-4bad-a840-85715eda4813
description: Erfahren Sie mehr über Personas, den einheitlichen Kontaktspeicher und wie Sie mit Kontakten arbeiten können, indem Sie das verwaltete EWS-API oder EWS in Exchange verwenden.
localization_priority: Priority
ms.openlocfilehash: f0590a0d8a99b8320cc1b316829177e05e443de6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457673"
---
# <a name="people-and-contacts-in-ews-in-exchange"></a>Personen und Kontakte in EWS in Exchange

Erfahren Sie mehr über Personas, den einheitlichen Kontaktspeicher und wie Sie mit Kontakten arbeiten können, indem Sie das verwaltete EWS-API oder EWS in Exchange verwenden. 
  
Kontakte sind Elemente in Exchange, die Informationen über eine Person, eine Gruppe oder eine Organisation speichern. Kontakte können Namen und e-Mail-Adressen sowie andere Informationen enthalten, einschließlich Chat Adressen, physische Adressen, Geburtstage, Familieninformationen und ein Foto oder Bild, das den Kontakt darstellt.
  
Kontaktinformationen werden an einem von zwei Orten gespeichert:
  
- Active Directory-Domänendienste (AD DS), wenn sich der Kontakt innerhalb der Organisation befindet.
    
- Der Ordner "Kontakte" oder ein anderer Ordner im Postfach eines Benutzers, wenn sich der Kontakt außerhalb der Organisation befindet.
    
Mehrere Kontaktelemente können eine einzelne Person darstellen. Exchange verwendet Personas, um diese verschiedenen Kontaktelemente zusammenzubringen. Bei einer *Persona* handelt es sich um eine Aggregation von Kontaktinformationen für dieselbe Person aus unterschiedlichen Quellen. Zusätzlich zu den Kontaktinformationen in Exchange können Personas auch aus Informationen im Empfängercache für das Postfach aggregiert werden, einem verborgenen Ordner für Chat-Kontakte namens QuickContacts und aus Drittanbieter-Datenquellen. Mit dem einheitlichen Kontaktspeicher in Exchange können Chat Clients diese Aggregation verwenden; der einzige Unterschied besteht darin, dass der einheitliche Kontaktspeicher keine Informationen aus AD DS aggregiert, wie in Abbildung 1 dargestellt. 
  
**Abbildung 1. Kontakt Informationsquellen für Personas und für den einheitlichen Kontaktspeicher**

![Eine Abbildung, welche die Quellen, die in Personas aggregiert werden, den Quellen gegenüberstellt, die im einheitlichen Kontaktspeicher enthalten sind. Der einheitliche Kontaktspeicher aggregiert keine Kontaktinformationen aus dem Verzeichnisdienst.](media/EX15_PersonaOverview.png)
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Arbeiten mit Kontakten**

|**Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode**|**Zu verwendender EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen eines neuen Kontakts  <br/> |Instanziieren eines neuen [Kontakt](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) Objekts und Verwenden von [Contact. Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) <br/> |
|Kopieren eines Kontakts  <br/> |[Contact. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.copy%28v=exchg.80%29.aspx) <br/> |[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Einen Kontakt verlagern  <br/> |[Contact. Migration](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.move%28v=exchg.80%29.aspx) <br/> |[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|Aktualisieren eines vorhandenen Kontakts  <br/> |[Contact. Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) und [Contact. Update](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.update%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/298fdd71-a83d-4407-9728-4f0a8e2d857c%28Office.15%29.aspx) <br/> |
|Löschen eines Kontakts  <br/> |[Contact. Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) und [Contact. Delete](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.delete%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
|Suchen nach einem Kontakt  <br/> |[ExchangeService.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
|Suchen nach Personen  <br/> |–  <br/> |[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |
|Erweitern einer Verteilergruppe  <br/> |[Datei "ExchangeService. expandgroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |
|Auflösen eines nicht eindeutigen Namens  <br/> |[Datei "ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |
|Abrufen einer Persona  <br/> |–  <br/> |[GetPersona](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |
|Arbeiten mit Kontaktfotos  <br/> |[Contact. SetContactPicture](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.setcontactpicture%28v=exchg.80%29.aspx), [Contact. GetContactPictureAttachment](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.getcontactpictureattachment%28v=exchg.80%29.aspx)oder [Contact. RemoveContactPicture](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.setcontactpicture%28v=exchg.80%29.aspx) <br/> |[GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) oder [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/> |
   
## <a name="personas"></a>Personas
<a name="PEOPLESEARCH"> </a>

Bis vor kurzem wurden Kontakte häufig an einem einzelnen Speicherort gespeichert – in der Regel auf einem e-Mail-Client. Heute wird es häufiger, Kontakte an vielen verschiedenen Orten zu speichern, beispielsweise auf einem Telefon, auf einer Website für soziale Netzwerke, in einem Kontakteordner in einem Exchange-Postfach oder im Verzeichnisdienst einer Organisation. Durch die Verbreitung von Kontaktinformationen ist es möglich, dass mehrere Kontakte, die dieselbe Person darstellen, unterschiedliche Informationen enthalten; Beispielsweise kann ein Kontakt eine geschäftliche Telefonnummer und eine andere eine persönliche Telefonnummer oder ein Kontakt, der in einem Kontakteordner gespeichert ist, möglicherweise einen anderen Namen haben als der Kontakt für dieselbe Person, die auf Ihrem Telefon gespeichert ist.
  
In Exchange Online Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, die mit Exchange 2013 beginnen, Kontakte aus unterschiedlichen Quellen, die dieselbe Person darstellen, miteinander verknüpft sind, ähnlich der Art und Weise, in der e-Mail-Nachrichten in Unterhaltungen aggregiert werden, mithilfe einer gemeinsamen Link-ID. Wenn aggregierte Kontaktinformationen von einem Exchange-Server zurückgegeben werden, enthält Sie eine Reihe von Attributen für jeden Kontakt, beispielsweise einen Quellordner, einen Anzeigenamen, eine ID und eine Quell-ID. Die Summe der zurückgegebenen Eigenschaften und Attribute wird als Persona bezeichnet, und die zurückgegebene Eigenschaftsgruppe wird als [Shape der Rolle](https://msdn.microsoft.com/library/61d87cd5-3270-40d1-bab7-d0d5bf938607%28Office.15%29.aspx)bezeichnet.
  
Da die Informationen, aus denen eine persona besteht, nicht an einem einzelnen Speicherort gespeichert werden und diese Informationen jederzeit geändert werden können, wird eine persona nur erstellt, wenn Sie eine Anforderung an einen Exchange-Server stellen. Sie verwenden den [FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) -EWS-Vorgang, um eine persona-Suchanforderung zu erstellen. Ihre Anforderung kann eine Sortierreihenfolge enthalten und kann gemäß einer Abfragezeichenfolge gefiltert werden, damit Sie die richtige Persona durch Sortieren und Filtern der Ergebnisse finden. Sie können beispielsweise den Anzeigenamen und eine Gruppe aller e-Mail-Adressen abrufen, die einem bestimmten Kontakt aus dem Ordner Kontakte, einem Hotmail-Konto, einem LinkedIn Konto und dem Verzeichnisdienst eines Unternehmens zugeordnet sind, oder Sie können eine Gruppe aller Personen mit Chat Adressen abrufen. Die Verknüpfung von Kontakten in Personas erfolgt automatisch basierend auf einem Algorithmus, der eine Beziehung zwischen auf verschiedenen Geräten gespeicherten Kontakten erkennt. 
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
**Tabelle 2. EWS-Vorgänge für das Arbeiten mit Personas**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Gibt alle verfügbaren Personen aus einem angegebenen Kontaktordner zurück oder ruft Kontakte ab, die mit einer bestimmten Abfragezeichenfolge übereinstimmen.  <br/> |
|[GetPersona](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Gibt eine Gruppe von Eigenschaften zurück, die einer bestimmten Rolle zugeordnet sind, beispielsweise alle Chat Adressen oder Anzeigenamen für eine angegebene Persona ID.  <br/> |
   
Sie können die **getpersona** -und **FindPeople** -Vorgänge verwenden, um Kontaktinformationen aus mehreren Quellen effizient abzurufen. Da alle Elemente im Zusammenhang mit einer Rolle einer Link-ID zugeordnet sind, können Sie diese Vorgänge in einer Vielzahl von Anwendungen verwenden, die Kontaktdaten verwenden. Im Folgenden finden Sie einige Beispiele: 
  
- Eine Mobiltelefon-APP, die den Vorgang " **getpersona** " verwendet, wenn ein Benutzer einen Kontakt anruft, und dann zusätzliche Telefonnummern für Anrufe anbietet, falls niemand antwortet. 
    
- Eine Anwendung, die den **FindPeople** -Vorgang zum Überprüfen von Posteingang-Nachrichten für e-Mail-Adressen verwendet, um zu bestimmen, ob Sie in einer vorhandenen Persona gefunden werden. Adressen, die noch nicht mit einer Persona verknüpft sind, können zum Erstellen von Verkaufsleads oder zum Auflisten aller aktuellen Kommunikationen mit der Person verwendet werden, die von dieser Rolle dargestellt wird. 
    
- [Eine Mail-App für Outlook](mail-apps-for-outlook-and-ews-in-exchange.md) , die unterschiedliche Begrüßungen anbietet, je nachdem, ob die Korrespondenz formell oder informell ist. Formelle Begrüßungen werden von den Anzeigenamen aus dem Verzeichnisdienst bereitgestellt, und formlose Begrüßungen stammen aus dem Anzeigenamen, der aus sozialen Netzwerkkontakten stammt. 
    
## <a name="unified-contact-store"></a>Einheitlicher Kontaktspeicher
<a name="PEOPLESEARCH"> </a>

Personas sind nicht nur auf einen e-Mail-Client limitiert. Wenn Sie einen Chat-Client entwickeln, können Sie sich eine oder alle der folgenden Fragen stellen:
  
- Wie kann ich lync-Clientanwendungen mit einer Standardgruppe von Chat Kontaktelementen anbieten?
    
- Wie kann ich Chat Kontakt-und Gruppen Listen verwalten?
    
- Wie kann ich den benutzerdefinierten lync-Clientzugriff für Chat-Kontakte und Chatgruppen verwalten?
    
Der einheitliche Kontaktspeicher arbeitet hinter den Kulissen in Exchange, um Kontaktdaten aus Exchange und anderen Quellen in einer einzelnen Entität oder Persona zusammenzufassen. Obwohl die EWS-Vorgänge, die Sie für den Zugriff auf den einheitlichen Kontaktspeicher verwenden, für Chatkontakte spezifisch sind, können Sie den einheitlichen Kontaktspeicher in Exchange verwenden, um mit Personas in allen Arten von Anwendungen zu arbeiten. Beachten Sie, dass der einheitliche Kontaktspeicher nicht auf Kontaktdaten AD DS zugreifen kann.
  
Chat-Kontakte werden in einem verborgenen Ordner namens QuickContacts gespeichert. Sie können die **AddNewImContactToGroup** -und **AddImContactToGroup** -Vorgänge verwenden, um Kontakte zu Gruppen hinzuzufügen, die in diesem verborgenen Ordner gespeichert sind. Da Sie den einheitlichen Kontaktspeicher zum Gruppieren von Chat Kontakten verwenden können, können Sie einfacher auf Kontaktgruppen zugreifen und diese aktualisieren. 
  
> [!NOTE]
> Die verwaltete EWS-API implementiert diese Funktion nicht. 
  
**Tabelle 3. EWS-Vorgänge für den Zugriff auf den einheitlichen Kontaktspeicher**

|**Name des Vorgangs**|**Beschreibung**|
|:-----|:-----|
|[AddNewImContactToGroup](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Fügt einer Chatgruppe einen neuen Chat Kontakt hinzu, maximal 1000 Kontakte.  <br/> |
|[AddImContactToGroup](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Fügt einer Chatgruppe einen vorhandenen Chat Kontakt mit maximal 1000 Kontakten hinzu.  <br/> |
|[AddImGroup](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Fügt eine neue Chatgruppe hinzu, maximal 64 Gruppen.  <br/> |
|[AddDistributionGroupToImList](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Fügt einer Sofortnachrichten Gruppe eine neue Verteilergruppe hinzu, maximal 64 Gruppen.  <br/> |
|[GetImItemList](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Ruft eine Liste von Chatgruppen und Chat Kontaktpersonen ab.  <br/> |
|[GetImItems](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Ruft Informationen zu bestimmten Chatgruppen und Chat Kontaktpersonen ab.  <br/> |
|[RemoveContactFromImList](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Entfernt einen Kontakt aus einer Chatgruppe.  <br/> |
|[RemoveImContactFromGroup](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Entfernt einen Chat Kontakt aus einer Chatgruppe.  <br/> |
|[RemoveDistributionGroupFromImList](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Entfernt eine Verteilergruppe aus einer Chatgruppe.  <br/> |
|[RemoveImGroup](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Entfernt eine Chatgruppe.  <br/> |
|[SetImGroup](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Ändert den Anzeigenamen einer Chatgruppe.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="PEOPLESEARCH"> </a>

- [Verarbeiten von Kontakten in Batches mithilfe von EWS in Exchange](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    
- [Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    
- [Abrufen von Benutzerfotos mithilfe von EWS in Exchange](how-to-get-user-photos-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch
<a name="PEOPLESEARCH"> </a>

- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Verwenden von Webdiensten in Exchange](start-using-web-services-in-exchange.md)
    
- [Übersicht über den EWS-Cliententwurf für Exchange](ews-client-design-overview-for-exchange.md)
    

