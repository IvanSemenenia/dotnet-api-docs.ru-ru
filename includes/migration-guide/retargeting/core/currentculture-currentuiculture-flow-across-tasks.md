### <a name="currentculture-and-currentuiculture-flow-across-tasks"></a><span data-ttu-id="157e8-101">Поток CurrentCulture и CurrentUICulture между задачами</span><span class="sxs-lookup"><span data-stu-id="157e8-101">CurrentCulture and CurrentUICulture flow across tasks</span></span>

|   |   |
|---|---|
|<span data-ttu-id="157e8-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="157e8-102">Details</span></span>|<span data-ttu-id="157e8-103">Начиная с .NET Framework 4.6 <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> и <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> хранятся в потоке <xref:System.Threading.ExecutionContext?displayProperty=name>, который проходит через асинхронные операции. Это означает, что изменения <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> или <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> будут отражены в задачах, которые позже выполняются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="157e8-103">Beginning in the .NET Framework 4.6, <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> and <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> are stored in the thread's <xref:System.Threading.ExecutionContext?displayProperty=name>, which flows across asynchronous operations.This means that changes to <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> or <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> will be reflected in tasks which are later run asynchronously.</span></span> <span data-ttu-id="157e8-104">Это поведение отличается от поведения предыдущих версий платформы .NET Framework (который будет сбросить <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> и <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> все асинхронные задачи).</span><span class="sxs-lookup"><span data-stu-id="157e8-104">This is different from the behavior of previous .NET Framework versions (which would reset <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> and <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> in all asynchronous tasks).</span></span>|
|<span data-ttu-id="157e8-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="157e8-105">Suggestion</span></span>|<span data-ttu-id="157e8-106">Это изменение затрагивает приложения может обойти ее, явно задав нужный <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> или <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> в качестве первой операции в асинхронной задачи.</span><span class="sxs-lookup"><span data-stu-id="157e8-106">Apps affected by this change may work around it by explicitly setting the desired <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> or <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name> as the first operation in an async Task.</span></span> <span data-ttu-id="157e8-107">Кроме того, старое поведение (не передачи <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) может быть согласие, задав следующий параметр совместимости:</span><span class="sxs-lookup"><span data-stu-id="157e8-107">Alternatively, the old behavior (of not flowing <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>/<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) may be opted into by setting the following compatibility switch:</span></span><pre><code class="language-C#">AppContext.SetSwitch(&quot;Switch.System.Globalization.NoAsyncCurrentCulture&quot;, true);&#13;&#10;</code></pre><span data-ttu-id="157e8-108">Эта проблема была устранена в WPF в .NET Framework 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="157e8-108">This issue has been fixed by WPF in .NET Framework 4.6.2.</span></span> <span data-ttu-id="157e8-109">Она также была устранена в .NET Frameworks 4.6 4.6.1 через [3139549 КБ](https://support.microsoft.com/kb/3139549).</span><span class="sxs-lookup"><span data-stu-id="157e8-109">It has also been fixed in .NET Frameworks 4.6, 4.6.1 through [KB 3139549](https://support.microsoft.com/kb/3139549).</span></span> <span data-ttu-id="157e8-110">Приложения, предназначенные для .NET 4.6 или более поздней версии автоматически получают правой поведение в приложениях WPF - <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name> / <xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) будет сохранено в рамках операциях диспетчера.</span><span class="sxs-lookup"><span data-stu-id="157e8-110">Applications targeting .NET 4.6 or later will automatically get the right behavior in WPF applications - <xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=name>/<xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=name>) would be preserved across Dispatcher operations.</span></span>|
|<span data-ttu-id="157e8-111">Область</span><span class="sxs-lookup"><span data-stu-id="157e8-111">Scope</span></span>|<span data-ttu-id="157e8-112">Дополнительный номер</span><span class="sxs-lookup"><span data-stu-id="157e8-112">Minor</span></span>|
|<span data-ttu-id="157e8-113">Версия</span><span class="sxs-lookup"><span data-stu-id="157e8-113">Version</span></span>|<span data-ttu-id="157e8-114">4.6</span><span class="sxs-lookup"><span data-stu-id="157e8-114">4.6</span></span>|
|<span data-ttu-id="157e8-115">Тип</span><span class="sxs-lookup"><span data-stu-id="157e8-115">Type</span></span>|<span data-ttu-id="157e8-116">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="157e8-116">Retargeting</span></span>|
|<span data-ttu-id="157e8-117">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="157e8-117">Affected APIs</span></span>|<ul><li><xref:System.Globalization.CultureInfo.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentCulture?displayProperty=nameWithType></li><li><xref:System.Globalization.CultureInfo.CurrentUICulture?displayProperty=nameWithType></li><li><xref:System.Threading.Thread.CurrentUICulture?displayProperty=nameWithType></li></ul>|
