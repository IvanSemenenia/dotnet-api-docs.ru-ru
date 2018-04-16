### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a><span data-ttu-id="3c244-101">Рабочий процесс теперь создает исходное исключение вместо NullReferenceException в некоторых случаях</span><span class="sxs-lookup"><span data-stu-id="3c244-101">Workflow now throws original exception instead of NullReferenceException in some cases</span></span>

|   |   |
|---|---|
|<span data-ttu-id="3c244-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="3c244-102">Details</span></span>|<span data-ttu-id="3c244-103">В .NET Framework 4.6.2 и более ранних версий, если метод Execute действия рабочего процесса создает исключение с <code>null</code> значение для <xref:System.Exception.Message> , System.Activities рабочего процесса вызывает <xref:System.NullReferenceException?displayProperty=name>, маскировка исходное исключение. В .NET Framework 4.7 ранее маскированные исключения.</span><span class="sxs-lookup"><span data-stu-id="3c244-103">In the .NET Framework 4.6.2 and earlier versions, when the Execute method of a workflow activity throws an exception with a <code>null</code> value for the <xref:System.Exception.Message> property, the System.Activities Workflow runtime throws a <xref:System.NullReferenceException?displayProperty=name>, masking the original exception.In the .NET Framework 4.7, the previously masked exception is thrown.</span></span>|
|<span data-ttu-id="3c244-104">Предложение</span><span class="sxs-lookup"><span data-stu-id="3c244-104">Suggestion</span></span>|<span data-ttu-id="3c244-105">Если код основан на обработку <xref:System.NullReferenceException?displayProperty=name>, измените его, чтобы перехватывать исключения, которые могут быть созданы из настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="3c244-105">If your code relies on handling the <xref:System.NullReferenceException?displayProperty=name>, change it to catch the exceptions that could be thrown from your custom activities.</span></span>|
|<span data-ttu-id="3c244-106">Область</span><span class="sxs-lookup"><span data-stu-id="3c244-106">Scope</span></span>|<span data-ttu-id="3c244-107">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="3c244-107">Minor</span></span>|
|<span data-ttu-id="3c244-108">Версия</span><span class="sxs-lookup"><span data-stu-id="3c244-108">Version</span></span>|<span data-ttu-id="3c244-109">4.7</span><span class="sxs-lookup"><span data-stu-id="3c244-109">4.7</span></span>|
|<span data-ttu-id="3c244-110">Тип</span><span class="sxs-lookup"><span data-stu-id="3c244-110">Type</span></span>|<span data-ttu-id="3c244-111">Среда выполнения</span><span class="sxs-lookup"><span data-stu-id="3c244-111">Runtime</span></span>|
|<span data-ttu-id="3c244-112">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="3c244-112">Affected APIs</span></span>|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|
