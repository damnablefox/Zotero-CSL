# 文件重命名
Zotero 会根据父条目的书目详细信息（标题、作者等）自动重命名保存到您文献库中的 PDF 和其他文件，让您无需费力整理一堆随机命名的文件，也无需手动将每个新文件重命名为您偏好的格式。

Zotero 始终会重命名从网络保存的文件（通过 Zotero 连接器、通过标识符添加条目或查找可用 PDF）。

默认情况下，它还会重命名您添加到条目的第一个存储的 PDF 和 EPUB，以及它成功检索到元数据的文件。您可以通过在 Zotero 设置常规窗格中取消选中“使用父元数据自动重命名附件文件”（在 Zotero 8 中为“自动重命名文件”）来禁用此功能。如果一个条目已有附件，则不会自动重命名其他文件，以避免更改补充材料的文件名。

从 Zotero 8 开始，当您更改父条目元数据（例如，更改标题）时，Zotero 将保持附件文件名同步。在以前的版本中，您需要右键单击附件并选择“根据父元数据重命名文件”，以便在编辑元数据后更新文件名。

默认情况下，链接文件不会自动重命名，但您可以启用“重命名链接的文件”设置，以将重命名也应用于这些文件。

您可以使用“重命名以下类型的文件”来调整哪些文件类型会被自动重命名。

## 附件标题 vs. 文件名
被重命名的附件文件名与条目列表中显示的附件标题是不同的。有关更多信息，请参阅[附件标题 vs. 文件名]。

>[附件标题 vs. 文件名]:https://www.zotero.org/support/kb/attachment_title_vs_filename

## 自定义文件名格式
默认情况下，Zotero 根据父条目的创作者（1-2 位作者或编辑）、年份和标题来命名文件：

`Lee et al. - 2023 - The First Room-Temperature Ambient-Pressure Superconductor.pdf`

虽然 Zotero 一直都有自动重命名文件的功能，但 Zotero 7 引入了一种新的、强大的语法来自定义文件名。您可以在 Zotero 设置的常规窗格中自定义默认格式。

这是默认的模板字符串：

`{{ firstCreator suffix=" - " }}{{ year suffix=" - " }}{{ title truncate="100" }}`

支持以下变量和参数：

### 变量
| 变量 | 描述 |
| :--- | :--- |
| `authors`         | 父条目的主要创作者（取决于条目类型，这些是作者或艺术家，但不包括编辑或其他贡献者）。 |
| `authorsCount`    | 父条目主要创作者的数量。（Zotero 7.0.16） |
| `editors`         | 父条目的编辑。 |
| `editorsCount`    | 父条目编辑的数量。（Zotero 7.0.16） |
| `creators`        | 父条目的所有创作者。 |
| `creatorsCount`   | 父条目所有创作者的总数。（Zotero 7.0.16） |
| `firstCreator`    | 父条目的创作者（1-2 位作者或编辑），与“创作者”列的值相同。 |
| `itemType`        | 父条目类型。可识别的条目类型完整列表可在此处找到。 |
| `attachmentTitle` | 正在被重命名或创建的附件的标题。 |
| `year`            | 年份，从父条目的日期字段中提取。 |
| `accessDate`      | UTC 格式的访问日期，如果存在 `timeZone` 参数，则转换为指定的时区。（Zotero 8） |
| 任何条目字段      | 字段的完整列表可在此页面底部找到。 |

如果变量值的开头或结尾包含空格（当与 `truncate` 参数一起使用时很可能发生），这些空格会从文件名中移除。

