# Visit: https://cavno.github.io/CreditExpansion/
# 信用扩张场景全景图

家庭 · 公司 · 银行 · 国家四层、三十个典型信用扩张场景的交互式地形图。每个场景按**抵押品强度 / 杠杆 / 反身性**三轴打分，合成一个脆弱度坐标，定位它在**对冲 → 投机 → 庞氏**谱系上的位置；越往上、越红，越接近庞氏那一端。

单文件、零构建、纯前端。整个应用就是一个 `index.html`，唯一的外部依赖是思源宋体（Google Fonts 的一行 `<link>`），加载失败时自动回退到系统衬线字，不影响功能。

## 包含什么

全景图按四层为列，纵轴是脆弱度（背景做成绿→琥珀→赤三段明斯基带）；节点颜色表示所属明斯基带，大小表示杠杆，空心菱形是「机制 · 政策」类（如派生存款、央行工具、总量调控），与借款人的杠杆头寸区分开。纵轴维度可切换为杠杆 / 反身性 / 抵押品薄弱，可按层筛选，可切到排行榜按任一维度排序，点任意节点或表行看运作机制。底部「读图说明 & 方法论边界」写明了打分口径与其作为代理的局限——三轴刻画的是结构脆弱度，最终的明斯基归类仍取决于现金流能否覆盖本息。

## 部署到 GitHub Pages

> 说明：部署需要你自己的 GitHub 账号与授权，我无法代为登录或创建仓库，下面两条路径任选其一，复制即可用。

### 路径 A：网页上传（最省事，无需 git）

1. 登录 GitHub，点右上角 **New repository** 新建一个仓库（例如命名 `credit-panorama`），可设为 Public。创建时不要勾选「Add a README」，保持空仓库。
2. 进入空仓库页面，点 **uploading an existing file**，把本文件夹里的 `index.html`（README 可选）拖进去，**Commit changes**。
3. 仓库页 → **Settings** → 左侧 **Pages** → Build and deployment → Source 选 **Deploy from a branch** → Branch 选 `main`、文件夹 `/ (root)` → **Save**。
4. 等一两分钟，页面顶部会出现访问地址：`https://<你的用户名>.github.io/credit-panorama/`。

### 路径 B：git 命令行

先在 GitHub 上新建一个空仓库（同上，不要带 README），然后在本文件夹内执行：

```bash
git init
git add index.html README.md
git commit -m "信用扩张场景全景图"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

若装了 GitHub CLI，前面几步可一行搞定：

```bash
gh repo create <仓库名> --public --source=. --push
```

推送完成后，仍按路径 A 的第 3 步在 **Settings → Pages** 里把 Source 指向 `main` 分支的根目录，保存即可拿到访问地址。

## 本地预览

直接双击 `index.html` 用浏览器打开即可，无需起服务器。
