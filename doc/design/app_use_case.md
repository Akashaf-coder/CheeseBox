## App Use Case Table

**基础功能**

- 表格 1 用户选择文件系统来源
  | 用例： 用户选择文件系统来源|
  | ----------------------------------------------------------------- |
  | 简单描述： 用户在左侧窗口点击选择文件系统，默认选择本地文件系统 |
  | 触发条件：用户在左侧窗口点击选择文件系统 |
  | 前置条件：用户选取文件系统根目录(默认安装文件夹下，可修改)|
  | 后置条件：右侧窗口展示文件树 |
  | 基本事件流: |
  |1. 点击选择文件系统 |
  |2. 创建文件系统管理进程|
  |3. 右侧窗口显示文件系统下文件树|

- 表格 2 用户更改显示目录
  | 用例： 用户更改显示的目录|
  | ----------------------------------------------------------------- |
  | 简单描述： 用户在右侧显示框中左键双击子树，右侧重新刷新 |
  | 触发条件：用户在右侧显示框中左键双击子树 |
  | 前置条件：系统右侧已经显示目录|
  | 后置条件：右侧窗口展示文件树 |
  | 基本事件流: |
  |1. 用户右侧显示框中左键双击子树 |
  |2. 系统访问地址重新定位|
  |3. 右侧窗口刷新文件系统下文件树|

- 表格 3 用户删除文件系统
  | 用例： 用户删除选中的文件系统|
  | ----------------------------------------------------------------- |
  | 简单描述： 用户在左侧文件系统列表中右键单击想要删除的文件系统，在弹出的操作列表中选择删除 |
  | 触发条件：用户选中想要删除的文件系统，选择删除 |
  | 前置条件：系统中存在至少一个文件系统|
  | 后置条件：系统删除掉选中的文件系统 |
  | 基本事件流: |
  |1. 用户在左侧文件系统列表中选择想要删删除的文件系统，选择删除 |
  |2. 系统更新文件系统列表，根据是否为当前文件系统选择删除|
  |3. 系统更新缓存|

- 表格 4 用户刷新当前文件系统
  | 用例： 用户刷新当前选择的文件系统数据|
  | ----------------------------------------------------------------- |
  | 简单描述：用户点击刷新按钮，系统刷新当前文件系统的缓存 |
  | 触发条件：用户点击刷新按钮 |
  | 前置条件：系统选择了一个文件系统|
  | 后置条件：系统刷新选中的文件系统 |
  | 基本事件流: |
  |1. 用户选择好了一个文件系统 |
  |2. 用户点击刷新按钮|
  |3. 系统刷新文件系统缓存|

- 表格 5 用户导入新的文件系统
  | 用例： 用户导入一个新的文件系统|
  | ----------------------------------------------------------------- |
  | 简单描述：用户点击导入按钮，用户选择对应的文件来源，系统加载该文件系统 |
  | 触发条件：用户点击导入按钮 |
  | 前置条件：无|
  | 后置条件：系统刷新文件系统缓存，更新文件系统列表 |
  | 基本事件流: |
  |1. 用户点击导入按钮 |
  |2. 用户在弹出的文件浏览器中选择对应的文件系统根文件夹|
  |3. 系统刷新文件系统缓存，更新文件系统列表|

- 表格 6 用户添加文件系统子节点
  | 用例： 用户添加文件系统子节点|
  | ----------------------------------------------------------------- |
  | 简单描述：用户选中文件树的某一个节点，点击"+"按钮，为当前的文件系统添加对应的节点(可以选择增加文件夹类型 or 文件类型) |
  | 触发条件：用户点击"+"按钮 |
  | 前置条件：用户选择了一个展示的文件树，用户选中了对应的非文件节点(可作为母结点到)|
  | 后置条件：系统刷新文件系统缓存，更新文件树的缓存与 UI |
  | 基本事件流: |
  |1. 用户选中对应的节点，点击"+"按钮 |
  |2. 用户选择增加节点类型以及名字，系统创建对应的文件|
  |3. 系统刷新缓存，刷新 UI|

- 表格 7 用户删除文件系统子节点
  | 用例： 用户删除文件系统子节点|
  | ----------------------------------------------------------------- |
  | 简单描述：用户选中文件树的某一个节点，点击"-"按钮，删除对应的子树|
  | 触发条件：用户点击"-"按钮 |
  | 前置条件：用户选择了一个展示的文件树，用户选中了对应的节点|
  | 后置条件：系统删除对应子树，刷新文件系统缓存，更新文件树的缓存与 UI |
  | 基本事件流: |
  |1. 用户选中对应的节点，点击"-"按钮 |
  |2. 系统删除子树，刷新缓存，刷新 UI|

- 表格 8 用户搜索
  | 用例： 用户根据输入方式搜索文件|
  | ----------------------------------------------------------------- |
  | 简单描述：用户点击搜索按钮，选择搜索模式，搜索文件 |
  | 触发条件：用户点击搜索按钮 |
  | 前置条件：无|
  | 后置条件：系统显示搜索结果，等待进一步操作 |
  | 基本事件流: |
  |1. 用户点击搜索按钮，选择搜索的模式(tag，文件名，文件内容)，匹配模式(正则，关键字) |
  |2. 系统搜索 tag 表 or 文件树，显示搜索结果|
  |3. 系统列出搜索结果，刷新 UI|