### 参数
| 参数 | 适用的变量 | 默认值 | 描述 |
| :--- | :--------- | :----- | :--- |
| `start`               | 所有         |              | 省略字符数。     <br> 将变量值省略前N个字符。例如，`{{ title    start="10" }}` 将被替换为父条目标题的值，但要省略前 10 个字符。它可以与 `truncate` 结合使用。 |
| `truncate`            | 所有         |              | 保留字符数。     <br> 将变量值保留前N个字符。例如，`{{ title truncate="10" }}` 将被替换为父条目标题的值，但只保留前 10 个字符。参数 `truncate` 在除 `prefix`、`suffix` 和 `case` 之外的所有其他参数应用之后进行。 |
| `prefix`              | 所有         |              | 前缀。           <br> 在变量前加上给定的字符。例如，`{{ title prefix="title" }}` 将被替换为父条目标题前加单词“title”。如果变量为空（例如，条目的父级没有标题），则整个语句（包括前缀）将被忽略。 |
| `suffix`              | 所有         |              | 后缀。           <br> 在变量后追加给定的字符。例如，`{{ title suffix="title" }}` 将被替换为父条目标题后加单词“title”。如果变量为空（例如，条目的父级没有标题），则整个语句（包括后缀）将被忽略。 |
| `case`                | 所有         |              | 变量值书写风格。 <br> 转换变量的大小写，接受以下值：`upper`（大写）、`lower`（小写）、`sentence`（句子首字母大写）、`title`（标题首字母大写）、`hyphen`（连字符连接）、`snake`（下划线连接）、`camel`（驼峰式）以及 Zotero 7.0.16 新增的 `pascal`（帕斯卡命名法）。例如，`{{ title case="snake" }}` 将在文件名中产生 `title_written_like_this`。 |
| `replaceFrom`         | 所有         |              | 正则表达式查找。 <br> 需要搭配 `replaceTo`   参数使用。使用正则表达式匹配变量中的字符串，并用 `replaceTo` 参数指定的值替换它。例如，`{{ title replaceFrom="problem" replaceTo="solution" }}` 会被替换为父条目标题，其中单词“problem”的首次出现被替换为“solution”。可以通过 `regexOpts` 参数进一步配置。 |
| `replaceTo`           | 所有         |              | 正则表达式替换。 <br> 需要搭配 `replaceFrom` 参数使用。定义使用正则表达式匹配时要使用的替换值（参见 `replaceFrom`）。可以指定在 `replaceFrom` 中定义的捕获组。例如，要将条目标题中所有出现的单词“dog”和“cat”都加上前缀“super-”，可以使用以下模板：`{{ title replaceFrom="(dog\|cat)" replaceTo="super-$1" regexOpts="gi" }}`。 |
| `regexOpts`           | 所有         | 'i'          | 正则表达式标志。 <br> 定义使用正则表达式匹配时的[标志(`flags`)]（参见 `replaceFrom`）。例如，`{{ title replaceFrom="\s+" regexOpts="g" }}` 会被替换为移除了所有空格的父条目标题（如果没有 `regexOpts="g"`，只会移除第一个空格）。 |
| `match`               | 所有         |              | 正则表达式判断。 <br> 使用正则表达式测试变量中是否存在匹配的字符串。此参数在条件语句中很有用，并且不能与除 `regexOpts` 之外的任何其他参数一起使用。例如，以下模板仅在 URL 的域名是 `zotero.org` 时才返回父条目的 URL：`{{ if {{ url match="^https?://zotero.org.*?$" }} }}{{ url }}{{ endif }}`。 |
| `max`                 | 创作者变量   |              | 限制使用的创作者数量，例如，`{{ editors max="1" }}` 将被替换为父条目的第一个编辑。 |
| `name`                | 创作者变量   | `family`     | 自定义创作者名称在文件名中的显示方式，接受以下选项： <br> `family-given` 将使用创作者的全名，以创作者的姓氏（last name）开头； <br> `given-family` 也使用全名但顺序相反； <br> 选项 `given` 和 `family` 将只使用父条目创作者名称的一部分。 |
| `name-part-separator` | 创作者变量   | (单空格字符) | 定义用于分隔名和姓的字符，在与 `initialize` 结合使用时特别有用。 |
| `join`                | 创作者变量   | ,            | 定义用于分隔连续创作者的字符。 |
| `initialize`          | 创作者变量   |              | 名称首字母缩写。 <br> 允许对创作者名称的部分或全部使用首字母缩写，接受以下选项：<br> `full` 将使用整个名称的首字母，<br> `given` 和 `family` 将仅对该部分名称使用首字母。<br> 名称部分的顺序由 `name` 参数控制，并且只有通过 `name` 参数包含的部分才能转换为首字母。例如，`{{ authors name="given-family" initialize="given" }}` 将被替换为一个逗号分隔的作者列表，其中每位作者的名被替换为首字母，后跟一个点和空格（例如 `J. Smith, D. Jones`）。 |
| `initialize-with`     | 创作者变量   | .            | 控制如果名称部分被首字母缩写初始化，追加到首字母后面的字符。 |
| `localize`            | `itemType`   |              | 是否使用条目类型变量的本地化值，例如，`{{ itemType localize="true" }}` 将被替换为 Zotero 当前语言拼写的父条目类型。 |
| `timeZone`            | `accessDate` |              | 将访问日期转换为指定的时区，例如 `{{ accessDate timeZone="America/New_York" }}` 将被替换为父条目的“访问日期”，并转换为纽约当地时间。[时区列表]。（Zotero 8） |

