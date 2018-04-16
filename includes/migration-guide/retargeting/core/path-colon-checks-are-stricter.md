### <a name="path-colon-checks-are-stricter"></a><span data-ttu-id="5f64d-101">Применяются более строгие двоеточие проверку путей</span><span class="sxs-lookup"><span data-stu-id="5f64d-101">Path colon checks are stricter</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5f64d-102">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="5f64d-102">Details</span></span>|<span data-ttu-id="5f64d-103">В .NET Framework 4.6.2 было внесено несколько изменений для поддержки ранее неподдерживаемые пути (как в формате и длина).</span><span class="sxs-lookup"><span data-stu-id="5f64d-103">In .NET Framework 4.6.2, a number of changes were made to support previously unsupported paths (both in length and format).</span></span> <span data-ttu-id="5f64d-104">Проверяет синтаксис диска разделителя (двоеточие) были внесены правильным, которой был побочный эффект для блокировки некоторых пути URI в несколько интерфейсов API выберите путь, где они используются для сбоев.</span><span class="sxs-lookup"><span data-stu-id="5f64d-104">Checks for proper drive separator (colon) syntax were made more correct, which had the side effect of blocking some URI paths in a few select Path APIs where they used to be tolerated.</span></span>|
|<span data-ttu-id="5f64d-105">Предложение</span><span class="sxs-lookup"><span data-stu-id="5f64d-105">Suggestion</span></span>|<span data-ttu-id="5f64d-106">Если передача URI в затронутых интерфейсы API, измените строку возвратят допустимый путь.</span><span class="sxs-lookup"><span data-stu-id="5f64d-106">If passing a URI to affected APIs, modify the string to be a legal path first.</span></span><ul><li><span data-ttu-id="5f64d-107">Удаление схемы из URL-адресов вручную (например, удалите <code>file://</code> из URL-адресов)</span><span class="sxs-lookup"><span data-stu-id="5f64d-107">Remove the scheme from URLs manually (e.g. remove <code>file://</code> from URLs)</span></span></li><li><span data-ttu-id="5f64d-108">Передать URI в <xref:System.Uri> класса и использовать <xref:System.Uri.LocalPath></span><span class="sxs-lookup"><span data-stu-id="5f64d-108">Pass the URI to the <xref:System.Uri> class and use <xref:System.Uri.LocalPath></span></span></li></ul><span data-ttu-id="5f64d-109">Кроме того, можно отключить новый путь нормализации, задав <code>Switch.System.IO.UseLegacyPathHandling</code> параметров AppContext переключатель в значение true.</span><span class="sxs-lookup"><span data-stu-id="5f64d-109">Alternatively, you can opt out of the new path normalization by setting the <code>Switch.System.IO.UseLegacyPathHandling</code> AppContext switch to true.</span></span>|
|<span data-ttu-id="5f64d-110">Область</span><span class="sxs-lookup"><span data-stu-id="5f64d-110">Scope</span></span>|<span data-ttu-id="5f64d-111">Пограничный случай</span><span class="sxs-lookup"><span data-stu-id="5f64d-111">Edge</span></span>|
|<span data-ttu-id="5f64d-112">Версия</span><span class="sxs-lookup"><span data-stu-id="5f64d-112">Version</span></span>|<span data-ttu-id="5f64d-113">4.6.2</span><span class="sxs-lookup"><span data-stu-id="5f64d-113">4.6.2</span></span>|
|<span data-ttu-id="5f64d-114">Тип</span><span class="sxs-lookup"><span data-stu-id="5f64d-114">Type</span></span>|<span data-ttu-id="5f64d-115">Изменение целевой платформы</span><span class="sxs-lookup"><span data-stu-id="5f64d-115">Retargeting</span></span>|
|<span data-ttu-id="5f64d-116">Затронутые API</span><span class="sxs-lookup"><span data-stu-id="5f64d-116">Affected APIs</span></span>|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|