- 表格 9 用户添加 tag
  | 用例： 用户给选中的文件树节点添加 tag|
  | ----------------------------------------------------------------- |
  | 简单描述：用户选中文件树节点(配合搜索使用)，为其增加 tag|
  | 触发条件：用户点击"添加 tag"按钮 |
  | 前置条件：用户选择了文件树节点|
  | 后置条件：系统刷新 Tag 表 |
  | 基本事件流: |
  |1. 用户选中对应的节点，点击添加 tag 按钮 |
  |2. 用户确认 tag 名称/规则|
  |3. 系统刷新 tag 表|

- 表格 10 用户备份本地文件系统
  | 用例： 用户备份本地文件系统文件|
  | ----------------------------------------------------------------- |
  | 简单描述：用户将选中的文件系统进行备份，备份至清华云盘|
  | 触发条件：用户点击"备份"按钮 |
  | 前置条件：用户选择了一个本地文件系统|
  | 后置条件：系统在清华云盘创建备份文件系统，保持对应的文件结构 |
  | 基本事件流: |
  |1. 用户选中本地文件系统，点击"备份"按钮 |
  |2. 系统在后台上传对应的文件系统到清华云盘|

- 表格 11 用户分享本地文件系统
  | 用例： 用户分享本地文件系统文件|
  | ----------------------------------------------------------------- |
  | 简单描述：用户将选中的文件树进行进行备份，并将其分享通过清华云盘分享|
  | 触发条件：用户点击"分享"按钮 |
  | 前置条件：用户选择了一个本地文件树|
  | 后置条件：系统在清华云盘创建备份文件系统，保持对应的文件结构，创建对应的分享链接 |
  | 基本事件流: |
  |1. 用户选中本地文件系统，点击"备份"按钮 |
  |2. 系统在后台上传对应的文件系统到清华云盘|
  |3. 系统请求清华云盘创建分享链接|

- 表格 12 用户在本地文件浏览器/自定义软件中打开对应的文件节点
  | 用例： 用户在本地文件浏览器/自定义软件中打开对应的文件节点|
  | ----------------------------------------------------------------- |
  | 简单描述：用户选中文件树节点，在设置的打开软件(默认为本地文件浏览器)中打开该节点|
  | 触发条件：用户点击"打开"按钮 |
  | 前置条件：用户选择了一个本地文件树|
  | 后置条件：系统使用设置的软件打开对应的节点 |
  | 基本事件流: |
  |1. 用户选中本地文件树，点击"打开"按钮 |
  |2. 系统使用设置的软件打开该节点|

- 表格 13 用户操作 UI 节点
  | 用例： 用户对于 UI 中节点进行操作，包括更改属性，展开节点，跳转目录等|
  | ----------------------------------------------------------------- |
  | 简单描述：用户对于 UI 中节点进行操作，包括更改属性，展开节点，跳转目录等|
  | 触发条件：用户点击 UI 节点 |
  | 前置条件：用户选择了本地某个文件系统|
  | 后置条件：系统根据操作进行处理 |
  | 基本事件流: |
  |1. 用户选中本地文件系统打开，对于 UI 进行操作 |
  |2. 系统根据用户操作进行命令执行|

---

**可添加功能**

- 表格 1 用户注册
  | 用例： 用户注册账号 |
  | ----------------------------------------------------------------- |
  | 简单描述： 软件用户注册一个应用账号，用于管理后续相关的代码和文件 |
  | 触发条件：用户在登录界面点击“注册账号” |
  | 前置条件：用户未登录 |
  | 后置条件：用户账号信息录入数据库，返回登录界面 |

- 表格 2 用户登录
  | 用例： 用户登录应用 |
  | ----------------------------------------------------------------- |
  | 简单描述： 用户凭借注册的信息进入应用，可以使用网络学堂文件下载等功能(如跳过登录直接进入则不可使用需要密码的项目) |
  | 触发条件：用户在登录界面点击“登录”、用户在应用页面中点击“登录”按钮 |
  | 前置条件：用户未登录 |
  | 后置条件：进入主应用界面 |

- 表格 3 用户退出登录
  | 用例： 用户退出应用 |
  | ----------------------------------------------------------------- |
  | 简单描述： 用户退出应用登录 |
  | 触发条件：用户在主界面点击“退出登录” |
  | 前置条件：用户已登录 |
  | 后置条件：用户退出登录状态，返回登录界面 |

- 表格 4 用户切换账号

  | 用例： 用户切换账号                          |
  | -------------------------------------------- |
  | 简单描述： 用户切换不同的账号                |
  | 触发条件：用户在应用页面中点击“切换账号”按钮 |
  | 前置条件：用户已登录                         |
  | 后置条件：进入选择账号界面                   |

- 表格 4 用户添加自定义文件系统

### Reference

1. [用例图与用例描述](https://www.jianshu.com/p/e1ff96af7e8c)