>注：创作者变量：`authors`, `editors`, `creators`
>[标志(`flags`)]:https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_expressions#advanced_searching_with_flags
>[时区列表]:https://en.wikipedia.org/wiki/List_of_tz_database_time_zones


## 示例
一个出版年份，后跟一个连字符分隔的作者列表，再跟一个截断为 30 个字符的标题：

模板：
```
{{ year suffix="-" }}
{{ authors name="family-given" initialize="given" initialize="-" join="-" suffix="-" case="hyphen" }}
{{ title truncate="30" case="hyphen" }}
```
文件名：`2023-lee-sukbae-kim-ji-hoon-kwon-young-wan-the-first-room-temperature-amb.pdf`

任何未包含在 `{{ }}` 括号内的内容都会原样复制到文件名中：

模板：
```
{{ itemType localize="true" }} from {{ year }} by {{ authors max="1" name="given-family" initialize="given" }}
```
文件名：`Preprint from 2023 by S. Lee.pdf`

从 Zotero 8 开始，可以包含条目的访问日期和时间，并转换为指定时区的本地时间。由于文件名中不允许使用“:”，我们应该替换它以避兔被移除。下面的示例使用“-”作为替换字符。

```
{{ accessDate timeZone="Europe/Berlin" replaceFrom=":" replaceTo="-" regexOpts="g" }}-{{ title truncate="100" }}
```

### 条件语句
模板也支持条件语句。可以使用 `if`、`elseif` 和 `else` 的组合来包含或排除模板的特定部分。条件必须以 `endif` 结束。以下模板将对期刊文章和预印本使用 DOI，对书籍使用 ISBN，对所有其他条目类型使用标题：

```
{{ if itemType == "book" }}
{{ ISBN }}
{{ elseif itemType == "preprint" }}
{{ DOI }}
{{ elseif itemType == "journalArticle" }}
{{ DOI }}
{{ else }}
{{ title }}
{{ endif }}
```

### 关系运算符
从 Zotero 7.0.16 开始，可以使用关系运算符（如 `<`、`<=`、`>` 和 `>=`）来比较像 `authorsCount` 这样的数值。例如，以下模板检查作者数量：如果有两位或更多作者，则使用第一作者姓名后跟 "et al."；如果有一到两位作者，则将所有姓名包含在文件名中。

```
{{ if {{ authorsCount > 2 }} }}
{{ authors max="1" suffix=" et al" }}
{{ else }}
{{ authors join=" & " }}
{{ endif }}
```

### 正则表达式
可以使用正则表达式来匹配值并改变模板的行为。例如，以下模板保留常见的附件名称（如 "Full Text"），但对于标题不匹配的附件，它使用标准的 Zotero 文件名模板：

```
{{ if {{ attachmentTitle match="^(full.*\|submitted.*\|accepted.*)$" }} }}
{{ attachmentTitle }}
{{ else }}
{{ firstCreator suffix=" - " }}{{ year suffix=" - " }}{{ title truncate="100" }}
{{ endif }}
```
--- --- ---

## 字段完整列表

abstractNote
applicationNumber
archive
archiveID
archiveLocation
artworkMedium
artworkSize
assignee
audioFileType
audioRecordingFormat
billNumber
blogTitle
bookTitle
callNumber
caseName
citationKey
code
codeNumber
codePages
codeVolume
committee
company
conferenceName
country
court
date
dateDecided
dateEnacted
dictionaryTitle
distributor
docketNumber
documentNumber
DOI
edition
encyclopediaTitle
episodeNumber
extra
filingDate
firstPage
format
forumTitle
genre
history
identifier
institution
interviewMedium
ISBN
ISSN
issue
issueDate
issuingAuthority
journalAbbreviation
label
language
legalStatus
legislativeBody
letterType
libraryCatalog
manuscriptType
mapType
meetingName
nameOfAct
network
numPages
number
numberOfVolumes
organization
pages
patentNumber
place
postType
presentationType
priorityNumbers
proceedingsTitle
programTitle
programmingLanguage
publicLawNumber
publicationTitle
publisher
references
reportNumber
reportType
reporter
reporterVolume
repository
repositoryLocation
rights
runningTime
scale
section
series
seriesNumber
seriesText
seriesTitle
session
shortTitle
status
studio
subject
system
thesisType
title
type
university
url
versionNumber
videoRecordingFormat
volume
websiteTitle
websiteType

--- --- ---
